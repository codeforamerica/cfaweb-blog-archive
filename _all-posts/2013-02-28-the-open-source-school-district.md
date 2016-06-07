---
id: 20511
title: The Open Source School District
date: 2013-02-28T13:51:05+00:00
author: Lauren Dyson
layout: post
guid: http://codeforamerica.org/?p=20511
permalink: /2013/02/28/the-open-source-school-district/
categories:
  - Cities
  - Commentary
  - News
---
_Join our next Municipal Innovation call on April 5, 2013. [Si](https://codeforamerica.wufoo.com/forms/x7p4s5/)[gn up here](https://codeforamerica.wufoo.com/forms/x7p4s5/)._

We’re always excited to see local governments adopt new ways of doing things — particularly in the area of software procurement and IT purchasing decisions. In-house open source development by local governments is one of the most exciting emerging trends, and though still few and far between, initiatives like [Georeporter and uReport](http://bloomington.in.gov/documents/viewDocument.php?document_id=6515) from Bloomington, Ind.; the [HTEZ Tsunami Evacuation app](https://github.com/Honolulu/HTEZ) from Honolulu; and [OpenTripPlanner](http://opentripplanner.com/) from Portland, Ore. and OpenPlans are paving the way.

Another promising example recently comes from the school district in Saanich, British Columbia. Faced with unsatisfactory and costly off-the-shelf options, they set to work to build an open source Student Information System (SIS) for a fraction of the cost that can also be reused by other British Columbia school districts — and eventually scale to other districts and states as well. 18 months into development, Saanich is set to [soon roll out version 1.0](http://www.timescolonist.com/news/local/saanich-school-district-builds-own-software-to-handle-student-data-defies-doubters-1.51944) of the [openStudent system](http://www.openstudent.ca/) that tracks student registrations, attendance, and grades.

[Gregg Ferrie](https://twitter.com/gferrie), IT Director for the Saanich school district, joined us for the February [Municipal Innovation](https://codeforamerica.wufoo.com/build/join-the-municipal-innovation-call) call to share some insights into how open source has changed the way they run their district, and how they made this project happen.

“This is what’s getting me excited about what’s happening in the government space,” commented open innovation expert [David Eaves](http://eaves.ca/) during the discussion. “We’re seeing lots of people at all levels of the organization who are making interesting choices to drive their organization to create and buy solutions that are radically cheaper and generate more interesting data.”

## The need for a new approach

In 2010, after being told that the current commercial Student Information System (called BCeSIS) used by 95% of the school districts in British Columbia was being discontinued and the district would have to transition to a new one, the Saanich school district decided to take matters into their own hands.

The district had seen at least five proprietary SISs come and go over the past 20 years, and each time the transition to a new system was costly and labor intensive. The last switch cost Saanich about $800,000 for training and staff time — not including licensing fees — while a neighboring district spent approximately $1.2 million.

“We wanted to get our costs under control, make it sustainable, and have [the system] under our own control,” said Ferrie. After meeting with stakeholders from other districts who expressed similar concerns about the performance, flexibility, and cost of another proprietary option, a team of Saanich district administrators went to the school board. They proposed that instead of following the lead of the ministry to switch to yet another commercial system, they take a risk and incubate a project to build their own open source SIS.

## Making the case

In conjunction with the team’s Project Manager Tim Agnew, the district developed a strong [business case](http://www.openstudent.ca/sites/openstudent.ca/files/openStudent%20Business%20Plan%20V-1.1.pdf) for the project:

> “To date, BCeSIS has cost the province and districts approximately $167 million to procure, implement and operate over the past 8 years. If we had collectively pursued a community source approach to a common SIS, we would have spent an estimated $33 million, which represents a potential savings of $134 million.”

Additionally, the district had already experienced success using open source in other areas to save money in the long run, which made getting support from senior stakeholders easier. By using [Ubuntu](http://www.ubuntu.com/), an open source operating system that allows the district more customized management of their computing resources, they have cut energy costs by a whopping 75%, saving $80,000 CAD annually — and the numbers have been verified by the provincial utility company BC Hydro, says Ferrie.

“Ubuntu or Linux provides more ‘open’ access to the operating system and its ancillary processes so we can write the scripts and administer how we manage the diskless clients much more effectively,” explained Ferrie in an email. “With Ubuntu we are free to modify or build systems that do precisely what we need them to do.” The district runs scripts on their servers that turn computers on only when they’re needed and turn off when they’re not. For example, library computers don’t turn on until around 9:00 A.M., when students are entering the library.

District officials on the business side understood that open source makes good economic sense, while educators also saw benefits since the district can offer students the latest version of software like [LibreOffice](http://www.libreoffice.org/#0) without paying for upgrades or licensing fees, and use those cost savings to invest in up-to-date equipment instead.

## &#8220;A completely different way of dealing with IT&#8221;

The board gave the a green light to move ahead with the project in 2011. With supportive leadership and some initial seed funding, the team engaged a project manager (Tim Agnew), stakeholder coordinator (Debby Davis), and two programmers, and converted three classrooms from a closed elementary school into a workspace. Eighteen months in, the team has grown to 8 and they are nearing completion of the core product.

In their development process, Ferrie says, “We’re trying to ensure we keep to our fundamental mantra of open source.” The team uses free and open source tools like [PostgreSQL](http://www.postgresql.org), [Drupal](http://drupal.org), and [Request Tracker](http://bestpractical.com/rt/), and has adopted Agile software development methodologies more often seen in Silicon Valley startups than government IT departments.

“We see it as a completely different way of dealing with IT. Most districts replicate the same services and buy the same services,” said Ferrie. Instead, openStudent is built to reduce duplication and cut costs by being available for use by districts across British Columbia — and possibly beyond — while still being modularly customizable at the district level and interoperable with the other software that school districts are already using.

“This system is built to scale for a state or province,” explained Ferrie. “The data model and architecture theoretically could be crafted to handle Texas or California — a district system that’s much bigger [than British Columbia].”

## What&#8217;s next?

The software is released under an [Educational Community Source](http://opensource.org/licenses/ecl1.php) license (an adaptation of the [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html) license designed with academic needs in mind), which means it is developed and maintained at cost for other districts to use and adapt for their own needs while still giving the openStudent team an appropriate level of control over the code. “We want the code to be available to other jurisdictions but we want to make it production ready first. At the end of the day, we want to make it available to the greater community,” said Ferrie. “If we build a successful [community] and engage other districts, we can sustain these shared services and be responsive to user needs.”

With the knowledge that collaboration is key to scaling the project further, the team is already in conversation with seven or eight other districts interested in joining forces to collaborate on the openStudent software by contributing time and resources. Precedents for successful community-sourced educational software exist, such as the [Kuali Foundation](http://kuali.org) and [BC Campus](http://www.bccampus.ca). However, it’s still proven challenging for local government and other public entities to build thriving open source communities around these projects. The openStudent team plans to establish a not-for-profit society (the Canadian equivalent of a foundation) to govern the project going forward.

Find out more about openStudent and how to get involved [here](http://www.openstudent.ca/forum/117).

[<img class="alignleft size-thumbnail wp-image-20675" title="lightbulb" src="http://codeforamerica.org/wp-content/uploads/2013/02/lightbulb-150x150.png" alt="" />](http://peernetwork.in)_Code for America’s Municipal Innovation discussions are held bimonthly. Interested in joining the next one in April? Sign up [here](https://codeforamerica.wufoo.com/forms/x7p4s5/)._

The Municipal Innovation discussions are a sample of the offerings of the [Code for America Peer Network](http://peernetwork.in), CfA&#8217;s new professional learning association for innovators in local government. Learn more [here](http://peernetwork.in).