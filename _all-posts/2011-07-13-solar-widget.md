---
id: 7117
title: Solar Widget
date: 2011-07-13T12:20:35+00:00
author: Ryan Resella
layout: post
guid: http://codeforamerica.org/?p=7117
permalink: /2011/07/13/solar-widget/
dsq_thread_id:
  - 357491315
categories:
  - News
---
[<img class="alignright size-full wp-image-7127" title="SolarScreenshot" src="http://codeforamerica.org/wp-content/uploads/2011/06/SolarScreenshot.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/06/SolarScreenshot.jpg)With solar energy gaining popularity, cities require ways to measure the potential benefits of implementation. [Solar Widget](http://solar-1.apphb.com/) is a web-based application that uses Esri mapping software to calculate solar potential for rooftops. The project aims to raise awareness about the potential use of solar panels in your neighborhood and community. With this tool, basic calculations can demonstrate the cost saving opportunities brought by a switch to solar power. Any city with the necessary geodata can use this application to spread public awareness of the benefits of solar energy&#8211;and take an important step towards greater energy efficiency.

In 2008, the City of Boston created this solar flex widget to manage the Solar Boston Initiative. This initiative was highly publicized in Esri&#8217;s Arcnew Fall 2008 edition, and you can read about it <a href="http://www.esri.com/news/arcnews/fall08articles/boston-showcases.html" target="_blank">here</a>.

The source code for the Solar Boston project was open sourced by the Boston Redevelopment Agency. The flex widget was initially built using ArcGIS Server Flex API 1.3. Since then Esri has updated to a new 2.3 version of the Flex API. With this update much of the original source code for the Solar Boston flex widget needed to be updated to work. For a Labs Friday project, Code for America took on the task of updating the Solar Widget to the new version of the Flex API, and last week, we released the updated version of the Solar Widget on the <a href="http://www.arcgis.com/home/item.html?id=8c15dd37aafc4e989b51d941c958e9d7" target="_blank">Esri web site</a>.

The demo of the updated widget can be found <a href="http://solar-1.apphb.com" target="_blank">here</a>: <a href="http://solar-1.apphb.com" target="_blank">http://solar-1.apphb.com</a>.

[<img class="alignnone size-full wp-image-7119" title="SolarBoston" src="http://codeforamerica.org/wp-content/uploads/2011/06/SolarBoston.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/06/SolarBoston.jpg)

The source code for the Solar Widget is available on <a href="https://github.com/codeforamerica/SolarWidget" target="_blank">github</a>, and you&#8217;re welcome to hack on it or even roll it out in your own city.

<small><em>(Note: To run the geoprocessing model with your own data, you will need ArcGIS Desktop/Server with the Spatial Analyst extension.)</em></small>