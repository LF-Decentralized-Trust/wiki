1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q3 Hyperledger Caliper

Created by Attila Klenik, last modified by Angelo de Caro on Sep 26, 2019

# Project

[Hyperledger Caliper](https://github.com/hyperledger/caliper)

Project Health

Caliper reached a significant milestone in the last quarter. The first official pre-release was published to both [NPM](https://www.npmjs.com/package/@hyperledger/caliper-cli) and [DockerHub](https://hub.docker.com/r/hyperledger/caliper). The published artifacts significantly increased the setup&amp;run experience for the community, resulting in fewer issues/questions both on GitHub and Rocket.Chat, which, in turn, freed up some maintainer efforts to focus on new features and upgrades. 

Community relations mainly happen on Rocket.Chat, and the questions are answered in detail, and on time. Furthermore, there is an increasing contributor interest related to the supported DLTs.

# Questions/Issues for the TSC

There are no issues at this time.

# Releases

The first official pre-release (after some significant repository restructuring and refactoring) was finally published on NPM and DockerHub, marking the v0.1.0 state of Caliper.

Since then, the maintainers have a stable code-base to build upon without worrying about breaking the release used by the community. This increased the momentum of development for the project.

The maintainers haven't decided on a regular publishing frequency yet, but they plan to bump versions after every added major feature or a set of bug-fixes (this means an approximately 3-4 weeks long release cycle).

# Overall Activity in the Past Quarter

- **Forum activities**
  
  Mostly the Rocket.Chat channel is used for Q&amp;A. Every question is answered in detail or redirected towards the relevant docs page. The questions are usually answered within a day (more often than not, even within an hour or realtime), keeping in mind that the active maintainers are mainly located in Europe.
- **Project stats (since the last report)**
  
  Issues closed: 83
  
  PRs merged: 42
  
  [Additional charts](https://docs.google.com/spreadsheets/d/e/2PACX-1vRZCaEWwKMZZCnHf-YVNcSpU3PYd81rozu9KVrSptg7NixRdyHp64isnLIKxq8fTJG7zg26UVpIgNaq/pubhtml?gid=1454794804&single=true)
- **Recent noteworthy dev-related activities**
  
  - Deprecated the old Fabric adapter, and replaced it with a more "modern" one (increased flexibility, feature set, maintainability)
  - Improving the new Fabric adapter (support SDK gateway mode, discovery, wallets)
  - Fixed some load generation performance-related issues
  - Fixed some Docker monitoring bugs
  - Increased CLI and runtime flexibility
  - Started to cover the codebase with unit tests
  - **Published v0.1.0**
  - Added version selection for docs page, and improved the content of some pages
  - Separated the sample benchmarks into a new [caliper-benchmarks](https://github.com/hyperledger/caliper-benchmarks) repository, which (coupled with the release) provides an easy entry point for the community to start experimenting with Caliper.
  - **A UI component was implemented by Jason You during the summer internship.** It is currently under review and further polishing. He did an excellent job during the summer, even though the Caliper code-base was under heavy development. This component will further help the adoption of Caliper in the community.

# Current Plans

The development tasks can be sorted mainly into the following categories:

- Stabilizing the core architecture
- Introducing support for new platforms
- Polishing the existing platform adapters
- Improving the documentation

### Stabilizing the core architecture

- The scope and goals of Caliper were a bit shady/undefined for some time, mainly the line between being a load generator and/or a monitoring framework.
  
  - The current consensus seems to indicate that Caliper will aim to be a full-fledged, flexible load generator framework for DLTs.
  - Correspondingly, the monitoring responsibility of Caliper will be delegated to tried-and-true industrial-grade tools and Caliper will provide integration with them.
  - As a first trial, a Prometheus integration was implemented and is currently under review.
- It's clear that Caliper should be a loosely coupled, distributed framework/system, capable of generating workloads on a large scale.
  
  - Until recently, Zookeeper was used to coordinate multiple Caliper "worker" nodes. It was an experimental feature, wasn't easy to deploy, not to mention that it required additional infrastructure elements (zookeeper nodes) beside Caliper.
  - To this end, this feature will be removed in v0.2.0
  - The plan is to introduce a more lightweight, embedded messaging solution between clients in v0.3.0, like ZMQ or other similar solutions. This would keep the Caliper artifacts self-contained (like Kafka vs Raft in Fabric), facilitating deployment.
- The last group of core-related work items is covering the code-base with unit tests as much as possible. Once the code-base is stabilized by the above items, hopefully, this task will become easier.

### Introducing support for new platforms

Currently, there are multiple platform support PRs under review. Namely for:

- Ethereum
- FISCO BCOS
- Corda

It's worth to note that each PR is submitted by the community ![(thumbs up)](images/icons/emoticons/thumbs_up.png)

### Polishing the existing platform adapters

A key selling point of Caliper is the ability to implement workloads in a DLT-agnostic way. "Write once, run anywhere."

The list of supported DLTs is getting longer, which will hopefully give some ideas about the required abstraction level of the Caliper API. However, the help of the specific platform's experts/maintainers will be probably needed to provide full-fledged support for the platforms.

### Improving the documentation

The issues/questions pressure towards the maintainers could be decreased further by improving the documentation:

- Clarifying the documentation of the general Caliper components and adapters.
- Providing detailed tutorials for writing benchmarks and other tips&amp;tricks.

There's already active work addressing this task group (independently/concurrently with the other tasks).

# Maintainer Diversity

Current maintainer list and affiliations, in alphabetical order: 

- Attila Klenik (Budapest University of Technology and Economics)
- Feihu Jiang (Huawei)
- Liam Grace (IBM), **new maintainer**
- Nick Lincoln (IBM)
- Yaoguo Jiang (Huawei)
- Yu Pan (Huawei)

# Contributor Diversity

There are currently 28 contributors to the repository, 18 of them with more than one commit. To the best of our knowledge, contributors are from various companies/organizations, such as Huawei, IBM, Intel, Soramitsu, Budapest University of Technology and Economics, Monax and the University of Oregon. The maintainers are also keeping in touch with other companies who are mainly interested in expanding the platform support of Caliper (e.g., with Corda).

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
