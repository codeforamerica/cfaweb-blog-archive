---
id: 8494
title: 'Ashish&#8217;s CfA Summer: Starting the Open311 Center'
date: 2011-09-09T16:14:42+00:00
author: Ashish Mittal
layout: post
guid: http://codeforamerica.org/?p=8494
permalink: /2011/09/09/ashishs-cfa-summer-starting-the-open311-center/
dsq_thread_id:
  - 409792061
categories:
  - 2011 Interns
  - News
---
I played the role of an intern at [Code for America](http://codeforamerica.org/) this summer (as a part of [Google Summer of Code 2011](http://socghop.appspot.com/gsoc/homepage/google/gsoc2011)), and it has been a wonderful experience working and interacting with people here. My focus this summer was building a lightweight, online [Open311](http://open311.org) system.

Over the past decade, cities such as San Francisco and New York City have implemented 311 systems to handle non-emergency service requests. Citizens now have an easier way to get graffiti removed or to fix a pothole. With the advent of the Open311 API, we can create applications that seamlessly interact with 311 systems across the nation. Most smaller cities and counties, however, don’t have the resources to setup a robust call center and workflow application to manage incoming 311 requests. 

The Open311 Center is a project initiated by Code for America that aims to create a lightweight system efficiently utilizing technology for working with 311 service requests. The goal is to integrate functionalities of collecting Open311 data, allowing the response coordinator in the city to look into the data and dispatch a notice to the agency/contractor &#8212; all within a single application. We have built the application using [Joget](http://joget.com/), a great open-source workflow engine for automating and monitoring processes, along with great assistance from Joget&#8217;s CEO, Michael Yap, and the Joget community.

Over the summer, I worked with a CfA fellow Michael Evans and Michael Yap to create a workflow oriented application for processing 311 service requests. The code repository for the project is available on [Github](https://github.com/codeforamerica/open311-on-joget). This application collects all the relevant information used for filing an service request from the user via a simple form and gives the administrator of the application the flexibility to add and manage the 311 data. The application is configured to provide different processing options according to various participants/users of the application. Based on the role of the user, the application executes processes which perform the operations.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/09/311-1.png" alt="" title="311-1" class="aligncenter size-full wp-image-8501" />](http://codeforamerica.org/wp-content/uploads/2011/09/311-1.png)

The above screenshot is of the request form which is used for accepting new open311 requests. It contains all parameters necessary for evaluating a service request and adds it to the database.

[<img src="http://codeforamerica.org/wp-content/uploads/2011/09/311-2.png" alt="" title="311-2" class="aligncenter size-full wp-image-8502" />](http://codeforamerica.org/wp-content/uploads/2011/09/311-2.png)

The above screenshot is of the data-list which displays all the requests along with its parameters and also allows the administrator to manage these listed requests.

Eventually, we aim to install the application as a part of Open311 centers established in various cities and enable a direct and a more efficient process of taking in and dealing with 311 service requests. It&#8217;s still in early beta, and we&#8217;re excited to keep working on it. Check back on the [CfA Blog](http://codeforamerica.org/blog) for updates.