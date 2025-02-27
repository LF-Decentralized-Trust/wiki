1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q4 Hyperledger Caliper

Created by Attila Klenik, last modified by Nathan George on Mar 31, 2020

# Project

[Hyperledger Caliper](https://github.com/hyperledger/caliper)

Project Health

Since the first published release, the maintainers are working on improving the quality of the core code-base. Besides the obvious reasons for this, we also expect that a cleaner code-base will lower the entry barrier for new contributors.

Community relations mainly happen on Rocket.Chat, and the questions are answered in detail, and on time. Furthermore, there is an increasing contributor interest related to the supported DLTs (both improving recent adapters and implementing new ones, like for Corda).

# Questions/Issues for the TSC

There are no issues at this time.

# Releases

v0.2.0 was released on 25th October (on npm and DockerHub), see the [GitHub release page](https://github.com/hyperledger/caliper/releases/tag/v0.2.0). 

v0.3.0 is coming soon.

# Overall Activity in the Past Quarter

- **Project stats (since the last report)**
  
  Issues closed: 27
  
  PRs merged: 73
- **Development-related**
  
  - Exposed Prometheus metrics about client-side observations
  - Added highly flexible logging subsystem
  - Added platform support for Ethereum, Hyperledger Besu and FISCO-BCOS (all of them community contributions)
  - Released v0.2.0
  - Consolidated CI tests
  - Improved the result reporting, including embedded charts
  - Deprecated the Composer support
  - Added Yeoman generators for Caliper-related benchmark artifacts (plugin skeletons, configuration files)

# Current Plans

Current development efforts are focusing on the following, core code-base related tasks (for the v0.3.0 release):

- Reimplementing the distributed workload generation (which was removed in a previous release) using MQTT
- Cleaning up the communication and dataflow in the worker and manager modules
  
  - Resulting in a highly modular architecture, which is easily extensible
  - Increasing workload generation performance by pushing aggregation tasks from the workers to the manager
- Preparing a CI/CD for a rolling unstable release upon every merged PR (so the stable releases will have robust feature sets)

Subsequent releases will target the improvement of platform supports, starting with the existing adapters.

# Maintainer Diversity

The list of maintainers remained unchanged since the last report.

# Contributor Diversity

There are currently 30 contributors to the repository, 17 of them with more than one commit. To the best of our knowledge, contributors are from various companies/organizations, such as Huawei, IBM, Intel, Soramitsu, Budapest University of Technology and Economics, Monax and the University of Oregon. The maintainers are also keeping in touch with other companies who are mainly interested in expanding the platform support of Caliper (e.g., with Corda).

# Additional Information

N.A.

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
