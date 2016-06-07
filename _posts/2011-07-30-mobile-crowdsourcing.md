---
id: 7806
title: Mobile Crowdsourcing
date: 2011-07-30T14:07:31+00:00
author: Max Ogden
layout: post
guid: http://codeforamerica.org/?p=7806
permalink: /2011/07/30/mobile-crowdsourcing/
dsq_thread_id:
  - 372818578
categories:
  - Dispatches
---
<h2 style="margin-top: 10px;">
  Some experiments in collecting images + location from mobile devices
</h2>

Over the last couple of years I&#8217;ve been fascinated with technology that collects and aggregates mappable information. Specifically I have been searching for or creating tools that have these properties:

  * Lets users discover things near them, allows submission of location, photos and text
  * Built on an open data API so that others can access and build on the data
  * Easy for new developers to clone and deploy the app. A big roadblock on this front has been the Apple App Store. $100 and weeks of back and forth just to publish a public data app that uploads photos? Rubbish.

My first foray into &#8220;civic web&#8221; applications was in the form of a project called Portland Smells, which was a map-wiki that collected smelly places (both good and bad) and threw them on a map.

<img src="http://substance-assets.s3.amazonaws.com/19/65ca390f66b525383a3779dc12844c/psmells.png" alt="" width="610px" />Portland Smells was meant to be more of an art project than a public utility. That is, until a local government representative contacted me regarding a project that was being built out (now available at [whatsinourair.org](http://www.whatsinourair.org/)) to help report and monitor illegal chemical dump sites in the Portland area. Apparently the functionality created for Portland Smells was greatly needed for social and environmental justice. Needless to say I got hooked on the idea of open data.

## From smells to carts and cats {#_section_ca68c1c6f31317117344a8109885fb09}

After mapping smells I took a stab at an application to map [food carts](http://www.foodcartsportland.com/) that also allowed users to keep food cart locations, menus and hours of operation up to date. The app was made in early 2010 ([code here](https://github.com/maxogden/pdx-food-carts-mobile)) using the Titanium Mobile framework and used [PDX API](http://pdxapi.com) as the backend. Unfortunately Microsoft also decided to [release a closed source](http://spinnerin.tumblr.com/post/1014484948/why-contribute-to-a-community-project-when-you-can) food cart application (with a huge marketing budget) which effectively killed my excitement about the cart mapping project. <img src="http://substance-assets.s3.amazonaws.com/7d/5ba7d7b536bf39861123d0d043e2ee/Screen-Shot-2011-07-29-at-5.23.43-PM.png" width="610px" alt="" />Developing a cross platform mobile application using [Titanium](http://www.appcelerator.com/products/titanium-mobile-application-development/) had it&#8217;s fair share of speedbumps, including buggy tools, lack of features and weird javascript DSLs. I would imagine that now, a year and a half later, a lot of these issues have been addressed. Then I got [obsessed with cats](http://www.wweek.com/portland/print-article-12542-print.html). While walking around neighborhoods in Portland you will run into them all over the freaking place. I started to wonder if certain cats were always out on porches and what neighborhoods had the highest cat density. Someone told me that if the humane society had access to cat density data then they could better target spaying and neutering education initiatives. I started [recording videos](http://www.vimeo.com/tag:catmapper) of cats that I found while walking around and prototyped a pure webapp CartsPDX-like interface using jQuery Mobile: [catmapper.com](http://catmapper.com)<img src="http://substance-assets.s3.amazonaws.com/6b/5483054d6c36b98f15e2c3e1cee5db/Screen-Shot-2011-07-29-at-5.53.32-PM.png"  width="610px" alt="" />

## Collecting photos {#_section_49f2f17fd71b268bd64b7ba3fb6d6d14}

The biggest tradeoff to consider when building mobile web apps vs. native apps is the inability of most mobile web browsers to natively upload photos. Generally speaking native applications require more commitment from the application developer but provide a better user experience. Here I will share some different approaches to the problem of collecting photos and locations

## Wrapping web apps in native functionality with Phonegap/Titanium {#_section_5298c1840675d4aeb8cb4805e4360b2c}

Rather than learning Objective-C and Java I would strongly prefer to stick to my high level dynamic language of choice, JavaScript. Both [Phonegap](https://github.com/phonegap) and [Titanium](https://github.com/appcelerator) provide a JavaScript DSL that abstracts native functionality for the developer and has the ability to &#8216;compile&#8217; to multiple mobile platforms.

Personally I am more a fan of Phonegap because of the team&#8217;s commitment to support and foster HTML5 and their ultimate goal of making Phonegap itself obsolete through cross platform open web standards. This also results in more of a &#8220;modern&#8221; JavaScript feel than what Titanium offers.

Regardless of which tools you choose to create native applications, the most tedious part will always be registering app store developer licenses, packaging and submitting applications for approval.

The [OpenElm](https://github.com/andrewgleave/OpenElm) Project is a great open source Phonegap application built using jQuery Mobile for the UI and CouchDB on the server. Andrew Gleave, lead developer on the project, even went the extra mile and wrote an [attachment uploader plugin](https://github.com/andrewgleave/CouchDBAttachmentUploader) for iOS Phonegap devices that makes uploading files and photos super smooth.<img src="http://substance-assets.s3.amazonaws.com/42/e7a15aa17cc6e8901be8d0cdba767f/Screen-Shot-2011-07-29-at-6.07.25-PM.png"  width="610px" alt="" />

## Email Submissions {#_section_3d604870e13165acbcade97494299754}

Many smartphones can interpret mailto: links and launch email composition forms pre-loaded with the recipient address from the mailto:. On Android devices users are given the option of adding attachments to an existing message, but on iOS there is no way to add an attachment to a message being composed &#8211; you have to start the interaction by visiting the photo browser and choosing &#8216;Share&#8217;, however there is no way to initialize the photo sharing interface from a mobile web app. This severely complicates the UX for iOS users.

Regardless of the UX complications, email can be a nice and simple way to offer photo submissions without going through the rigamarole of registering native developer credentials. There are two ways that I&#8217;ve tried initiating email submissions

## Visiting a mobile web app first and being given a mailto: link {#_section_0a7de7447c708cdcad2f04517f4f1a20}

Catmapper.com (source), a prototype application, is an example of first collecting location and then providing an email address where photos can be submitted later. The requires that users remember to visit catmapper.com when they are walking down the street and visit a cat, and also that they are able to take an email address from a website and successfully email photos to it.

<img src="http://substance-assets.s3.amazonaws.com/cb/3ad60ae34b1ac58234e55c7f7806b8/Screen-Shot-2011-07-29-at-5.53.32-PM.png" alt="" width="610px" />

## Sending photos to a particular email address first and receiving instructions in a reply email {#_section_26d05c71d462465f954bd6c604c3aabf}

Pictured below is another now defunct prototype that was meant to demonstrate how defibrillator locations might be submitted by thoughtful citizens who encounter them. First the smartphone must have GPS enabled so that the photos contain coordinates in the embedded EXIF data. Photos are emailed in and users will receive a response email containing a visualization of the GPS coordinates from the EXIF information. Upon tapping on the map they are taken to a catmapper-style mobile interface that lets them update the specific coordinates for their submission.

<img src="http://substance-assets.s3.amazonaws.com/a8/b4d051dc6477185ac39f861f9539b2/Screen-Shot-2011-07-29-at-6.12.44-PM.png" alt=""  width="610px" />

This particular email processing workflow was implemented using a Ruby server that accessed a gmail account through IMAP. You can get the code by visiting the older commits in [this repository](https://github.com/codeforamerica/aedmapper). Warning: trying to write a realtime IMAP client for Gmail was pretty painful and prompted me to write a realtime node.js email processor, [haraka-couchdb](http://github.com/maxogden/haraka-couchdb).

## Tweets with geolocation and photos {#_section_0507cd9a6fdd88edba2b3f1479e44174}

There are tons of native Twitter applications that allow uploading to third party image sharing services like yfrog or twitpic. Some colleagues of mine at Code for America took a [Node.js daemon](https://github.com/codeforamerica/muralmapper) from civic hacker Mark Headd and extended it to save images + latitude/longitude from tweets into CouchDB. This approach requires users to enable geolocation in their Twitter client. It also has an interesting social property that can boost photo sharing engagement.

<img src="http://substance-assets.s3.amazonaws.com/6c/4c0b8bb4f10a849ecd72dfe8fd7100/Screen-Shot-2011-07-29-at-6.30.27-PM.png" alt="" width="610px" />

## MMS Gateways {#_section_774f74c4e3e9368bf1bb024c8fe5f0fe}

This would be super cool for bridging the gap from smartphones to feature phones but unfortunately is not supported by the major telephony API providers (Twilio and Tropo).

## Desktop uploading {#_section_b1eae94353d1fb43829f54874ca3c458}

Photos often don&#8217;t need to be uploaded in the field and can be synced and uploaded at a later time. This broadens the range of cameras that can be used to capture images and lets users without smartphones participate in using your application. Here is another prototype, [aedmapper.com](http://aedmapper.com/) ([code here](https://github.com/codeforamerica/aedmapper)), that is meant to show how to collect accurate information about defibrillator locations using address autocompletion, web based mapping and drag and drop photo upload forms.

<img src="http://substance-assets.s3.amazonaws.com/43/af19e69b4d2d349432e055a134840f/Screen-Shot-2011-07-29-at-6.41.03-PM.png" alt="" width="610px" />

Using the same code I created two separate [upload forms](http://open211.org/#upload) for another project, Open211, a directory of social services. One form collects locations while the other offers dropbox-like attachment uploading functionality.

<img src="http://substance-assets.s3.amazonaws.com/c9/8bbadecdb367cd0c474c30231212ba/Screen-Shot-2011-07-30-at-1.14.07-PM.png" alt="" width="610px" />

## Pen + Paper {#_section_b131ae06cb6d28e9b65925a686baa817}

The most ubiquitous mobile crowdsourcing interface comes in the form of [walking papers](http://walking-papers.org/), a project by Michal Migurski. Designed as a tool for collecting data for OpenStreetMap, the computer vision technology that powers walking papers could also prove useful for large scale low technology data collection deployments. I haven&#8217;t yet had a chance to use this tech but am itching at the opportunity.<img src="http://substance-assets.s3.amazonaws.com/3d/36cd4193c7bd70371e4ca41da172ab/5042873815_d1f17898fb_z.png" width="610px" alt="" />OpenStreetMap contributors have gathered for _mapping parties,_ which consist of treks through unmapped neighborhoods where participants document what they see by writing down landmarks, roads, parks and playgrounds on a special map that can be scanned and uploaded to walking-papers.org where they are then georectified and traced directly onto OpenStreetMap.

(Note: This was originally published on [maxogden.com](http://maxogden.com/#blog/mobile-crowdsourcing-interfaces).)