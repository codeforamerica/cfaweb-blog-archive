---
id: 9488
title: See Click Mural
date: 2011-10-21T12:24:30+00:00
author: John Mertens
layout: post
guid: http://codeforamerica.org/?p=9488
permalink: /2011/10/21/see-click-mural/
dsq_thread_id:
  - 449780674
categories:
  - CfA Labs
  - Philadelphia
---
[<img class="alignleft size-full wp-image-9492" title="seeclickmural" src="http://codeforamerica.org/wp-content/uploads/2011/10/seeclickmural.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/10/seeclickmural.png)Moments after giving a talk on open data and code reuse at the Code for America Summit, Ben Berkowitz (SeeClickFix) and Aaron Ogle (CfA) grabbed me and said, &#8220;can we make a simple map mashup of all the murals verses graffiti reports in Philly?&#8221;

Of course we can. And, of course, we can do it with free and open source resources.

I give you <a title="SeeClickMural" href="http://seeclickmural.herokuapp.com/" target="_blank">SeeClickMural</a>.  I&#8217;m not exactly sure what correlations come up, but it is an interesting exercise in quickly combining multiple feeds of open data.

Here&#8217;s how we did it:

  * The graffiti reports came from this <a href="http://seeclickfix.com/philadelphia/issues?end_date=Any&format=json&num_results=500&page=1&search=graffiti&sort=issues.created_at&start_date=Any&status%5BAcknowledged%5D=true&status%5BArchived%5D=true&status%5BClosed%5D=true&status%5BOpen%5D=true&at=philadelphia+pa" target="_blank">SeeClickFix feed</a>.
  * The mural data came from MuralFarm.org (via <a href="http://x.iriscouch.com/murals/_design/geo/_spatiallist/geojson/full?bbox=-180,-90,180,90" target="_blank">this geocouch instance</a>).
  * The actual map uses <a title="Polymaps homepage" href="http://polymaps.org/" target="_blank">Polymaps</a> (from <a title="SimpleGeo" href="http://simplegeo.com/" target="_blank">SimpleGeo</a> & <a title="Stamen" href="http://stamen.com/" target="_blank">Stamen</a>).
  * The backend and frontend framework came from <a href="https://github.com/zachwill/flask_heroku" target="_blank">zachwill&#8217;s flask_heroku</a>.  It is a dead-simple way to setup a static web server with the best of HTML5 boilerplate and bootstrap CSS already baked in &#8211; and all of it is ready for deployment to Heroku. (btw Zach is a 2012 CfA fellow.)

[cc-mkplc app="SeeClickFix"]