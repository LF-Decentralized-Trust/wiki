1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Cactus

Created by Hart Montgomery, last modified by Gari Singh on Feb 05, 2021

This is the 2021 Q1 Hyperledger Cactus quarterly report.  We will cover more than a quarter's worth of material, though, since Cactus was left off the 2020 Q4 calendar.

Project Health

Cactus continues to progress as a project.  While we have not added any new major contributors or maintainers, Cactus continues to build momentum and has maintained all of its core members.  We are also particularly excited about an academic group of people led by Rafael that are looking at Cactus from a theoretical as well as practical perspective, and we think this academic effort has the potential to add a lot to the project.  The Cactus maintainers (and even some non-maintainer contributors) have given a number of talks and presentations on Cactus to outside audiences, which has bolstered interest. 

# Questions/Issues for the TSC

We don't have any issues or questions for the TSC at this time.  We've said it before, but we'll say it again:  as we roll out interfaces for different Hyperledger blockchains, though, we would appreciate reviews and comments from people affiliated with said blockchains.  So please expect contact from us in the future!  We are presenting at the TSC meeting on the due date of this report, so we hope the TSC members will have questions for us then!

# Releases

We've had two releases since our last report.  We released v0.2 as promised in December, and very recently v0.3.  The changes in these releases are best described as moving towards a modular, efficient blockchain integration platform that can be used with both the Accenture and Fujitsu applications (as well as others).  The precise changes in each release are much too long for this report, but thankfully Peter has done a wonderful job of documenting them here ([https://github.com/hyperledger/cactus/releases](https://github.com/hyperledger/cactus/releases)).  Please take a look if you'd like to see all of the release details.

# Overall Activity in the Past Quarter

We have made a concerted attempt to improve our response times and responses on communication tools.  While some of our contributors have always been excellent (e.g. Peter), as a project, we thought we could do better, and have been making an effort which thus far seems to be working. 

The number of technical changes that we've made and the improvements we've completed are quite numerous and varied.  We've worked on the testing infrastructure, validation, examples, and CII badging, just to name a few things.

# Current Plans

Our goal is to move forward with incremental releases targeting more and more features of our modular architecture.

Over the next quarter, one of our major foci will be the ledger plugin module.  This is (in a nutshell) the part of Cactus responsible for integration with each different ledger, and can be viewed as a "connector"–it's not responsible for any business logic.  Our goal is to complete modular, interoperable ledger plugins for a variety of supported blockchains in a number of different languages, which would allow us to start using Cactus in many different novel applications.  We are also aiming to make Cactus more workable across platforms, including offering Windows support.

If you'd like to see a detailed list of things we're working on, please check out our github issues ([https://github.com/hyperledger/cactus/issues](https://github.com/hyperledger/cactus/issues)).  We have 100+ issues currently, so this is a very detailed list.  But if you're curious (or want to add an issue of your own), please feel free to check it out.

# Maintainer Diversity

We still have four maintainers.  They are:

Shingo Fujimoto – Fujitsu

Jonathan Hamilton – Accenture

Peter Somogyvari – Accenture

Takuma Takeuchi – Fujitsu

We are more than open to adding additional maintainers outside of the core Accenture/Fujitsu group, and hopefully in the not too distant future.

# Contributor Diversity

We recommend the following for detailed contributor information:  [https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard](https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard).  Thanks Ry!

Our contributor list is starting to get too long to efficiently list in this report.  We encourage you to check out the above link if you'd like to see all of the information.  However, the organizations that lead contributors are still Accenture and Fujitsu, with other notable contributions coming from those at Red Hat and the University of Lisbon.  We have also 5 contributors whose affiliations are unknown to the initial author of this report.   We hope that the academic interest in Cactus will drive more contributors.  

# Additional Information

We are looking forward to our presentation to the TSC!  Thanks for your time.

We also note that there is an IBM interoperability project that is in the process of being open-sourced as well.  We are working with the developers of that project to look at common ground between Cactus and their code/project philosophy. 

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
