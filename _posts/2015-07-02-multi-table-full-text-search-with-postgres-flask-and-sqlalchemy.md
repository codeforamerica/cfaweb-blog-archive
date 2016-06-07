---
id: 33775
title: Multi-Table Full Text Search with Postgres, Flask, and Sqlalchemy
date: 2015-07-02T17:35:04+00:00
author: Ben Smithgall
layout: post
guid: http://www.codeforamerica.org/blog/?p=33775
permalink: /2015/07/02/multi-table-full-text-search-with-postgres-flask-and-sqlalchemy/
categories:
  - 2015 Fellows
  - Pittsburgh
---
One of the projects I’ve been working during my Code for America fellowship is a <a href="http://pittsburgh-purchasing.herokuapp.com/wexplorer/" target="_blank">search-based application</a> over contracts in the City of Pittsburgh. A common problem among people in the City is that they need to look up information about contracts when they go to buy something. They might need to get the right identifier for the City Controller to pay the invoice, or figure out which specific height of fence post they can buy. Right now, they are often leafing through large stacks of printed documents, spreadsheets scattered across shared drives, and several websites. The goal of this project is to unify that data and make it searchable.

Over time, we have been collecting more and more information about these contracts that we want to expose via search. This information is stored in several different database tables. For awhile, using naïve substring-based search was fine for our purposes, but obvious weaknesses have been a blocker for our users. After reading <a href="http://blog.lostpropertyhq.com/postgres-full-text-search-is-good-enough/" target="_blank">Postgres full-text search is Good Enough!</a>, and <a href="https://robots.thoughtbot.com/implementing-multi-table-full-text-search-with-postgres" target="_blank">Implementing Multi-Table Full Text Search with Postgres in Rails</a>, I figured that I would try implementing Postgres full-text search. I ended using a very similar approach to the one outlined in the Rails post.

Why didn’t I use [ElasticSearch/Solr/some other perfect solution]? There are two reasons: first, the app (and its accompanying database) is (very) small, so going all the way to elasticsearch or an equalivalent seemed like overkill. Second, the use case is perfect for Postgres full-text search: we are using Postgres already, and I just needed to implement some additional search functionality without the added requirement of an indexing step. Overall, I used a process similar to the one outlined in the Rails post linked above – a database migration sets up the majority of the functionality, a SQLAlchemy Model is created to give access to the model, and everything ends up working out fine.

**Write the migraton**

The first piece of the puzzle is writing the migration (note: I’m using alembic to manage migrations). I needed the migration to accomplish the following things:

  * Set up GIN indices on all of my TSVector columns
  * Create view refresh triggers on all of the appropriate tables

I’m going to include example snippets from the project. You can find the whole thing <a href="https://github.com/codeforamerica/pittsburgh-purchasing-suite" target="_blank">here</a>

**Create the materialized view**

Full code <a href="https://github.com/codeforamerica/pittsburgh-purchasing-suite/blob/master/migrations/versions/21c0f59b5214_add_fulltext_view.py" target="_blank">here</a>

<pre class="language-python"><code>

from alembic import op
import sqlalchemy as sa

trigger_tuples = [
    ('contract', 'description'),
    ('company', 'company_name'),
    ('contract_property', 'value'),
    ('line_item', 'description'),
]

index_set = [
    'tsv_contract_description',
    'tsv_company_name',
    'tsv_detail_value',
    'tsv_line_item_description'
]

