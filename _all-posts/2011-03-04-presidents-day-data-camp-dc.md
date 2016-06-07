---
id: 4099
title: 'Presidents&#8217; Day Data Camp DC'
date: 2011-03-04T06:00:38+00:00
author: Jeremy Canfield
layout: post
guid: http://codeforamerica.org/?p=4099
permalink: /2011/03/04/presidents-day-data-camp-dc/
dsq_thread_id:
  - 245449361
categories:
  - Dispatches
  - News
tags:
  - dc
---
Across the country, Presidents&#8217; Day is known for the sales that car makers and clothiers hold to draw consumers out of their post-holiday budget freeze. D.C. has always been a little bit different, though. This is a town that watches election results like most watch the Superbowl. In the morning, a contingent of people from around the region converged on Petworth in Northwest D.C., not to snag the latest shoes or wheels, but to engage in a different kind of consumption. Data consumption.

<img class="alignright size-medium wp-image-4134" title="datacampers" src="http://codeforamerica.org/wp-content/uploads/2011/03/photo-1-300x225.jpg" alt="civic hackers hacking happily" />

On Monday, in partnership with DevHouseDC and Big Window Labs, Code for America&#8217;s DC team held a Presidents&#8217; Day Data Camp. The event brought together a couple dozen data geeks, civic hackers, and open government aficionados. It was a brilliant opportunity to learn and explore the open data released in and around our fair District. After some coffee and mingling, we kicked it off unconference-style with a three word intro from each of our eager hackers. Then the real fun began.

Jessy Kate, ring leader of DevHouseDC and one of the premier hacker-organizers about town led us in a brainstorming session, linking up the potential civic data projects the campers thought-up with the campers who had skills or energy to contribute. After a short huddle, we identified topics and data sets we wanted to set upon: homelessness, transit, nutrition data, food availability, and restaurant inspection garnered the most interest.  The campers formed into groups around these and began digging in. Mostly, we spent the first part of the day just researching, formulating and scoping the project. Then, once a reasonable amount of research was done, the teams started the hard work of coding up their projects. Because the data is not always in a format that computers can easily read, translating this can require a good deal of effort and is often a solid project for a data day by itself.  Nevertheless, by lunch break most of the projects were already coming together; the restaurant inspection data, for instance, was not only found but a version 1 scraper was already chewing it&#8217;s way through DC&#8217;s inspection records.

