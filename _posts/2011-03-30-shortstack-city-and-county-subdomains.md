---
id: 4806
title: 'ShortStack: City and County Subdomains'
date: 2011-03-30T17:58:38+00:00
author: Dan Melton
layout: post
guid: http://codeforamerica.org/?p=4806
permalink: /2011/03/30/shortstack-city-and-county-subdomains/
dsq_thread_id:
  - 267196236
categories:
  - CfA Labs
tags:
  - labs
---
I&#8217;ve been working lately on a labs product called ShortStack ([code](https://github.com/codeforamerica/shortstack)). The idea behind it is simple. Can we aggregate information about a city&#8217;s technology stack?  For instance, if we know a city website, can we scrape it for data about software they&#8217;ve bought?  Maybe we can probe for WordPress, Drupal or Joomla usage.  <!--more-->

To start, I pulled in the city and county websites from the [SBA](http://www.sba.gov/api/).  They keep an ongoing list of websites (unsure update frequency).  Roughly 8669 cities and counties are represented in the data set.  There about [I&#8217;ve been working lately on a labs product called ShortStack ([code](https://github.com/codeforamerica/shortstack)). The idea behind it is simple. Can we aggregate information about a city&#8217;s technology stack?  For instance, if we know a city website, can we scrape it for data about software they&#8217;ve bought?  Maybe we can probe for WordPress, Drupal or Joomla usage.  <!--more-->

To start, I pulled in the city and county websites from the [SBA](http://www.sba.gov/api/).  They keep an ongoing list of websites (unsure update frequency).  Roughly 8669 cities and counties are represented in the data set.  There about ](http://www.nlc.org/about_cities/cities_101/142.aspx) (counties and cities) across the US.  Not all cities or counties will have a website, so any research on ShortStack will be constrained by those who do.

Today&#8217;s project is about subdomains. Subdomains are the characters following &#8216;http://&#8217; and preceding the domain name. &#8216;codeforamerica.org&#8217;. In the full url http://www.codeforamerica.org, &#8216;www&#8217; is the subdomain.  A lot of subdomains are becoming more popular, like mobile.\*, data.\*, and gis.* in cities.  But, how popular?  I&#8217;m also curious about standardization. Are there standard subdomains that cities gravitate towards?

First, let&#8217;s get subdomains on cities.  I chose google search as my primary tech.  You can do all kinds of interesting domain searches using google search. For instance, consider San Francisco&#8217;s site (<http://www.sfgov.org/>).  Let&#8217;s look for potential subdomains besides &#8216;www.&#8217; Goto google.com and enter in &#8216;site:sfgov.org&#8217; as the query. [You should see this](http://www.google.com/search?source=ig&hl=en&rlz=&q=site%3Asfgov.org&aq=f&aqi=&aql=&oq=).  Let&#8217;s remove the www portion, &#8216;-www site:sfgov.org&#8217;, [like this](http://www.google.com/search?source=ig&hl=en&rlz=&q=site%3Asfgov.org&aq=f&aqi=&aql=&oq=#sclient=psy&hl=en&source=hp&q=-www+site:sfgov.org&aq=&aqi=&aql=f&oq=&pbx=1&bav=on.2,or.r_gc.r_pw.&fp=5b48774d4519ce9c), and voila, San Francisco&#8217;s site has mission, drop-sfers, repromail and others as subdomains.  Now, we can iterate through this list and keep excluding subdomains to find more, [like this](http://www.google.com/search?source=ig&hl=en&rlz=&q=site%3Asfgov.org&aq=f&aqi=&aql=&oq=#sclient=psy&hl=en&q=-www+-mission+-drop-sfers+-repromail+site:sfgov.org&aq=f&aqi=&aql=f&oq=&pbx=1&bav=on.2,or.r_gc.r_pw.&fp=5b48774d4519ce9c).

Note, I&#8217;m using Google, which means a city might have a subdomain that doesn&#8217;t show up in Google.  But, if it isn&#8217;t on Google, then I doubt citizens can find it anyway.

Using distributed &#8216;workers&#8217; on Heroku and a series of custom google search queries, I crunched through 8669 city and county websites in about 25 minutes (after a few hours on the actual code). Here&#8217;s what I found:

About 8240 city and county websites worked (after correcting for 404, 302 and other header errors).  Collectively, 8240 websites have a whopping **4626** distinct subdomains.  Really? Are there any standards or trends?

How about the top subdomains? At first pass, the top 250 subdomains returned some weird vendor related hosting issues (i.e. 30 websites were linked to govoffice2.com like the city of Cleveland www.clevelandmn.govoffice2.com).  After removing those, the top subdomains list looks like this:

<table style="margin-top: 10px; margin-bottom: 20px; border-bottom: 3px solid #ccc; border-top: 3px solid #ccc;" border="0" cellspacing="0" cellpadding="10" width="50%" bordercolor="#000000">
  <tr height="15">
    <td align="right">
      <strong>Number of Occurences</strong>
    </td>
    
    <td width="75">
      <strong>Subdomain</strong>
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      6237
    </td>
    
    <td width="75">
      www
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      944
    </td>
    
    <td>
      www.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      685
    </td>
    
    <td>
      www.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      591
    </td>
    
    <td>
      ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      328
    </td>
    
    <td>
      co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      225
    </td>
    
    <td>
      gis
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      110
    </td>
    
    <td>
      www.town
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      94
    </td>
    
    <td>
      maps
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      80
    </td>
    
    <td>
      mail
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      78
    </td>
    
    <td>
      town
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      73
    </td>
    
    <td>
      www2
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      60
    </td>
    
    <td>
      secure
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      58
    </td>
    
    <td>
      library
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      57
    </td>
    
    <td>
      gis.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      49
    </td>
    
    <td>
      www.twp
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      44
    </td>
    
    <td>
      webmail
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      41
    </td>
    
    <td>
      ftp
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      39
    </td>
    
    <td>
      apps
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      35
    </td>
    
    <td>
      police
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      egov
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      parks
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      twp
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      28
    </td>
    
    <td>
      search
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      28
    </td>
    
    <td>
      webtrac
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      27
    </td>
    
    <td>
      home
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      25
    </td>
    
    <td>
      council
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      25
    </td>
    
    <td>
      egram.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      24
    </td>
    
    <td>
      recreation
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      23
    </td>
    
    <td>
      gisweb
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      23
    </td>
    
    <td>
      maps.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      22
    </td>
    
    <td>
      webapps
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      21
    </td>
    
    <td>
      jobs
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      21
    </td>
    
    <td>
      landshark.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      21
    </td>
    
    <td>
      permits
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      19
    </td>
    
    <td>
      courts
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      19
    </td>
    
    <td>
      gov
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      19
    </td>
    
    <td>
      tax
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      19
    </td>
    
    <td>
      village
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      19
    </td>
    
    <td>
      www3
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      18
    </td>
    
    <td>
      gis.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      18
    </td>
    
    <td>
      health
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      18
    </td>
    
    <td>
      planning
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      18
    </td>
    
    <td>
      web
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      18
    </td>
    
    <td>
      ww
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      18
    </td>
    
    <td>
      www.city
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      17
    </td>
    
    <td>
      atlas
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      17
    </td>
    
    <td>
      fire
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      17
    </td>
    
    <td>
      schools
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      17
    </td>
    
    <td>
      www.village
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      16
    </td>
    
    <td>
      advocate
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      16
    </td>
    
    <td>
      bids
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      16
    </td>
    
    <td>
      city
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      16
    </td>
    
    <td>
      elections
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      16
    </td>
    
    <td>
      m
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      16
    </td>
    
    <td>
      www2.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      ag
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      apps.dmv
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      business
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      childrensauthors
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      cms.calema
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      fishers
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      iedc
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      incors
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      jobs.spb
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      rbra
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      rules.calbar
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      secure.arb
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      services
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      spb
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      spms.indot
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      15
    </td>
    
    <td>
      upland
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      14
    </td>
    
    <td>
      finance
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      14
    </td>
    
    <td>
      rcda
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      14
    </td>
    
    <td>
      tehamacourt
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      14
    </td>
    
    <td>
      treasurer
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      assessor
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      bogs
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      bronxda
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      dev
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      dycd.ra
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      gypsymoth
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      lincoln
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      my
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      new
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      pubadvocate
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      purchasing
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      sagic
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      vil
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      13
    </td>
    
    <td>
      www1
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      clerk
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      ddcftp
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      dnr
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      doa
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      drl
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      guardian
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      home2
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      hr
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      its
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      news
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      publicnotices
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      react
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      records
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      smokefree
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      weblink
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      12
    </td>
    
    <td>
      www.dot
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      cares
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      edn
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      eservices
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      ftp.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      library.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      map
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      mcsdmv
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      mobile
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      ndr-efs
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      neo
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      publicdefender
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      publicworks
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      quitnow
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      rod
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      support
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      volunteers
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      webtrac.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      workforceplanning
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      ww2
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      11
    </td>
    
    <td>
      wwww
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      alert
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      billpay
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      c2g
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      calendar
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      catalog
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      email
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      ftp.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      nde
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      nrrs
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      p2c
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      portal
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      secure.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      secure2
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      sheriff.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      10
    </td>
    
    <td>
      water
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      agenda
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      click2gov
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      community
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      data
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      development
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      payments
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      recorder
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      revenue
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      9
    </td>
    
    <td>
      sheriff
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      blog
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      da
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      docs
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      events
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      forums
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      gis2
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      history
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      housing
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      intranet
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      maps.ci
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      secure.co
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      senatedems
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td>
      video
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      8
    </td>
    
    <td style="text-align: left;" align="right">
      311
    </td>
  </tr>
</table>

How about the top 20 websites with the most subdomains?

<table style="margin-top: 10px; margin-bottom: 20px; border-bottom: 3px solid #ccc; border-top: 3px solid #ccc;" border="0" cellspacing="0" cellpadding="10" width="50%" bordercolor="#000000">
  <tr height="15">
    <td align="right">
      <strong>Number of Occurrences</strong>
    </td>
    
    <td width="75">
      <strong>City or County</strong>
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      36
    </td>
    
    <td width="75">
      Cuyahoga County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      35
    </td>
    
    <td>
      Seattle, WA
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      35
    </td>
    
    <td>
      Monroe County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      34
    </td>
    
    <td>
      Los Angeles, CA
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Westchester County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Olive Hill, KY
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Montgomery County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Frankfort, KY
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Livingston County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Grant County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Gallatin County
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      33
    </td>
    
    <td>
      Bellefonte, KY
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Middleville, MI
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Eden Valley, MN
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Township of Cormorant, MN
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Sun Valley, ID
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Fraser, MI
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Eden Valley, MN
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      Lincoln Park, MI
    </td>
  </tr>
  
  <tr height="15">
    <td align="right">
      32
    </td>
    
    <td>
      East Gull Lake, MN
    </td>
  </tr>
</table>

It&#8217;s getting a bit late, but before I log off, a few interesting thoughts:

  * 2548 city and county websites still use some form of www.ci, www.co, ci and other outdated circa mid90s domains even after accounting for redirects
  * Over 100 cities use 311 in some way, but only 8 have a 311 subdomain
  * My favorite is gypsymoth!
  * About 451 cities and counties have some sort of gis facing portal

What other data would you be interested in using ShortStack and domain names?

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;