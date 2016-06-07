---
id: 28533
title: 'The Intentional Stack: Technology Choices in Civic Projects'
date: 2013-12-20T15:30:50+00:00
author: Dave Guarino
layout: post
guid: http://www.codeforamerica.org/?p=28533
permalink: /2013/12/20/the-intentional-stack-technology-choices-in-civic-projects/
categories:
  - Commentary
  - Fellowship
  - Technology
---
<p dir="ltr">
  An oft-discussed subject in the civic tech world is the cavernous divide in the underlying technologies used by the private tech sector as opposed to those used by government entities. Some stylized examples:
</p>

<li dir="ltr">
  <p dir="ltr">
    open source vs. proprietary;
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Ruby on Rails vs. .NET;
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    cloud services like Heroku or Amazon Web Services vs. in-house server hosting;
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Unix-y operating systems vs. Windows (everyone’s favorite).
  </p>
</li>

<p dir="ltr">
  Many of these differences exist for good — or, if not good, then at least rational — historical and institutional reasons. Many government IT projects represent core infrastructure, where goals like stability, integration across multiple systems, and the ease of auditing dominate considerations like user experience, development speed, and cost. Government critics tend to overlook that this attitude is endemic to the “enterprise” world generally — including the private sector — and that government entities just happen to fall into that broader category.
</p>

<p dir="ltr">
  But this divide presents a challenge for developers looking to build technology with and for government. How do you choose a stack that both allows you to build useful, modern technology while navigating the very legacy choices that hamper governments’ attempts to do so on their own?
</p>

<p dir="ltr">
  The CfA Fellows confront this choice every year. As someone recently out the other end of this tunnel, my thinking can be summed up in one sentence:
</p>

<p dir="ltr">
  <strong>     It’s all about the goals.</strong>
</p>

Many of the technology discussions out there become acrimonious because they hide implicit disagreements about what the whole damned point is in the first place. And it’s hard to agree on tactics when you don’t even know what the end-goal is.

<p dir="ltr">
  Here are some of the most common goals I hear implicitly employed in these discussions:
</p>

<p dir="ltr" style="padding-left: 30px;">
  <strong>1. Projects can be developed rapidly</strong>
</p>

<p dir="ltr" style="padding-left: 30px;">
  With the knowledge that many projects are design experiments, a “proof of the possible” rather than long-lasting software like core infrastructure; this goal would prioritize stacks developers already know, and is a particularly relevant consideration for single-developer teams.
</p>

<p dir="ltr" style="padding-left: 30px;">
  <strong>2. Projects contain modular, reusable components</strong>
</p>

<p dir="ltr" style="padding-left: 30px;">
  This approach sacrifices speed, but possibly leads to more reusable output than a bespoke, monolithic app.
</p>

<p dir="ltr" style="padding-left: 30px;">
  <strong>3. The project is maintainable by government IT partners</strong>
</p>

<p dir="ltr" style="padding-left: 30px;">
  This was an explicit goal in CfA&#8217;s Louisville, Ken. team&#8217;s use of PHP this past year.
</p>

<p dir="ltr" style="padding-left: 30px;">
  <strong>4. CfA projects are a place for experimenting with novel web technologies</strong>
</p>

<p dir="ltr" style="padding-left: 30px;">
  One argument in this vein is if CfA won&#8217;t be the place a city experiences the benefits of Node.js, what will be? It is also a goal for many Fellows who want to learn new technologies in their fellowship year.
</p>

<p dir="ltr" style="padding-left: 30px;">
  <strong>5. The project is easy to collaborate on</strong>
</p>

<p dir="ltr" style="padding-left: 30px;">
  Either across teams, or across the Fellow/community divide; this goal would writing approachable code, even at the expense of elegance or speed.
</p>

<p dir="ltr" style="padding-left: 30px;">
  <strong>6. The project is potentially maintainable by a large number of people</strong>
</p>

<p dir="ltr" style="padding-left: 30px;">
  I.e., built on technologies with wide usage in the developer world; this is similar to the above, but more specifically targeted at addressing the sustainability paths of a project.
</p>

<p dir="ltr">
  Now I personally agree with many of these goals, some more than others. But what’s important to note is that many are divergent in their implications for tech choices. So (to borrow a line): what is to be done?
</p>

<p dir="ltr">
  I would argue it boils down to intentionality and good process. In the fellowship context, this means:
</p>

<li dir="ltr">
  <p dir="ltr">
    Understanding and making explicit the specific context of a government partner (e.g., internal IT capacity vs. outside sustainability options) as well as team context (e.g., single vs. multiple developers, experience levels and language flexibility)
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Teams deciding together on the goals, and their prioritization, for their projects — and writing these down (preferably in big font on a wall nearby)
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Making intentional tech decisions that support the broader, agreed-upon goals
  </p>
</li>

<p dir="ltr">
  All technology choices have tradeoffs. The best way to manage them is to discuss those tradeoffs in terms of goals or outcomes desired, rather than in terms of particular technologies that implicitly support one goal over another.
</p>

* * *

<p dir="ltr">
  Questions? Comments? Hit us up <a href="http://twitter.com/codeforamerica" target="_blank">@codeforamerica</a>.
</p>