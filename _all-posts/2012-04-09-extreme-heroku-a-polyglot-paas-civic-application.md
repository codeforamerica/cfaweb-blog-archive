---
id: 12212
title: 'Extreme Heroku: A Polyglot PaaS Civic Application!'
date: 2012-04-09T17:47:06+00:00
author: Jesse Bounds
layout: post
guid: http://codeforamerica.org/?p=12212
permalink: /2012/04/09/extreme-heroku-a-polyglot-paas-civic-application/
dsq_thread_id:
  - 642668618
categories:
  - 2012 fellows
  - CfA Labs
tags:
  - labs
---
<p style="text-align: left;">
  Code for America fellows are presented with a unique and fun challenge: Create innovative web applications using bleeding edge technologies that cities can eventually host themselves.
</p>

<p style="text-align: left;">
  The issue there is often the &#8220;bleeding edge&#8221; part of that equation can be a bit painful for cities and other organizations that don&#8217;t have Ruby, Python, Javascript, Amazon Web Services, or similar technology expertise on staff. <a href="http://en.wikipedia.org/wiki/Platform_as_a_service">Platform as a Service</a> (PaaS) solutions like Heroku help make delivering web apps a little simpler because potential worries like server maintenance, deployment schemes, and scaling strategy are eliminated or reduced.
</p>

<p style="text-align: left;">
  However, PaaS solutions can be, at least at first glance, a bit restrictive. Questions arise about how to run long lived processes, communicate between disparate yet related applications, and share resources such as databases. I started to explore these issues recently on Heroku in a far more critical way than I have before. I decided to attempt to architect a contrived application that:
</p>

  * Uses a Python application to capture all tweets in a geo-bounded box (drawn over Chicago)
  * Uses a Node.js application to display all of the tweets the Python application captures, in real time, on a map, to connected browsers with [Socket.io](http://socket.io/)
  * Uses [redis pub/sub](http://redis.io/topics/pubsub) to allow communication between the Python and Node apps
  * Uses [TileMill](http://mapbox.com/tilemill/) custom tiles and MapBox tile hosting with [leaflet/wax](http://mapbox.com/wax/) to render and display the map
  * Runs worry free on Heroku

I figured this would be a fun way to explore Heroku and, at the very least, a fun visualization. What I ended up with is <a href="http://civiz.herokuapp.com/" target="_blank">Civiz</a>!

[<img class="size-full wp-image-12225  " title="Civiz" src="http://codeforamerica.org/wp-content/uploads/2012/04/civiz_wide.png" alt="Civiz" />](http://civiz.herokuapp.com/) 

You can learn all about how Civiz was created and how to make your own version and host it for free on Heroku by going to the <a href="https://github.com/boundsj/civiz_server" target="_blank">Civiz github repo</a>. My current opinion is that there are a lot of elegant and creative ways to avoid the limitations of PaaS vendors like Heroku and deploy infinitely scalable, less troublesome applications. PaaS solutions are not a magic bullet &#8211; the issues I encountered while working on this project could fill a few more blog posts! But, web apps delivered on PaaS solutions can potentially mean less headaches for clients and, importantly for CfA fellows, less headaches for our city partners! Have fun out there and make awesome things!