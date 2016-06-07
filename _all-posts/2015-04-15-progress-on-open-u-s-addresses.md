---
id: 33094
title: Progress on Open U.S. Addresses
date: 2015-04-15T01:39:43+00:00
author: Tom Lee
layout: post
guid: http://www.codeforamerica.org/blog/?p=33094
permalink: /2015/04/15/progress-on-open-u-s-addresses/
categories:
  - News
---
_Cross-posted from  [Progress on Open U.S. Addresses on the Mapbox blog](https://www.mapbox.com/blog/us-national-address-summit/). Read more about Code for America’s work on open data and OpenAddresses at [Mapzen and our work on geographic open data](http://www.codeforamerica.org/blog/2015/03/03/mapzen-and-our-work-on-geographic-open-data/)._

The National Address Database Summit wrapped up last week. For two days about a hundred people from private, federal, state, county, city and tribal authorities came together to talk about creating a unified source for U.S. address data. After that much conversation it’s clear that there’s plenty of work to be done. But the levels of enthusiasm and agreement on hand were great news for anyone who cares about open data.

![](https://farm8.staticflickr.com/7610/16912889830_7231dd7789_d.jpg)

The need for better address data has been obvious for a while – [this GAO report](http://www.gao.gov/assets/670/668493.pdf) covers the situation well. An address database can seem like an abstract topic. But U.S. Department of Transportation’s CIO Richard McKinney opened the day with a story about flagging down an ambulance coming to help his father that was lost in foggy weather. That made the case for fixing this problem much more concrete.

A usable, unified set of addresses is a piece of national infrastructure that becomes more important by the day, and right now we don’t have one. A combination of bureaucratic, legal and organizational challenges have stood in the way of fixing this problem. The Department of Transportation convened the summit to find a way through those roadblocks.

Everyone quickly agreed on three things:

  * The database must be open
  * Address data has to be created and maintained at the local level
  * A unified database would save government money and [unlock economic value](http://data.worldbank.org/sites/default/files/1/value-assessment-danish-address-data-uk-2010-07-07b.pdf)

There are technical questions that remain unanswered. Should 3D addressing be supported? Parcel polygons, or just points? How many different input formats will have to be supported? What metadata needs to be captured? Plenty of careful thought has already been given to these and [related problems](https://www.fgdc.gov/standards/projects/FGDC-standards-projects/street-address/index_html).

But although anticipating questions like these is important, there’s a risk of premature optimization and overspecification whenever the government designs a new system. For instance, concerns were repeatedly raised about the security of personal information. But no one could actually explain how publishing an address and coordinate pair – both observable from the street – might endanger anybody. Committee meetings and big spec documents are poor substitutes for working prototypes.

Luckily, we already have a working prototype. [Ian Dees](http://www.ian.dees.name/) was on hand to talk about [OpenAddresses.io](http://openaddresses.io), and explained how it satisfies the most important goals of a national address database. There’s more work to be done to make a system that meets all the needs of government. But with over 118 million address points, [open collaboration with governments](https://github.com/openaddresses/openaddresses/issues/344#issuecomment-52983936), and data that’s in real-world production use, officials should take a serious look at using OA as a model for – and perhaps an initial version of – a U.S. national address database.

The most important unanswered questions are structural. Local governments are ready to help if they’re given resources and leadership. But who has the funding, authority and technical chops to lead such an effort? That challenge will have to be met by some smart civil servants. The open data community is ready to help with the rest.

_Photo by [Michael Coghlan](https://www.flickr.com/photos/mikecogh/7589477990/)_