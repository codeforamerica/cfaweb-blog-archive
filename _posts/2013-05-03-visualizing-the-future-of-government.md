---
id: 21667
title: Visualizing the Future of Government
date: 2013-05-03T17:50:39+00:00
author: Renee DiResta
layout: post
guid: http://codeforamerica.org/?p=21667
permalink: /2013/05/03/visualizing-the-future-of-government/
categories:
  - Guest Post
  - Hackathon
  - News
---
I believe that the future of government is one of increased transparency and collaborative problem-solving. What gets us there is creating a culture of participation, in which citizens across industries contribute their expertise to help solve our shared difficult problems.

In November I got to participate in furthering open government at Code for America’s “Data Deathmatch” hackathon. California’s Fair Practice Political Commission (FPPC) provided hackers with a set of recently-digitized <a href="http://www.mercurynews.com/breaking-news/ci_22683694/state-political-watchdog-agency-seeks-expand-searchable-online" target="_blank">Statement of Economic Interest</a> (Form 700) judicial gift disclosure and campaign filings data. They asked us to help them come up with tools that would generate insights and increase transparency.

The team I joined — Team OpenJudge — consisted of seven talented people with diverse backgrounds and skill sets. Three of us spent hours working on a system for cleaning the data; although the digitization done by <a href="http://captricity.com/" target="_blank">Captricity</a> was phenomenal, the “human factor” (judges not following directions when filling out the form) caused significant messiness and the subsequent need for manual review.

During the cleaning process we found some interesting activity: one judge, impressively, had managed to receive two different “1/2 iPad” gifts. One donor had given the same painting of a courthouse to nine different judges. To present the information, we made “leaderboards” showing top donors, judges who had received the most gifts, and the highest-value gifts. We also created a word cloud to highlight the relative frequency of different gift types: lunches, dinners, gift certificates, baseball tickets, etc.

But the really important insights emerged when we made a network graph\*. In the visualization below, red dots are judges, and blue are donors\*.

[<img class="aligncenter size-full wp-image-21669" title="Screen shot 2013-05-03 at 3.40.03 PM" src="http://codeforamerica.org/wp-content/uploads/2013/05/Screen-shot-2013-05-03-at-3.40.03-PM.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2013/05/Screen-shot-2013-05-03-at-3.40.03-PM.png)

&nbsp;

Even though I’d spent hours looking at that dataset, the pockets of interconnectedness that you see above didn’t pop out. And that’s the power of visualization: it can make those relationships immediately obvious. It enables a degree of transparency far beyond simply making a database of judges and donors available to the public; it makes the data comprehensible to citizens, not just motivated analysts and engineers.

The FPPC invited us to Sacramento to present our work, and we spoke at their Commission meeting. They were excited about what we’d managed to accomplish in one weekend, and spoke of their vision of making meaningful information available to the people of California. When we got to the network visualization, they immediately grasped the potential, and asked a lot of questions about how it would handle new data, and what it could display. One of the commissioners happened to know a donor I clicked on during the demo, and approached us afterward to check out the details.

I share this not because it’s a great visualization — there are important factors in the judge/donor relationship that aren’t encoded here — but because I am struck by how new and potentially game-changing data visualization is for public servants. As they consider what kind of tools to commission to make data more open and transparent, we’ve helped inspire them to make something far more interactive and compelling than a data table on a static site. We’ve hopefully also demonstrated that with the right partners, transparency and usability can be achieved both rapidly and inexpensively.

Though implementing more transparent data visualizations won’t revolutionize government transparency and problem-solving on its own, I do think this is a meaningful first step toward bringing tech tools into government. I’m proud to have spent a weekend with a talented team who contributed valuable time and expertise to realizing a scaled-down — but nonetheless effective — culture of participation which successfully generated insights and enhanced transparency. And I’m looking forward to the next Code for America hackathon!

_*identity information has been removed; it will be available on their site._

&nbsp;

Questions? Comments? Hit us up <a href="http://twitter.com/codeforamerica" target="_blank">@codeforamerica</a>.