---
id: 31669
title: 'Technical Aspects of Opening Data: How it&#8217;s Made'
date: 2014-08-26T14:23:46+00:00
author: Garrett Jacobs
layout: post
guid: http://www.codeforamerica.org/blog/?p=31669
permalink: /2014/08/26/open-data-how-its-made/
categories:
  - Data
  - Gov2.0
  - Open Data
  - Open Gov
---
Opening data is a complex, sometimes messy, undertaking. It&#8217;s a technical issue, but like the old Reese&#8217;s commercial, there&#8217;s more than one way to get it done.

Simply understanding the language and process can help lead to a workable approach for opening data in your city or agency.

To help clarify some of the technical aspects of opening data, we recently sat down with the Director of Analytics and Performance Management for the City of Chicago Tom Schenk, Open Data Program Manager for Chicago Jon Levy, and <a href="http://daguar.github.io/2014/03/17/etl-for-america/" target="_blank">master data wrangler</a> and 2013 CfA fellow Dave Guarino.



We’ll go over some lingo and processes in a second, but if you only get this far, **know that the talent you need to run an open data initiative probably already exists in your department or city.** Identifying the right people for the job means you need to know what to look for and you need to know enough to identify when you&#8217;re in the dark.

**Laying the foundation for open data &#8211; ETL**

The basic components of the problem of publishing data are often described in the enterprise world by the acronym &#8220;ETL.&#8221; While the acronym is casually thrown around the data warehousing world, it&#8217;s often not used explicitly in the context of governments opening data. ETL stands for three steps in the process of data publishing; Extract, Transform, and Load.

It is the process of taking data from one place, making it useful, and presenting it to the world. Figuring out how to solve these pieces of the problem is core to creating a sustainable and enduring open data system.

  * Step 1: Extract &#8211; simply means getting data from an original source system where updates are stored and new data is added, like a 311 or police database.
  * Step 2: Transform &#8211; involves making changes or additions to the data that make it easier to use, for example taking a parcel identifier and making it into a street address.
  * Step 3: Load &#8211; getting that transformed data into an easily-accessible place — in our case on an open data site or portal.

Many people who can wield these tools are probably currently inside your city and can be found in a data warehousing team, a GIS unit, or a business intelligence operation. Getting an open data site up is a good start. However, without the internal human capital and a focus on automation, it can become more burdensome than beneficial.

**Diving in &#8211; Techniques for Opening Data**

ETL describes the structure of the data problem which can be approached in a number of ways. We highlight three general categories of tools:

  * Programmatic Approaches &#8211; writing code.
  * Graphical UGI tools &#8211; developed to be user-friendly with drag and drop process
  * The inevitable _‘others’_

