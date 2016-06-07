---
id: 8159
title: 'Ronaldo&#8217;s CfA Summer'
date: 2011-08-26T09:57:31+00:00
author: Ronaldo Barbachano
layout: post
guid: http://codeforamerica.org/?p=8159
permalink: /2011/08/26/ronaldos-cfa-summer/
dsq_thread_id:
  - 396624750
categories:
  - 2011 Interns
  - CfA Labs
---
As one of the first interns at CfA, I am pleased with my experience with both [CFA](http://codeforamerica.org "Code For America") and [Google Summer of Code](http://socghop.appspot.com/gsoc/homepage/google/gsoc2011 "GSOC 2011"). This summer I was assigned to develop PHP libraries on existing government related projects.

Much of my work has focused on v2 of the Open311 API spec, National Health Library API&#8217;s, creating a API base class, and implementing continuous integration strategies using [SimpleTest](http://www.simpletest.org/ "Simple Test") and [Jenkins](http://jenkins-ci.org/ "Jenkins"). With the [new](https://github.com/codeforamerica/PHP-API-Template "PHP Base Class") base class, I was quickly able to create the following libraries :

  * [product\_recall\_php](https://github.com/codeforamerica/product_recall_php "PHP Product Recall API Library") &#8211; Search known Federal Product Recall data.
  * [usa\_spending\_php](https://github.com/codeforamerica/usa_spending_php "USA Spending") &#8211; Search databases that track USA spending.
  * [faa_php](https://github.com/codeforamerica/faa_php "Faa") &#8211; Query FAA for Airport delays/updates.
  * [chronicling-america-php](https://github.com/codeforamerica/chronicling-america-php "Chronicling America") &#8211; Search American periodicals.
  * [world\_bank\_php](https://github.com/codeforamerica/world_bank_php "World Bank") &#8211; Search database with World Bank statistics.
  * [open311_php](https://github.com/codeforamerica/open311_php "Open311") &#8211; For interacting with municipal based help-ticket system; updated for v2.
  * _National Health Library API&#8217;s_
  *  [RxNorm](https://github.com/codeforamerica/rxNorm_php "RxNorm") &#8211; Semantic Medications Tool.
  *  [NDF-rt](https://github.com/codeforamerica/ndfRT_php "NDF-RT") &#8211; Searches drug interactions.
  * [Toxnet](https://github.com/codeforamerica/toxnet_php "Toxnet") &#8211; Searches known toxin databases.
  * [Pillbox](https://github.com/codeforamerica/pillbox_php "Pillbox") &#8211; Search drugs based on physical pill descriptions.

Of these API&#8217;s I was able to quickly put together a small web App [RXNix](http://rxnix.com) for the RxNorm API which was recently created this summer. This [App](https://github.com/codeforamerica/rxNormRef_php "rxNormRef_php") interfaces with a database created by [the National Library of Health](http://www.nlm.nih.gov/ "National Library of Health") to give healthcare professionals a single location to convert a variety of existing medical codes (for concepts, drugs, ingredients and related) to the new Unified Medical Language System.

[<img class="aligncenter size-full wp-image-8160" title="rxnix_ss" src="http://codeforamerica.org/wp-content/uploads/2011/08/rxnix_ss.jpg" alt="" />](http://codeforamerica.org/wp-content/uploads/2011/08/rxnix_ss.jpg)

(Editor&#8217;s Note: _Over the summer of 2011, over a dozen students interned with Code for America. They brought great energy, passion, and skills to bear on our projects and our mission to make government more open and efficient. Over the next week, we&#8217;ll be posting their summaries of their work and learnings, in addition to an overview of the summer._)