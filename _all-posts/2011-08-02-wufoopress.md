---
id: 7890
title: WufooPress
date: 2011-08-02T15:49:40+00:00
author: Abhi Nemani
layout: post
guid: http://codeforamerica.org/?p=7890
permalink: /2011/08/02/wufoopress/
dsq_thread_id:
  - 375473349
categories:
  - CfA Labs
tags:
  - labs
---
Last year, we got through 362 applications for the fellowship without printing out one application. (And yes, that was also because last year, at this point, we didn&#8217;t own a printer that could have handled that; still don&#8217;t actually.) This year, we&#8217;ve gotten even more applications, and to handle them, we decided to automate the process a little.

[<img class="alignright size-medium wp-image-7896" title="wufoo" src="http://codeforamerica.org/wp-content/uploads/2011/08/wufoo-300x177.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/08/wufoo.jpeg)We handle applications online through the popular and effective form software, [Wufoo](http://wufoo.com), which allows for a straightforward data entry mechanism. To get those applications into a useful format for our [selection committee](http://codeforamerica.org/2011/04/13/2012-fellow-selection-committee/) to review, however, we designed a custom separate site for display, commenting, and sorting (aptly named, The Sorting Hat), which was built on top of WordPress ([more details here](http://codeforamerica.org/2010/09/09/getting-to-23-our-attempt-at-a-more-modern-selection-process/)). This system has proven rather useful for our reviewers. But there was one problem for us: connecting Wufoo and WordPress. In the past, this had to be handled manually with a data export from Wufoo, data manipulation locally on (gasp) Excel, and then finally an import into WordPress through a plugin. And yet, efficiency is one of our values&#8230; Enter the hack.

Fortunately, Wufoo has a [well-documented API](http://wufoo.com/docs/api/v3/), which allows you to call all the entries attached to a form, and WordPress has programatic post-creation functionality through its API through the [XML-RPC protocol](http://codex.wordpress.org/XML-RPC_Support). I was able to connect the two together with a little PHP script that when run will first check for the last entry already in WordPress, see if there are new submissions in Wufoo, and then publish them as new posts in WordPress. Basically, it&#8217;ll let you keep an up-to-date Worpress site with your Wufoo entries. Hence the name, [WufooPress](https://github.com/codeforamerica/Wufoopress).

The script is fairly simple (I&#8217;m not much of a hacker) and could use some cleaning up and additional functionality. (It&#8217;d be great to automate the checking and posting process, or even hash this out as a proper WordPress plugin.) Code is on [github](https://github.com/codeforamerica/Wufoopress) if there are any takers. For now, I thought it might be of some use to other people who both love and use Wufoo and WordPress &#8212; like we do here at Code for America.