Programmatic Tools and Techniques:

  * A lightweight approach for a proof of concept or pilot: just have a data page for the city &#8211; not a portal &#8211; with links to downloadable datasets. Tap someone in your organization that has programming knowledge like unix or Linux. Have them set up nightly cron (chronological &#8211; a scheduler tool) jobs that open a connection to the database with a python call, creating a csv of the desired data and automatically throw it onto your shared server. Then drop a link to its location on the public facing web page.
  * Use Python, it’s readable language with a wealth of tools and online databases. [Opening data is a complex, sometimes messy, undertaking. It&#8217;s a technical issue, but like the old Reese&#8217;s commercial, there&#8217;s more than one way to get it done.

Simply understanding the language and process can help lead to a workable approach for opening data in your city or agency.

To help clarify some of the technical aspects of opening data, we recently sat down with the Director of Analytics and Performance Management for the City of Chicago Tom Schenk, Open Data Program Manager for Chicago Jon Levy, and <a href="http://daguar.github.io/2014/03/17/etl-for-america/" target="_blank">master data wrangler</a> and 2013 CfA fellow Dave Guarino.



We’ll go over some lingo and processes in a second, but if you only get this far, **know that the talent you need to run an open data initiative probably already exists in your department or city.** Identifying the right people for the job means you need to know what to look for and you need to know enough to identify when you&#8217;re in the dark.

**Laying the foundation for open data &#8211; ETL**

The basic components of the problem of publishing data are often described in the enterprise world by the acronym &#8220;ETL.&#8221; While the acronym is casually thrown around the data warehousing world, it&#8217;s often not used explicitly in the context of governments opening data. ETL stands for three steps in the process of data publishing; Extract, Transform, and Load.

It is the process of taking data from one place, making it useful, and presenting it to the world. Figuring out how to solve these pieces of the problem is core to creating a sustainable and enduring open data system.

  * Step 1: Extract &#8211; simply means getting data from an original source system where updates are stored and new data is added, like a 311 or police database.
  * Step 2: Transform &#8211; involves making changes or additions to the data that make it easier to use, for example taking a parcel identifier and making it into a street address.
  * Step 3: Load &#8211; getting that transformed data into an easily-accessible place — in our case on an open data site or portal.

Many people who can wield these tools are probably currently inside your city and can be found in a data warehousing team, a GIS unit, or a business intelligence operation. Getting an open data site up is a good start. However, without the internal human capital and a focus on automation, it can become more burdensome than beneficial.

**Diving in &#8211; Techniques for Opening Data**

ETL describes the structure of the data problem which can be approached in a number of ways. We highlight three general categories of tools:

  * Programmatic Approaches &#8211; writing code.
  * Graphical UGI tools &#8211; developed to be user-friendly with drag and drop process
  * The inevitable _‘others’_

Programmatic Tools and Techniques:

  * A lightweight approach for a proof of concept or pilot: just have a data page for the city &#8211; not a portal &#8211; with links to downloadable datasets. Tap someone in your organization that has programming knowledge like unix or Linux. Have them set up nightly cron (chronological &#8211; a scheduler tool) jobs that open a connection to the database with a python call, creating a csv of the desired data and automatically throw it onto your shared server. Then drop a link to its location on the public facing web page.
  * Use Python, it’s readable language with a wealth of tools and online databases.](https://pypi.python.org/pypi/csvkit/0.8.0) is a great command-line tool for working with CSV files. Many GIS teams are already using Python, so you may have a GIS unit that can be an asset for the open data team.
  * SQL and Java are, of course, great general purpose tools for writing code to handle data.

Graphical/GUI Tools: These are generally applied when the programming techniques need to scale and non-programmers (such as those with more analysis backgrounds) might be integrated into the open data process.

  * <a href="http://community.pentaho.com/projects/data-integration/" target="_blank">Pentaho</a> Data Integration (Kettle) is a free and open source product with available paid technical support and training.
  * <a href="http://www.safe.com/" target="_blank">SafeFME</a> Data Integration is a paid service. Free trials periods are available for testing workflow or using to prove your concept.
  * While we have heard the most of the previous two some others include, <a href="http://www.informatica.com/us/#fbid=woJ59QPwFRN" target="_blank">Informatica</a> and <a href="https://www.talend.com/products/talend-open-studio" target="_blank">Talend Open Studio</a>

The inevitable _‘others’_:

  * <a href="http://openrefine.org/" target="_blank">OpenRefine</a> (previously Google Refine) is good for cleaning and exploring data. Its use is optimal for one-off or infrequent data transformations, since it is not designed for automation or reuse.
  * Excel and Visual Basics for Applications (VBA) are skills that a lot of people in government, particularly with public policy and economics backgrounds have. It’s possible to write a VBA Macro script to retrieve data from a shared drive.
  * Windows Task Scheduler is an easy way to automate processes in a Windows environment (from VBA code to using Socrata’s DataSync tool to upload a CSV to an open data site).
  * Your agency may also already have licenses for tools that are not being used, which can be applied to opening data. For example, IBM Cognos is a business intelligence/reporting tool that can tap into many databases and pull out data by dumping everything into a CSV.

Lastly, as Dave points out, remember that the ETL processes is most effective when it is automated. So, in the words of Ron Popeil, “Set it and forget it!”

If you would like to dive deeper into this discussion join us for our session on day three of this year’s <a href="http://www.codeforamerica.org/summit" target="_blank">Code for America Summit</a> next month &#8211; _So You&#8217;re Ready to Open Data: Now What?_

**Additional Relevant Resources:**

  * <a href="http://sunlightfoundation.com/blog/2014/03/21/data-plumbers/" target="_blank">Sunlight Foundation on Data Plumbing  </a>
  * <a href="http://wiki.pentaho.com/display/EAI/03.+Hello+World+Example" target="_blank">Pentaho Tutorial</a>
  * <a href="http://digital.cityofchicago.org/index.php/how-a-table-becomes-a-dataset-openrefine/" target="_blank">From Table to Dataset</a>, Chicago example
  * <a href="http://daguar.github.io/2014/03/17/etl-for-america/" target="_blank">Dave’s original data plumbing post</a>