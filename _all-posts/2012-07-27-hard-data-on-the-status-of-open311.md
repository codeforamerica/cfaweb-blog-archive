---
id: 15322
title: Hard Data on the Status of Open311
date: 2012-07-27T18:01:34+00:00
author: Ben Sheldon
layout: post
guid: http://codeforamerica.org/?p=15322
permalink: /2012/07/27/hard-data-on-the-status-of-open311/
dsq_thread_id:
  - 782633176
categories:
  - 2012 fellows
  - News
  - Open Gov
  - Open Source
  - Open311
---
<p style="text-align: center;">
  <a href="http://open311status.herokuapp.com"><img class="aligncenter size-full wp-image-15324" title="open311status.herokuapp" src="http://codeforamerica.org/wp-content/uploads/2012/07/open311status.herokuapp.png" alt="" width="100%" /></a>
</p>

With the recent announcement of [311 Labs](http://codeforamerica.org/2012/07/12/hello-311-labs/) and Code for America&#8217;s recent [podcast featuring me](http://codeforamerica.org/2012/07/23/open311-reality-check-how-usable-is-the-api-for-developers/) talking about my perspective on Open311, this write-up about [Open311Status](http://open311status.herokuapp.com) is probably long overdue.

[Open311Status](http://open311status.herokuapp.com)&#8212;still a work in progress&#8211;polls Open311 servers in 30 cities and aggregates configuration, performance and utilization statistics about those Open311 endpoints. I built Open311Status for two reasons: first, to provide a high-level view of how different endpoints are performing as a developer sanity check (&#8220;is my app broken or the server?&#8221;); and second, to provide some hard data to the anecdotes and experiences I&#8217;ve used in [advising the City of Chicago](http://codeforamerica.org/2012-partners/chicago/) and others in how to improve Open311&#8242;s potential for positive impact in their cities and beyond.

In designing Open311Status I took advantage of the huge benefit of the Open311: interoperability. By adopting the Open311 API for exposing civic data, cities are enabling civic developers like myself to build reusable tools and apps. To access data from 30 cities, Open311Status doesn&#8217;t need an adapter for each individual city, [only a server URL](https://github.com/codeforamerica/open311status/blob/master/lib/endpoints.json) that it can expect to interact and deliver data in the same way as described by the [Open311 API documentation](http://wiki.open311.org/GeoReport_v2). Sure, there are some minor interoperability issues (for example, [Toronto doesn&#8217;t like datetimes submitted with milliseconds](http://tracker.open311.org/ticket/95)), but these have been minor speed bumps for development, not major deal breakers.

A major limiting factor in the utility of Open311 isn&#8217;t these minor technical issues, but in how the Open311 servers are configured. If Open311 is supposed to provide a rich API for developers to interact with there should be a broad number of categories (&#8220;types&#8221;) of requests that can be submitted, as well as a comprehensive listing of previously submitted requests that can be analyzed or dashboarded. Compare the Boston and Washington, D.C. Open311 implementations: Washington, D.C. currently provides 83 categories of service requests (from &#8220;Tree Inspection&#8221; to &#8220;Roadway Marking Maintenance&#8221;) while Boston only provides six. Washington, D.C. provides access to all requests regardless of whether they were entered via Open311, the 311 call center, or city work crews or departments; Boston only displays service requests made via the Open311 API. These configuration decisions have a huge impact on the comprehensiveness of the data and thus the potential applications third party developers can build on top of the Open311.

If server configuration determines the potential for an innovative application, server performance determines whether such an app will be useable. Because a potential Open311 application will be heavily reliant upon a city&#8217;s Open311 server, the speed and robustness of that server will determine the responsiveness of the application. At the obvious extreme, if the server goes down, that app will probably be useless. If the server is functioning yet takes several seconds to respond to every request, the application and its users will experience significant slow-downs and frustration. As I&#8217;ve witnessed through Open311Status, usually about 10 percent of the servers take longer than one second to respond at any given time. That&#8217;s not a stable infrastructure for third party developers to build upon.

Open311Status helps measure the distance between the potential of Open311 and the current reality. It&#8217;s cause to celebrate that here are 30 cities (and more to add to Open311Status) who have adopted both open data and open standards; this is hugely important progress! But there is still a lot of work to be done beyond the specification for Open311 to enable a rich and robust third party application developer ecosystem.

Some technical details: [Open311Status](http://open311status.herokuapp.com) is built on [Node.js](http://nodejs.org/) with the [Express](http://expressjs.com/) web framework and aggregates data in [MongoDB](http://www.mongodb.org/) through the [Mongoose](http://mongoosejs.com/) ORM. The application is single process and uses cron and async modules to poll the cities&#8217; Open311 servers every five minutes. A fun/dumb feature is that individual service requests are streamed to the browser using [Socket.io](http://socket.io/), but because many servers publish service requests an hour (or more!) after they&#8217;ve been submitted, Open311Status streams the previous day&#8217;s service requests in &#8220;real time&#8221; as if they were today&#8217;s (or rather, &#8220;real time minus one day&#8221;). Tests are done with [Mocha](http://visionmedia.github.com/mocha/) in BDD style with [Should](https://github.com/visionmedia/should.js) using [Sinon](http://sinonjs.org/) for mocks and stubs (though coverage could&#8211;always&#8211;be better). Open311Status is hosted on [Heroku](http://www.heroku.com/).