---
id: 25908
title: My Summer at Code for America
date: 2013-09-18T14:28:56+00:00
author: Santiago Munin
layout: post
guid: http://www.codeforamerica.org/?p=25908
permalink: /2013/09/18/my-summer-at-code-for-america/
categories:
  - 2013
  - Commentary
tags:
  - google summer of code 2013
---
On May 27 this year I received wonderful news: I had been accepted as a Google Summer of Code student at Code for America! That meant that I was going to spend the next three months working on a project whose [idea](http://www.google-melange.com/gsoc/project/google/gsoc2013/santiagomunin/79001) I had submitted just days before.

My idea was to create a wrapper of the [GeoReport API](http://wiki.open311.org/GeoReport_v2) (part of the [Open311](http://open311.org/) standard) to make it easier for other users to create applications related to the standard. I elected Java as the programming language for this project because it is the one I know best and it would allow building Android applications too.

Days after, I met my mentor, [Shaunak Kashyap](http://www.linkedin.com/in/ycombinator), for the first time. We discussed the idea I had proposed deeply and thought about which tools and methodologies we were going to use. He did an awesome job helping me to create the library and improve myself as a software developer. During the summer we met once a week through Google Hangouts to discuss the status of the project and our next steps.

I think we did quite a good job, the result is a fully functional library with some features such as:

  * Very simple usage (and easy-to-follow documentation)
  * Data caching (avoiding a lot of costly network operations)
  * Logging system
  * Compatible with some non-standard endpoints
  * [Most of the library is supported by unit tests](http://codeforamerica.github.io/open311_java/cobertura/index.html)

In case you would like to learn more about the library, here are some interesting links:

  * [GitHub repository](https://github.com/codeforamerica/open311_java) (the best way to get to know it).
  * [Blog posts](http://santimunin.blogspot.com.es/search?q=open311) showing the process of the development.
  * [Library page](http://codeforamerica.github.io/open311_java/) with information regarding Javadocs, code coverage, dependencies.
  * [Blog post with a usage example (Android app)](http://santimunin.blogspot.se/2013/08/building-android-app-upon-open311-java.html).

Thanks to Google, Code for America, and (especially) Shaunak for this great experience.

&nbsp;

* * *

&nbsp;

Questions? Comments? Hit us up [@codeforamerica](http://twitter.com/codeforamerica).