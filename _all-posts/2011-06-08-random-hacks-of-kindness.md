---
id: 6021
title: Random Hacks of Kindness
date: 2011-06-08T09:23:24+00:00
author: Chacha Sikes
layout: post
guid: http://codeforamerica.org/?p=6021
permalink: /2011/06/08/random-hacks-of-kindness/
dsq_thread_id:
  - 325870523
  - 325870523
categories:
  - News
---
Went up to my Code for America city (Seattle) this weekend to participate in Random Hacks of Kindness, or #RHOK3. [Random Hacks of Kindness](http://rhok.org) is a movement of software developers, hackers, and humanitarian workers who get together for intensive weekends building tools to support emergency relief efforts.

In Seattle, we had about 80 people actively developing projects this weekend. I helped to facilitate the large group collaboration, helping people who don&#8217;t know each other to quickly find alliances in the group so as to have productive working teams. This was called a &#8220;[Brain Collision](http://www.cnn.com/2011/TECH/innovation/06/08/hacks.kindness.followup/)&#8221; on CNN, and I was excited to know that this was the first time that some of movers &#038; shakers at NASA were able to attend a participatory coding event like RHOK. I&#8217;m grateful to Willow Brugh ([Jigsaw Renaissance](http://www.jigsawrenaissance.org/) &#038; Johnny Diggz [Tropo](http://www.tropo.com)for bringing me up there to participate.

Microsoft had given us space on their campus in Redmond, and we had hundreds of feet of whiteboard plastered with wireframes, post-it notes as we created many working prototypes. It was awesome. Have a look:



[Slideshow](http://www.flickr.com//photos/linepithemate/sets/72157626915607946/show/)

Pascal Shuback, who is an emergency manager for King County, created SAARAA, which is a situational reporting mobile application which allows for crowd-sourcing information about emergency situations. For example, you can report a drowning child (using the similar data intake methods that emergency responders use currently) or a fire or other situation. And you can upload pictures. The idea is to have as much information about an emerging situation so as to understand it and respond more effectively.

There were a number of people from NASA (including Michael Laine, of the Space Elevator idea, who prototyped a &#8220;smoke detector on a string&#8221; or &#8220;tethered tower&#8221; which is a tool that can help assess air quality or temperature, which emergency relief workers could drop down the side of a tall building, or float up in a weather balloon, to get an understanding of the location of a fire or other disaster.

### MoveFood

The project I worked on at RHOK was called MoveFood. MoveFood is a tool that allows people with food to announce that the food is available, and then people who need food can claim it. This can help in everyday situations, but the tool would also be useful in the event of an ongoing disruption to the supply chain of food.

There were **FOUR** groups in other cities that also worked on this. We struggled with the tension between real disasters and this form of everyday disaster. One important thing about disasters is that you should, ideally, be as prepared as you can be: ahead of time.

At the event, we created an API for the food transactions, and a javascript+html front end, so that the tool could be used as a web application. I worked on the front end, and also made it possible that any food items could be announced in short format via twitter and text (using a service called &#8220;[SMSified](http://smsified.com/)&#8220;.) For example, a message would say: Apples 40 pounds (37.788299, -122.399983) EXP: 2011-07-11 t.co/abcdef. Replying with a text message would allow you to claim the item. Johnny Diggs, who&#8217;s company makes SMSified &#038; Tropo, helped me figure out how to connect our database to text message.

Kip Silverman, from Portland, has been thinking about this idea for over two years, and brought a lot of knowledge about the legal implications of food sharing. I&#8217;m definitely planning to continue working on this project, and am excited to see how this could help in our cities. Not only is food an issue with people not having enough to eat, but also a huge source of waste in cities. Making it easier to distribute the food would help reduce waste. Practicing this form of resource distribution in non-emergency situations will also help in the event of an actual emergency.

### Disaster Response

Like most people, I&#8217;m in awe of first responders and people who rescue people in need. It was a tremendous opportunity to be able to collaborate with real life first responders like Pascal Shuback (he was a fireman.) Claire from Microsoft&#8217;s disaster response team, said that software that is developed to work in a crisis situation can also normally be used in everyday situations, such as at the grocery store.

I enjoyed trying to help my own team conceptualize and wireframe our project. I said &#8220;Imagine if an earthquake or flood happened right now. What would we build to help coordinate food exchange?&#8221; I can definitely say that this form of thinking help to weed out some of the philosophical technological ideas that often inhabit the minds of developers like myself. Thinking about emergency response has some interesting form factors. The technology you use should be stable, ubiquitous, easy to fix, use clear language, work quickly, not have too many parts and be redundant in the event of failures of various grids: electrical, internet, mobile. For MoveFood, we imagined a &#8220;disaster switch&#8221; that could kick into effect. This would allow a dispatcher to help coordinate food distributions.

### Other projects

**iRecord**
  
A way to have offline emergency communications routed through phones, basically having an interface to the cloud. (*I think I have this name right.)

**Eco-tricorder**
  
A way to get information about water quality, superfund sites, and government representatives for a location &#8211; to understand the state of the environment and be able to help out the EPA or similar organizations to recommend areas that have low quality environmental factors (poor air quality, bad water.)

**HelpSauce**
  
A tool to map emerging twitter hashtags to figure out where a situation is working. Talking about using !help (instead of #help) as a twitter way to indicate that you are actually participating in an event (vs. talking about it) Ex. !earthquake or #earthquake. !help !sos

**Open211**
  
[&#8220;Redirectory&#8221;](http://rectangl.es) &#8211; an open social services directory. More work was done to bring this to Portland, Oakland, & Seattle and other cities.

We had about 80 people working on these projects, and teams were generally 5-10 people. 2 days of development. Multiple programming languages and skillsets, and most people did not know each other already. I really learned so much about designing software for emergency situations, and I&#8217;ve already started sharing this with the other Code for America fellows. They don&#8217;t know it yet, but I might declare one of our Labs Fridays &#8220;Emergency Friday&#8221; where we hack for emergencies. So thanks to everyone who participated.