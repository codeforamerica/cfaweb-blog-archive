---
id: 8552
title: Open311 at Code for America
date: 2011-09-20T14:51:36+00:00
author: Michael Lawrence Evans
layout: post
guid: http://codeforamerica.org/?p=8552
permalink: /2011/09/20/open311-at-code-for-america/
dsq_thread_id:
  - 420637633
categories:
  - News
---
We&#8217;re deeply committed to [Open311](http://www.open311.org) &#8212; an interoperable standard that allows developers to seamlessly interact with 311 systems across the nation. 311 is an increasingly popular communication system for cities to enable citizen issue reporting. Open311 is an attempt to standardize the protocol so 311 apps built anywhere can be used everywhere. Thanks to [Google Summer of Code](http://code.google.com/soc/), we were able to bring some great additional talent onto our Open311 projects, and we think the results are exciting. Here&#8217;s a summary of what we&#8217;ve done so far and where we&#8217;re looking to go:

### Open311 Dashboard

Late in 2010, our CTO, Dan Melton, had the idea for an [Open311 Dashboard](http://codeforamerica.org/?cfa_project=open311-dashboard). We want to help cities visualize and analyze 311 data on a clean, interactive dashboard. Early this year, I took it on as a 20% project, and soon thereafter I started to focus on it as project lead. This summer, Chris Barna and Bailey Smith joined my team to help design and build the back-end with Django and an advanced geospatial database. We&#8217;re especially interested in trend analysis by block and by neighborhood. Over the next month, my team will be putting the finishing touches on the first release of the dashboard. More details and screenshots of the project can be found in [Chris&#8217;s update](http://codeforamerica.org/2011/08/31/chriss-cfa-summer-preview-the-open311-dashboard).

### Open311 Center on Joget

Michael Yap, the CEO of [Joget](http://www.joget.org), and I worked with Ashish Mittal in creating a prototype of an [Open311 Center](http://codeforamerica.org/2011/09/09/ashishs-cfa-summer-starting-the-open311-center/); it&#8217;s a lightweight 311 back-end using Joget&#8217;s open source workflow management system. Michael Yap and I are now planning to add a set of simple analytical tools for small cities to analyze request trends in real-time. More details on the Open311 Center can be found in [Ashish&#8217;s update](http://codeforamerica.org/2011/09/09/ashishs-cfa-summer-starting-the-open311-center/).

### Open311 Developer Libraries

Two of our Google Summer of Coders, Zach Williams and Ronaldo Barbachano, built [Python](https://github.com/codeforamerica/open311_python) and [PHP](https://github.com/codeforamerica/open311_php) libraries for Open311. The libraries make it easier for developers to use the API. The libraries also build on the success of Code for America&#8217;s [Ruby library for Open311](http://rubygems.org/gems/open311), built by Dan Melton and Erik Michaels-Ober. The PHP library is currently being used to create an updated Open311 Facebook application and an [Open311 plugin for Ushahidi](https://github.com/tskochanski/Open311-Plugin-for-Ushahidi).

### Open311 Facebook App

Stanford Rosenthal updated San Francisco&#8217;s 311 Facebook app. Henry Jiang, who built the initial Facebook app for the City of San Francisco, worked closely with Stanford on the updated application. It now works with the latest version of the API. Also, with Dave Mitchell&#8217;s help, the Facebook application has been extended to work in Boston.

San Francisco implemented the application and a demo can be found here: <http://apps.facebook.com/sf_requests>

We see great potential for the development of Open311 from the entire community, and we&#8217;re excited to continue working on it this year and into the future.