def upgrade()
    conn = op.get_bind()
    # create the materialized view
    conn.execute(sa.sql.text('''
        CREATE MATERIALIZED VIEW search_view AS (
            contract.id as contract_id,
            [...]
        )
    '''))
    # create unique index on ids
    op.create_index(op.f('ix_search_view_id'), 'search_view', ['id'], unique=True)

    # create remaining indices on the tsv columns
    for index in index_set:
        op.create_index(op.f(
            'ix_tsv_{}'.format(index)), 'search_view', [index], postgresql_using='gin'
        )

    # for triggers, we need to build a new function which runs our refresh materialized view
    conn.execute(sa.sql.text('''
        CREATE OR REPLACE FUNCTION trig_refresh_search_view() RETURNS trigger AS
        $$
        BEGIN
            REFRESH MATERIALIZED VIEW CONCURRENTLY search_view;
            RETURN NULL;
        END;
        $$
        LANGUAGE plpgsql ;
    '''))
    for table, column in trigger_tuples:
        conn.execute(sa.sql.text('''
            DROP TRIGGER IF EXISTS tsv_{table}_{column}_trigger ON {table}
        '''.format(table=table, column=column)))
        conn.execute(sa.sql.text('''
            CREATE TRIGGER tsv_{table}_{column}_trigger AFTER TRUNCATE OR INSERT OR DELETE OR UPDATE OF {column}
            ON {table} FOR EACH STATEMENT
            EXECUTE PROCEDURE trig_refresh_search_view()
        '''.format(table=table, column=column)))
</code></pre>

This neatly accomplishes all of the tasks needed – it materializes a search_view, which will <a href="http://www.postgresql.org/docs/9.4/static/sql-refreshmaterializedview.html" target="_blank">concurrently refresh</a> whenever any of the underlying columns to be searched changes.

**Set up the Sqlalchemy model**

In my <a href="https://github.com/codeforamerica/pittsburgh-purchasing-suite/blob/master/purchasing/data/models.py" target="_blank">models</a>, I set up a SearchView model that matched up with the schema of the table created in the migration. Once this is set up and the migration is run, we can access the data as we normally might. In a python shell:

<pre class="language-python"><code>

>>> search_result = SearchView.query.first()
# &lt;purchasing.data.models.SearchView object at 0x1070d2710>
>>> type(search_result)
# &lt;class 'purchasing.data.models.SearchView'>
# the city of pittsburgh has two contracts related to scuba gear,
# one for actual gear, one for maintenance.
>>> print db.session.query(SearchView.contract_description, SearchView.company_name).filter(SearchView.contract_description.match('scuba')).all()
# [(u'SERVICE OF SCUBA EQUIPMENT', u'SPLASH WATER SPORTS'), (u'SCUBA SUPPLIES', u'DIVE RESCUE INTERNATIONAL'), (u'SCUBA SUPPLIES', u'SPLASH WATER SPORTS')]
</code></pre>

There is one remaining problem to be ironed out before we can move on, though: if we attempt to do any migrations from this point forward, alembic will generate a SearchView table. We need to get alembic to ignore this. I found <a href="https://gist.github.com/utek/6163250" target="_blank">this gist</a>, which describes a good solution to this problem.

In our alembic.ini:

<pre class="language-python"><code>

# set tables to ignore
[alembic:exclude]
tables = search_view
</code></pre>

In our env.py (see <a href="https://github.com/codeforamerica/pittsburgh-purchasing-suite/blob/master/migrations/env.py" target="_blank">here</a> for full changes):

<pre class="language-python"><code>

def exclude_tables_from_config(config_):
    tables_ = config_.get('tables', None)
    if tables_ is not None:
        tables = tables_.split(',')
    return tables

exclude_tables = exclude_tables_from_config(config.get_section('alembic:exclude'))

def include_object(object, name, type_, reflected, compare_to):
    if type_ == "table" and name in exclude_tables:
        return False
    else:
        return True
</code></pre>

This handles the migration side of things. Now we need to actually implement our search.

**Set up the search**

The most recent versions of sqlalchemy support full-text search operations, including match, so getting set up with basic full-text search is fairly straightforward.

<pre class="language-python"><code>

# db is an instance of &lt;class 'flask_sqlalchemy.SQLAlchemy'>
# search_term is a string that will get converted to a `tsvector` type by sqlalchemy

def search(search_term):
    return db.session.query(
        db.distinct(SearchView.contract_id)
    ).filter(db.or_(
        SearchView.tsv_company_name.match(search_term, postgresql_regconfig='english'),
        SearchView.tsv_line_item_description.match(search_term, postgresql_regconfig='english'),
        SearchView.tsv_contract_description.match(search_term, postgresql_regconfig='english'),
        SearchView.tsv_detail_value.match(search_term, postgresql_regconfig='english')
    )).all()

