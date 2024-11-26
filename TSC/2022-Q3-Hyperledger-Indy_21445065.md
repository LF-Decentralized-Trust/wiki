1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Indy

Created by Stephen Curran, last modified by Tracy Kuhrt on Aug 29, 2022

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
- [indy-node-container](https://github.com/hyperledger/indy-node-container)

Project Health

This quarter we achieved a quality Ubuntu 20.04-based Hyperledger Indy release candidate – a big milestone. The Release Candidate includes both Indy Plenum and Indy Node, each of which were built, tested and published using a modern, automated CI/CD pipeline. The maintainers are working on the downstream plugins to enable deployment on existing networks. Several new networks that are starting up have been deployed using the new release candidates. This release is also the hold up for the deployment of \`did:indy\`.

The community worked a lot this quarter on a couple of reported vulnerabilities (CVEs). Both can be addressed in the current (pre-Ubuntu 20.04) and later versions, and fixes have been created. One is a documentation advisory for configuring Indy nodes. It is still being finalized, but is close to completion. The second is a new release of Indy that is now available and ready for all "pure Indy" deployments. Downstream releases are in process. The pain of producing this (hopefully) final Ubuntu 16.04-based release demonstrates why the need for the modern CI/CD pipeline is so desperately needed.

Much progress has been made this quarter in defining AnonCreds ZKP-based verifiable credentials (which started life in Indy) as an open standard (see the [spec](https://anoncreds-wg.github.io/anoncreds-spec/) being created). Much progress has been made recently in making AnonCreds ledger agnostic, meaning that it is not dependent on Hyperledger Indy, but can be supported by other ledgers and mechanisms. That change will reduce the resistance to the use of AnonCreds by those thinking it is "proprietary", but should also help Indy, as it is the easiest way to deploy the capability.

The interest in deploying instances of Indy continues to be strong, with lots of questions on Hyperledger Chat from people learning to run their own instances.

Per the [Indy Activity Dashboard (2022-04 to 2022-06)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-04-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-06-30T07%3A00%3A00.000Z%22%7D), there were 133 commits from 16 contributors. both of which are about the same as last quarter. However, that does not count the CVE repos that are still private until the vulnerabilities have been deployed in production instances.

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: The Ubuntu upgrade is complete and producing releases – including a release candidate. Awaiting final testing and downstream artifacts to be tested before declaring the release ready.

### **Diversity of Contributor Community**

**Update**: Little change this quarter in contributor community. Lots of interest, but the core maintainers continue to do most of the work.

# Releases

- indy-plenum (Ubuntu 16.04) – CVE release
- indy-plenum (Ubuntu 16.04) – v1.13.2-rc2
- indy-node (Ubuntu 16.04) – CVE release
- indy-node (Ubuntu 16.04) – v1.13.1-rc0, v1.13.2-rc2

# Overall Activity in the Past Quarter

In the past quarter (as in the previous quarter), ledger code development focused on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04. 

# Current Plans

With the new CI/CD Indy Node and Plenum pipelines complete, and the Ubuntu 20.04 upgrade available, the core maintainers are focused on their downstream releases.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. Topics and attendance has increased recently, with more and more interested parties showing up, and new contributors weighing in on the conversations.

# Contributor Diversity

From the last report: The "Indy Contributors" course was presented in early 2022 and was extremely well received. The edX course about Indy, Aries and Ursa ([here](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)) was updated early in 2021 (this was missed in the last Quarterly report – even though the author of the quarterly report was the course creator...).

# Additional Information

- Key channels on Hyperledger Discord: #indy, #indy-sdk, #indy-node, #indy-maintainers
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
