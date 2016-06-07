---
id: 8089
title: 'A Google Summer of Code: Civic Developer Tools'
date: 2011-08-24T20:17:34+00:00
author: Dan Melton
layout: post
guid: http://codeforamerica.org/?p=8089
permalink: /2011/08/24/a-google-summer-of-civic-coding/
dsq_thread_id:
  - 395160675
categories:
  - CfA Labs
  - News
---
Last fall, Luigi Montanez and I were sitting in the auditorium at the International Open Data Conference brainstorming about ways to get developers more interested in civic coding.  He had just completed a whirlwind tour of ruby meetups, conferences and codeathons promoting Sunlight Labs tools and projects. At CfA, we were just getting started thinking about our own strategies.  One idea came up. What if we got a bunch of developers to spend a summer hacking on tools that make it easier to interact with government APIs?  <!--more-->

For noncoders, APIs (application program interfaces) are gaining popularity across the web. APIs enable you as end user to click that Facebook Connect button or that Twitter share button. APIs help developers interact with a set of data, without gaining access to the database. They also scale and throttle usage and allow updates or new data submissions.

I think part of the success of APIs (including Twilio, Facebook, Twitter, etc) is the thriving ecosystem of development tools like ruby gems, python eggs, php libraries or SDKs.  These tools make is really easy for a developer to incorporate the external data, which reduces development time and ultimately provides a faster product and often better experience for the end user.  Plus, we can leverage each other&#8217;s work as coders with tools that we collectively maintain, rather than each writing our own wrapper or API request.

Every month, there is another new api or interesting government data set online. From the [FCC](http://www.fcc.gov/developers) to the [World Bank](http://data.worldbank.org/developers), developers can access millions of data points. But, those APIs don&#8217;t often include development tools to make it easier for coders to quickly develop applications off the APIs.

Building on the concept, we held an [initial hackathon at Stanford](http://codeforamerica.org/2011/04/17/hackathon-at-stanford-opening-up-government-data/) in the spring, and in one day, built out six development tools, which have collectively been downloaded/used a couple hundred times.

The event was such a success, that we wanted to scale it up for the summer&#8230;. but how? Enter [Google Summer of Code](http://code.google.com/soc/).  We submitted as a newly minted organization, hoping to get selected.  Not only did we, but we had over 100 applications and ended up with 10 spots. Six of those spent the summer building out development tools.

When we started this summer, we counted roughly 50 or so government APIs that could use developer libraries and roughly 20 development tools supporting them. At the end, we added nearly 40 new tools in php, ruby and python. Each of the GSoC students will write up a blog piece about their tools, so, you can check those out in the week to come.

This summer was an infrastructure sprint.  I think part of our job is producing tools to help others be more successful.  Adding 40 tools will help deepen the infrastructure and ultimately the ecosystem for civic coding.

You can check out our repos at <http://www.github.com/codeforamerica>. In the search box, type php, ruby or python to see the tools.

Also, all the tools will be available on google code and language specific sites like <http://rubygems.org>