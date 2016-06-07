---
id: 30433
title: Help Finding Help
date: 2014-04-17T16:13:24+00:00
author: Greg Bloom
layout: post
guid: http://www.codeforamerica.org/blog/?p=30433
permalink: /2014/04/17/help-finding-help/
categories:
  - Health
  - News
---
In 2013, Code for America’s Fellows in San Mateo County were assigned the rather lofty mission of reducing hunger in in the County. (In fact, the project’s initial name was “Bytes to Bites.”)

In the course of their research, they observed that many of the social services available (not just food pantries — but child care, legal counsel, various other programs that served the fundamental needs of the community) were not easy to find information about. They observed that everyone struggled with to find information, not just by help-seekers, but case managers, program officers — pretty much anyone in the health and human service sectors.

As it happened, the San Mateo County Library produces a directory including hundreds of organizations that provide all kinds of supportive services — with detailed information including where the services are located, who’s eligible for them, and how to access them. But this directory was only available in a printed booklet, only in two languages, and only published once a year (which meant it was often out of date soon after it was distributed). Aside from the booklet, this incredibly valuable database was sitting there, unused.

The San Mateo fellows recognized that this was an obvious opportunity. By augmenting this community resource directory database with an API (short for Application Programming Interface), San Mateo County could enable their painstakingly produced data to be accessed by anyone, anywhere — making it usable by many more people, in many more ways, than could ever be possible through a printed booklet alone. The team developed this API and named it Ohana, which means family in Hawaiian.

<p style="text-align: center;">
  ~~~~~
</p>

Meanwhile, across the country in the District of Columbia, I was working on a similar problem. In D.C., the government operates a 2-1-1 call center system that is supposed to refer callers to community resources that can meet their needs — but the data is often found to be unreliable (because it hasn’t been regularly updated). As a result, quite a few health and human service agencies in D.C. have been producing their own resource directories for years (in Access databases, or Excel spreadsheets, or even just Microsoft Word documents). It takes a lot of staff time and energy, but DC’s social workers need this information to be able to help their clients, so they’ve simply done it themselves.

<p dir="ltr">
  As early as 2009, we began asking: how can we consolidate our data and energies into an open, collaborative community resource directory platform? In an <a href="beyondtransparency.org/chapters/part-5/towards-a-community-data-commons/" target="_blank">essay published</a> in Code for America’s recent book, <em>Beyond Transparency</em>, I imagined a future in which we’ve solved this problem:
</p>

<p style="padding-left: 30px;">
  A social worker doing intakes on a tablet is able to reference the same data that is displayed on a single mother’s phone as she scans through emergency shelter options; this same data is queried by a directory application for which area librarians are trained to offer hands-on technical assistance for their patrons; a journalist sees this same data while researching city contracts; FEMA accesses this data during a crisis; a community planning consortium sees the data in its mapping tools. All of these instances involve different applications, and each of these applications might solicit its own kind of feedback, which can update, qualify, and expand the common data pool. And this shared knowledge about the services available in a community is combined with other shared knowledge bases—about the money flowing into and out of these services, about the personal and social outcomes produced by the services, etc.—to be understood and applied by different people in different ways throughout this ecosystem as a collective wisdom about the “State of Our Community.”
</p>

Technologically, this is not at all far-fetched. In San Mateo County, thanks to the Ohana API, the enabling technology is already there.

And now in the District, thanks to the help of Code for DC (our local CfA brigade), we’ve merged multiple community-produced resource directories into a consolidated dataset, redeployed Ohana and loaded it with this DC service directory data. Without even having a local government program, or our own CfA fellowship team, we [now have an open platform, too](http://communityresourcedata.codefordc.org/solution.html).

<p style="text-align: center;">
  ~~~~~
</p>

An API, however, is only one piece of this puzzle, and it’s not necessarily even the first one that should be put in place. To realize the vision of an ecosystem of services sharing the same data, so many institutional and human behavior changes need to take place that the technology seems comparatively easy. To build that future of open, interoperable community resource directory data, we’re going to need a common standard for structuring this data — and we’re going to need to support people and organizations as they implement that standard and with all the trial and error, and learning, and behavior shifting, and, indeed, cultural change that this entails.

This is what prompted us to launch [the Open Referral initiative](http://openreferral.org/).

In Open Referral, we’re bringing a diverse set of front-line stakeholders (like hospitals and health clinics, social workers and community colleges) together with vendors (like Single Stop USA and Purple Binder) and subject matter experts (like academics and interoperability specialists), to sit at the same table. Together, we’ll collaboratively build, test, and evaluate these open platforms. Through this process, we aim to produce a new set of standards for structuring, sharing, and circulating community resource directory data on the web.

The first chapter of this Open Referral initiative will be written primarily in the San Francisco Bay Area and D.C., where we’ll coordinate the work of service providers, user groups, startups, and incumbents, funders and CfA brigade volunteers, as they experiment, learn, and plan for the future. By 2015, we hope to see a second wave of pilots join us, and soon after that, we aim to have a validated standard gaining adoption all across the country — and even the world.

However, you won’t have to wait until then to learn more or get involved! You can receive updates on this initiative by subscribing to our <a href="http://openreferral.org/" target="_blank">updates list</a>. You can join <a href="http://groups.google.com/forum/#!forum/openreferral" target="_blank">our community forum here</a>. You can check out our D.C. and San Francisco Bay pilots. And you can follow the development of our code-base through GitHub here. [Onwards!]

&nbsp;

* * *

&nbsp;

Questions? Comments? Hit us up <a href="http://twitter.com/codeforamerica" target="_blank">@codeforamerica</a>.