---
layout: post
title: "Clean Development: Data Mining for Corruption Risks"
author: Dylan Fitzpatrick
pic: "world-bank.jpg"
published: true
---
<img src="/img/posts/worldbank-team.png">

Every year, the [World Bank Group](http://worldbank.org) lends billions of dollars to fund infrastructure and other development projects around the globe. Projects vary widely in scale and scope, ranging from [developing hydropower systems](http://www.worldbank.org/en/news/feature/2014/03/20/transformational-hydropower-development-project-paves-the-way-for-9-million-people-in-the-democratic-republic-of-congo-to-gain-access-to-electricity) to [rehabilitating coral reefs](http://www.worldbank.org/en/news/feature/2014/06/05/it-takes-villages-to-conserve-indonesia-precious-coral-reefs) to [improving roads, health, education and agriculture systems](http://www.worldbank.org/en/news/feature/2014/06/04/nuevas-carreteras-y-sistemas-de-riego-mejoran-la-vida-en-ecuador). 

Contractors on these projects are typically hired through a competitive bidding process, in which prospective suppliers of labor, raw materials, or equipment submit proposals to complete the necessary work. Occasionally, prospective contractors attempt to game the competitive system in some way by colluding with other contractors, bribing government officials, or otherwise manipulating the system. Collusion has far-reaching effects on the price and quality of contract delivery, and is difficult to detect. 

Investigators at the World Bank’s [Integrity Vice Presidency (INT)](http://worldbank.org/integrity) are responsible for investigating collusion, as well as the other sanctionable offenses of coercion, fraud and corruption in World Bank-financed projects.  The challenge with a global portfolio is how to detect collusion or corruption, particularly if no one reports the incident. 

Our team at Data Science for Social Good is working with anti-corruption and data experts at INT to help address this challenge. For the rest of the summer, we will focus on developing predictive models that can pinpoint suspicious patterns of behavior in contract bidding data. Due to the scale of project lending in different regions, developing scalable, data-driven approaches to identifying areas of high risk can improve the outcomes of investigative work and aid in prevention of sanctionable practices. 

From the perspective of our partners at the World Bank’s [International Corruption Hunter’s Alliance (ICHA)](http://web.worldbank.org/WBSITE/EXTERNAL/EXTABOUTUS/ORGANIZATION/ORGUNITS/EXTDOII/0,,contentMDK:23195265~pagePK:64168427~piPK:64168435~theSitePK:588921,00.html), this work can make an important contribution to the toolbox of enforcement and prevention authorities internationally. These tools and skills represent critical resources for ICHA members in their growing efforts to leverage data in managing corruption risks and protecting development resources.

####DSSG Goes to Washington

To kick off the project, three members of our team flew to Washington, D.C. for several days of meetings and collaboration with our project partners at INT and the World Bank’s Office of the Controller. The trip was a fantastic opportunity to glean all the information we could from our partners about what corruption, fraud, and collusion look like in reality.

During the visit, we learned that INT investigators have identified several patterns in bidding behavior that could point to collusion or other forms of corruption. Regular, periodic rotation of contract awards among a small group of contractors, for example, might indicate that bidders are working together to set prices or distribute contracts. Contractors may split large projects into multiple small ones, keeping individual contract values below a threshold that triggers additional review or competitive bidding. The total number of bidders shrinking over time might indicate that potential contractors are being pushed out of the market through some form of illegal coercion. While none of these findings represent clear-cut evidence of collusion, they are detectable clues that can help direct investigative efforts and ensure that the integrity of development is not compromised.

Another priority during the trip was asking questions and learning about the data that will provide our window into the problems that INT is working to address. To data scientists, diving into analysis and model-building right away can be an enticing prospect when presented with an exciting new data set, but engaging with stakeholders and domain experts at the earliest stages can help guide analysis and save considerable time down the road. 

<img src="/img/posts/worldbank-meeting.png">

Asking the right questions can help to show the problem in a new light, and might even turn up new data sets that provide a key missing component for solving the problem at hand. Successful data science is all about bringing together deep qualitative understanding of the subject matter with sophisticated computational tools. Our trip to Washington was designed to foster exactly this type of collaboration in the coming months.

On our last day in Washington, we helped the World Bank host a "Data Sprint," in which members of the public interested in data analysis and social problems could come together and work with World Bank data to answer specific questions of interest. The event was a wonderful illustration of how data science can draw on people with vastly different backgrounds and skill sets to make progress on difficult problems.

<img src="/img/posts/worldbank-talk.png">

Our team completed some preliminary analyses of contract bidding patterns, working with Data Sprint participants to identify potential corruption in bidding for Mexican development projects. Now, back in Chicago, the task at hand is to expand this type of analysis to multinational data sets, and to develop more sophisticated models for teasing out evidence of corruption, fraud, and collusion across the globe.

####Data Custodians

Data cleaning is not always an appealing task, but it lays the groundwork for answering important questions. We are working with procurement data, which contains information about individual contracts for completing development projects around the world. Of course, each country and international lending organization has different protocols for data entry and quality control. 

<img src="/img/posts/worldbank-data.png">

The first step in tackling a new question with data is often determining which of the defining properties of big data are most relevant to the problem at hand: volume, velocity, or variety. Here at DSSG, each project team is experiencing the "3Vs" in various combinations and to varying degrees. On the World Bank project, the variety of our data presents the greatest challenge. 

A major preliminary task involves reconciling the differences and quality issues across many different data sets so that they can be combined and analyzed together. A field labeled "date" could mean bid submission date, contract signing date, or project start date depending on which data set it comes from. The cost of various contracts could be represented in hundreds of different currencies, some of which experience wild fluctuations in exchange rates. 

To resolve this particular issue, we need to first scour the internet for daily, historical exchange rates that we can link to specific contracts using signing or award dates. We can then convert all contract amounts to a single standard currency and easily compare the value of contracts across countries and time. This is the reality of data science for social good -- that data cleaning, reshaping, and reconciliation can be as -- if not more -- important than the statistical or visualization tools one chooses for analysis.

Still, we are close to clearing this crucial hurdle and getting started on answering questions with the data. The next step for us will be to work with the available data to construct models of past sanctionable behavior and known patterns of collusion. Our work on data cleaning over the past few weeks has paved the way for meaningful analysis, which will guide INT in its investigative work moving forward. Visualizing and reviewing preliminary results with the World Bank team will be an exciting next step.