print search('scuba')
# [(548,), (541,)]
</code></pre>

Going past this gets a bit more challenging. For example, the <a href="http://www.postgresql.org/docs/9.4/static/textsearch-controls.html#TEXTSEARCH-RANKING" target="_blank">ts_rank function</a> is not supported out of the box, so we have to <a href="https://github.com/codeforamerica/pittsburgh-purchasing-suite/blob/master/purchasing/database.py" target="_blank">write that</a> ourselves:

<pre class="language-python"><code>

class TSRank(GenericFunction):
    package = 'full_text'
    name = 'ts_rank'

# TSRank is now available as db.func.full_text.ts_rank()
</code></pre>

We also want to concatenate all of our search documents together with weights to get a good ranking. This caused some problems because the db.func.concat() function returns a text/string type, converting from the required TSVector type. This type coercion causes incorrect ranking. However, db.func.concat() also works on a Column-level, which is what is needed for Postgres to properly concatenate TSVector columns. Additionally, we have to coalesce the columns to catch NULL values. Failing to do so can really screw up the results:

<pre class="language-python"><code>

def search(search_term):
    return db.session.query(
        db.distinct(SearchView.contract_id),
        SearchView.contract_description,
        SearchView.company_name,
        db.func.max(db.func.full_text.ts_rank(
            db.func.setweight(db.func.coalesce(SearchView.tsv_company_name, ''), 'A').concat(
                db.func.setweight(db.func.coalesce(SearchView.tsv_contract_description, ''), 'D')
            ).concat(
                db.func.setweight(db.func.coalesce(SearchView.tsv_detail_value, ''), 'D')
            ).concat(
                db.func.setweight(db.func.coalesce(SearchView.tsv_line_item_description, ''), 'B')
            ), db.func.to_tsquery(search_term, postgresql_regconfig='english')
        )).label('rank')
    ).filter(db.or_(
        SearchView.tsv_company_name.match(search_term, postgresql_regconfig='english'),
        SearchView.tsv_line_item_description.match(search_term, postgresql_regconfig='english'),
        SearchView.tsv_contract_description.match(search_term, postgresql_regconfig='english'),
        SearchView.tsv_detail_value.match(search_term, postgresql_regconfig='english')
    )).group_by(
        SearchView.contract_id, SearchView.contract_description, SearchView.company_name
    ).order_by(db.text('rank DESC')).all()

search('scuba')
# [(541, u'SCUBA SUPPLIES', u'DIVE RESCUE INTERNATIONAL', 0.0607927), (541, u'SCUBA SUPPLIES', u'SPLASH WATER SPORTS', 0.0607927), (548, u'SERVICE OF SCUBA EQUIPMENT', u'SPLASH WATER SPORTS', 0.0607927)]
fences = search('fence')
# the city has a bunch of fencing contracts. some of them have
# 'fence' in the name of the awarded company, some in other places
print len(fences)
# 12
print fences[0]
# (280, u'FENCING INSTALLATION, REPAIRS, ETC.  (CD)', u'ALLEGHENY FENCE CONSTRUCTION', 0.665342)
# note that the with the company name containin the word fence, we have a higher rank
print fences[-1]
(421, u'GRASS SEED AND LANDSCAPING SUPPLIES II', u'KEYSTONE TURF PRODUCTS', 0.243171)
# here, the word 'fence' is part of the a line item associated with the contract, so the
# rank is lower.
</code></pre>

Now we are getting somewhere! The last thing that I want to do was to allow users to filter their search results. For example, users might only want to find contract line items that match their search term.

In order to do this, we can write a function which returns a list of columns we want to filter by, and pass that into our query:

<pre class="language-python"><code>

