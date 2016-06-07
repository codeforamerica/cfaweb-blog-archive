---
id: 15470
title: Put Your Civics Where Your Houseplant Is
date: 2012-08-14T14:07:08+00:00
author: Ben Sheldon
layout: post
guid: http://codeforamerica.org/?p=15470
permalink: /2012/08/14/put-your-civics-where-your-houseplant-is/
dsq_thread_id:
  - 805297840
categories:
  - 2012 fellows
  - Commentary
  - News
---
<p style="text-align: center;">
  <a href="http://civicsgarden.herokuapp.com"><img class="aligncenter size-large wp-image-15473" title="civicsgarden-large" src="http://codeforamerica.org/wp-content/uploads/2012/07/civicsgarden-large-1024x455.png" alt="" /></a>
</p>

The core assumption of engagement applications is that people will do an activity consistently and repeatedly if you just structure the experience and incentivize it correctly — even if it’s asinine.  The justification for _civic_ engagement apps can be similarly foolish: people will perform a potentially beneficial activity that they aren&#8217;t currently doing if we give them the ability to do it on the internet (or via SMS, or iPhone, etc.). That&#8217;s why I built [Civics Garden](http://civicsgarden.herokuapp.com).

A few months ago a Code for America email thread came around asking how &#8220;If you could tell the story of how government works, what would you say?&#8221; I pushed back with the idea that one cannot know government without participating in it, and since we are a government of, by, and for the people, the best place to start would be reflecting on one&#8217;s own civic life and civic actions.

A tried and true method of reflection is journaling. Hundreds of millions of people keep a journal called Twitter, reflecting and writing on their days experiences, tribulations, meals, and cat sightings (this is not a comprehensive list). If people naturally do this, why not ask them to reflect specifically on their civic actions&#8212;voting, volunteering, checking out a library book, picking up a piece of trash, smiling at a stranger&#8212;and write down that reflection (however brief) on a regular basis?

Projecting from my own nature, people are fickle, lazy, unreliable creatures. That&#8217;s why gamification is the hotness. &#8220;How can I get you to look at my ads every day? I&#8217;ll make it a game.&#8221; Sure, this is no different than historical incentives (&#8220;How can I get you to work in my coal mine? I&#8217;ll pay you money.&#8221;), but now it&#8217;s on the internet where advertising is easier to place than coal mines. One form of gamification I really enjoy are virtual pets: like [tomagatchi&#8217;s you feed with Unit Tests](http://www.happyprog.com/tdgotchi/), or [flowers you water with foreign language vocabulary](http://www.memrise.com/). They encourage you to perform an activity because you instinctively (unless you&#8217;re a sociopath) feel good when they&#8217;re healthy and bad when they&#8217;re sickly&#8230; despite the fact you know they aren&#8217;t actually alive.

Civics Garden combines these concepts: by signing up, users adopt a virtual plant that they keep healthy by regularly &#8220;watering&#8221; it by writing down their civic deeds. If they go too long without a journal entry, the plant will wither and eventually die. Just like owning real houseplants, it has exhilarating potential.

<p style="text-align: center;">
  <img class="aligncenter size-full wp-image-15474" title="bamboo-states" src="http://codeforamerica.org/wp-content/uploads/2012/07/bamboo-states.png" alt="" />
</p>

I built Civics Garden with Node.js and MongoDB using Twitter for authentication. Each new user receives a healthy bamboo plant to caretake by writing short journal entries. To keep people reflecting regularly, one&#8217;s plant will wither after two days, and die after four&#8211;though users can replant it as many times as necessary. To keep them coming back to the site, users receive a tweet from [@civicsgarden](http://twitter.com/civicsgarden) to let them know when their plant needs refreshing. As an minimum viable product (MVP), it&#8217;s high-on-concept/low-on-looks, but Diana and Emily helped with the graphics.

I&#8217;ve tested it internally with Code for America fellows and it should be a rousing success. All of us, as active civic participants performing important civic deeds should be able to briefly but consistently reflect upon and record our actions, right? See for yourself on Civics Garden and [test your ability to reflect on a healthy civic commitment](http://civicsgarden.herokuapp.com).

…or maybe people just don&#8217;t like bamboo.

<p style="text-align: center;">
  <img class="aligncenter size-full wp-image-15479" title="civicsgarden-result" src="http://codeforamerica.org/wp-content/uploads/2012/07/civicsgarden-result.png" alt="" width="100%" />
</p>

&nbsp;

Question? Comments? Hit us up [@codeforamerica](http://twitter.com/codeforamerica).