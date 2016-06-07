---
id: 8613
title: 'Reroute.it: Better Transportation Choices'
date: 2011-09-27T14:04:28+00:00
author: Aaron Ogle
layout: post
guid: http://codeforamerica.org/?p=8613
permalink: /2011/09/27/introducing-reroute-it/
dsq_thread_id:
  - 427602429
categories:
  - News
---
We all care how the decisions we make will impact our lives. In many cases, those impacts are self-evident. If I keep my air conditioner running during a hot summer, I will consume more electricity, and my utility bill will be more than if I suffered through the heat.

But understanding the impacts of our transportation choices is difficult. We can grasp the cost of a ride on public transit because we pay for individual trips, but we don&#8217;t have a directly comparable sense of cost every time we drive off in a vehicle we already own. How much did that trip cost? We also know that it is better for the environment and healthier to walk than it is to drive, but calculating all of these factors is very difficult. And it&#8217;s even more difficult to try compare these factors for every transportation choice we make.

<a href="http://reroute.it/" target="_blank">Reroute.it</a> makes it easy. Calculating and understanding many of the impacts of our transportation choices is now as simple as getting driving directions on your mobile phone.

Let&#8217;s say, for instance, that I&#8217;m going to a tech meet up in SOMA after work. It&#8217;s a little[<img class="alignright size-full wp-image-8617" title="Reroute.it Screenshot" src="http://codeforamerica.org/wp-content/uploads/2011/09/Screen-Shot-2011-09-20-at-11.15.34-AM.png" alt="Reroute.it Screenshot" />](http://codeforamerica.org/wp-content/uploads/2011/09/Screen-Shot-2011-09-20-at-11.15.34-AM.png) over a mile away so I can realistically take any mode of transportation &#8211; walk, bike, public transit, taxi, or drive. I don&#8217;t have a bike or a car, so I&#8217;m down to three options. My first inclination may be that walking is too far and instead think that public transit or a taxi are the way to go. But look at what Reroute.it tells me &#8211; taking a cab will be over three times more expensive than transit, but over twice as fast. I also realize that it&#8217;s not going to take as long to walk as I thought, and since I&#8217;ve been coding all day, could stand to burn a few more calories, and like that I won&#8217;t be contributing any carbon emissions, I decide to walk. It&#8217;s the best transportation choice for my specific trip.

Reroute.it is a mobile web application, meaning that it is not a native app that is specific to a mobile platform. Any user with a smart phone can simply go to [http://reroute.it](http://reroute.it/) and immediately use it for free. It was built using <a href="http://jquerymobile.com/" target="_blank">jQuery Mobile</a> on the front-end and <a href="http://www.sinatrarb.com/" target="_blank">Sinatra</a> on the server-side. It is powered by the <a href="http://msdn.microsoft.com/en-us/library/ff701717.aspx" target="_blank">Bing Routes API</a> (Google [doesn&#8217;t support transit](http://code.google.com/apis/maps/documentation/javascript/services.html#TravelModes) in their API) and raw <a href="http://code.google.com/p/googletransitdatafeed/wiki/PublicFeeds" target="_blank">GTFS</a> data for transit fare. You can find the source code and the assumptions we made for our calculations on <a href="https://github.com/codeforamerica/transpochoices/" target="_blank">GitHub</a>.

Reroute.it was also designed with city scalability in mind. As is, it will work everywhere in the United States but will not include features where the necessary data is not available. For example, transit information is only available in <a href="http://www.bing.com/community/site_blogs/b/maps/archive/2010/09/16/bing-maps-gets-transit-directions.aspx" target="_blank">cities supported by Bing Maps</a> and taxi fares where supported by TaxiFareFinder.com. Reroute.it is currently available with full features in San Francisco and Seattle. We expect full support soon in Philadelphia once GTFS fare data become available from our friends at <a href="http://septa.org/" target="_blank">SEPTA</a>. Reroute.it was developed by <a href="http://twitter.com/atogle" target="_blank">Aaron Ogle</a> (that&#8217;s me!) and <a href="https://twitter.com/yenthefirst" target="_blank">Talin Salway</a>, with design by <a href="https://twitter.com/#!/peterfecteau" target="_blank">Pete Fecteau</a>.

Reroute.it is designed to help people make fully informed transportation choices. It provides you the information, so that you can a weigh the pros and cons of each option.