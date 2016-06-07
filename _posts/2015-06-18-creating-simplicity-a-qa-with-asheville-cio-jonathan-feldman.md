---
id: 33738
title: 'Creating SimpliCity: A Q&#038;A with Asheville CIO Jonathan Feldman'
date: 2015-06-18T19:10:53+00:00
author: Cyd Harrell
layout: post
guid: http://www.codeforamerica.org/blog/?p=33738
permalink: /2015/06/18/creating-simplicity-a-qa-with-asheville-cio-jonathan-feldman/
categories:
  - Design
  - Digital Front Door
  - News
  - Summit
---
In May, the City of Asheville formally released a beta application called [SimpliCity](http://cityofasheville.github.io/simplicity-ui/#/search), which we wrote about [here](http://2014.codeforamerica.org/category/changing-people-and-practices#asheville-cio). SimpliCity aggregates open data from several different agencies and systems to provide residents with a simple, beautiful view of everything the City knows about a particular address. [Try it out by using](http://cityofasheville.github.io/simplicity-ui/#/search) “92 Patton Ave” as an address.

[<img class="aligncenter size-full wp-image-33742" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/06/simplicity-blog.jpg" alt="simplicity-blog" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/06/simplicity-blog.jpg)

CfA Product Director, [Cyd Harrell](http://www.codeforamerica.org/people/cyd-harrell/), caught up with [Asheville CIO Jonathan Feldman](http://www.ashevillenc.gov/Departments/ITServices.aspx) to talk about how his team built a delightful experience on top of legacy software.

**CH: So, what’s Simplicity?**

JF: Simplicity is a tool that dramatically simplifies the way residents get information they need from city government. It’s a step in the lifecycle replacement of a 10-year-old tool that we called “MapAsheville.”

**CH: How is this going to make a difference in Asheville?**

JF: I remember one Code for America presentation talking about “what if government felt like the Apple Store instead of DMV?” This is one small step in that direction.

**CH: How did you set the goal for the application?**

JF: We had an ESRI end of life product and we had to redo it. So, we said we might as well make it good. Instead of having eight different [MapAsheville](http://www.ashevillenc.gov/Departments/ITServices/OnlineServices/mapAsheville.aspx) products, it made sense to have a single framework from a user perspective. The code that looks up recycling is very different from the code that looks up building permits, but the user doesn&#8217;t have to know.

I would venture to say for most municipalities, finding information about your trash pickup will take you five minutes. _Here it takes you five seconds._

We got a taste of what it&#8217;s like to delight customers when we implemented [PublicStuff](http://www.publicstuff.com/). For example, instead of a resident calling and waiting on hold just to have our operator inform them that it won’t be possible to report graffiti without an exact address, PublicStuff asks for a picture from your phone and says thank you.  And when &#8211; 24-48 hours later &#8211; it follows up with &#8220;thank you, we have fixed it&#8221;, people go out to check and it&#8217;s true. We get these notes that are just glowing. It&#8217;s awesome to delight instead of aggravate!

**CH: We often hear that cities don’t have the time or resources to do this kind of work in-house. What’s makes the City of Asheville different?**

JF: Nothing! We&#8217;re very small, and we&#8217;re not resource rich. We&#8217;re 1.9 percent of the city budget, whereas some shops are 4 percent. Honestly, it takes less effort than people think to follow these basic design principles.

I think we’re showing that it’s possible to give people what they need on a budget. They don&#8217;t have to download gigantic pdfs on a mobile device and then scroll left and right. _And some basic user-testing early on might actually save you time and money in the long run._

**CH: Simplicity has been a “pilot” for some time, what made you feel like it was ready to go live?**

JF: We&#8217;ve iterated based on what we heard from more user experience testing, and we&#8217;ve tweaked it. There&#8217;s been a lot of back-end work. This thing is a beautiful, modern looking application, which frankly is sitting on some very old-school databases and systems.

We&#8217;re in the cloud with AWS and all this very modern stuff, and it&#8217;s very Google looking, but underneath it&#8217;s the same old ARC-GIS, Accela. It&#8217;s packaging a lot of diverse, very traditional, big bang, giant enterprise kind of systems.

There&#8217;s been a certain amount of back-end work, a certain amount of heavy lifting so the front-end can be fast and easy. Because that&#8217;s the goal. We don&#8217;t want to offer another horrible-looking, green-screen-ported-to-the-web type of application. We want to offer something better.

When we did the usability testing, we found that we had \*major\* delays in the old system, on the old architecture. Simplicity doesn&#8217;t totally replace MapAsheville, but it does replace the gigantic, cluttered screen, map metaphor where you zoom in and it takes 45 seconds.

With Simplicity, it’s so fast that people were refreshing and thinking, &#8220;it didn&#8217;t take my query.&#8221; The team fixed that by putting in a fake spinning thing. Haha!

This is not City of Asheville&#8217;s data center, it&#8217;s AWS &#8211; we&#8217;re doing a huge data load to them every night. It&#8217;s a native cloud application.

**CH: How many designers do you have on staff to make it look this great?**

JF: Well, Cyd, the short answer is none. But the real story is that we hired a GIS team that appreciates the value of good design!

We had an opening about a year ago, so [Scott Barnwell](https://www.codeforamerica.org/people/scott-barnwell/) and I talked about the hire. We have one staff member who&#8217;s a student of design, but we knew we weren&#8217;t going to be able to hire a designer. My hiring process is like my project management process &#8211; if everything is a priority, nothing is a priority.

We decided to hire a GIS person who also had some design sense and skills. We did a very interactive hire (they also had to be someone familiar with traditional big enterprise systems and Github and Postgres). When we did the hiring process, not only did we do the traditional resume screen and interview, we did a &#8220;live fire&#8221; exercise.

We asked people to do a very simple prototype of an application we might need down the road. We had five applicants; one said &#8220;no way, that&#8217;s too much work&#8221; &#8211; we were thrilled, we were able to identify that person as someone who either didn&#8217;t have the skills we needed or couldn&#8217;t handle curve balls. We said you have to post your code on Github and the design has to be relatively usable. It was probably half a day of work. We got three submissions that were pretty darn good. As an aside, we had been so active in the community with hackathons and other activities that it was clear that we love what we do and people want to work here. The prototype that was done during the job interview became the [Graffiti Mapper](123graffitifree.com).

So the short answer is, we still don&#8217;t have a designer on staff, because there are so many other things that need attention. But we made it a criteria in hiring.

**CH: Why is design important to hire for in government?**

JF: Do you want the Apple Store or DMV experience for residents? If you want Apple Store, figure out how you’re going to incorporate design.

**CH: What would you recommend to folks that want to bring Simplicity to their City?**

JF: Talk to us! We’re on [GitHub](https://github.com/cityofasheville) and on [Twitter](https://twitter.com/avlcio).