1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q3 Hyperledger Indy

Created by Stephen Curran, last modified by Troy Ronda on Aug 20, 2020

# Projects

##### **Distributed Ledger**

- [indy-node](https://github.com/hyperledger/indy-node)
- [indy-plenum](https://github.com/hyperledger/indy-plenum)

##### **Client Tool**

- [indy-sdk](https://github.com/hyperledger/indy-sdk)

##### **Shared Components**

- [indy-hipe](https://github.com/hyperledger/indy-hipe)
- [indy-test-automation](https://github.com/hyperledger/indy-test-automation)
- Soon to be added: [indy-node-monitor](https://github.com/bcgov/indy-node-monitor)

Project Health

Indy is a healthy project, but has a current lack of contributors.  The maintainers are working to address that issue.

Per the [Indy Activity Dashboard](https://lfanalytics.io/projects/hyperledger%2Findy/dashboard), Indy’s codebase has 21,028 commits from 238 unique contributors. This quarter there were 61 commits from 8 contributors.

# Questions/Issues for the TSC

We continue to track some of the same issues as in [previous quarters](https://lf-hyperledger.atlassian.net/wiki/display/HYP/2020+Q1+Hyperledger+Indy).

### **Measuring the size and make-up of our user community**

Update: Thanks to the awesome work of [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence), the [Indy Activity Dashboard](https://lfanalytics.io/projects/hyperledger%2Findy/dashboard) shows the activity in the Indy community.

### **Build Issues**

Update: No Progress - issue repeated.

The volunteers who were working on migrating the build from Jenkins to GitLab CI were not able to complete a functional system. The build is complex due to the variety of target environments for LibIndy and the requirement of running an Indy Node pool for testing. The approach taken in Jenkins is significantly different than the approach favored by GitLab CI or Azure Pipelines, and migration will require significant effort.

Future work planned:

- We need a new commitment from the various teams who have expressed interest.

### **Diversity of Contributor Community**

Update: No progress - issue repeated.

As agent implementers have moved to the Aries project, Indy was left with few contributors to the ledger who all primarily come from a single organization. The health of the project requires broadening this list.

Future work planned:

- Current initiatives are being led by different organizations, which we hope will become consistent contributors in the future.
- New: Developer Conference planned for September, 2020: [Indy Interop-a-thon - Making "Network of Networks" Real](https://lf-hyperledger.atlassian.net/wiki/spaces/II/overview)

# Releases

### **June 2020:**

##### Indy Node 1.12.3

- A response to an identified security vulnerability that if exploited could take down an Indy network instance.

# Overall Activity in the Past Quarter

In the past quarter, ledger development has slowed to the release of a security fix. Some work has occurred in the indy-sdk, but no releases are planned. The difficulty in releasing is a challenge for the community.

# Current Plans

There is little ledger activity occurring. Previous work on "rich schemas" to support W3C VCs has been put on hold and will likely be replaced with a focus on BBS+ ZKPs, which likely has the benefit of eliminating (well, deprecating) features from Indy vs. adding. Our focus for client libraries is to break LibIndy into separate components that can be evolved to fit the proposed Aries architecture. Work on an improved revocation has progressed slowly, delayed within the Ursa community.

We are planning an "[Indy Interop-a-thon - Making "Network of Networks" Real](https://lf-hyperledger.atlassian.net/wiki/spaces/II/overview)" virtual conference.  Details of the goal of the conference can be found in the link.

The need for a better CI/CD solution is rising. There are currently no active maintainers available to drive releases. Resources can be called on for help, but there are no active participants available to do that independently.

# Maintainer Diversity

The weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. The Maintainers who work exclusively on Indy is decreasing as many of them move on to help with the Hyperledger Aries project. We are hoping the [Indy virtual conference](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=19890190) in September will trigger an increase in maintainers.

# Contributor Diversity

The team at British Columbia Government is leading the effort to evolve LibIndy, although that is largely at the lower levels – not yet in Indy (e.g. at the Rust crates layer). ABSO continues to contribute, as do members of several other organizations.

# Additional Information

- Key channels on Hyperledger Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

# Reviewed by

- Angelo De Caro
- Arnaud J Le Hors
- Christopher Ferris
- Dan Middleton
- Gari Singh
- Hart Montgomery
- Mark Wagner
- Nathan George
- Swetha Repakula
- Tracy Kuhrt
- Troy Ronda

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