[<img class="alignleft size-medium wp-image-4132" title="in the eye of the hacking, redvines and clementines" src="http://codeforamerica.org/wp-content/uploads/2011/03/photo-3-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/03/photo-3.jpg)Some people floated between the groups, grazing off the collective wisdom of a vibrant community of hackers, others focused on one project for the day. Some helped out by pointing us to similar projects or ideas (Alex Howard, we&#8217;re looking at you). By day&#8217;s end, we had had a lot of fun, eaten some pizza, sandwiches, learned a ton of new tools and data sets, and most importantly, introduced a few new faces to the civic hacker scene in DC. The day was meant to help teach ourselves new skills and build community and not necessarily to produce results, but there were still some pretty amazing accomplishments for one days worth of coding.

Check out our group [brainstorming](http://meetingwords.com/cONVyW6Y4A).  Or read on to find out all the awesome projects our intrepid civic hackers were able to put together.

### [Homeless Helper Hot Meals data set](http://scraperwiki.com/scrapers/dcfoodrss/)

[<img class="alignleft size-medium wp-image-4144" title="Services for Homeless in DC" src="http://codeforamerica.org/wp-content/uploads/2011/03/Screen-shot-2011-03-02-at-11.38.32-AM-300x242.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/03/Screen-shot-2011-03-02-at-11.38.32-AM.png)This project created a data set to feed [AppForTheHomeless](http://appforthehomeless.com/), a mobile app (previously developed) that allows passersby the ability to point homeless people to nearby services, such as hot meals, shelters and assistance. After some serious [spec work](https://docs.google.com/a/codeforamerica.org/document/d/1mX9esOQ2sIyHU1Z-iFOFbpzRBpfEX94v0gHOroDFgjo/edit?hl=en&authkey=CLDU75EF#), the team built a scraper: an app which grabs a [feed](http://creatorexport.zoho.com/showRss.do?viewlinkId=3&fileType=rss&link=true&complete=true&sharedBy=dcfoodfinder) of the locations of hot meals and transforms the data into a nicely formed [data set](http://scraperwiki.com/scrapers/dcfoodrss/) for inclusion into the app, or any other app that wants it. Built by Michelle Koeth (CfA) and Chris Gotcu, AppForTheHomeless built by Scott Johnson.

### [DC Foodshed Map](http://dcfoodshed.appspot.com/)

[<img class="alignleft size-medium wp-image-4136" title="Foodshed Maps" src="http://codeforamerica.org/wp-content/uploads/2011/03/Screen-shot-2011-03-01-at-9.49.41-AM-300x272.png" alt="Map of food deserts in Washington, D.C." />](http://codeforamerica.org/wp-content/uploads/2011/03/Screen-shot-2011-03-01-at-9.49.41-AM.png)The DC Foodshed Map displays the areas in DC that have good access to fresh food and groceries (and those that don’t). Green dots identify grocery stores, the surrounding green circles represent a 1/2 mile, and the red circles represent 3/4 mile. These distances are based on ease of transporting groceries for shoppers who would be walking or taking public transportation  The project started with a data set from [data.dc.gov](http://data.dc.gov/) for the [locations of grocery stores](http://data.dc.gov/Metadata.aspx?id=2220). Led by Michael Bernstein (CfA) with help from Kate Chapman on data transformation and mapping and Kelli Shewmaker on the copy explaining the map.

&nbsp;

### [The Nutritional Index App](https://bitbucket.org/tauberer/foodnut/src)

<img class="alignleft size-medium wp-image-4135" title="Food Browser" src="http://codeforamerica.org/wp-content/uploads/2011/03/nutrition-300x228.png" alt="2 axis food browser" />

Another project explored nutrition, though from a very different angle. This project created a website that visualizes food items from the USDA National [Nutrient Database](http://www.ars.usda.gov/Services/docs.htm?docid=8964).  Food items can be explored vertically on a heart-healthy dimension that ranks foods on a nutrients-per-calorie scale. And food items can be explorer horizontally to browse through different types of foods. The horizontal axis, which didn&#8217;t turn out as useful as hoped, is based on a statistical &#8220;dimensionality reduction&#8221; technique from the original nutrient data. Images are pulled from Google Image Search. The app&#8217;s current code, built by Chris Musialek and Josh Tauberer is [here](https://bitbucket.org/tauberer/foodnut/src).

### The [DC Health Inspection Map](http://geocommons.com/maps/54678) and App

[<img class="alignleft size-medium wp-image-4143" title="Health Inspection Map" src="http://codeforamerica.org/wp-content/uploads/2011/03/Screen-shot-2011-03-02-at-11.27.39-AM-300x256.png" alt="where not to eat" />](http://codeforamerica.org/wp-content/uploads/2011/03/Screen-shot-2011-03-02-at-11.27.39-AM.png)Another group also attacked the food, (it&#8217;s worth noting that everyone decided what they were going to work on before lunch arrived) but from yet a different angle. This group tackled it from the food safety perspective, parsing the [health inspection records](http://washington.dc.gegov.com/webadmin/dhd_431/web/index.cfm) of D.C.&#8217;s eateries, correlating those with Yelp&#8217;s data on customer restaurant reviews (the [idea](http://eaves.ca/2011/01/31/how-yelp-could-help-save-millions-in-health-care-costs/) came from David Eaves, who suspects integrating inspection data with restaurant reviews could save millions in health care costs), and mapping it. D.C. uses a risk rating for its inspections, with a 5 indicating the highest risk, and 1 the lowest. Travis Pinney, with help from Kate Chapman, parsed and cleaned [the data](http://www.google.com/fusiontables/DataSource?snapid=143817) ([scraper code](https://github.com/tlpinney/foodscrape/)), Sean Gorman took it and developed a [sweet map](http://geocommons.com/maps/54678), Aaron Frank and Jeremy Canfield ported it to [ScraperWiki](http://scraperwiki.com/scrapers/dcrestaurantinspection/) and worked on some [javascript](http://jsfiddle.net/m9TRa/7/) to integrate the restaurant inspections with Yelp, which is still in progress.

<a href="http://geocommons.com/maps/54678" target="_blank"></a>

Of course that wasn&#8217;t all we worked on, and a number of projects wound up finding existing solutions to the problems they set out to solve, or discovered that the problem was a bit too big to take on for one day.

All told, not bad for a day&#8217;s work. Too bad about missing all those Presidents&#8217; Day sales, though.