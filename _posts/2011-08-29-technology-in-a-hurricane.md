---
id: 8197
title: Technology In A Hurricane
date: 2011-08-29T13:48:40+00:00
author: Abhi Nemani
layout: post
guid: http://codeforamerica.org/?p=8197
permalink: /2011/08/29/technology-in-a-hurricane/
dsq_thread_id:
  - 399256579
categories:
  - Commentary
---
As Hurricane Irene has now passed through the east coast &#8212; which just so happened to overlap with my brief trip to New York &#8212; the most common terms I&#8217;ve heard in response sound something like &#8220;overhyped&#8221; and &#8220;underwhelming.&#8221; (All in all, that&#8217;s probably a good thing; the opposite would be much, much worse.) With that lens, however, we risk glazing over the nitty gritty of the weekend &#8212; that is, what was done to prepare, manage, and respond to the storm. And in particular, we risk missing an opportunity to take stock of what I think was a watershed moment in the Gov 2.0 movement.

### Before the Storm: NYC.Gov

As Irene approached New York City, there was understandably a lot of confusion and concern about, frankly, what was going on. Was the hurricane going to hit the city? Was there going to be an evacuation? If so, when and where? And notably in the midst of that confusion, citizens turned to their government, particularly their government&#8217;s website, for clarification. New York City aptly posted evacuation maps and crisis guides online for easy access, but there was in fact so much traffic on [NYC.gov](http://nyc.gov) that the site went down on Friday afternoon. Not good. While this suggests the city should consider a more scalable infrastructure &#8212; maybe take the popular recommendation of the cloud &#8212; I found two immediate reactions more interesting.

First, Civic Commons&#8217; Philip Ashlock [mirrored the data and info](http://crisis-response.s3-website-us-east-1.amazonaws.com/irene.html) that he had downloaded onto Amazon&#8217;s (usually) reliable cloud, sharing the link all around. Instead of being embarrassed, the City&#8217;s Chief Digital Officer [Rachel Sterne even tweeted](http://codeforamerica.org/wp-content/uploads/2011/08/rsterne.png) out the link herself. They understood, it was the information, not the host that mattered.

Second, the city [&#8220;optimized&#8221; their website](http://gov20.govfresh.com/as-nyc-gov-buckles-city-government-pivots-to-the-internet-to-share-hurricane-irene-resources/). NYC.gov has a wealth of information and even editorialized content, but with more data, comes higher load times and the need for more bandwidth. Neither of which are preferable in a crisis. So after the site went down, it soon came back up, slimmed down. Significantly. See for yourself:

[<img class="aligncenter size-large wp-image-8210" title="nyc-irene" src="http://codeforamerica.org/wp-content/uploads/2011/08/nyc-irene-616x1024.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/08/nyc-irene.jpg)

It clocks in at a lean 54 kilobytes and a 3.2 second load time, according to Chrome. What&#8217;s more notable than the tweaks &#8212; I doubt this version will stay up long &#8212; is the utilitarian and practical thinking. I&#8217;d imagine it was a something of a bitter pill to swallow, chopping off so much of the sites, but it&#8217;s good that they remembered that websites don&#8217;t need to be all things at all times.

### During the Storm: Twitter & Crisis Mapping

A growing trend in the civic technology space is the use of mobile devices and people on-the-ground to crowdsource information reporting: platforms such as SeeClickFix, CitySourced, and Ushahidi and have gained traction in cities around the world, with the latter especially coming to relevancy in crisis situations. As [Alex Howard of O&#8217;Reilly Radar](http://radar.oreilly.com/2011/08/social-mapping-and-crisis-data.html) put it, &#8220;In this information ecosystem, media, government and citizens alike will play a critical role in sharing information about what&#8217;s happening and providing help to one another.&#8221; And Irene was a proof point. His post details the numerous data reporting platforms in use during the hurricane, and in New York alone, I counted at least three: [CrowdMap](http://www.mobilecommons.com/blog/2011/08/text-irene-to-877877-to-report-hurricane-damages/), [NYTimes/WNYC](http://www.wnyc.org/articles/wnyc-news/2011/aug/26/your-signs-prepared-or-unprepared-new-york/), and of course [311](http://www.nyc.gov/apps/311/allServices.htm?requestType=topService&serviceName=Hurricane+Damage+Report). While these are likely valuable tools for citizens and governments alike, the multiplicity and the possible redundancy therein suggests the need for better integration and standardization across various platforms. And here&#8217;s why:

[<img class="aligncenter size-full wp-image-8215" title="warning" src="http://codeforamerica.org/wp-content/uploads/2011/08/warning.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/08/warning.png)

That was the warning prompt sitting atop the [NYC&#8217;s Severe Weather CrowdMap](http://nycsevereweather.crowdmap.com/), and it reads (excerpted), &#8220;This is an information sharing site. Insofar as any posts made concern weather conditions and weather-related service disruptions, the City will not take action.&#8221; This disconnect between information and action acts as a hollow barrier for meaningful civic participation. Not only is there a skewed perception then of the actual damage, there&#8217;s also a bad image of hundreds of seemingly unresolved problems. Just putting dots on a map is sometimes a bad thing. Especially in the context of service requests and citizen/government interaction, [where it&#8217;s said](http://www.innovations.harvard.edu/cache/documents/1285/128521.pdf) that so much trust is built through two-way dialogue and conversation.

([Current efforts](http://open311.org/2011/07/ushahidi-and-the-open311-ecosystem/) to align Ushahidi with the Open311 specification should start to help with this ongoing challenge of standardization.)

Another tool government turned to, especially here in New York, was social media, and in particular, twitter. (Of course, they weren&#8217;t the only ones, and for those of us trapped indoors, [@Irene](http://twitter.com/irene) was an entertaining read.) [@NYCMayorsOffice](http://twitter.com/@NYCMayorsOffice) seemed to led the way in New York with their updates on the storm and evacuation plans more than doubling their monthly tweet rate, according to TweetStats (see left).

[<img class="aligncenter size-full wp-image-8231" title="nyc-chart" src="http://codeforamerica.org/wp-content/uploads/2011/08/nyc-chart.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/08/nyc-chart.jpg)

This activity was rewarded. On Thursday, August 25, @NYCMayorsOffice had 24,507 follows; today, August 29, it has 52,228, according to [TwitterCounter](http://twittercounter.com/NYCMayorsOffice). **That&#8217;s a 113 percent increase (+27,721) in four days.** Hopefully, the city will continue to leverage that resource moving forward not just in the clean up, but for future engagement.

### After?

I came across many posts this weekend of people asking, something along the lines of &#8220;What if we had all of this technology during Katrina?&#8221; I&#8217;m not sure how to answer that, honestly. I can only hope things would have turned out differently. But I don&#8217;t think that&#8217;s where our focus should be right now. We&#8217;ve got now a strong and growing infrastructure for civic action in a crisis &#8212; an infrastructure that has proven useful for coordination and communication. And I&#8217;ve only touched on a small piece of it. We should continue building it, developing and integrating our systems, and roll it out everywhere with a different question in mind: &#8220;With the best technology imaginable, what will the next crisis look like?&#8221;