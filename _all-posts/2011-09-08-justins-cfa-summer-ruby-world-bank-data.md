---
id: 8455
title: 'Justin&#8217;s CfA Summer: Ruby &#038; World Bank Data'
date: 2011-09-08T11:25:49+00:00
author: Justin Stoller
layout: post
guid: http://codeforamerica.org/?p=8455
permalink: /2011/09/08/justins-cfa-summer-ruby-world-bank-data/
dsq_thread_id:
  - 408491909
categories:
  - 2011 Interns
  - CfA Labs
tags:
  - cfalabs
  - labs
---
When the summer started off, we broke into teams of two or three and worked on to build out developer tools for our chosen datasets, though soon enough we were constantly conferring and getting advice from each other. (We literally all worked side by side at what quickly became the &#8220;Interns&#8217; Table&#8221;.)

I choose with my usual foolishness the largest, most complicated API we had on the table, the [World Bank&#8217;s Development Indicators](http://data.worldbank.org/indicator). I didn&#8217;t just choose this API for the challenge, but also because it, though global in scope, represented to my one of the most important data sets we had to work with. The World Bank&#8217;s Catalog of Development Indicators is over 7,000 strong, holding metrics from the percentage of women who receive prenatal care, to percentage of land occupied by forest, to industry by industry rates of pollution, as well as all things economic. This data represents the humanity&#8217;s best attempt to measure the health of the world, economically, environmentally, and socially, country by country for the last half a century.

I began this task, honestly, having never written either a Ruby gem or an API wrapper before. In another life I had been a geeky construction worker and manager and quit only a little while ago to follow what a career in what truly interested me. I had, however, written scripts to consume different API&#8217;s. Having this experience left we wanting to mimic or learn how to program in a style of some of the best Ruby API wrappers. I sat, pouring over the source code for the Twitter gem on Github for hours. How could I make the World Bank&#8217;s wealth of information as accessible as Twitter&#8217;s?

To start with I created the a list of aliases for each country, so a developer needn&#8217;t remember that the two letter country code for Algeria is &#8216;DZ&#8217;.<sup><a href="#f1">1</a></sup> If you know the codes perfect, otherwise typing in &#8216;algeria&#8217; will return the same information to you (and misspelling will raise an error with an error that suggests possible countries you meant). Then I began looking into the simple chaining of methods on a “query” object. This would allow you to programatically build your query in several steps instead of passing one long gargantuan parameter list into the API in the same manner that Rails and Jquery ease searching. (You can read an excellent tutorial on doing this by the original author of the Twitter gem [here](http://railstips.org/blog/archives/2010/10/24/the-chain-gang/).) 

Finally I created the ability to receive from and pass into the API native Ruby objects. When you searched for “featured indicators” you can receive either a simple array of data hashes or you can receive back an array of “Indicator” objects. These instead of having to parse to find their ID and return that string back to a new query for information within that data set, you can simply pass that Indicator object into the query and it will submit its ID to the query when you send in the request.

For an example, if I wanted to look at a list of “featured” indicators I can call <sup><a href="#f2">2</a></sup>:

> WorldBank::Indicator.featured.cycle 

Sorting through the returned array I can inspect the names, note, organization that supplies the information, and what topic it falls under. After some sorting I pull the “Forested Area (% of total land)” Indicator and save it in a variable called &#8216;@forests&#8217;.

If in some other part of my program I was working with Ruby Date objects, say my birthday as the variable &#8216;@birth&#8217; and the present date as the variable &#8216;@now&#8217;, and I wanted to know the percentage of land occupied by forest in Brazil and how it&#8217;s changed during my life time I can submit a query like this:

> WorldBank::Data.country( &#8216;brazil&#8217; ).indicator( @forests ).dates( @birth&#8230;@now ).fetch 

This is far from a final solution to the challenge of accessing all of the World Bank&#8217;s information, but it is my humble attempt. I hope that it helps ease the process of working with what I believe is one of the world&#8217;s most important datasets. A dataset that we can use to compare exactly how our economic, environmental, and social goals are progressing as a planet.

Of course, if you do have an issue of any kind I plan to continue to maintain and work on this gem. Don&#8217;t hesitate to contact me through the [project&#8217;s Github page](https://github.com/codeforamerica/world_bank_ruby) or my own [personal Github page](https://github.com/justinstoller).

### Notes

<a name="f1">1</a> To geek out on you for a minute: the World Bank&#8217;s API allows you to sort through its information using a number of parameters, it also allows you to inspect its information on the parameters you can pass to filter data. It has a number of global options for any query, and the terms it uses to sort data and to inspect those parameters is of course the same. Depending on how the terms are placed within the search path, however, you could, say, get back Syria&#8217;s Agricultural datasets, or instead, a list of meta information about the Agricultural datasets that are on record for Syria. Obviously this distinction is a footnote in the actual documentation and you cannot actually refer to &#8216;Syria&#8217; in a request or sort by &#8216;Agricultural Data&#8217;. You must use one of the World Bank&#8217;s partial implementations of either the country&#8217;s two letter or three letter country code, refer to topics by ID, and pull out information using the Indicator&#8217;s ID (percentage of forested land in a country is listed by &#8216;AG.LND.FRST.ZS&#8217;, naturally&#8230;).
  
// end geek out

<a name="f2">2</a> The cycle method will repeat the request for each successive page of results – the &#8216;short&#8217; featured list is 7 pages long!

(Editor’s Note: Over the summer of 2011, over a dozen students interned with Code for America. They brought great energy, passion, and skills to bear on our projects and our mission to make government more open and efficient. Over the next week, we’ll be posting their [summaries of their work and learnings](http://codeforamerica.org/category/interns/), in addition to an overview of the summer.)