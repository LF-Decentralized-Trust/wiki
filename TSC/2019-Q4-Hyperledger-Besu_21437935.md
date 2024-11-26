1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q4 Hyperledger Besu

Created by Danno Ferrin, last modified by Swetha Repakula on Dec 11, 2019

# Project

Hyperledger Besu

Project Health

Besu is strong and growing. This quarter Besu has prioritized switching to the Hyperledger tools and growing its community. Besu has been successful on both fronts while also delivering its 1.3 Release in October 2019.

# Questions/Issues for the TSC

- RocketChat presents an unneeded point of friction bring in members from the larger Ethereum community.  With Gitter we could send a link directly to our project room and anyone could read it without logging in.  Similar links for rocket chat (example: [https://chat.hyperledger.org/channel/besu](https://chat.hyperledger.org/channel/besu)) present a never ending loading screen unless the user has already logged in.
- - We ask the Hyperledger operations employees to enable a configuration option that would permit read-only access to chat rooms without authentication (“Allow Anonymous Read”).
- The Besu team is still looking for clear guidance on active status from the TSC. Per the latest communication from the TSC, we believe they want 3 maintainers from different organizations (Note that this is on track to be achieved on 10 Dec). Can we gain confirmation that is the requirement that will enable the TSC to vote “yes” on active status?

# Releases

Besu has released one minor version update (1.3, 3 Oct) and six bi-weekly patch releases (1.2.4 on 23 Sep and 1.3.1 through 1.3.5 on 15 Oct, 22 Oct, 5 Nov, 5 Nov, and 20 Nov respectively).

Major functional improvements include

- Support for Ethereum Classic and Classic testnets (from Edward Mack and Greg Markou of Chainsafe Labs)
- Support external mining for PoW networks (from Antoine Toulme of [Whiteblock.io](http://Whiteblock.io))
- Ethereum Mainnet Istanbul support
- Added state pruning of blockchain data

# Overall Activity in the Past Quarter

Hyperledger Besu was fully transitioned from a PegaSys project to a Hyperledger project this quarter.

- Github repos moved to Hyperledger org
- Bug tracking moved to the Hyperledger JIRA
- Chat support room moved from Gitter to Hyperledger’s Rocket Chat
- CI/CD build infrastructure moved from Jenkins to Hyperledger’s CircleCI
- Established a bi-weekly contributor call

As a part of joining the Hyperledger community, the Besu team has participated in the community by:

- Added support for Besu in Caliper (Oct. 20)
- Participated in the CI/CD working group conversations and sharing our project’s research and best practices (Sep.- Oct.)
- Attended the Maintainer summit in Minneapolis (Oct. 8-9)
- Presented a talk at the Hyperledger booth at Sibos (Sep. 23-25)
- Submitted several talks and were approved to present at the Hyperledger Global Forum (Sep. - Nov.)
- Attended the Hyperledger meet-up at Devcon in Japan (Oct. 9)
- Presented privacy solution at Architecture WG - Privacy Confidentiality track (Sep. 20)
- Presented at Hyperledger meet-up in Japan (Dec. 3)

# Current Plans

The Besu project team has several upcoming priorities:

1. The project team is currently working towards its 1.4 Release, scheduled for February 2019. The 1.4 Release is expected to include the following features:
   
   1. Multi-tenancy
   2. End to end TLS on network protocols
   3. Public network hard forks (Muir Glacier and Aztalan potentially)
2. The Besu team is also focusing on finalizing and publishing performance metrics with its work on Hyperledger Caliper. Besu was successfully integrated with Caliper in Q4 and the team is now in the process of testing various scenarios for Caliper. We think publishing these performance metrics will help provide the community additional context on the project’s useability for a variety of use cases.
3. Besu is also continuing to engage with its community and grow the diversity of its maintainer and contributor base. The Besu team is hoping to continue to grow attendance for its bi-weekly contributor calls to grow engagement across contributors.

# Maintainer Diversity

Our maintainer diversity is growing.  Early next week we should have maintainers representing three different organizations.

- At the beginning of the quarter Besu was still a PegaSys project, so all the maintainers at the beginning of the quarter are PegaSys employees.
- Ivaylo Kirilov of Web3 Labs was added because of strong contributions in EEA Privacy
- Edward Mack of Chainsafe labs is in the process of being added because of strong contributions in Ethereum Classic support.

Our process for adding Maintainers was featured on the Hyperledger Blog as a best practice for a maintainer governance process - [https://www.hyperledger.org/blog/2019/11/07/best-practices-and-lessons-learned-from-hyperledger-besu-establishing-a-maintainer-process](https://www.hyperledger.org/blog/2019/11/07/best-practices-and-lessons-learned-from-hyperledger-besu-establishing-a-maintainer-process)

100% of current maintainers made a contribution this quarter.

# Contributor Diversity

Since the Besu project was approved by the TSC into the Hyperledger community at the end of August 2019, there have been a total of 39 code contributors.

- 23 contributors from PegaSys (58% of contributors)
- 16 contributors from outside of PegaSys (42% of contributors)
- 7 different organizations that can be identified
- 7 contributors whose organization were not determined.

Additionally, there have been content contributions in the community, including technical content enablement materials.

# Additional Information

None at this time.

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
