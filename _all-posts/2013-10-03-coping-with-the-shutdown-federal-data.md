---
id: 26490
title: 'Coping with the Shutdown: Federal Data'
date: 2013-10-03T00:42:14+00:00
author: Michal Migurski
layout: post
guid: http://www.codeforamerica.org/?p=26490
permalink: /2013/10/03/coping-with-the-shutdown-federal-data/
categories:
  - Data
  - News
---
The Federal Government has shut down operations. It’s not the first such event (there were [three in 1977 alone](http://www.washingtonpost.com/blogs/wonkblog/wp/2013/09/25/here-is-every-previous-government-shutdown-why-they-happened-and-how-they-ended/ "Here is every previous government shutdown, why they happened and how they ended")), though it does have [certain unique characteristics](http://www.theatlantic.com/politics/archive/2013/09/your-false-equivalence-guide-to-the-days-ahead/280062/ "Your False-Equivalence Guide to the Days Ahead"). Leaving the politics aside for the moment, what’s a civic hacker or data journalist to do [when most of the government web and FTP presence is unreachable as well](http://shutdowngov.tumblr.com/ "Shutdown.gov")?

[<img class="size-medium wp-image-26494  alignleft" title="U.S. On Verge Of Full-Scale Government Hoedown (The Onion)" alt="U.S. On Verge Of Full-Scale Government Hoedown (The Onion)" src="http://www.codeforamerica.org/wp-content/uploads/2013/10/government-hoedown-300x169.jpg" />](http://www.theonion.com/articles/us-on-verge-of-fullscale-government-hoedown,34057/?ref=auto)

We have two responses brewing at Code for America.

Team 2013 Las Vegas and other fellows have been iterating on an API for the [North American Industry Classification System](http://web.archive.org/web/20130929215439/https://www.census.gov/eos/www/naics/ "North American Industry Classification System") (NAICS) for use in their city project. Normally available as a series of Excel spreadsheet files, Lou Huang and team have developed a simple JSON-based API for searching and accessing this useful data and made it available at [NAICS.us](http://naics.us/). The source code behind the service is available under [GitHub.com/codeforamerica](https://github.com/codeforamerica/naics-api). We’d been adding documentation and search capabilities when the government shutdown began, but it’s an opportune time to push it out of the nest early.

In the land of U.S. Census geographic and demographic data, the FTP server at [ftp.census.gov](ftp://ftp.census.gov) is ordinarily a stable repository of extensive, high-quality files in downloadable ZIP form. This week, it’s unresponsive for the foreseeable future.

A community of census data users have worked with Code for America to [pool their collected backups](http://forever.codeforamerica.org/Census-API/shutdown-2013.html) and made them available online in lieu of the normal Census.gov service. [IRE Census Reporter](http://censusreporter.org/) developer Ian Dees has set up a [selection of 2012 data hosted on Amazon S3](https://census-backup.s3.amazonaws.com/index.html "Census Backup"). Experimental cartographer Eric Fischer has made available his [complete collection of 2013 TIGER/Line edge shapefiles](http://trafficways.org/tiger/edges/). CUNY Mapping Service director Steven Romalewski supplied [2013 districts](http://forever.codeforamerica.org/Census-API/shutdown-2013-districts-2013.html). @OpenNebraska sent [2012 TIGER/Line edges](http://forever.codeforamerica.org/Census-API/shutdown-2013-tiger-2012.html). Darrell Fuhriman provided valuable [demographic summary files](http://forever.codeforamerica.org/Census-API/shutdown-2013-data-2010-2011.html) from 2010. GeoCommons reminded us that [6,000 Census-derived datasets can be found on their service](http://geocommons.com/search?query=census).

This potluck-style process highlights the survivalist-style utility of big, dumb physical servers with actual hard drives. I think of my neighbor’s rain-catchment system, the chest freezer in the basement or my recently-earned Ham Radio license and laugh, but [Sunlight Foundation’s Eric Mill reminds us of the critical role of bulk data](http://sunlightfoundation.com/blog/2013/10/02/government-apis-arent-a-backup-plan/ "Government APIs Aren't A Backup Plan"):

> The only reliable way to preserve data online is to make copies — and the more copies, the better!
> 
> That&#8217;s why **a government API will never be enough**. It&#8217;s just so much easier to copy data when it&#8217;s directly downloadable in bulk. APIs can be extremely useful, but they also centralize control and form a [single point of failure](http://fcw.com/articles/2013/10/01/private-sector-apps-api-shutdown.aspx). Ultimately, [APIs are optional](http://sunlightfoundation.com/blog/2012/03/21/government-do-you-really-need-an-api/) — data is a necessity.
> 
> …
> 
> Just as importantly: hosting static files requires fewer people, smaller systems, and less technical expertise. It&#8217;s vastly simpler and cheaper than hosting a live, &#8220;smart&#8221; data service. In the face of hard funding decisions, that&#8217;s going to matter.

We’re not exactly [getting our mail from Kevin Costner](http://en.wikipedia.org/wiki/The_Postman_(film)) yet, but these real and direct consequences of the federal shutdown remind us of the fragile pieces loosely joined that make up our digital platforms. Whether caused by GOP deadlock or [east coast electrical storms](http://aws.amazon.com/message/67457/), the data and services we build on are periodically stressed. What are you doing to prepare for the unexpected?

* * *

Questions? Comments? Hit us up [@codeforamerica](http://twitter.com/codeforamerica).