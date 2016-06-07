---
id: 11102
title: 196 Github Repositories
date: 2012-04-11T14:08:49+00:00
author: Ryan Resella
layout: post
guid: http://codeforamerica.org/?p=11102
permalink: /2012/04/11/196-github-repositories/
dsq_thread_id:
  - 645415415
categories:
  - CfA Labs
---
At the time of this writing our GitHub page has 196 repositories: <a href="http://www.github.com/codeforamerica" target="_blank">github.com/codeforamerica</a>

Everything that we build at Code for America is a open source.  On our Github we have various government API wrappers in Ruby, PHP, and Python. We also have many applications that we built last year like <a href="https://github.com/codeforamerica/classtalk" target="_blank">ClassTalk</a> and <a href="https://github.com/codeforamerica/adopt-a-hydrant" target="_blank">Adopt-A-Hyrdant</a> to name a few.

With 196 GitHub repositories and growing how does anyone find any of these projects?

Lately, Twitter has been releasing many of their open source projects.  The most popular one is the Twitter Boostrap.  For their open source projects Twitter created this GitHub page for all their repositories: <a href="http://twitter.github.com" target="_blank">twitter.github.com</a>. It simple to see and sort what Twitter&#8217;s up to.

Luckily the code is open source. I thought this would be a good starting point for us, so I created a page for this on Code for America&#8217;s GitHub page.  In just a few minutes, using the Twitter GitHub page, I was able to make an organization page for us: <a href="http://codeforamerica.github.com" target="_blank">codeforamerica.github.com</a>

The walk through is quite simple.

Clone this repository: <a href="https://github.com/twitter/twitter.github.com" target="_blank">github.com/twitter/twitter.github.com</a>

git clone: <a href="https://github.com/twitter/twitter.github.com.git codeforamerica.github.com" target="_blank">github.com/twitter/twitter.github.com.git codeforamerica.github.com</a>

cd codeforamerica.github.com

rm -rf .git

I removed all instances of the word &#8220;Twitter&#8221; and replace it with &#8220;Code for America.&#8221;  I also swapped the Code for America logo for the Twitter logo.

I then changed the repository to point to the Code for America organization page which can be seen <a href="https://github.com/codeforamerica/codeforamerica.github.com/blob/master/index.html#L65" target="_blank">here</a>.

To create the organization page using GitHub pages I just had to create a repository called codeforamerica.github.com.  I pushed up the repo to GitHub and GitHub pages did what it does to serve up the pages.

[![](http://codeforamerica.org/wp-content/uploads/2012/02/Code-for-America-Projects-300x166.png "Code for America Projects")](http://codeforamerica.org/wp-content/uploads/2012/02/Code-for-America-Projects.png)

Now we have a GitHub page with our repositories in a nicer more digestible format for people to explore.
  
Thanks Twitter for creating that repository for other people to share and create similar pages.