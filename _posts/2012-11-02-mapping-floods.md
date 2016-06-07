---
id: 18468
title: Mapping Floods With Lightweight Technology
date: 2012-11-02T11:50:29+00:00
author: Emily Wright Moore
layout: post
guid: http://codeforamerica.org/?p=18468
permalink: /2012/11/02/mapping-floods/
dsq_thread_id:
  - 911367827
categories:
  - Austin
  - Fellowship
  - Gov2.0
  - News
---
**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    ](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.54.00-PM.png) 
  * **Bootstrap and HTML/CSS files
  
** Download a [Bootstrap](http://twitter.github.com/bootstrap/) template and customize it to give it your own style, or use [this one](https://github.com/emilyville/floodwatch). ATXfloods uses tabs to display some extra content like the Twitter hashtag #atxfloods, some extra tips, and links to helpful resources.
  
    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    ](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.54.00-PM.png) 
  * **Bootstrap and HTML/CSS files
  
** Download a [Bootstrap](http://twitter.github.com/bootstrap/) template and customize it to give it your own style, or use [this one](https://github.com/emilyville/floodwatch). ATXfloods uses tabs to display some extra content like the Twitter hashtag #atxfloods, some extra tips, and links to helpful resources.
  
](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.56.37-PM.png) 
  * **Tabletop.js and Google Docs
  
** Next, we needed a good way for people to know when looking at the map how current the information is. We used [Tabletop.js](https://github.com/jsoma/tabletop) to easily integrate Google Docs spreadsheets and display the most recent status update at the top of the page.
  
    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    ](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.54.00-PM.png) 
  * **Bootstrap and HTML/CSS files
  
** Download a [Bootstrap](http://twitter.github.com/bootstrap/) template and customize it to give it your own style, or use [this one](https://github.com/emilyville/floodwatch). ATXfloods uses tabs to display some extra content like the Twitter hashtag #atxfloods, some extra tips, and links to helpful resources.
  
    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    [**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

[**[<img class="alignright size-medium wp-image-18476" title="Flooded crossing" src="http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3-300x200.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Daniel-Herrera3.jpg)**

## Turn Around, Don&#8217;t Drown

[Low water crossings](http://en.wikipedia.org/wiki/Low_water_crossing) aren&#8217;t something we get a lot of here in San Francisco, but many Austinites are intimately familiar with them. [Flash floods](http://en.wikipedia.org/wiki/Flash_flood) and sudden high-volume rain cause runoff and will quickly fill or overflow riverbeds and low lying areas and cause low water crossings to close, making streets impassable.

[<img class="alignright size-medium wp-image-18477" title="image001" src="http://codeforamerica.org/wp-content/uploads/2012/11/image001-300x225.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/image001.png)

When this happens, it’s important that drivers have enough information to know which routes to take. In person, it’s difficult to tell how quickly water is flowing, or even how deep it is. [Oregon Trail](http://en.wikipedia.org/wiki/The_Oregon_Trail_(video_game))-style attempts to ford these crossings result in multiple casualties each year.

In June, when I met Matt Porcher of the [Watershed Department](http://www.austintexas.gov/department/watershed-protection), for him to close crossings required leaving a message with the on-duty officer at [Austin Homeland Security and Emergency Management](http://www.austinhsem.com/). When they called back he would relay to them the closed crossing(s). Which the officer would then post to the website, [here](http://www.austinhsem.com/go/doctype/3603/81175/). Site visitors could then view the list to figure out if any of the listed closures were along their intended routes.

This was a great opportunity for lightweight technology to make this process better and easier. So we did. Matt and I built [ATXfloods.com](http://atxfloods.com/) using CartoDB, Google Docs, HTML, CSS, and a little bit of JavaScript. It’s lightweight, easy to setup, and completely free. It’s also a responsive design that works on a smartphone or tablet.

[<img class="alignnone size-large wp-image-18478" title="Screen Shot 2012-11-01 at 4.50.53 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM-1024x562.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.50.53-PM.png)

[<img class="alignright size-medium wp-image-18488" title="atxfloods_eoc" src="http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc-300x225.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg)Having something on a map makes it more usable, shareable, and easier to track. We&#8217;ve been delighted to see the use of it spread and increase the effectiveness of other efforts. For example, the Austin Fire Department uses it to track closures so they know which route to take for emergencies.

](http://codeforamerica.org/wp-content/uploads/2012/11/atxfloods_eoc.jpeg) 

&nbsp;

## **Here’s how it works:**

  * **CartoDB
  
** With a CartoDB account, you can import a CSV file of locations.
  
    For help setting it up, here’s a great [tutorial](https://github.com/boundsj/maplate) by 2012 Fellow [Jesse Bounds](http://codeforamerica.org/jesse-bounds/).
  
    To see how to set up the open/closed status of the points in CartoDB, check out the readme on the github repo, [here](https://github.com/emilyville/floodwatch/tree/gh-pages).
  
    [<img class="alignnone size-medium wp-image-18479" title="Screen Shot 2012-11-01 at 1.55.17 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM-300x270.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-1.55.17-PM.png)    ](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.54.00-PM.png) 
  * **Bootstrap and HTML/CSS files
  
** Download a [Bootstrap](http://twitter.github.com/bootstrap/) template and customize it to give it your own style, or use [this one](https://github.com/emilyville/floodwatch). ATXfloods uses tabs to display some extra content like the Twitter hashtag #atxfloods, some extra tips, and links to helpful resources.
  
](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.56.37-PM.png) 
  * **Tabletop.js and Google Docs
  
** Next, we needed a good way for people to know when looking at the map how current the information is. We used [Tabletop.js](https://github.com/jsoma/tabletop) to easily integrate Google Docs spreadsheets and display the most recent status update at the top of the page.
  
](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.57.53-PM.png) Google Docs happens to be blocked in most of Austin City employees, so I used a Google form that can be filled out on a phone, or from email, and will directly update the [spreadsheet](https://docs.google.com/a/emilyville.com/spreadsheet/pub?key=0AvUsRT_oqcQvdC1uN2VIUERTLV9IRlBHby1IdjhjU3c&output=html) and ATXfloods.com.
  
    [<img class="alignnone size-medium wp-image-18483" title="Screen Shot 2012-11-01 at 4.58.06 PM" src="http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.58.06-PM-300x114.png" alt="" />](http://codeforamerica.org/wp-content/uploads/2012/11/Screen-Shot-2012-11-01-at-4.58.06-PM.png)

Also note that if you don’t have your own URL or hosting, you can host it on [GitHub Pages](http://pages.github.com/), like [this version](http://emilyville.github.com/floodwatch/).

Share it. [Fork it](https://github.com/emilyville/floodwatch/tree/gh-pages). Use it to map something cool!

****Questions? Email us.
  
**** Emily Wright: emily[@]codeforamerica.org
  
Matt Porcher: matthew.porcher[@]austintexas.gov

&nbsp;

Questions? Comments? Hit us up [@codeforamerica](http://twitter.com/codeforamerica).