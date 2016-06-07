---
id: 8343
title: 'Zach&#8217;s CfA Summer: <br />&#8220;Made With [EPA] Data&#8221;'
date: 2011-09-02T14:06:16+00:00
author: Zach Williams
layout: post
guid: http://codeforamerica.org/?p=8343
permalink: /2011/09/02/zachs-cfa-summer-made-with-epa-data/
dsq_thread_id:
  - 403008965
categories:
  - 2011 Interns
  - News
---
[<img src="http://codeforamerica.org/wp-content/uploads/2011/09/epa.jpg" alt="" title="epa" class="alignright size-full wp-image-8344" />](http://madewithdata.org)When Code for America selected me as a Google Summer of Code Intern for the [Government Gems and Eggs project](http://codeforamerica.org/?cfa_project=government-rubygems-pythoneggs-gsoc) this summer, I knew the next few months were going to be awesome. For the first time ever, I was able to meet and work with people truly committed to making government data more accessible.

Most developers don&#8217;t especially enjoy working with APIs. It normally consists of reading a large amount of documentation with few examples, followed by a fair amount of troubleshooting whenever things don&#8217;t work as expected. On top of that, visualizations and graphs aren&#8217;t generally made overnight — a fair amount of development is spent working with data formats you might not be especially fond of (I&#8217;m looking at you XML).

But, when data and APIs become accessible, developers can make visualizations and applications that allow multiple individuals to grasp the larger picture of what&#8217;s taking place around them (the immediate examples that come to mind are the <a href="http://nyc.longliveman.com/" target="_blank">NYC Graffiti Snapshot</a> or <a href="http://www.zeit.de/datenschutz/malte-spitz-data-retention" target="_blank">Zeit&#8217;s visualization</a> of mobile telecom data).

This summer I ended up writing 8 different Python API wrappers — all of which are available on Code for America&#8217;s Github page — along with a <a href="https://github.com/codeforamerica/Python-API-Module" target="_blank">base module other developers can use</a> going forward.

The big news from our work this summer, in my opinion, are matching <a href="https://github.com/codeforamerica/epa_ruby" target="_blank">Ruby</a> and <a href="https://github.com/codeforamerica/epa_python" target="_blank">Python</a> <wbr>wrappers for the EPA&#8217;s API (an API so large and complex that no other wrappers had previously been written for it). A wealth of government data and information is now available to developers — and the <a href="https://github.com/codeforamerica/epa_python" target="_blank">documentation on the Github repositories</a> features tons of working examples.</wbr>

Throughout my last few weeks as an intern at Code for America, I worked on finishing <a href="http://madewithdata.com/" target="_blank">madewithdata.com</a> — a simple site that currently allows users to explore the radiation and water pollution information now made available through the EPA API wrappers. I actually learned quite a few things while developing the site:

  * The <a href="http://en.wikipedia.org/wiki/List_of_United_States_cities_by_population" target="_blank">top 25 most-populated US cities</a> are made up of 531 ZIP Codes.
  * 2190 facilities in those ZIP Codes have permits to pollute public water sources.
  * The ZIP Code 32218 in Jacksonville, Florida has the most polluters — 178 facilities have been granted EPA permits to pollute public water sources (some of the records date back to the 1970s).

Also, all the code I used to make the site (and find the number of polluters) is available on my <a href="https://github.com/zachwill" target="_blank">personal Github page</a>.