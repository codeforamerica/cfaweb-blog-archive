---
id: 3012
title: 'CfA Pitching In During Boston&#8217;s &#8220;Snow-pocalypse&#8221;'
date: 2011-02-17T15:48:27+00:00
author: Talin Salway
layout: post
guid: http://c4a.me/?p=3012
permalink: /2011/02/17/cfa-bostons-snowpocalypse/
dsq_thread_id:
  - 232895581
categories:
  - Dispatches
  - News
tags:
  - boston
  - Boston Snow GeoRSS JSON ruby opensource Open311 Groundcrew
---
A few weeks ago, Boston was experiencing a snow-pocalypse. Inches upon inches of snow had piled up, cutting off businesses and trapping citizens in their home. But early that morning, the Code for America offices received an email:

> &#8220;Hi CFA team &#8211; Boston is currently in the middle of a blizzard! We are exploring a possible partnership with GroundCrew, called SnowCrew, which will enable citizens-volunteers to self-organize around snow shoveling for their neighbours.&#8221;

The email was from Nigel Jacobs from Boston&#8217;s Department of New Urban Mechanics &#8212; the department spearheading interesting and innovative new efforts to solve city problems &#8212; and they had found a way out of snow-pocalypse. Cellphone-using citizens would send pictures &#038; GPS locations of unshoveled sidewalks to the government, and a set of volunteers would track the posts, ready to take action, watching for reports of snowy sidewalks, and use the [GroundCrew program](http://groundcrew.us/) to coordinate their efforts to help out.

There remained only one problem: they couldn&#8217;t see where to go. 

In order to display the reports on a map, Groundcrew needed to get its data in GeoRSS format &#8212; a common mappable data format &#8212; but Boston&#8217;s reported data didn&#8217;t generate the right output. There was technical barrier between a civic problem and a citizen solution. And that&#8217;s where we came in.

After receiving Nigel&#8217;s note, we were able to review the situation with the data, and fortunately found that this was just a quick coding mission. In a few hours that morning, we wrote a short script</a> to translate city&#8217;s reports of snow issues to mappable GeoRSS, which piped in neatly into Groundcrew&#8217;s citizen mobilization platform. With a little bit of work on Groundcrew&#8217;s end, the citizen volunteers were able to see where help was needed, and they could take action and get involved.

<img src="http://codeforamerica.org/wp-content/uploads/2011/01/snowcrew-311-1024x554.jpg" alt="" title="snowcrew-311" class="aligncenter size-large wp-image-3216" />

_[Source code available on GitHub.](https://github.com/YenTheFirst/open311-to-georss/)_