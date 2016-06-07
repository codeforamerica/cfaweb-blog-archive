---
id: 33831
title: Impacts and Lessons for CalFresh
date: 2015-07-08T15:31:34+00:00
author: Jacob Solomon
layout: post
guid: http://www.codeforamerica.org/blog/?p=33831
permalink: /2015/07/08/impacts-lessons/
categories:
  - Hidden
---
# Introduction

About six weeks ago, we shared a [report on the barriers to CalFresh participation](http://calfresh-barriers.herokuapp.com). This report showed that:

  * It is hard to find high quality information about CalFresh online
  * Existing online applications don’t work on mobile phones
  * Many potential applicants do not successfully submit applications
  * After applying, many clients do not successfully complete the interview or verification steps
  * It is hard to submit verification documents in many counties
  * After enrolling, clients have challenges staying enrolled and managing their benefits

This second report identifies six key impacts and lessons learned during Code for America’s work to address these barriers. The impacts detailed here represent improvements delivered to clients in their experience of applying for and receiving CalFresh. We hope to use these insights to inform our continued development of a simple online application for CalFresh.

&nbsp;

# The Enrollment Process: Impacts & Lessons

## _GetCalFresh.org_

[GetCalFresh.org](http://getcalfresh.org "GetCalFresh.org") is a simple online application for CalFresh that works on mobile phones, takes about 10 minutes to complete, and is written in plain language. This is in contrast to the existing online applications for CalFresh, which, as documented in the prior report, are long, often confusing, and do not work on mobile phones. Here is how GetCalFresh.org works:

<!-- iframe plugin v.3.0 wordpress.org/plugins/iframe/ -->

As of this writing we have completed two pilots of GetCalFresh.org &#8211; one in San Francisco and a second statewide. This section summarizes the impacts and lessons learned from GetCalFresh.org to-date.

&nbsp;

### Impact: Increased CalFresh enrollment

In San Francisco, 187 clients have submitted CalFresh applications with a 59% approval rate. This suggests that a shorter initial application process can yield positive applicant outcomes in San Francisco.

We are also currently conducting a statewide pilot. As of this writing, 172 additional clients have submitted CalFresh applications through GetCalFresh.org across 31 California counties. Our approach for the statewide pilot involves reaching clients directly through online advertising channels because, as [prior evidence suggests](http://calfresh-barriers.herokuapp.com/before_applying/search.html "prior evidence suggests") that online search is an effective yet underutilized outreach channel. With this approach there are  four steps to enrolling someone in CalFresh:

  1. Potential applicants **see an online advertisement** when they search Google or Microsoft Bing for ‘CalFresh’ or related keywords
  2. The applicant **clicks the ad** and goes to [GetCalFresh.org](https://www.getcalfresh.org/)
  3. The applicant successfully **submits an application for CalFresh**
  4. The applicant gets **approved for CalFresh**

Here is a summary of the conversion and cost-effectiveness of each stage:

<table>
  <tr>
    <td>
      Stage
    </td>
    
    <td>
      Gross #
    </td>
    
    <td>
      % of prior stage
    </td>
    
    <td>
      $ per
    </td>
  </tr>
  
  <tr>
    <td>
      1. Ad impressions
    </td>
    
    <td>
      ~17000
    </td>
    
    <td>
      100%
    </td>
    
    <td>
      $.06
    </td>
  </tr>
  
  <tr>
    <td>
      2. Ad clicks
    </td>
    
    <td>
      747
    </td>
    
    <td>
      4.00%
    </td>
    
    <td>
      $1.50
    </td>
  </tr>
  
  <tr>
    <td>
      3. CalFresh applications
    </td>
    
    <td>
      172
    </td>
    
    <td>
      23%
    </td>
    
    <td>
      $6.52
    </td>
  </tr>
  
  <tr>
    <td>
      4. CalFresh approvals
    </td>
    
    <td>
      80
    </td>
    
    <td>
      46%
    </td>
    
    <td>
      $14.17
    </td>
  </tr>
</table>

This means that of 1000 Californians who see online advertisements for CalFresh, about 40 will click the ad, about 9 will submit CalFresh applications, and about 4 will get approved for CalFresh. In total, it currently costs about $14 in online advertising outreach to get someone successfully enrolled in CalFresh through GetCalFresh.org. We intend to further decrease this cost per approval over time as we add features and work with counties on business processes to increase the approval rate.

&nbsp;

### Impact: Most people apply for CalFresh in under 10 minutes

[<img class="alignnone  wp-image-33893" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/image01.png" alt="image01" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/image01.png)

The median time to submit a CalFresh application through GetCalFresh.org is 8:12 and the average is 11:47. This is approximately 1/3 the time of the existing online applications for CalFresh. Although we don’t have access to robust comparison data, the Code for America team has collected preliminary data based on 14 semi-structured interviews with MyBenefitsCalWIN users. Of the users who successfully submitted a CalFresh application on MyBenefitsCalWIN, the self-reported average time to complete was 28 minutes. Users who started the application but did not submit one spent an average of 33 minutes working on the application before giving up.

&nbsp;

### Impact: People can apply for CalFresh from their mobile phones

Over one quarter (26%) of users are applying on a mobile phone or tablet. As documented in the prior report, this is a critically important feature to increase access to CalFresh for the 13% of American adults who depend on their smartphones to the internet. Nonetheless this is not possible on any of the existing online applications for CalFresh.

&nbsp;

### Impact: A simple online application improves program access for clients in greater need

For example, two GetCalFresh.org applicants noted significant challenges in completing the process without an effective online application:

  * “Because I have a sleep disorder, please have CalFresh Rep. call me in the afternoon hours and, if possible, a heads-up email for when I might expect the call would be helpful, too.”
  * “I have very bad social anxiety and PTSD which have thus far made it extremely difficult to come and do this in person. Also very hard to get myself to medical appointments. PLEASE HELP!!”

More generally, about 10% of GetCalFresh.org applicants — all of whom came through online search channels — identify themselves as homeless.

&nbsp;

### Lesson: There are nearly 250,000 Google searches for CalFresh on mobile phones every year

As documented in the [Barriers to CalFresh Participation](http://calfresh-barriers.herokuapp.com/) report, there over approximately 700,000 Google searches related to CalFresh or food stamps each year in California. Approximately 35% of those searches happen on mobile devices. For example, here is more detailed information for two of the most common Google queries:

[<img class="alignnone size-full wp-image-33851" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/adwords.png" alt="Adwords" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/adwords.png)

### Lesson: The majority of applicants want to receive application updates via email and text message

Over 60% of GetCalFresh.org applicants chose to receive updates about their application over email and 50% over text message.

&nbsp;

### Lesson: A simple online application for CalFresh can work for clerical staff and eligibility workers

We interviewed approximately 25 clerical staff, eligibility workers, managers, and program specialists who process CalFresh applications across 5 counties. Counties included:

  * San Francisco
  * Solano
  * Placer
  * Marin
  * Contra Costa

We summarize key points below.

Application clearing is the process of creating or identifying a case in CalWIN or C4. In order to clear a case, clerical staff must uniquely identify all individuals in CalWIN or C4. If staff cannot successfully clear the case they must contact the client to gather more information, which can prolong or stall the application process. Counties need 4 pieces of information per household member on the application in order to successfully clear a case. They are:

  * Full name
  * Address (or homeless status)
  * Social security number, if available
  * Date of birth

Common problems that interfered with the application clearing process include:

  * Missing dates of birth
  * Missing household members; applicants frequently ONLY include the primary applicant and do not provide any information about additional household members.
  * Incorrect household; applicants are either erroneously included or excluded with respect to the CalFresh definition of “household”.  Adding additional household members to a case is much more difficult than removing household members.

A simple and effective online application could support applicants in submitting this crucial information and thus reduce the number of applications that counties fail to clear.

After the application clearing process the next step is for eligibility workers to conduct the interview and make an eligibility determination. In order to complete an effective interview, eligibility workers need:

  * Reliable contact information
  * Verification of identity
  * Thorough verification of income

Common application problems for eligibility workers include:

  * Missing or invalid phone numbers
  * Clients misunderstand the distinction between gross and net income and therefore submit insufficient verifications (e.g., bank statements only show net income)
  * Missing household members; eligibility workers cannot add new household members to a case because they need to go through the clearing process first. This can delay the application process for clients.
  * Clients get upset when EWs ask the same questions that were already asked during the initial application
  * Clients get upset when their benefit allotment is less than anticipated

A simple and effective online application could support applicants in submitting accurate contact information, household information, and moderate their expectations for the interview process and likely benefit allotment. Further, we found that much of the information on the online application for CalFresh are not used by eligibility workers to make eligibility determination. A simple and effective online application does not require clients to enter information that is not useful for making eligibility determinations, thus decreasing the client burden when applying.

&nbsp;

### Lesson: A simple online application should help clients submit verification documents after the initial application

As described in our first report on the barriers to CalFresh participation, [eligibility workers report](http://calfresh-barriers.herokuapp.com/after_applying/ew_survey.html) that many or most clients need to submit additional verification documents after the initial application. This is currently a challenge for many clients across many counties.

The statewide GetCalFresh.org pilot has shown that counties vary significantly in their capacity to receive verification documents from clients through accessible channels. Some counties support centralized submission via fax, email, and online, while other counties do not accept fax or email submission at all. For example, Fresno accepts verification documents in person, via postmail, via a county website (<https://dsswebupload.co.fresno.ca.us/>), and via a centralized fax number while Alameda and many LA offices only accepts verifications in-person or via postmail.

We plan to better understand these operational differences in the future.

&nbsp;

# The CalFresh Client Experience: Impacts & Lessons

## _Balance_

[Balance](www.codeforamerica.org/apps/balance/ "Balance") is a free service that lets anyone check their EBT balance by text message.

&nbsp;

### Impact: In the last year, more than 3,000 CalFresh clients have checked their EBT balance via text message

In the last year, clients from all 31 California area codes have used this service and more than 1,000 CalFresh clients check their EBT balance over 4,000 times via text message each month. The majority (62%) of clients who try the service once return to use it again.

&nbsp;

### Lesson: Clients want deposit alerts

Many users have explicitly asked for deposit alerts. Here is a small sample of incoming text messages:

  * &#8220;When is my next  drop&#8221;
  * &#8220;When will I receive my food stamps ?&#8221;
  * &#8220;When will i get my food check?&#8221;
  * &#8220;When will my stamps be available&#8221;
  * &#8220;When do I get my benefit again&#8221;
  * &#8220;When will my cash benefits come in?&#8221;
  * &#8220;When do I get my next benefits&#8221;
  * &#8220;Can you find out when your money goes on&#8221;
  * &#8220;When will be deposited for next&#8221;
  * &#8220;when does food stamps get updated&#8221;
  * &#8220;When do i get my foodstamps&#8221;
  * &#8220;when does janurary stamps get put on&#8221;
  * &#8220;When will be the nxt EBT Benifits?&#8221;
  * &#8220;When is the pay period?&#8221;

The demand for deposit alerts also manifests in a spike of activity at midnight as clients anticipate their monthly deposit:

[<img class="alignnone size-full wp-image-33849" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/balance.png" alt="balance" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/balance.png)

Clients have offered almost unanimously positive feedback:

  * &#8220;&#8216;And I was like FINALLY, FINALLY! It&#8217;s so annoying to have to call every time and type in all those numbers. Now I just copy paste copy paste!&#8217;&#8221;
  * &#8220;very useful, quicker than getting on the phone and have to listen to people speaking, so much easier&#8221;

&nbsp;

## _EBTNearMe_

[EBTNearMe.org](http://www.ebtnearme.org "EBTNearMe.org") helps anyone in California find nearby EBT retailers and surcharge-free ATMs.

&nbsp;

### Impact: Approximately 13,700 people have used EBTNearMe.org

Since launching the service in July 2014, EBTNearMe.org has been used by residents in 42 of California’s 58 counties and has been officially integrated into Los Angeles’s Department of Public Social Services Mobile application.

[<img class="alignnone size-full wp-image-33850" src="http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/ebtnearme.png" alt="ebtnearme" />](http://www.codeforamerica.org/blog/wp-content/uploads/2015/07/ebtnearme.png)

&nbsp;

&nbsp;

### Lesson: Surcharge-free ATM data has inaccuracies

The ATM fee data is collected by Xerox when clients use their California Advantage card at ATMs throughout California. Code for America received the data through OSI, which gets periodic reports from Xerox.

To date we have received 31 user-generated reports of bad ATM data, 18 of which reported that ATMs charged a fee despite being listed as “free.” ** **We have not yet tried to validate the data in a representative way. Individual reports are available online at  <http://bit.ly/ebtnearme-feedback>

&nbsp;

### Other lessons

  * The majority (66%) of EBTNearMe users are on mobile devices.
  * Clients want better information about restaurants and hot meal programs. Approximately 40% of EBTNearMe.org users found the website while searching for information for restaurants that accept EBT. Because the hot meal program is relatively restricted, this may be a sign of confusion among CalFresh participants about the nature of their benefit (for most enrollees, restricted to unprepared food purchases).

&nbsp;

# **Thank you**

As always, thank you for your work and for thank you for supporting ours.

Best,

Jake Solomon
  
Dave Guarino
  
Alan Williams
  
Rebecca Coelius