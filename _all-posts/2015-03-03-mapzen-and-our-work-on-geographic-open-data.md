---
id: 32812
title: Mapzen and our work on geographic open data
date: 2015-03-03T17:02:54+00:00
author: Michal Migurski
layout: post
guid: http://www.codeforamerica.org/blog/?p=32812
permalink: /2015/03/03/mapzen-and-our-work-on-geographic-open-data/
categories:
  - Data
  - Maps
  - News
---
[Mapzen](https://mapzen.com) has been supporting Code for America’s work on geographic open data for the past half-year.

> &#8220;Land parcels are the atomic unit of government&#8217;s view of the physical world.&#8221;

We began our collaboration with Mapzen at the idea of research for an open parcels data standard. Land parcels are important, they are the atomic unit of government’s view of the physical world. It’s also a confusing term, as we learned talking with experts like Nancy Von Meyer of [Fairview Industries](http://www.fairview-industries.com).

There are ownership parcels, rights parcels, assessment parcels, usage & zoning parcels tracked at many different levels. For Code for America&#8217;s interest in economic development, real estate, or tax parcels looked like they could be very valuable. Parcel datasets might include information about ownership, value, tax rate, and relationship to municipal zoning codes that can help established and new businesses choose locations. Easy-to-understand data on parcels would be useful to entrepreneurs, residents, and civic startups like [Open Counter](http://opencounter.us) and their [Zoning Check product](http://zoningcheck.us).

The problem is that open standards are a notoriously tough nut to crack, and we did not want to end up with yet another unused standard in a world with many existing standards. This problem is shown well in the below xkcd cartoon:

[![standards](http://www.codeforamerica.org/blog/wp-content/uploads/2015/02/standards.png)
  
XKCD, No. 927](http://xkcd.com/927/)

> [Transcript](http://www.explainxkcd.com/wiki/index.php/927:_Standards): How Standards Proliferate
> 
> (See: A/C chargers, character encodings, instant messaging, etc.)
  
> Situation: There are 14 competing standards.
  
> Cueball: 14?! Ridiculous! We need to develop one universal standard that covers everyone&#8217;s use cases.
  
> Ponytail: Yeah!
  
> Soon:
  
> Situation: There are 15 competing standards.

So, we chose to look at existing data via an ongoing project, [OpenAddresses](http://openaddresses.io), to decide what we could learn from data that’s already open and available to use. Addressing and parcels are not the same thing, but in a country of single-family homes they overlap significantly enough to be worthwhile. Land parcels are a common source of open data used in the year-old OpenAddresses project, and addresses are a crucial component of any full-stack mapping service. Georeferenced address services come up every year in Code for America’s fellowship program, most recently in [Team Lexington’s 2014 Streetscope project](https://github.com/codeforamerica/streetscope/).

[OpenAddresses](http://openaddresses.io), started by Ian Dees in spring 2014, is a worldwide searchable database of roughly 100 million address points. It collects publicly available, open land parcel and address data, and produces a single output file that covers the world.

[![Map of OpenAddresses coverage](http://www.codeforamerica.org/blog/wp-content/uploads/2015/02/render.png)](http://data.openaddresses.io)

Based on experience from the early days of [OpenStreetMap](http://openstreetmap.org), we believe that providing a visible peek into the state of the project will spur contributions, so we’ve been working to build and improve [data.openaddresses.io](http://data.openaddresses.io), a service that makes it much easier to see the result of adding data to the OpenAddresses database. It does this by performing continuous integration on the OpenAddresses database, automatically building it and visually showing the changes every two days.

We’ve been running this process since the beginning of November, 2014. It’s helped OpenAddresses to identify and fix issues in many data sources:

[![OpenAddresses growth over time](http://www.codeforamerica.org/blog/wp-content/uploads/2015/02/openaddresses-totals.png)](http://www.codeforamerica.org/blog/wp-content/uploads/2015/02/openaddresses-totals.png)

We’ve created a positive feedback mechanism to accelerate OpenAddress’s growth, and a place to collaborate with other members of the open data community like Tom Lee, Nick Ingalls, Nelson Minar, and OpenAddresses founder Ian Dees. Our close relationship with Mapzen allowed us to identify OpenAddresses as a place where we could make a difference in the quality and quantity of foundational open data for the civic ecosystem.

What&#8217;s next? If you&#8217;re a data owner at the city or county level, it&#8217;s a great time to contribute to Open Addresses and help build a valuable piece of open geographic data infrastructure. To get started and add a source, check out <http://openaddresses.io/contribute/>.