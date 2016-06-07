---
id: 4067
title: Transportation Standards and the Break of Gauge
date: 2011-03-01T10:57:05+00:00
author: Michael Bernstein
layout: post
guid: http://codeforamerica.org/?p=4067
permalink: /2011/03/01/break-of-gauge/
dsq_thread_id:
  - 243007622
categories:
  - Commentary
  - Dispatches
---
After spending a month in San Francisco attending the CfA training, I got off my flight to Washington DC and walked to the WMATA Metro station. I was suddenly struck with deja-vu:

<p style="text-align: center;">
  <img src="https://lh4.googleusercontent.com/tOfPXC1pwg0MEnlLtDXXTvPcKWi35NUIGfVtVZFM5NDWU8SlCpB2uxCQGIo7BwkdesEeifyjVNESskZWC3t2CwIVNHQVaMQMVrDj9jGo3ilPsdjoL0U" alt="" width="254px;" height="203px;" /> <img src="https://lh3.googleusercontent.com/t58JQBFxw9zUyfeTwAU-sJzxG7WJZBBEUXM9Zi--Y8B6gnalyiJ5k_k6Miq7nV5JXnart6Wy0YLi8ADHf3r5ZW7KHpcAX-jUVwGXfOWGqS88ZHbCeOM" alt="" width="270px;" height="203px;" />
</p>

Even the paper tickets are clearly using an identical format:

<div style="text-align: center;">
  <img src="https://lh6.googleusercontent.com/SdRhqLlzPWjRTCaShO3CnJipFMSEshExZCJb800iBg1SmLXbhqs2oPpmpO6V7BM4A8A3l7gqjx78WNcV76hXCusqVatU8WoaBEdoVGItgVrIwqpn4EI" alt="" width="244px;" height="370px;" /> <img src="https://lh6.googleusercontent.com/KBE0ggmE3R1F6misJZtjT22A21ZGk12Q0h8Kh_ObkTHcAwfmSeSJaKsotUZMKiUgM13wye93bI5L-X_5d8rmgenRD7HtxcaCozfRu5Q3EDzwq1zQC6g" alt="" width="228px;" height="370px;" />
</div>

And yet, despite the commonality (and presumed compatibility) of the equipment, a ticket bought for one system will not work in the other (yes, I tried).

Incompatibilities in US transportation networks are nothing new. In the 1800s, as regional rail networks in the US began to interconnect, whenever goods or passengers needed to move between two networks, they frequently had to be unloaded from one train and loaded on another, often resulting in unpredictable delays. This was due to each network having a different gauge, or distance between the rails. This mismatch is known as a [break of gauge](http://en.wikipedia.org/wiki/Break-of-gauge). In most cases engines and cars designed for one gauge could not run on another without modification. The gauge could be anywhere between 4ft and 6ft, and there were over twenty different gauges in use. The rising cost of transshipment in both labor and time [put pressure on the rail networks to standardize](http://en.wikipedia.org/wiki/Broad_gauge#United_States), notwithstanding [the usual resistance to change from those who are benefiting from the status-quo](http://en.wikipedia.org/wiki/Erie_Gauge_War). In 1886, the southern rail networks were the last to convert to standard gauge when, in a [massive effort over the course of two days](http://southern.railfan.net/ties/1966/66-8/gauge.html), tens of thousands of workers pulled the spikes from the west rail of all the rail lines in the South, moved them 3 inches east and spiked them back in place.

A century later, a similar story played out with computer networking standards. Many local PC networking systems existed in the 1980’s, each with their own proprietary cabling, protocols, cards, and network operating system, creating a new ‘Break of Gauge’ problem. By contrast, the many different vendors in the Unix workstation world converged on TCP/IP and Ethernet, and eventually the PC world followed suit, such that now nearly all network connections, between systems as close as the same room or on the other side of the planet, use these standards to seamlessly transfer data.

Fast forward to 2005. [Bibiana McHugh](http://trimet.org/difference/bibi.htm) of Portland’s TriMet got frustrated over her inability to find transit data online, and had a vision of making planning a transit trip much easier by standardizing on a format for transit data that search engines could consume, and through collaboration with Google’s engineers made that standard format happen. Today, nearly 500 transit agencies worldwide are publishing their schedule data using the General Transit Feed Specification format Bibiana helped create ([166 here in the US](http://www.citygoround.org/agencies/us/?public=public)), and [a whole ecosystem of transit applications has sprung up that use the format](http://www.citygoround.org/apps/).

Despite the advances of present-day trip-planning solutions, several challenges have yet to be overcome. For example, riders face payment challenges when using multiple modes of transportation. In Portland, between 10-15% of transit riders also use their bicycles to get to and from the transit center. Similar to rail and PC networking, this is yet another ‘break of gauge’ problem, this time though, it’s people being inconvenienced, not just data or rail freight. To address this problem, TriMet funded [OpenPlans](http://openplans.org/) to merge several projects into [OpenTripPlanner](http://opentripplanner.com/), an open source system that transit agencies can deploy to make multi-modal trip planning seamless, including walking, biking, bus, and rail. [Several companies provide services around OTP](http://opentripplanner.com/contact), and it has been deployed around the world, including ones in Poland, Spain, and India.

Meanwhile, many regional transit agencies have been working to integrate their payment systems. For example, the NYC MTA network has been unified over time from seven incompatible networks.

Multi-modal trip planning and unified payment within a city or regional transit system is just the beginning. Just as in the 1880’s and 1980’s, as isolated systems grow and interconnect with each other, and with yet other systems (for example, passenger rail and even air travel), the ‘break of gauge’ becomes increasingly prominent and annoying, prompting new solutions and standardization. For example, the NYC metrocard can already be used with other regional transit lines like the New Jersey PATH trains.

Given nearly identical equipment at both ends, an interoperable computer network already strung across the country, and emerging standards for transit data and payment, it’s not hard to see a future where a seamless door-to-door trip from San Francisco to Washington D.C. can be planned by whatever travel options are available, and paid for just once with a single ticket.

Along the way, though many vested interests may attempt to slow or stop this sort of standardization, its likely that those attempts will fail, and eventually, we will have an end-to-end system connecting our cities into an ever growing network of networks, an inter-network, of transit.