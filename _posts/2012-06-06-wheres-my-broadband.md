---
id: 13226
title: 'Where&#8217;s My Broadband?'
date: 2012-06-06T17:53:27+00:00
author: Nick Doiron
layout: post
guid: http://codeforamerica.org/?p=13226
permalink: /2012/06/06/wheres-my-broadband/
dsq_thread_id:
  - 716328398
categories:
  - 2012 fellows
  - Commentary
  - Macon
  - News
---
Since 2011, federal agencies have surveyed Americans&#8217; access to broadband on BroadbandMap.gov. In addition to visualizations on their website, you can [download shapefiles for each state](http://www.broadbandmap.gov/data-download "BroadbandMap.gov shapefile download").

<img class="alignright size-medium wp-image-13492" title="Broadband Gap on a Map" src="http://codeforamerica.org/wp-content/uploads/2012/05/Screen-Shot-2012-05-24-at-10.41.40-AM-300x207.png" alt="Broadband Gap on a Map" />

When I first searched for Macon (my CfA partner city), I saw that most of the city was covered by multiple Internet Service Providers (ISPs). What surprised me were hundreds of gaps &#8211; big and small &#8211; which had been carved out of their service areas. High-speed internet might be available on one block but not the next.

Some of these gaps are lakes, highways, and railyards &#8211; areas without potential subscribers. What concerned me were neighborhoods and business complexes without internet access. Residents of these areas are finding themselves on the losing side of the [digital divide](http://codeforamerica.org/2012/05/24/does-the-digital-divide-have-a-silver-lining/ "Digital Divide Article"). How can we make sense of these maps and advise policy-makers?

A tentative answer to that question is [BBandXplor](http://bbandxplor.heroku.com "BBandXplor"), a crowdsourcing app using Google Street View. When volunteers look inside each broadband dead zone, they can identify and report which ones have houses and businesses that would benefit from faster internet access. [<img class="alignright size-medium wp-image-13491" title="Broadband Gap on StreetView" src="http://codeforamerica.org/wp-content/uploads/2012/05/Screen-Shot-2012-05-24-at-10.43.41-AM-300x179.png" alt="Broadband Gap on StreetView" />](http://codeforamerica.org/wp-content/uploads/2012/05/Screen-Shot-2012-05-24-at-10.43.41-AM.png)

The source code is [available on GitHub](https://github.com/codeforamerica/BBandXplor), complete with directions on how to set it up for your own city.

Much thanks to OpenPlans&#8217;s [Beautiful.st](http://beautiful.st) for inspiration, and the NTIA and FCC for their excellent broadband data.