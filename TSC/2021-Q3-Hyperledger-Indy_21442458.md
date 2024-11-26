1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Indy

Created by Stephen Curran, last modified by Arun .S.M. on Nov 01, 2021

# Projects

##### **Distributed Ledger**

- [indy-node](https://github.com/hyperledger/indy-node)
- [indy-plenum](https://github.com/hyperledger/indy-plenum)

##### **Client Tool**

- [indy-sdk](https://github.com/hyperledger/indy-sdk)
- [indy-vdr](https://github.com/hyperledger/indy-vdr)
- [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs)

##### **Shared Components**

- [indy-hipe](https://github.com/hyperledger/indy-hipe)
- [indy-test-automation](https://github.com/hyperledger/indy-test-automation)
- [indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)

Project Health

The work on the Indy DLT (indy-node and indy-plenum) slowed this quarter to a focus only on the CI/CD capabilities and upgrading to Ubuntu 20.04; no new functionality was added. The transition of the CI/CD from an older, undocumented Jenkins/manual process to a GHA-based CI/CD pipeline has been slow. The work on the CI/CD and OS Upgrade has prevented any progress on new features – blocking most notably the upgrade to the new "did:indy" DID Method. With the change of the W3C DID Specification to "Proposed Standard" it is appropriate that work start (and finish) soon.  In addition to the CI/CD work, the team is add some tooling to make it much easier to get started doing development on the project. The goal is to promote the tribal knowledge about the projects into easily followed steps to deploy for development, make changes, debug and run tests. To be clear, these changes are focused on making it easier to make changes to the DLT code itself.

On a positive note, the interest in deploying instances of Indy continues, with lots of questions on Hyperledger Chat from people learning to run their own instances. Further, there are no significant bugs that are pending action, and no demand for new functionality from the user base. Indy "just works". For example, the Sovrin networks (MainNet, StagingNet and BuilderNet, operated by more than 50 organizations) is celebrating its 5th birthday this month, and coming up to 2 years without an outage. Even demand for the new "did:indy" DID Method is moderate at best. 

Work has proceeded on the replacements for Indy SDK – indy-vdr and indy-shared-rs, with a tagged release of both projects.  

Per the [Indy Activity Dashboard (2021-04 to 2021-06)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-04-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-06-30T07%3A00%3A00.000Z%22%7D), there were just 34 commits from 7 contributors. which is a significant drop from the last quarter.

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: Work was not completed last quarter as expected on this task. We'll see how it goes this quarter...

### **Diversity of Contributor Community**

**Update**: Contributor community diversity remains a top of mind issue with the maintainers.  We are considering a "Contributor Campaign" in conjunction with Hyperledger Staff to build attention to both Indy and the new "did:indy" DID Method. The need is not for "drive-by" devs doing their first commit, but rather those that are building their businesses on Indy and should be contributing to the evolution of the project. To a degree, the project is a victim of its quality and completeness, as mentioned in the "Project Health" section.

# Releases

- indy-sdk 1.16.0
- indy-shared-rs 0.3.0
- indy-vdr 0.3.0

# Overall Activity in the Past Quarter

In the past quarter, ledger code development has slowed as we focus on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04.  

There was no progress on the new Indy DID Method. The work left at the end of the last quarter remains: wrapping up the specification and defining the backlog of work for indy-node, indy-sdk and indy-vdr. With the CI/CD work blocking progress on indy-node, it's very difficult to convince contributors in the community to work on the DID Method if it is so hard to test and impossible to release.

# Current Plans

The push will be to complete the new CI/CD Indy Node and Plenum pipelines, the Ubuntu 20.04 upgrade, and tools to make it easier to do Indy Node development. Until that is completed, there will not be changes to the functionality.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. Topics and attendance has dropped recently, somewhat due to holidays, but also due to the lack of topics other than "how is the CI/CD work coming along?"

# Contributor Diversity

See the comments in the "Issues" section (above). With work limited to CI/CD work on the Indy DLT side, there is little else to be done until that is complete.

# Additional Information

(***Note* – no change**)

- Key channels on Hyperledger Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
