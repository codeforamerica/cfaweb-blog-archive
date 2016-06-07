---
id: 5091
title: Github pushes, Screaming Hawks, and a Culture of Collaboration
date: 2011-04-26T09:00:00+00:00
author: Talin Salway
layout: post
guid: http://codeforamerica.org/?p=5091
permalink: /2011/04/26/github-pushes-screaming-hawks-and-a-culture-of-collaboration/
dsq_thread_id:
  - 288973068
categories:
  - CfA Labs
tags:
  - labs
---
It&#8217;s a busy day in the Code for America offices. Coders and Designers work in twos and threes, building out four or five different projects. Suddenly, over the bustle of discussion, a loud [falcon scream](http://www.youtube.com/watch?v=33DWqRyAAUw) pierces the air, followed by a robotic voice reading out &#8220;Scott Silverman pushed to homework_notifier: Fixed secondary button gradient colors in Firefox.&#8221; Around the office, some fellows stop and look up for a second, offering applause, congratulations, or just laughing at the absurdity of the sound.

What&#8217;s happening here?

A couple weeks ago, some of the Fellows on Team Boston, myself included, were working late into the night on our [&#8220;Homework Notifier](http://codeforamerica.org/?cfa_project=whatsassign-me)&#8221; app. I pushed a minor bugfix to our [Github repository](https://github.com/codeforamerica/homework_notifier), and a few seconds later, one of the other fellow&#8217;s iPhone beeped. They had set up the github service hook to notify them via Notifo whenever someone updated our repository. &#8220;That&#8217;s kind of interesting,&#8221; I pondered, &#8220;but _why_ would you want to do that?&#8221;

Their response kind of surprised me: &#8220;Well, it gives you an idea of what&#8217;s going on with the project, so you know what the rest of the team is up to.&#8221; Not long after, one of my teammates Max came up with an idea: &#8220;Hey, could we make those speakers scream out a hawk sound on every commit?&#8221; People here love the screaming hawk sound. I think it started with a homonym of my name, _Talin_, and grew from there.

My favorite projects are the simple scripts that directly accomplish what you want. Thus was born the Github Screamer: a little [Sinatra](http://sinatrarb.com) script on the computer powering the speakers, with a github [post-receive hook](http://help.github.com/post-receive-hooks/) to fire it off on every push. After setting this up for the homework notifier app, I decided to include other current projects as well. At the time, I figured it would just be a bit of an amusing annoyance the next day at work, and we&#8217;d run it for a day or so before someone shut it off. A good joke, but nothing more. (Although, unexpected to me, Scott ended up working even later that night. At 3am, he was the hawk scream&#8217;s first victim. muahahaha!)

The actual response the next day, again, surprised me. After people figured out what was going on, it was actually something highly appreciated. Features were requested and added, the notifications gained a text-to-speech synthesizer, and user-customizable sounds.

Now, the audible &#8220;scream&#8221; notifications are a part of daily life here in the CfA offices. A hawk scream lets me know that a fellow Boston teammate has pushed to our project, and I should probably check out what&#8217;s changed. But, in addition, there&#8217;s now a Chewbacca cry when Alan updates the [Engagement Toolkit](https://github.com/codeforamerica/engagement_toolkit), an intercom noise when Aaron works on some [open census data](https://github.com/codeforamerica/census2pgsql), or a clip from Duck Soup&#8217;s &#8220;[Barbara Streissand](http://youtu.be/uu_zwdmz0hE)&#8221; when Michelle pushes to the [RedesignGov](https://github.com/codeforamerica/designforamerica) repo. These sounds not only help us keep track of what everyone is up to, it really helps us bond as a class of fellows.

The source for our Github Screamer is available [here](https://github.com/codeforamerica/github_scream). You can copy that down and set this up in your office. Also, check out some of our other open source projects on our [github profile](https://github.com/codeforamerica/) (you can also see an overview [here](http://codeforamerica.org/projects/)). Write some code for America, and when you commit it, you can know that somewhere in San Francisco, you can surprise a CfA fellow with a full-volume hawk scream.