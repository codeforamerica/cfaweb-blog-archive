---
id: 5669
title: 'Applications for Good SF: <br />&#8220;All Income Foods&#8221; App Wins!'
date: 2011-05-13T10:39:49+00:00
author: Michelle Koeth
layout: post
guid: http://codeforamerica.org/?p=5669
permalink: /2011/05/13/code-for-america-fellows-part-of-winning-team-at-applications-for-good-sf/
dsq_thread_id:
  - 302999282
categories:
  - News
---
Having only attended one other code-a-thon before in my life, in <a href="http://codeforamerica.org/2011/03/04/presidents-day-data-camp-dc/" target="_blank">Washington D.C.</a>, last weekend&#8217;s [Applications for Good](http://applicationsforgood.org/contest-announcement/san-francisco/sf-comes-together-to-build-applications-for-good/) competition gave me the opportunity to experience civic app development, West coast-style.

<div style="float: right; margin-left: 10px;">
  <a href="http://codeforamerica.org/wp-content/uploads/2011/05/codeathon1.jpg"><img class="size-medium wp-image-5672 " title="Applications for Good Registration Table" src="http://codeforamerica.org/wp-content/uploads/2011/05/codeathon1-300x197.jpg" alt="" /></a>
</div>

Moderated by Arthur Grau of <a href="http://www.one-economy.com/" target="_blank">One Economy</a>, the event began with a round table introduction of everyone in attendance &#8212; who they were, what they wanted to build, and how they wanted to be involved. The usual suspects were assembled: technology entrepreneurs, local community activists, civic developers, and <a href="http://lalanaisage.com" target="_blank">lawyers who are developers and musicians on the side</a>. Wait, what? Like I said, this is San Francisco after all.

And this was not your usual code-a-thon. After introductions, everyone split off into teams and began working on a project that interested them. For what you have to sacrifice spending most of a Saturday indoors at a computer, one of the benefits of participating in code-a-thons is that you can learn about a new technology in a relaxed and fun environment. So I decided to work on Code for America Fellow <a href="http://codeforamerica.org/author/jeremy/" target="_blank">Jeremy Canfield&#8217;s</a> team, as his project seemed like it might involve some mapping visualizations; something I&#8217;m interested in learning more about. Jeremy&#8217;s project, pitched on Friday by S.F. Dept. of Technology staff, was to make information regarding retailers that accepts food stamps (<a href="http://www.fns.usda.gov/snap/" target="_blank">SNAP</a> for Federal, or <a href="http://www.dss.cahwnet.gov/foodstamps/default.htm" target="_blank">CalFresh</a> in California), such as grocery stores, farmer&#8217;s markets, and restaurants, more accessible to people using SNAP/CalFresh. We wanted to find a way to make sure that people who needed this important information could get it easily, immediately, and anywhere.

Jeremy and I were joined by two other local developers, [Aaron Bannert](http://www.codemass.com/), and [Ysiad Ferreiras](http://www.ysiad.com/). We had not met Aaron or Ysiad until the day of the code-a-thon, but our shared interest in the challenge of writing a food stamp retailer app made for quick bonding and a division of tasks to get to work immediately. Jeremy took on the telephony piece using a web service called <a href="https://www.tropo.com/home.jsp" target="_blank">Tropo</a>, Ysaid got to work building a <a href="https://github.com/ysiadf/AllIncomeFoods" target="_blank">GitHub</a> repo and the <a href="http://rubyonrails.org/" target="_blank">Ruby on Rails</a> framework, and Aaron and I set to work on importing into Rails, and providing query language for a dataset from the <a href="http://www.snapretailerlocator.com/" target="_blank">USDA</a> for retailers that accept food stamps from the State of California.

<div style="float: right; margin-left: 10px;">
  <a href="http://codeforamerica.org/wp-content/uploads/2011/05/codeathon2.jpg"><img class="size-medium wp-image-5674 " title="Heads down and working hard" src="http://codeforamerica.org/wp-content/uploads/2011/05/codeathon2-300x179.jpg" alt="" /></a>
</div>

After the _usual_ ice breaking &#8212; <a href="http://twitter.com/#!/brianbehlendorf" target="_blank">Apache project people we&#8217;ve met</a>, why Rails is worthwhile to learn, and why <a href="https://www.eff.org/issues/patents" target="_blank">reexamination</a> is a great patent troll avoidance strategy &#8212; Aaron and I set to work with our back-end data piece. Four hours later, we had the core app written, a strategy for finding nearest locations, and a query for getting the data from the database. Then we met up with our teammates and brought together all of our pieces. What we ended up with was the **All Income Foods app: SMS-based service which you could text into with your location, and it&#8217;d reply back with the nearest grocery stores that accepted food stamps.**

Around 5pm, each team presented their projects before the judges. Projects ranged from a simple phone app which allows Goodwill recipients easy access to information on job, health and other support services available to them, to a prototyped community stories app, enabling locals to share their anecdotes and educate students about the block they live on.

Out of all of [San Francisco which came together to build applications for good](http://applicationsforgood.org/contest-announcement/san-francisco/sf-comes-together-to-build-applications-for-good/), &#8220;PointRunner,&#8221; an app to gamify outdoor running routines, won the Audience Favorite award, &#8220;Wellness Garden,&#8221; an app to positively encourage health and recovery activities won third place, &#8220;Tap Cloud,&#8221; an augmented reality app won second place, and our app, named the &#8220;All Income Foods&#8221; app, won first place. **Our team was honored and excited to win first place!** 

Now the bigger task is before us to build more features into our app for submission to the [National contest, which ends May 16, 2011](http://applicationsforgood.org/contests/). More importantly, we want to make this app as useful and effective as possible for those who need it. Help us out on [GitHub](https://github.com/ysiadf/AllIncomeFoods).