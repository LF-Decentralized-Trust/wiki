1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Indy

Created by Stephen Curran, last modified by Angelo de Caro on Dec 09, 2021

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
- [indy-did-method](https://github.com/hyperledger/indy-did-method) - "did:indy" [DID Method specification](https://hyperledger.github.io/indy-did-method/)

Project Health

The work on the Indy DLT (indy-node and indy-plenum) continued slowly this quarter with a focus only on the CI/CD capabilities and upgrading to Ubuntu 20.04. A small team of 3 working on the project. Again this quarter no new functionality was added to Indy. The transition of the CI/CD from an older, undocumented Jenkins/manual process to a GHA-based CI/CD pipeline has been slow but seems to have turned a corner. The work on the CI/CD and OS Upgrade has prevented progress on new features – blocking most notably the upgrade to the new "did:indy" DID Method.

The "did:indy" method has a new repo ([https://github.com/hyperledger/indy-did-method](https://github.com/hyperledger/indy-did-method)) and the spec has been moved from a HackMD document to.a published [specification](https://hyperledger.github.io/indy-did-method/). The task backlog to implement the new DID Method is still to be created, and work will start once the CI/CD and Ubuntu upgrades are sufficiently stable.

Work has accelerated this quarter on the new client-side Indy library indy-vdr, with 3 tagged releases. More teams are deploying that code and contributing to the code base. Non indy-sdk or indy-shared-rs tags were created.

The interest in deploying instances of Indy continues to be strong, with lots of questions on Hyperledger Chat from people learning to run their own instances. There are no significant bugs that are pending action, and little demand for new functionality (beyond the "did:indy" method) from the user base. Indy "just works". 

Per the [Indy Activity Dashboard (2021-07 to 2021-09)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-07-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-09-30T07%3A00%3A00.000Z%22%7D), there were 72 commits from 14 contributors. which is up a little from the last quarter.

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: Steady progress, with GHAs implemented, the test automation process updated and the Ubuntu upgrade nearing completion.

### **Diversity of Contributor Community**

**Update**: Contributor community diversity remains a top of mind issue with the maintainers. The Hyperledger Staff (particularly [David Boswell](https://lf-hyperledger.atlassian.net/wiki/people/70121:0a14f738-3039-421f-a6a9-a83d19f23227?ref=confluence) and [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) – thanks!) working on getting an "Indy Contributors" course in place for early in 2022 in conjunction with the [ToIP Foundation](https://trustoverip.org). We have also had a number of new contributors joining Aries projects that have a reliance on Indy.  We expect that to result in a focus on the "did:indy" work that is needed. As noted, interest and contributions to indy-vdr have increased.

# Releases

- indy-did-method (first draft)
- indy-vdr 0.3.1, 0.3.2, 0.3.3

# Overall Activity in the Past Quarter

In the past quarter (as in the previous quarter), ledger code development focused on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04.  

There has been some progress on the new Indy DID Method, but not code. The work left at the end of the last two quarters remains (albeit now as a repo vs. HackMD doc): wrapping up the specification and defining the backlog of work for indy-node, indy-sdk and indy-vdr. With the CI/CD work blocking progress on indy-node, it's been difficult to convince contributors in the community to work on the DID Method if it is so hard to test and impossible to release.

# Current Plans

The push will be to complete the new CI/CD Indy Node and Plenum pipelines, the Ubuntu 20.04 upgrade, and tools to make it easier to do Indy Node development. In parallel, we expect coding to begin on the "did:indy" method.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. Topics and attendance has dropped recently, mostly because of the lack of topics other than "how is the CI/CD work coming along?"

# Contributor Diversity

Work has begun on putting together an "Indy Contributors" course for presentation in early 2022. The edX course about Indy, Aries and Ursa ([here](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)) was updated early in 2021 (this was missed in the last Quarterly report – even though the author of the quarterly report was the course creator...).

# Additional Information

- Key channels on Hyperledger Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Former user (Deleted)](https://lf-hyperledger.atlassian.net/wiki/people/712020:4f2bf4bc-35ef-43ea-bb8c-33564383f8ed?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [Kamlesh Nagware](https://lf-hyperledger.atlassian.net/wiki/people/5d258d2afd3b8b0c278eb1aa?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
