---
id: 7910
title: 'Farmers&#8217; Market API'
date: 2011-08-08T14:13:25+00:00
author: John Mertens
layout: post
guid: http://codeforamerica.org/?p=7910
permalink: /2011/08/08/farmers-market-api/
dsq_thread_id:
  - 380546428
categories:
  - CfA Labs
tags:
  - labs
---
[<img class="alignleft size-full wp-image-7918" title="Farmers-Market-Map" src="http://codeforamerica.org/wp-content/uploads/2011/08/Farmers-Market-Map1.png" alt="" />](http://usda.iriscouch.com/farmers_markets/_design/geo/_rewrite/#4.57/39.256/-96.913)

I love getting my fruit and veggies from my local Farmer&#8217; Market. Unfortunately, as a recent SF transplant I wasn&#8217;t sure how to find my local Farmers&#8217; Market. A quick search led me to a <a title="USDA AMS Farmers' Market Search" href="http://search.ams.usda.gov/farmersmarkets/" target="_blank">USDA website which seemed to contain most of the markets in the country</a>.

Being an open data geek, I looked for an API. Finding none, I decided to [make one](http://usda.iriscouch.com/farmers_markets/_design/geo/_spatiallist/geojson/full?bbox=-122.61248930742187,37.655669842383595,-122.24788054277343,37.83240550745524). To do this, I:

  1. Used the &#8220;Export to Excel&#8221; function to download the whole dataset.
  2. Cleaned it up in <a title="Learn more about Google Refine" href="http://code.google.com/p/google-refine/" target="_blank">Google Refine</a>; normalized some fields, geocoded some records, added a geojson fields.
  3. Uploaded it to a <a title="Free CouchDB hosting " href="http://iriscouch.com" target="_blank">free couchdb instance</a>.
  4. Added the open source <a title="Download from GitHub" href="https://github.com/maxogden/geocouch-utils" target="_blank">geocouch-utils</a> CouchApp (which gives you a <a title="The Farmers' Markets Map" href="http://usda.iriscouch.com/farmers_markets/_design/geo/_rewrite/#4.57/39.256/-96.913" target="_blank">nice map out of the box</a>).

All of this was done in about an hour and at a cost of $0.

So if you&#8217;re a developer who also likes fresh fruit & veg, build something [on it](http://usda.iriscouch.com/farmers_markets/_design/geo/_spatiallist/geojson/full?bbox=-122.61248930742187,37.655669842383595,-122.24788054277343,37.83240550745524). I&#8217;ll be <a title="Info on the Fillmore Farmers' Market" href="http://www.pcfma.com/market_home.php?market_id=13" target="_blank">down on Fillmore</a>.