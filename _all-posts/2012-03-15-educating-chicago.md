---
id: 11824
title: Educating Chicago
date: 2012-03-15T15:49:53+00:00
author: Ben Sheldon
layout: post
guid: http://codeforamerica.org/?p=11824
permalink: /2012/03/15/educating-chicago/
dsq_thread_id:
  - 612464842
categories:
  - 2012 fellows
  - News
---
[<img class="aligncenter size-full wp-image-11826" title="school-tiers" src="http://codeforamerica.org/wp-content/uploads/2012/03/school-tiers.png" alt="" width="100%" />](http://codeforamerica.org/wp-content/uploads/2012/03/school-tiers.png)

Chicago parents have a new tool for understanding the public school selection process: [Chicago Public School Tiers](http://cpstiers.opencityapps.org/), an app launched last week by [Open City](http://opencityapps.org/). The application is a perfect example of how independent civic developers can use open data to improve complicated yet important public processes; an approach that Code for America supports by helping the City of Chicago build its [open data platform](http://codeforamerica.org/2012-partners/chicago/).

The School Tiers app highlights and explains an important part of the school selection process, giving students from lower socioeconomic parts of the city a better chance of being accepted into a top Chicago Public School (CPS) Magnet or Selective School (e.g. Regional Gifted Centers, Classical Schools, International Gifted Programs). Depending on socioeconomic factors of the geographic area in which a student lives, they are assigned to one of four &#8220;tiers&#8221; that can give the student priority in the school enrollment process. While CPS provides a [static PDF map](http://cpsmagnet.org/apps/news/show_news.jsp?REC_ID=118406&id=0) of these tiers, the School Tiers app can map one&#8217;s exact address to its tier and contextualizes that with the area&#8217;s socioeconomic data.

The application was built by Forest Gregg, Derek Eder, and Juan-Pablo Velez who are part of Open City, a civic startup that builds open gov and open source apps to make cities work better. Juan-Pablo Velez describes their approach as &#8220;a certain opportunism: &#8216;hey, nobody&#8217;s done anything with this data yet. let&#8217;s think about how this would be useful for people and build something.&#8217;&#8221;

The specific process they went through to conceptualize the School Tiers app is described by Forest Gregg:

> I started reading [CPSobsessed](http://cpsobsessed.com), a really amazing blog by a CPS parent trying to understand the school system. CPS&#8217;s selective schools just did their enrollment for next year, and parents were talking about the way that these schools give spots to student. Reading about the Tier system, I found there was no really simple way to find out what Tier you were in.This seemed like an easy thing to fix. Derek already had code for doing a searchable map based on fusion tables, and I pulled together the data by combining the Tier information from a PDF document with a 2010 Census shapefile. Things got more complicated because we decided that we need to provide some explanation for what these Tiers were. In order to do that, we had to make sure we understand it ourselves. That pushed us to do a lot more research and to include the census information. Juan and I collaborated on that and wrote the copy together.

The application contains data scraped from PDFs released by CPS, socioeconomic data from the American Community Survey, and census tract shapefiles from the City of Chicago&#8217;s Data Portal. Derek Eder explains: &#8220;Going through the steps to organize, make sense of, and release this data is where a lot of the value of this project lies.&#8221;

Open City is just one example of a new generation of civic developers building on top of public data. As more more cities further open up their data&#8212;and release it in more accessible formats&#8212;we hope to see more developers launching applications and creating sustainable business models on top of public data. As a fellow serving with the City of Chicago on their Open311 platform, I hope that the work I do enables developers like Open City to add value to the platform, the City, and its residents.

[cc-mkplc app="chicago public school tiers"]