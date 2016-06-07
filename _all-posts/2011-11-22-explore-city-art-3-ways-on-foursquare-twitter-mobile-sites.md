---
id: 9782
title: 'Explore City Art 3 Ways: On Foursquare, Twitter &#038; Mobile Sites'
date: 2011-11-22T14:01:17+00:00
author: Anna Bloom
layout: post
guid: http://codeforamerica.org/?p=9782
permalink: /2011/11/22/explore-city-art-3-ways-on-foursquare-twitter-mobile-sites/
dsq_thread_id:
  - 480588347
categories:
  - News
---
[<img class="alignleft size-large wp-image-9803" title="art-app-team-hangout3" src="http://codeforamerica.org/wp-content/uploads/2011/11/art-app-team-hangout3-1024x246.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/11/art-app-team-hangout3.jpg)

&nbsp;

&nbsp;

&nbsp;

Above, see the team Google+ Hangout photo shoot.

The two hip dudes holding the heart? That&#8217;s Michael Ellsworth and Corey Gutch, the dynamic design team duo from the Seattle creative agency [Dumb Eyes](http://www.dumbeyes.com/) who also help to run Seattle&#8217;s [monthly art walks](http://seattleartwalks.org/).

The refined, bearded gentleman? That&#8217;s Matt Blair, the culture-loving smartphone developer from Portland who created [Portland&#8217;s first public art app](http://publicartpdx.com/) that launched last April.

The two with the toothy grins? That&#8217;s me and John Mertens at Code for America&#8217;s offices in San Francisco.

Together over the course of the last six months, our team collaborated with developers, designers, residents, and city staff from Portland, Seattle, San Francisco, Philadelphia, and Boston, and county staff from King County, Washington, to help make public and street art more discoverable in cities. Today we are proud to announce three new ways to explore art in these five cities. Including:

**1. Foursquare.**
  
In four cities &#8212; Boston, Philadelphia, Seattle, and San Francisco &#8212; you are now able to check in, comment, and explore nearly 3,000 pieces of public art.

**2. Twitter.**
  
Anywhere you go, if you find street art or public art, you can Tweet a geo-located image at @publicartapp and help map it. The results appear at [artmapper.org.](http://artmapper.org)

This app, developed by John with help from civic hacker Mark Headd, is currently a part of an art exhibit, &#8220;Here Be Dragons: Mapping Information and Imagination,&#8221; at the [Intersection for the Arts in San Francisco](http://www.theintersection.org/calendar/index.php?op=view&id=4280), and won honorable mention for the first annual [Summer of Smart hackathon](http://www.summerofsmart.org/about/). The technology was also used in [Public Art Spaces](http://www.summerofsmart.org/projects/public-art-spaces-2/), an award-winning app from the same competition that enables the public to tag spaces in cities where they would like to see public art.

**3. One smartphone app, and five city-specific mobile websites help you to find public art near you:
  
** _(Design by the Dumb Eyes team; meant for display on smartphones.)_

In Boston, <http://bos.publicartapp.mobi>
  
In Seattle, <http://sea.publicartapp.mobi>
  
In San Francisco, <http://sf.publicartapp.mobi>
  
In Philadelphia, <http://phl.publicartapp.mobi>
  
In Portland, go to [Public Art PDX](http://publicartpdx.com/) to download an app for iPod, iPad or iTouch.

In all of these cities, we also published the location data and other details for public art in a machine-readable format for anyone to use. We look forward to seeing other inspired developers mix and mash this data up and create new apps that help people interact and explore the history and culture that capture the spirit of these cities.

Special thanks to the following people and organizations that supported this project and helped make it possible:

**City Staff**
  
Kate Patterson, public relations manager, San Francisco Arts Commission
  
Allison Cummings, senior registrar, San Francisco Arts Commission
  
Jeffrey Pierce, web and technology coordinator, Seattle Office of Arts & Cultural Affairs
  
Lori Patrick, public relations manager, Seattle Office of Arts & Cultural Affairs
  
Tina Hoggatt, coordinator of outreach and and education for King County&#8217;s Public Art 4Culture
  
Moira Baylson, cultural officer, Philadelphia Office of Arts Culture & the Creative Economy
  
Margot Berg, public art director, Philadelphia Office of Arts Culture & the Creative Economy
  
Steve Weinik, administrative and IT services manager, City of Philadelphia Mural Arts Program
  
Karen Goodfellow, staff director, Boston Art Commission

**Advisory Board
  
** George Oates, Project Lead and Designer for The Internet Archive&#8217;s Open Library and cofounder of Flickr
  
Jay Nath, Director of Innovation for the City of San Francisco
  
Josette Melchor, Executive Director of the Gray Area Foundation for the Arts
  
Nathaniel Vaughn Kelso, Design Technologist at Stamen Design
  
Richard Koci Hernandez, Emmy-Award-winning multimedia producer; UC Berkeley Graduate School Professor
  
Dan O’Neil, Executive Director at Smart Chicago Collaborative; cofounder of EveryBlock
  
Michael Evans, 2011 Code for America Fellow now a technologist at Stamen Design

**Additional Support**
  
Aaron Ogle, Code for America fellow
  
Max Ogden, Code for America fellow
  
Karen Johnson, Seattle journalist, and lover of cities

**Tech links**

****All of the code developed for the project is open source and can be found on GitHub:

  * <a href="https://github.com/mertonium/public_art_finder/blob/master/foursquare_uploader/uploader.rb" target="_blank">Source code for the Foursquare uploader</a>
  * <a href="https://github.com/mertonium/muralmapper" target="_blank">Source code for Artmapper.org</a>
  * <a href="https://github.com/mertonium/public_art_finder/tree/master/viewer_couchapp" target="_blank">Source code for the mobile app</a>

The data powering each site can be accessed via the following REST APIs:
  
(returned as GeoJSON unless noted)

  * <a href="http://sf.publicartapp.mobi/all" target="_blank">http://sf.publicartapp.mobi/all</a> &#8211; every record (use sparingly &#8211; we&#8217;re on a free host)
  * <a href="http://sf.publicartapp.mobi/data?bbox=-122.4148,37.7731,-122.3848,37.8031" target="_blank">http://sf.publicartapp.mobi/data?bbox=-122.4148,37.7731,-122.3848,37.8031</a> &#8211; every record within the given bounding box (central San Francisco in this case)
  * <a href="http://sf.publicartapp.mobi/kml" target="_blank">http://sf.publicartapp.mobi/kml</a> &#8211; every record downloaded as a KML file
  * <a href="http://sf.publicartapp.mobi/api" target="_blank">http://sf.publicartapp.mobi/api</a> &#8211; access to the standard CouchDB API

<div>
  <span style="font-size: small;"><span class="Apple-style-span" style="line-height: 24px;">Just swap out &#8220;sf&#8221; in the above urls to switch data sets.</span></span>
</div>