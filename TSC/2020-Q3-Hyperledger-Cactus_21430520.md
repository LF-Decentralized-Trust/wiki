1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q3 Hyperledger Cactus

Created by Jonathan Hamilton, last modified by Gari Singh on Oct 22, 2020

# Hyperledger Cactus Quarterly Report

Project Health

Cactus continues to build momentum and has a solid group of sustained contributors, in addition to the core Maintainers.    We have presented at several Hyperledger meetups, including the Tokyo &amp; London meetups, which had significant turnout (&gt;50) attendees) despite Covid / virtual setup.  We also presented at multiple sessions of the Hyperledger Member summit and solicited further interest there.  Ultimately, while we aspire to further community involvement, we see the project participation growing at a moderate and manageable pace.

# Questions/Issues for the TSC

We don't have any issues or questions for the TSC at this time.  As we roll out interfaces for different Hyperledger blockchains, though, we would appreciate reviews and comments from people affiliated with said blockchains.  So please expect contact from us in the future!

# Releases

We have made material progress towards a 0.2 Release, but have yet to finalize the scope.  The project's aspirations are well articulated in the whitepaper, but not yet clearly mapped across release milestones.  Therefore, we will put extra focus into roadmapping out key features early in Q4 and soliciting community inputs to guide our release objectives.

# Overall Activity in the Past Quarter

- We have explored and initiated the development of Ursa being compiled to Javascript (which we intend to use in Cactus which is a NodeJS+Browser project at heart)
- Researched the security aspect of the plugin architecture from the point of view that malicious plugins could be installed if someone tricked the administrators of a Cactus node to do so. Special thanks to [Clive Boulton](https://lf-hyperledger.atlassian.net/wiki/people/70121:cd28b3ec-0f42-4c0a-a8a5-83954ab74aad?ref=confluence)for bringing this up to begin with and the continued support during our exploration
- Created a fabric all in one (AIO) docker container image and the one for corda is not far behind. These allow us to have self-contained test automation where each test case can be pulled up with a brand new, clean slate ledger if necessary.
  
  - The ledger connectors are not far behind from being completed either, but we still have some kinks to work out and alignment to make among the maintainers as to how exactly we would want them to fit into the current architecture of the project so this part is still work in progress.
  - The fabric AIO image still has a to do item for it regarding the peer containers port mapping functionality. This is not a blocker issue because we can restrict the test execution to one-at-a-time instead of parallel execution and therefore the randomized port publishing feature of Docker is not necessary for the fabric AIO container to work properly.
- In the spirit of open source, we contributed to other (non Hyperledger) projects while in the process of developing certain features for Cactus itself (OpenAPI generator, webpack to name a couple)
- Introduced an initial implementation of a cross-platform (NodeJS, Browser) signature generation and validation component. 
  
  - We intend this to be superseded by the Ursa Javascript build once that is available on npm as a package (stay tuned)
- Initiated the draft for a research paper we'll write collaboratively as a team. Special thanks to [Rafael Belchior](https://lf-hyperledger.atlassian.net/wiki/people/712020:0476fdbd-25a2-41d4-9ba2-27de7ea0f715?ref=confluence)for organizing.

# Current Plans

Our plans are essentially the following:

1. Make headway with the performance benchmarks as the research paper depends on this as well
2. Make progress on the research paper's first edition
3. Merge all of the functionality from the Fujitsu and Accenture solutions into our plugin architecture.
   
   1. In-Progress
4. Add functionality for immediately needed use cases
   
   1. Comprehensive examples for said use cases
5. Design future architectures for things that are needed to scale Cactus to bigger use cases, such as identity management.

# Maintainer Diversity

We currently have four maintainers.  They are:

Shingo Fujimoto – Fujitsu

Jonathan Hamilton – Accenture

Peter Somogyvari – Accenture

Takuma Takeuchi – Fujitsu

We are more than open to adding additional maintainers outside of the core Accenture/Fujitsu group, and hopefully in the not too distant future.

# Contributor Diversity

We recommend the following for detailed contributor information:  [https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard](https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard).  Thanks Ry!

That being said, our contributors are as follows:

Rafael Belchior – Technico Lisboa

Patrick Erichsen – Target

Shingo Fujimoto – Fujitsu

Jonathan Hamilton – Accenture

Tracy Kuhrt – Accenture

Hart Montgomery – Fujitsu

Sownak Roy – Accenture

Peter Somogyvari – Accenture

Takuma Takeuchi – Fujitsu

Doris Benda

Dilum Bandara

程阳 – Aliyun

Suyu Ku - Accenture

Jacob Weate - Accenture

# Additional Information

Thanks for reading this!  

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:503b5691-8e92-4d2d-83d3-e9e74d296436?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
