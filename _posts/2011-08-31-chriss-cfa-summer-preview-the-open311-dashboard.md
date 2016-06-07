---
id: 8274
title: 'Chris&#8217;s CfA Summer: Preview the Open311 Dashboard'
date: 2011-08-31T18:32:17+00:00
author: Chris Barna
layout: post
guid: http://codeforamerica.org/?p=8274
permalink: /2011/08/31/chriss-cfa-summer-preview-the-open311-dashboard/
dsq_thread_id:
  - 401383860
categories:
  - 2011 Interns
  - News
---
Fifteen months ago, Federal CIO Vivek Kundra [announced](http://www.whitehouse.gov/blog/2010/03/03/open-311) the [Open311 API](http://open311.org/) that allows citizens to monitor and report problems to their city government through a unified web service. Two cities have implemented the API so far (San Francisco and Boston) with more planning to roll out next year. With all that data so easily accessible, 2011 fellow Michael Evans took on a project to make creative visualizations with it. Thus, the Open311 dashboard was born. 

With the Open311 Dashboard, we aim to take the deluge of data that 311 provides and translate it into a clean and interactive dashboard that will help set citizens’ expectations of service request response times, identify 311 trends in a city and across the country, and provide city administrators data about the efficiency of various city services.

I spent that last two months as a [Google Summer of Code](http://code.google.com/soc/) intern helping Michael with the backend of the San Francisco dashboard and playing around with the plethora of [geographic data](http://gispub02.sfgov.org/website/sfshare/index2.asp) that the city provides. Today, I have some screenshots of the dashboard in its current inception.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/08/dash1.png" alt="" title="dash1" width="610px" class="aligncenter size-full wp-image-8281" />](http://codeforamerica.org/wp-content/uploads/2011/08/dash1.png)

The homepage shows (at a glance) how responsive the city has been week-over-week.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/08/dash2.png" alt="" title="dash2" width="610px" class="aligncenter size-full wp-image-8282" />](http://codeforamerica.org/wp-content/uploads/2011/08/dash2.png)

You can drill down into specific neighborhoods.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/08/dash3.png" alt="" title="dash3" width="610px" class="aligncenter size-full wp-image-8283" />](http://codeforamerica.org/wp-content/uploads/2011/08/dash3.png)

And even individual city blocks.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/08/dash4.png" alt="" title="dash4" width="610px" class="aligncenter size-full wp-image-8284" />](http://codeforamerica.org/wp-content/uploads/2011/08/dash4.png)

We’re also playing around with a block-based heat map to show where certain request types are popular or take a long time for the city to fill.

I had a lot of fun interning at Code for America and learned more than I could imagine about Python, Postgres, and GIS. Stay tuned for future Open311 Dashboard updates from Michael Evans.