def build_filter(req_args, fields, search_term, filter_form, _all):
    '''Build the where clause filter
    '''
    clauses = []
    for arg_name, _, filter_column in fields:
        if _all or req_args.get(arg_name) == 'y':
            if not _all:
                filter_form[arg_name].checked = True
            clauses.append(filter_column.match(search_term, postgresql_regconfig='english'))
    return clauses

# filter form is a small form that presents a series of
# checkboxes on the web page for users to filter
filter_form = FilterForm()
fields = [
    ('company_name', 'Company Name', SearchView.tsv_company_name),
    ('line_item', 'Line Item', SearchView.tsv_line_item_description),
    ('contract_description', 'Contract Description', SearchView.tsv_contract_description),
    ('contract_detail', 'Contract Detail', SearchView.tsv_detail_value),
]

def search(search_term, filter_where):
    return db.session.query(
        db.distinct(SearchView.contract_id),
        SearchView.contract_description,
        SearchView.company_name,
        db.func.max(db.func.full_text.ts_rank(
            db.func.setweight(db.func.coalesce(SearchView.tsv_company_name, ''), 'A').concat(
                db.func.setweight(db.func.coalesce(SearchView.tsv_contract_description, ''), 'D')
            ).concat(
                db.func.setweight(db.func.coalesce(SearchView.tsv_detail_value, ''), 'D')
            ).concat(
                db.func.setweight(db.func.coalesce(SearchView.tsv_line_item_description, ''), 'B')
            ), db.func.to_tsquery(search_term, postgresql_regconfig='english')
        )).label('rank')
    ).filter(db.or_(*filter_where)).group_by(
        SearchView.contract_id, SearchView.contract_description, SearchView.company_name
    ).order_by(db.text('rank DESC')).all()

# this time, let's search for tree contracts, because
# they are scattered across a bunch of categories
search_term = 'tree'
filter_none = build_filter(
    {}, fields, search_term, filter_form, True
)
trees = search(search_term, filter_none)
print len(trees)
# 16
print trees[0]
# (308, u'PRUNING AND REMOVAL OF TREES IN CD AREAS ONLY', u'BENTLEY TREE CARE', 0.650144)
# now, let's filter by line items

filter_line_items = build_filter(
    {'line_item': 'y'}, fields, search_term, filter_form, False
)
trees = search(search_term, filter_line_items)
print len(trees)
# 5
</code></pre>

When plugged into a fairly light interface with some added features, it looks something like this:

[<img src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/06/wexplorer.gif" alt="wexplorer" class="alignnone size-full wp-image-33790" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/06/wexplorer.gif)
  
_Search! Filter! Sort!
  
_ 

**Test it**

One side effect of this is that when writing tests, you can no longer use SQLAlchemy’s create\_all() method, because it will incorrectly create a table as opposed to materializing a view. My solution to this is the run the database migrations on test set up. One thing to note, however, is that running the migrations takes longer than the create\_all() method, so only do that in cases where you are actually testing the full-text search. One caveat is that in the tearDown method, I had no success trying to drop the materialized view only. Instead, I had to drop the whole and recreate the whole schema to make sure the database was clean between tests. If you are using flask-migrate, you can do the following:

<pre class="language-python"><code>

class TestMySearch(BaseTestCase):
    def setUp(self):
        # in this case, we don't want to run the super()
        # because that will incorrectly do a create all!
        from flask_migrate import upgrade
        upgrade()

    def tearDown(self):
        db.session.execute('''DROP SCHEMA IF EXISTS public cascade;''')
        db.session.execute('''CREATE SCHEMA public;''')
        db.session.commit()
        db.session.remove()
        db.drop_all()
        # make sure we dispose of our session completely
        db.get_engine(self.app).dispose()
</code></pre>

**Some notes**

As noted in the piece about a similar implementation in Rails, the approach is pretty fragile if you decide you need to add a new table later. You will have to do some pretty serious mucking around in the migrations should that become necessary.

However, this implementation has worked out pretty well for this project, but I’m not sure if it’s the best way to go about it. If you have comments or suggestions, let me know <a href="https://twitter.com/bsmithgall" target="_blank">on twitter</a>.