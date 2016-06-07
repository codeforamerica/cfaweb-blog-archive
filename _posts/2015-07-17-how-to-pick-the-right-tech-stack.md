---
id: 33938
title: How to Pick the Right Tech Stack
date: 2015-07-17T13:13:42+00:00
author: Amy Mok
layout: post
guid: http://www.codeforamerica.org/blog/?p=33938
permalink: /2015/07/17/how-to-pick-the-right-tech-stack/
categories:
  - 2014 Fellows
  - Civic Hacking
  - Data
  - News
  - Technology
---
What technology stack is best for this project? That’s always a hard question to answer.

During [my fellowship year](https://www.codeforamerica.org/geeks/our-geeks/2014-fellows/), 10 teams made 10 different decisions about what technology stack to use. For many, the choice was not based on what was easiest for us to use, or what we were most familiar with. Choosing the tools to use was a balancing act. Our apps needed to be easy for government staff to update and also help them improve their programming skills and introduce better project workflows. **Sometimes, the code needed to just get out of the way so non-technical teams could inherit our work.** In the end, we needed to create long-lasting software that would have a real impact on the cities we worked with.

[<img class="aligncenter size-full wp-image-33949" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/tech-stack-blog.jpg" alt="How to pick the right tech stack" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/tech-stack-blog.jpg)

I reflected on the experience of choosing a technology stack with developers from different teams and found we all made very different choices.

**Denver: Familiar and different at the same time**

Denver already has a well-established team of developers using a mostly .NET stack. When the fellowship team first started working with Denver, they were asked to use .NET for development. The city was confident using well-known technologies would allow their staff to maintain the applications after the fellows moved on.

The [fellowship team](https://www.codeforamerica.org/governments/denver/) first explored the style and standards Denver used in their .NET applications. The fellows saw the opportunity to use a different framework from the .NET ecosystem. This experiment helped city developers explore new technical concepts while using a language they were very familiar with.

The fellows’ app, Denver Street Sweeping, was well-received by the city and has become an important part of the city’s digital services. To integrate the app with existing city websites, Denver decided to expose the Street Sweeping API as a service to use in their ecosystem. The fellows’ technical decisions paved the way for Denver to continue maintaining and enhancing the Street Sweeping app, and to improve other apps the city has built.

**San Antonio: Delivering code and the agile methodology**

I worked with the City of San Antonio during my fellowship. San Antonio has a strong GIS programming team focused on building mapping and information systems with JavaScript, ESRI tools, and other programming languages. Their team was very capable and open to learning something new. We chose to use Ruby on Rails with some JavaScript to build Homebase, an app that helps homeowners get the permits they need to fix their home. We wanted to explore building in a new way — with open source tools and libraries — but not take on too many new languages that might make learning difficult. Ruby is easy to learn and the code is easy to read. The Rails framework has many free resources available on the web that allowed the San Antonio team to pick it up quickly.

Because we were introducing a new programming language and a new process for building applications, we started our hand-off a few months before the end of the fellowship. The city was very open to learning new concepts, so we decided to coach them on more than just using new languages and frameworks.

We found that the current methodology they use to develop software is a very waterfall-like workflow. The programmers get a list of requirements from department directors that form the base of development projects. These requirements are created by departments executives based on the problems they believe their users face, but aren’t always informed by direct user feedback.

The city programmers never talked to users. They relied on the requirements that were passed down. In typical waterfall fashion, these departments would add new features and requirements throughout the project, making it hard to estimate the time the programmers needed to deliver software. Oftentimes these departments would add new features and requirements throughout the project. The lack of flexibility in the programming team’s waterfall process made it hard for them to deliver projects on time. We saw an opportunity to coach them on user-centered design and agile development to help them adjust to changing requirements, and arm them with knowledge of how their software would be used to help them open up a conversation about new requests.

We experimented with different training styles to see what worked best. We started with lecture-style lessons to give them an overview of the concepts. Then, we had them practice with small exercises that put their new skills to work. We eventually moved to the current backlog of projects their team was working on, and tried to determine how Agile could help them work more effectively.

In the end, the [San Antonio team](https://www.codeforamerica.org/governments/sanantonio/) continued development on Homebase and learned about how to help manage their relationships with client departments.

**Atlanta: Hide the code and empower city staff to use their expertise**

The [Atlanta fellows](https://www.codeforamerica.org/governments/atlanta/) were tasked with increasing the transparency and accessibility of the city&#8217;s procurement process. Their app, ATL Procurement, was first developed as a simple, statically-generated site using Jekyll.

When the fellows demoed the project to the city, and started showing how city staff would maintain the project using Markdown, the city grew uncomfortable. Updating the site seemed difficult with the current setup, which could have spelled the end for the ATL Procurement project after the fellows finished their term. The procurement team did not have any technical staff that will be able to keep the project running, and there would be too large a learning curve to bring the existing team up to speed on building the site.

The fellows decided it was time to change the technical stack to something their city partners were more comfortable with. The fellowship team re-implemented the project in WordPress, a platform with a less-intimidating admin interface. This decision allowed the procurement team to focus on the content of the site — helping the public understand purchasing and available contracts — using the simple WordPress visual editor.

**Know the Needs**

Each city had a unique need. Denver wanted to ensure their staff could start building out of the gate with existing skills. San Antonio wanted their team to learn new skills and expand their toolkit to include new development methodologies. Atlanta wanted something that could be easily updated using a visual editor.

Figuring out these needs required each city to be honest with the fellows about their technical capabilities, and for the fellows to carefully observe and experiment with different technology choices to find the best option for their government partners.

There’s no clear winner when choosing languages, frameworks or processes to develop government apps. The decision isn’t simple, and requires thought and consideration. In the end, we worked to ensure the technology we delivered would empower city staff to do their jobs more effectively, and continue to serve residents long after the fellowship wrapped up.