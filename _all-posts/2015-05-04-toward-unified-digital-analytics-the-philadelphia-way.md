---
id: 33268
title: 'Toward Unified Digital Analytics: The Philadelphia Way'
date: 2015-05-04T14:01:15+00:00
author: Lauren Ancona
layout: post
guid: http://www.codeforamerica.org/blog/?p=33268
permalink: /2015/05/04/toward-unified-digital-analytics-the-philadelphia-way/
categories:
  - Data
  - Digital Front Door
  - News
  - Philadelphia
---
As part of our [Digital Front Door](http://www.codeforamerica.org/our-work/initiatives/digitalfrontdoor/?source=blog) initiative, we&#8217;re highlighting great examples of local governments taking data-driven approaches to designing and redesigning their websites. We caught up with [Lauren Ancona](https://twitter.com/laurenancona), a Data Scientist in the City of Philadelphia’s Office of Information and Technology, who played a key role in launching a [public, near real-time dashboard](http://phillyinnovates.com/2015/0s /20/toward-unified-digital-analytics/) that shows traffic to the City of Philadelphia&#8217;s webpages using Google Analytics and Google Tag Manager.

[<img class="alignnone size-full wp-image-33283" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/analytics.gif" alt="analytics" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/analytics.gif)

**Here&#8217;s her story:** 

When I started at the City in December, the first thing I wanted to see was the Google Analytics account for phila.gov. One of the biggest challenges in getting meaningful data from any analytics tool is considering the source: what does the implementation look like? In our case, the City’s website had gone through numerous iterations in the past several years, parts of which were built by contractors. This meant that we had an analytics account that was reporting on traffic dating back to 2010, but no way to know how much of the site was included in that account, when the snippet may have been added or removed from parts of the site, and even duplicated in others.

Reliable benchmarking would have been nice, but since we really needed to measure current usage and track the impact of upcoming releases, it wasn’t the end of the world. Now we needed to determine how many sites were not yet included in the tracking. I figured we could just start with a list of all city sites and check if we were seeing traffic in Google Analytics&#8230;except there was no list.

Factors leading to the fragmented nature of the City’s web properties are outside the scope of this project, but suffice to say it’s not a problem that’s unique to Philadelphia. Offices and departments have a huge spectrum of technological needs, and have had to solve for their use-cases as both time and [funding](http://www.phila.gov/openbudget/ "funding") allows. The result is that we had to make our own list, and start reaching out to departmental IT directors to invite participation.

The most difficult part of rolling out a unified analytics program within a government structure with many siloed web properties (including many that aren’t part of the primary .gov domain) is managing deployment. For this, we turned to [Google Tag Manager](http://www.google.com/tagmanager/ "Google Tag Manager"), a mature product that was developed for and mostly utilized by marketers. It provides a graphic interface to manage advertising tracking beacons: single-pixel images used to count sales conversions, and was designed to seamlessly integrate with Google Analytics.

<div id="attachment_33279" style="width: 730px" class="wp-caption alignnone">
  <a href="http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/gtmdashboard_720.png"><img class="wp-image-33279 size-full" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/gtmdashboard_720.png" alt="" /></a>
  
  <p class="wp-caption-text">
    Example &#8216;Tags&#8217; in the Google Tag Manager dashboard
  </p>
</div>

However, its true beauty is the ability to (securely) make adjustments to an analytics implementation without direct access to the site’s codebase. Vendor lock in is less of a worry, too; though GTM itself is a Google product, if ever we wanted to move to a different analytics tool, it’s as simple as swapping out the Google Analytics “tag” with the new tool’s tracking snippet&#8230;in **one place**: the Tag Manager dashboard.

An example snippet looks like:

[<img src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/google-snippet.png" alt="Example snippet" class="alignnone size-full wp-image-33299" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/google-snippet.png)

<noscript>
</noscript>


  
<!-- End Google Tag Manager -->

Let me say that again: once the container is installed (it looks similar to the standard Google Analytics snippet), you do not need to touch the code to add data to your reporting configuration, including custom dimensions and metrics. It’s capable of one-to-many management of Google Analytics properties as well, which means we can send reporting to multiple analytics accounts from within a single container, simply by adding a new “tag” (GTM’s name for the equivalent of the analytics snippet). For example, if the agency has its own analytics property, it’s easy to send data to both the agency’s account and the umbrella or “rollup” account you’re using to aggregate government-wide traffic.

<div id="attachment_33287" style="width: 730px" class="wp-caption alignnone">
  <a href="http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/container-vis_720.png"><img class="wp-image-33287 size-full" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/05/container-vis_720.png" alt="" /></a>
  
  <p class="wp-caption-text">
    Visualization of relationships between tags, triggers, & variables in a Google Tag Manager container
  </p>
</div>

Our toolbox for rolling out Unified Analytics looks like this:

**Reporting**

  * [Google Analytics](http://www.google.com/analytics/?utm_expid=71218119-7.lBgmrTO8R3uEDwsxNxa_Nw.0)
  * [Google Tag Manager](http://www.google.com/tagmanager/)
  * [Google Webmaster Tools](https://www.google.com/webmasters/tools/home?hl=en)

**Testing**

  * [Screaming Frog SEO Spider Pro](http://www.screamingfrog.co.uk/seo-spider/)
  * [Tag Assistant](https://chrome.google.com/webstore/detail/tag-assistant-by-google/kejbdjndbnbjgmefkgdddjlbokphdefk) (Chrome extension)
  * [Google Analytics Debugger](https://chrome.google.com/webstore/detail/google-analytics-debugger/jnkmfdileelhofjcijamephohjechhna) (Chrome extension)
  * [Page Analytics by Google](https://chrome.google.com/webstore/detail/page-analytics-by-google/fnbdnhhicmebfgdgglcdacdapkcihcoh) (Chrome extension)

With the exception of Screaming Frog, all of the software used in this project is free, and all code used in the new [analytics.phila.gov](http://analytics.phila.gov) is open source.

This initial version includes a live count of users, updated each minute, an hourly count of users for the current day, and the top 20 most-visited pages over 3 periods: right now, the past week, and past month.

## Want to roll out unified analytics in your city or state?

Check out the City of Philadelphia&#8217;s [step-by-step guide](http://laurenancona.github.io/unified-analytics/) — starting from scratch — to start a basic “rollup” reporting profile using Google Analytics and Google Tag Manager. They’ll continue building out instruction over the coming months. Learn more about analytics and website redesigns in CfA&#8217;s [Digital Front Door Resources](http://www.codeforamerica.org/our-work/initiatives/digitalfrontdoor/#resources?source=blog).