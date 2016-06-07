---
id: 18517
title: Demolition hotspots and smarter data
date: 2012-11-14T18:31:10+00:00
author: Nick Doiron
layout: post
guid: http://codeforamerica.org/?p=18517
permalink: /2012/11/14/demolition-hotspots-smarter-data/
categories:
  - 2012 fellows
  - Macon
  - News
  - Open Data
  - San Francisco
---
One thing that stands out about San Francisco is its neighborhoods. Months after moving to the city, I still hear of new neighborhoods and their specialties. There are some projects for digital maps that make sense of fuzzy neighborhood boundaries &#8211; maps using [online consensus](http://hood.theory.org/) or [Flickr geotags](http://www.crowdsourcing.org/document/exploring-place-through-user-generated-content-using-flickr-tags-to-describe-city-cores/6396/36). For the most part, though, our datasets are oblivious to the streets intertwining below them.

I tried feeding one of these datasets into [Neo4j](http://neo4j.org/learn/), a NoSQL network database, to search for food deserts and demolition hotspots in my partner city: Macon, Ga. It&#8217;s hard to pick a high-risk neighborhood out of a spreadsheet or a list of coordinates.

Once you broaden the scope of the data to include connecting streets, the immediate neighborhood adds context, hints at whether a street connects to a major artery or a maze of back roads, reveals whether a condemned house is around the corner or across a highway.

The project showed that among houses cited by the City, neighborhoods of demolished houses stood out. Where most cited houses had 0-5 demolished houses in their network, networks of demolished houses peak at around 10-12 demolitions.

![](http://demodexter.herokuapp.com/images/DemosInDemoNetworks.png)

**What else might we see in data tied to streets instead of spreadsheets?**

I&#8217;m launching an experimental site and API for San Francisco called [DemoDexter](http://demodexter.herokuapp.com). At its core are 2,800 streets from [OpenStreetMap](http://openstreetmap.org). Each street is open for you to add your own data and get analysis back.

_Two examples:_

I added a &#8220;BART&#8221; tag to every street with a BART station. An API endpoint (/access/bart) helps map streets by how many links away they are from a station:

&nbsp;

<img class="aligncenter size-full wp-image-18776" title="SF BART Access" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-13-at-9.49.36-AM.png" alt="SF BART Access Map" />

[Link to interactive map](http://tiles.mapbox.com/mapmeld/map/sfbart)

Jessica, another Code for America fellow, told me that urban planners are concerned about choice. People are happiest when they have access to multiple supermarkets and parks, not just one nearby. Here&#8217;s a different map from the API, with streets color-coded by access to the two closest Chipotles (/choice/chipotle). Streets off of <a href="https://maps.google.com/maps?q=market+street+sf&ll=37.781027,-122.411385&spn=0.173391,0.339546&fb=1&gl=us&hq=market+street&hnear=San+Francisco,+California&t=m&fll=37.781027,-122.411385&fspn=0.173391,0.339546&z=12" target="_blank">Market Street</a> have bright color-coding, while those near the <a href="http://en.wikipedia.org/wiki/Sunset_District,_San_Francisco" target="_blank">Sunset&#8217;s</a> one Chipotle are more subdued.

&nbsp;

<img class="aligncenter size-full wp-image-18777" title="SF Chipotle Choice" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-13-at-9.52.36-AM.png" alt="SF Chipotle Choice Map" />

[Link to interactive map](http://tiles.mapbox.com/mapmeld/map/BARTChoice)

[DemoDexter](http://demodexter.herokuapp.com) is open if you&#8217;d like to add tags showing how neighborhoods are served by [local libraries](http://tiles.mapbox.com/mapmeld/map/LibraryAccess), farmers&#8217; markets, or hackerspaces. If you have the right datasets, you could search for hotspots of business development or blight. For other cities, such as [Oakland](http://oaklandexter.herokuapp.com), take the code [from GitHub](https://github.com/codeforamerica/DemoDexter) and the underlying street map from Michal Migurski&#8217;s [OpenStreetMap metro extracts](http://metro.teczno.com/).

&nbsp;

Questions? Comments? Hit us up <a href="http://twitter.com/codeforamerica" target="_blank">@codeforamerica</a>.