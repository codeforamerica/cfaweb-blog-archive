---
id: 33717
title: Using Heroku API to Make Code for America Products Easier to Adopt
date: 2015-07-09T18:04:59+00:00
author: Michal Migurski
layout: post
guid: http://www.codeforamerica.org/blog/?p=33717
permalink: /2015/07/09/using-heroku-api-to-make-code-for-america-products-easier-to-adopt/
categories:
  - Digital Front Door
  - News
---
Code for America has developed a [new way to deploy civic tech applications](http://www.codeforamerica.org/blog/2015/07/09/making-code-for-america-products-easier-to-adopt/). We’re trying it out with three popular and widely-useful apps, [RecordTrac](https://www.codeforamerica.org/apps/recordtrac/), [CityVoice](https://www.codeforamerica.org/apps/cityvoice/), and the [City Analytics Dashboard.](https://www.codeforamerica.org/apps/city-analytics-dashboard/)

Every application Code for America has ever written is open source and available via Github. We strive to provide useful README documents, and we are starting to centralize core documentation on deploying different kinds of codebases in our [How-To collection](https://github.com/codeforamerica/howto). However, we’re also finding that publicly available code in a source repository is not sufficient for city staff adoption of civic technology. Code works for fellows, community hackers, and the most adventurous government staff.

Last year, our primary platform-as-a-service vendor Heroku released their [Platform API app-setups feature](https://devcenter.heroku.com/articles/setting-up-apps-using-the-heroku-platform-api), and we saw a possible new way to help our government partners deploy applications. Instead of asking our visitors to learn Git and the command line, we can step them through a wizard-like application setup process that results in a real, live, running app on their own Heroku account.

For example, [CityVoice](http://www.codeforamerica.org/blog/2015/06/16/cityvoice-a-better-way-for-cities-to-listen/) combines [the voice features of Twilio](https://www.twilio.com/voice) with a geographic map interface and printed neighborhood signs. Configuration involves numerous linked accounts and data sources. The wizard-like builder application we’ve built on Heroku’s app-setups API wraps a narrative around this process, making it easy for a non-technical city staffer to follow directions and deploy a complete, working application to Heroku. We want more people to have [the same experience as Matthew Moyers](http://www.codeforamerica.org/blog/2015/06/16/cityvoice-a-better-way-for-cities-to-listen/) from South Bend Parks and Recreation:

> Not only did more residents call in to CityVoice than attend any of the roughly 30 public input meetings, but the residents who used CityVoice gave us much richer, more useful feedback. What made it better? The feedback was location-specific.

[<img style="border: 2px solid #999595;" src="/blog/wp-content/uploads/2015/06/cityvoice.png" alt="Screenshot of CityVoice setup app" />](https://cityvoice-setup.codeforamerica.org/)

#### 3 Code for America Products You Can Adopt Right Now

[RecordTrac](https://recordtrac-setup.codeforamerica.org), built with Oakland in 2013, provides citizen and staff interfaces to public records requests. It’s been in public use in Oakland for two years, and has replaced other means of handling records requests.

[CityVoice](https://cityvoice-setup.codeforamerica.org), built with South Bend Indiana in 2013, provides a flexible voice-based map survey tool for rapidly gathering nuanced feedback from residents, thanks to Twilio’s phone service.

The [City Analytics Dashboard](https://dashboard-setup.codeforamerica.org), adapted from a project by our friends at GOV.UK, helps website owners see the usage and search patterns of their visitors in a dynamic, big-screen format. It’s a core part of our [Digital Front Door initiative](http://www.codeforamerica.org/our-work/initiatives/digitalfrontdoor/), helping government staff to understand the hard-to-see web visitors using digital services.

  * Set up [RecordTrac](https://recordtrac-setup.codeforamerica.org)
  * Set up [CityVoice](https://cityvoice-setup.codeforamerica.org)
  * Set up [City Analytics Dashboard](https://dashboard-setup.codeforamerica.org)