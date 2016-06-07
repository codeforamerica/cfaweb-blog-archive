---
id: 8191
title: 'Blake&#8217;s CfA Summer'
date: 2011-08-30T06:28:50+00:00
author: Blake Hall
layout: post
guid: http://codeforamerica.org/?p=8191
permalink: /2011/08/30/blakes-cfa-summer/
dsq_thread_id:
  - 399967811
categories:
  - 2011 Interns
  - News
---
This summer I worked with four other interns on building up Code for America&#8217;s Developer Tools. We found a bunch of open Government APIs for different agencies and dataset. We then built wrappers for the APIs to allow developers better access to the data. 

Justin Stoller &#8212; a fellow intern &#8212; and I worked on making Ruby Gems for the [World Bank](https://github.com/codeforamerica/world_bank_ruby), [Fed Spending](https://github.com/codeforamerica/fed_spending_ruby), [EPA EnviroFacts](https://github.com/codeforamerica/epa_python), NTIA &#038; FCC&#8217;s <a href="http://broadbandmap.gov/" target="_blank">BroadbandMap.gov</a>, and a few others. I then built a quick little web app to help demonstrate some of the [broadband data](https://github.com/codeforamerica/broadband_map_ruby) that you can access: <http://compare-broadband.heroku.com/>

[<img src="http://codeforamerica.org/wp-content/uploads/2011/08/wireless.png" alt="" title="wireless" width="610px" class="aligncenter size-full wp-image-8192" />](http://compare-broadband.heroku.com/)

The app, [Compare Broadband](http://compare-broadband.heroku.com/), uses the <a href="http://broadbandmap.gov/" target="_blank">BroadbandMap.gov</a> gem I wrote to check to locations against <a href="http://broadbandmap.gov/" target="_blank">broadbandmap.gov</a>&#8216;s data and return a comparison of each locations broadband providers, both wireline and wireless, as well as each provider&#8217;s advertised speeds. This is just a minuscule example of what can be done using these government API&#8217;s that can now be accessed easily through our gems, eggs, and libraries.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/08/broadband-1024x279.png" alt="" title="broadband" width="610px" class="aligncenter size-large wp-image-8193" />](http://compare-broadband.heroku.com/)

_(Over the summer of 2011, [over a dozen students interned](http://codeforamerica.org/2011/06/15/meet-the-2011-cfa-interns/) with Code for America. They brought great energy, passion, and skills to bear on our projects and our mission to make government more open and efficient. Over the next week, we’ll be posting their summaries of their work and learnings, in addition to an overview of the summer.)_