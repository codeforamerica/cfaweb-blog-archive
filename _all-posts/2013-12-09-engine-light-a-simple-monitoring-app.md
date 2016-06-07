---
id: 28114
title: 'Engine Light: A Simple Monitoring App'
date: 2013-12-09T19:05:46+00:00
author: Erica Kwan
layout: post
guid: http://www.codeforamerica.org/?p=28114
permalink: /2013/12/09/engine-light-a-simple-monitoring-app/
categories:
  - News
---
[Code for America has lots of projects](http://github.com/codeforamerica). These projects are written in different languages, hosted in different places, and have different levels of complexity. When I joined CfA in October, a few of these apps used New Relic and a couple were monitored via Pingdom.

It important for us to have a basic view of an app&#8217;s state. In effort to be consistent, my first thought was to expand CfA&#8217;s usage of Pingdom, or find an alternative. This wasn&#8217;t a great solution, because our apps only needed a small set of features provided by third party monitoring tools, and pricing was prohibitive given the quantity of CfA&#8217;s apps.

So I built a simple monitoring application called Engine Light. Engine Light surfaces a small set of app details and monitors an app&#8217;s state. This basic set of functionality let&#8217;s users know if an app is okay or not. Engine Light is a Rails 4 app that uses Mozilla Persona for user authentication. Mozilla Persona provides an easy way to authenticate users via email whether they are CfA staff or fellows, or users outside of CfA, such as city contacts. The first iteration of Engine Light used Bootstrap 3. It now has a shiny, custom designed UI.

To display app information or check the app&#8217;s state, Engine Light fetches JSON via the app&#8217;s status API endpoint. Here&#8217;s an example of what a JSON response would look like:

<pre style="margin-left: 1em;">{
  "status": "ok",
  "updated": 1380064049,
  "dependencies": [ "Postgres", "Sendgrid" ],
  "resources": { "Sendgrid": 17.8475 }
}</pre>

<var>Status</var> may contain either &#8220;ok&#8221; or an error message. The app determines what an errored state is. <var>Updated</var> is a unix timestamp indicating when the status check occurred by the app. <var>Dependencies</var> are third party services the app uses, and <var>resources</var> are third party services or data stores with usage limitations. An app sends current resource usage information as a percentage.

Engine Light updates its information when a user views the an app&#8217;s details, as well as every 10 minutes. If the check that occurs every 10 minutes indicates an app goes down, Engine Light will email the app owners and continue to send an email every time the check occurs. Once the app becomes available, Engine Light will email the app owners again.

I dealt with a couple of challenges when implementing Engine Light. It took a while to integrate Bootstrap 3 with Rails 4, as there were no good instructions on how to do this at the time. I ended up putting the bootstrap Javascript and css in Engine Light&#8217;s vendor directory and fiddled with configuration until everything worked. Figuring out how and when to cache app status turned out to be a bit complicated. Originally, Engine Light checked the status of apps every 10 minutes to determine whether email notifications should be sent and would check the status of apps real-time when a user viewed apps throught the UI. After adding 10+ apps, the app index page became pretty slow due to all the API calls it was making. To fix this, I stored apps&#8217; statuses in the database. The stored status would be updated either every 10 minutes as part of the regularly scheduled status checks or whenever a user viewed an app&#8217;s details page. The app index page used statuses stored in the database. This meant the app index page no longer displayed real-time data, but the data displayed was still relatively recent.

Engine Light is part of a concerted effort to make CfA apps more sustainable. When developers add their app to Engine Light, it encourages them to think about app dependencies, plus anything that could cause their application stop functioning and surface this information to other stakeholders.

For more details, checkout Engine Light&#8217;s github page: <https://github.com/codeforamerica/engine-light>

&nbsp;

* * *

&nbsp;

Questions? Comments? Hit us up <a href="http://twitter.com/codeforamerica" target="_blank">@codeforamerica</a>.