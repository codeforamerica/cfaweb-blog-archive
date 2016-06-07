---
id: 30995
title: Keeping Food on the Table, via Text
date: 2014-06-23T23:17:24+00:00
author: Garrett Jacobs
layout: post
guid: http://www.codeforamerica.org/blog/?p=30995
permalink: /2014/06/23/keeping-food-on-the-table-via-text/
categories:
  - CfA Training
  - Fellowship
  - News
---
Truly affecting human services in this country means [developing empathy](http://www.codeforamerica.org/blog/2014/01/06/people-not-data/) with those soliciting benefits and expressing it through every interaction. In San Francisco, we&#8217;ve recently made some steps in the right direction. Clients can now opt-in to receive a text message notification when their benefits for CalFresh, California&#8217;s food stamp program, are running out. In this post we&#8217;ll talk about how that service — called [Promptly](http://promptly.io) — was developed with the San Francisco Human Service Agency (HSA).

The pressures for more effective means of communication with HSA clients were mounting: the 2008 recession increased CalFresh applicants and the Affordable Care Act&#8217;s new &#8220;no wrong door&#8221; practices created more points of entry into an already complex system. Local and state advocates continuously asked the HSA to improve timeliness, quality assurance, and quality control, pointing to the fact that only 50% of those eligible for CalFresh are receiving the benefit.

Leo O’Farrell, the Director of [CalFresh](http://www.dss.cahwnet.gov/foodstamps/) for San Francisco HSA, told us in a [recent webinar](http://codeforamerica.org/peer-network-training/06-03-2014/ "HSA Communication Webinar") that customer service has always been a focus for benefit programs. A challenge is that clients are required to periodically report on status or obtain certifications to keep their benefits. Many miss these deadlines and temporarily drop off the program, then shortly re-enroll in the program, a phenomenon called &#8220;churn.&#8221; This wastes valuable staff and client time, but more importantly, leaves people without enough food on the table during the interim.

The main way that HSA communicates with CalFresh clients is via paper notices of action. These are confusing letters in small print and bureaucratic language, delivered via snail mail. It&#8217;s often a challenge for a client to understand what they need to do to keep their benefits and take the necessary action.

Promptly is a tool developed to help clients navigate this process. It sends text messages to clients to let them know when they need to take action to keep their benefits, using simple, clear language. The app is [open source](https://github.com/codeforamerica/promptly%20) and the app developers made a wonderful [guide on how to](https://github.com/codeforamerica/promptly/wiki/How-to-Promptly%20) apply this tool to any program.

### “Instead of planning, it was really a focus on learning” &#8211; Jake Solomon

Promptly was developed through the [2013 Code for America Fellowship](http://codeforamerica.org/geeks/our-geeks/2013-fellows/) in San Francisco. Using Human Centered Design (HCD) methodologies, the Fellows started by talking to the users of HSA services to understand their needs. HCD is about listening to users, scoping a problem statement informed by user needs and then prototyping, testing, and iterating lightweight solutions. The Fellows tested three solutions in San Francisco.

  1. After speaking with over 100 staff and clients, the Fellows wanted to clarify the convoluted application process for CalFresh. They created a &#8220;how to&#8221; guide and put it on a website. The guide didn&#8217;t get much usage. But a tool at the bottom of the site allowed you to enter your cell number if you wanted text message updates about your application status. This caught everyone’s attention.
  2. Focusing on the text message requests, they decided, in partnership with the HSA team, to send a reminder to clients a week before their paperwork was due for quarterly reports. They tested it out on 27 people, and called each person afterwards to get their feedback on the experience.
  3. In those calls a story surfaced. A woman discovered her benefits had been canceled while in line at the grocery store. All the items had been collected, scanned, and bagged — and then her card was declined, causing an embarrassing moment. The Fellows decided to focus on solving this problem of clients not knowing that their benefits were going to be cut off suddenly.

The Fellows also worked closely with HSA&#8217;s Tiana Wertheim on the content and implementation details of Promptly. The basic purpose of the text message system is to simplify the &#8220;legalese&#8221; of the paper notices of action into plain language explanations with a clear call to action. Clients who were about to lose their benefits would receive the message. This targeted use case with a limited group of users meant the case workers could handle the response calls and fewer clients would panic.

### Internal Hurdles Addressed

<li dir="ltr">
  <p dir="ltr">
    Privacy: The Fellows worked closely with the City Attorney to develop a consent form, keeping the language vague so the county can apply the same form to other benefit programs.
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Data Entry: The current platform used by CalWIN, the regional consortium of 18 counties, did not have fields for cell numbers, email addresses, or text message opt-ins. An appeal was made to customize the platform.
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Staff Training: Over 100 eligibility officers were trained to use the consent forms and became acquainted with the nature of response calls, ensuring their comfort in managing the new process.
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Outreach: A message about the new service went out to all CalFresh clients, resulting in 1,200 opt-ins. HSA also began including the consent form in new application materials. There are now a total of 4,200 clients who have opted to receive text notifications via Promptly.
  </p>
</li>

<li dir="ltr">
  <p dir="ltr">
    Sustainability: The consent form is now included in all new applications and with every biannual re-enrollment process.
  </p>
</li>

<p dir="ltr">
  Initial usage show that the new service is generating good results. From 600 text messages sent to clients, the HSA received 250 response calls. A dozen people even called within five minutes of receiving the notification. This amounts to a 41% call response rate: higher than any other notification method used.
</p>

### Scaling the Lesson Statewide

The State of California is decentralized by county. Teri Olle, the Director of Policy and Advocacy at the SF Marin Food Bank, explained that the challenge for the state lies in identifying successful innovations in isolated counties and replicating their efforts across all 58 counties. This has proven challenging.

Ollie remarked, &#8220;As advocates, users, and administrators we need to make these processes consistent across the counties to fulfill the ultimate goal for consumers: to enroll easily, maintain their service, and have an easy outlet for understanding the process.&#8221;

Scaling a tool like Promptly statewide means thinking not only about the time and money for implementation, but also all the other contingencies: policy changes, client waivers, or structural change across various IT systems. A team of stakeholders is currently working to bring Promptly to other counties and agencies — while there has been a lot of interest, there&#8217;s still a lot of work to go.

### Next Steps with Promptly

Promptly is freely available as open source software — find the [code located here](https://github.com/codeforamerica/promptly%20). The tool allows human service providers to meets clients where they are, in the speed they’re already communicating, on devices that many use on a daily basis. Learn how to redeploy the texting service, for any government offering, [with this guide](https://github.com/codeforamerica/promptly/wiki/How-to-Promptly%20) and [watch the recent webinar](http://codeforamerica.org/peer-network-training/06-03-2014/) for more details.

* * *

Questions? Comments? Hit us up <a href="http://twitter.com/codeforamerica" target="_blank">@codeforamerica</a>.