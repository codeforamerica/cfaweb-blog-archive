---
id: 32555
title: How a bumpy ride turned into a golden ticket
date: 2014-12-22T19:37:21+00:00
author: Jeff Maher
layout: post
guid: http://www.codeforamerica.org/blog/?p=32555
permalink: /2014/12/22/how-a-bumpy-ride-turned-into-a-golden-ticket/
categories:
  - 2014 Fellows
  - Fellowship
---
_“What the heck is this?”_
  
[<img class="aligncenter wp-image-32563" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/form.png" alt="old registration form" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/form.png)

I was staring at a giant illegible square on paper. My teammates, Anna-Marie Panlilio and Andrew Maier, had just returned from a visit to Rhode Island and were filling me in on what they had found. It was a completely unusable form that was&#8230;well&#8230;still being used.

A common issue in a child’s education is the breakdown of the relationship between parents and schools. Schools have trouble keeping parents involved (lack of good contact info, parents don’t have time, etc.). Parents have impersonal and poor interactions with schools that don’t always leave reasons for trust and good faith. This registration form is one of those interactions.

The three of us were doing a year-of-service as [Code for America Fe](http://www.codeforamerica.org/)[llows during 2014](http://www.codeforamerica.org/governments/rhodeisland/), partnering with the [Rhode Island Office of Digital Excellence](https://twitter.com/RI_ODE). We only had a year to do something, so there was no illusion that we’d be able to fix the entire school-parent relationship in that time. However, it seemed like we could help get that relationship off to a good start by improving the first impression: school registration. By late July, we had a whimsical, colorful, and usable online registration prototype called Ticket to RIDE (RIDE being the Rhode Island Department of Education). Parents loved it and schools were excited by the data entry time it would save them.

[<img class="aligncenter" style="float: center; margin: 10px 10px 10px 10px;" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/ticket-to-ride.png" alt="ticket to ride screen grab" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/ticket-to-ride.png)

**The application failed**. There would be **_no_** Ticket to RIDE.

**Why?**

I’d like to illustrate what we learned from the experience. It’s my hope that other folks doing year-of-service-y work can learn from our experience rather than repeat our mistakes.

These were our most grievous mistakes:

  * **We didn’t test our ideas soon enough**
  * **We didn’t do the hard part early in the process**
  * **We failed to think about who would sustain the project after we left**

## We didn’t test ideas rapidly

Our team came to a consensus in late April that we’d work on school enrollment, but it wasn’t until late July that we had done a substantial user test on the idea itself. Instead, we focused our efforts on trying to built out a mostly functioning system. This could have been catastrophic to our year-of-service if our idea had not resonated with parents in July &#8212; we would have built most of a system that wouldn’t have been accepted by its primary user.

While we dodged that bullet by lucky intuition, it still had the detrimental effect that we were building a system that we didn’t entirely know the direction of. For example, we were torn on whether to present the enrollment forms as mad libs or straight questions/responses. The result is that we pulled in a lot of technologies to support the mad libs style forms, which wound up not being the favored approach. We had to spend a significant amount of time unraveling the code from the mad libs style when we settled on straight questions/responses. In other words, we were making big decisions affecting the quality of the project that were difficult to back up from.

Towards the end of the project, this came to bite us. Our code base was sloppy and inflexible. Whenever we had to adjust something, we had too much code to change and that it was hard to do it cleanly under time constraints. If we had tested our ideas with lower fidelity prototypes (like testing with pen/paper or just 2-4 screens at a time), we could have adapted quicker and then produced higher quality code for the final project.

## We tried the hard part too late

The hardest part of making Ticket to RIDE successful was to get the enrollment information we’d collect to be transferred into schools’ student information systems (SIS’s). They’re malleable in all the wrong places, inflexible in areas around integrating with other education software, and have miserable user experiences. (To illustrate how bad they are, one school we worked with had dedicated SIS training for all of July! Imagine how unintuitive a product must be if every person has to spend 80-160 hours learning how to use it?)

While the primary goal of Ticket to RIDE was to give parents a better first impression of their child’s school, a very close secondary goal was to improve the efficiency of school staff so that they could focus on more important things than typing in paper registration forms to the SIS’s. It was also the way to get schools jazzed about using it.

It was completely my failure to not have started figuring our how to do this part immediately in April. In some ways, this is the same as the first mistake: test ideas early. We should have tested system integration early on, because that part flopped when we approached it in September. (Note: The SIS’s had minimal to no documentation on how to do this, and the vendors were uncooperative to helping us. We tried for two months to get it to work ourselves, but fell short. Instead, the vendors charge cash strapped schools $300-600 per hour even though the schools already pay tens/hundreds of thousands of dollars already for the software and support.)

In short, if your project hinges on a complicated and vital aspect, make sure you can overcome the hurdle early on. An example for us would have been getting some dummy data imported in May or June. If we had learned how hard it was to do this early, we might have pivoted to an altogether different project earlier on.

## Who would continue our work?

A large responsibility Code for America places on its fellows is to expose government to [user-centered design](http://www.codeforamerica.org/governments/principles/#needs) , or identifying the people that will use a service early on and tailoring it to their needs and wants (communications folks know this as “know thy audience”). The most common way user-centered design is expressed in software is by making interfaces user-friendly.

However, user-centered design should extend to all parts of a project, including how it’s made and how to make it easy to sustain for the folks it’s for. We didn’t put ourselves in the shoes of RIDE’s IT department and didn’t think about what they needed from us to make Ticket to RIDE sustainable for them. We were making the application in a programming language/framework called Ruby on Rails on our Macs. All they were experienced with was a language called C# on Windows.

When we arrived with several months deep project asking if and how they would sustain Ticket to RIDE, they reasonably pushed back. With that said, RIDE reasonably refused to sustain the application. We had made it in a technology stack that they were not familiar with and could not feasibly take the time to learn given their current workload. In this way, we had not thought about one of our most important users and stakeholders.

This is a common failure in the civic technology and year-of-service worlds. Projects are built from the ground up with sustainability being an after thought. Who pays the bills to keep the project or service alive? Is the project documented in a way that a stakeholder understands how it works? Does anyone have time and the skills to maintain the project later on?

We should have had definitive answers to these questions early on, but didn’t.
  
[<img class="aligncenter" style="float: left; margin: 0px 20px 20px 0px;" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/ticket-logo.png" alt="ticket to ride logo" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/ticket-logo.png)

## Learning from the lessons!

In addition to user-centered design, another [principle](http://www.codeforamerica.org/governments/principles/) Code for America encourages governments to embrace is experimentation and learning. By taking risks, any person or organization learns valuable lessons about what does and doesn’t work. An example is the classic Tom Edison and the lightbulb one: he learned something valuable from every failed try until he had a eureka moment and there was light.

In July (in the middle of our work on Ticket to RIDE), another potential project came along. RIDE’s Early Childhood team wanted to find a way to make it easy to register children for the state’s pre-kindergarten lottery. They were hoping to grow the number of freely available pre-K classrooms, but were having trouble scaling the registration and lottery selection processes. These were things technology could very much help with. This project came to be known as [Golden Ticket](https://github.com/codeforamerica/golden-ticket). Golden Ticket collected  registrations without parents having to leave home and ran the lottery selection process faster than you can erase a whiteboard.

Because of our experience with Ticket to RIDE (and, admittedly, some tighter time constraints), we did not make the same mistakes with Golden Ticket.

## Ideas were tested rapidly

[<img style="float: left; margin: 20px 20px 20px 20px;" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-ticket.png" alt="golden-ticket" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-ticket.png)

Within the first week, my teammate Andrew had used a drawing application called Balsamiq to simply sketch the screens we envisioned in Golden Ticket. Over two weeks, we honed the designs with the RIDE Early Childhood team to make sure everyone understood what we were trying to solve and what the application should look like.

But that was only one part of the equation. Would parents use it? Would they embrace the idea of registering online? Would they trust an electronic selection process as much as they trusted people sitting in a room picking names off a paper list?

Instead of building a web application from scratch right from the get go, we decided to do the project in three phases, testing our hypotheses as we went, and only proceeding when they were validated.

Phase 1 was seeing if parents would use it. We created a modest Google Form in an hour and put it online for parents to use. And they used it! About a thousand students were entered into the lottery via the form.

[<img class="aligncenter size-full wp-image-32559" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-doc.png" alt="golden-doc" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-doc.png)

We moved onto phase 2, doing an electronic selection. We took under a week to create a tool with no user interface (command line) that ran the lottery selection process. It ran much quicker than the paper lottery (2 seconds vs. a week) and folks questioned the results no more than they had the paper one. Another hypothesis validated.

Phase 3 was making a clean, usable, and repeatable process by creating a full web application. Unlike Ticket to RIDE, when we had learned about our users and had confirmation that our ideas were solid. We built with more confidence and didn’t have to fumble around with as many little decisions.

As we were building it though, we routinely checked in with the RIDE Early Childhood team to validate that what we had built was what they wanted. Things that were wrong were adjusted quickly and flexibly as a result.

## We tried the hard part early on

The hard part of the project was the lottery selection process. It wasn’t simply a matter of throwing names in a barrel and picking them out at random, but one weighted by location, income level, and gender.

As was mentioned earlier, our phased approach played out nicely for seeing if we could do the lottery in a way that would meet their needs and credibility. We didn’t build out a beautiful web application that conducted the lottery, but focused on a simple tool with a single text command to run the lottery.

Because we had done this, we knew that when we got more ambitious with making a more thorough project, we knew the hard part would be feasible.

## RIDE would continue the work

From the beginning, we knew that our partners in RIDE’s Early Childhood team wanted the app, but we were uncertain about whether RIDE’s IT department would sustain the application after our fellowship ended.

Not anxious to repeat our blunder from Ticket to RIDE, we invited the IT department into our early planning meetings before phase 2 started. We asked, “what do you need us to do so that you can own this next year?” The only ask was to make it in the technology stack they used. A few days later, I installed Windows on my computer and was learning C#.

When we completed phase 2 and were starting phase 3, we iterated with the IT department on documenting the app, how it would be deployed, and how new features or bugs would get attention after the fellowship. Not only did we have buy-in from a sustainer, but we also had a plan.

[<img style="float: left; margin: 0px 20px 0px 0px;" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-1.png" alt="golden-1" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-1.png)

[<img style="float: center; margin: 20px 20px 0px 0px;" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-2.png" alt="golden-2" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/golden-2.png)

## A happy ending!

Golden Ticket was used for the 2014-2015 lottery and saved parents and administrators a ton of time (we estimate 800+ hours). Additionally, Golden Ticket was included in a Federal grant application to expand pre-K offerings to help demonstrate the state’s capacity to handle registrations should many more students/cities be eligible for the lottery (as a result of more funding). [RIDE won the grant](http://www.ride.ri.gov/InsideRIDE/AdditionalInformation/News/ViewArticle/tabid/408/ArticleId/193/R-I-receives-grant-to-add-preschool-classrooms-in-high-need-communities.aspx) and will be receiving $19 million in funding to expand from 17 classrooms to 60 between 2015 and 2019. More kids will get a [great start](http://www.centerforpubliceducation.org/Main-Menu/Pre-kindergarten/Pre-Kindergarten) in life!!!
  
[<img style="float: center; margin: 20px 20px 0px 20px;" src="http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/twitter-1-golden.png" alt="twitter-1-golden" />](http://www.codeforamerica.org/blog/wp-content/uploads/2014/12/twitter-1-golden.png)

## Recap

So now you’re out to try something new, software or otherwise. Awesome! Just remember to:

  * **Focus on the user**
  * **Test your ideas early and iteratively**
  * **Understand the hard parts sooner than later**
  * **Think about the long term game**