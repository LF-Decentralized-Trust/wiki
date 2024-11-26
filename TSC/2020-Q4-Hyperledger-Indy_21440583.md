1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Indy

Created by Stephen Curran, last modified by David Enyeart on Nov 19, 2020

# Projects

##### **Distributed Ledger**

- [indy-node](https://github.com/hyperledger/indy-node)
- [indy-plenum](https://github.com/hyperledger/indy-plenum)

##### **Client Tool**

- [indy-sdk](https://github.com/hyperledger/indy-sdk)
- [indy-vdr](https://github.com/hyperledger/indy-vdr)

##### **Shared Components**

- [indy-hipe](https://github.com/hyperledger/indy-hipe)
- [indy-test-automation](https://github.com/hyperledger/indy-test-automation)
- [indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)

Project Health

Indy is a healthy project, particularly at the deployments and business interest level, but has a current lack of contributors.  The maintainers are working to address that issue.

Per the [Indy Activity Dashboard](https://lfanalytics.io/projects/hyperledger%2Findy/dashboard), Indy’s codebase has 22,520 commits from 241 unique contributors (up from 238 last report). This quarter there were 70 commits from 14 contributors, up from 8 in the previous report.

This quarter the [Indy Interop-athon](https://lf-hyperledger.atlassian.net/wiki/spaces/II) was held that attracted more than a 100 attendees to a two-day virtual conference about the future of Indy, and notably about creating interoperability between independent deployments of Indy. At this time there are at least 6 independent implementations of Indy in production (Sovrin Foundation), test (Indicio, IDUnion) or planning (Bedrock, CanCred and FIndy).

# Questions/Issues for the TSC

## Issues from previous reports:

### Incompatible agent implementations

**Update**: This is progressing well and is really being dealt with at the Aries level.  Closing this issue from an Indy perspective.

### Measuring the size and make-up of our user community

**Update**: The work of Ry Jones on the Indy Activity Dashboard has resolved this issue. Closing.

### Build Pipelines

**Update**: Progress is being made on converting the CI/CD pipeline from Jenkins to GitHub Actions, particularly for indy-node.

We had one minor release of indy-node in the last quarter. We are currently preparing another release of indy-node that is largely focused on the CI/CD pipelines to integrate and deliver the release, transforming those pipelines from Jenkins (circa 2018) to GitHub Actions. We have a small team that have agreed to do that with the guidance of the early Indy developers from Evernym.

### **Diversity of Contributor Community**

Update: Progress was made with the Indy Interop-athon Conference attracting a large audience that demonstrated there is strong interest in the conference. Attendance at the regular Indy Contributors call has been good, and work has (slowly) been starting.  A number of groups (BC Gov, Sovrin) are looking at ways to create opportunities for contributions, such as bringing together groups to fund capabilities. 

There two additional efforts in the community that will add contributors – a specification effort related to a W3C standard DID Method for Indy ("did:indy") to enable cross-deployment interoperability, and changes to indy-node to support the new DID Method.

# Releases

### **August 2020:**

##### Indy Node 1.12.4

- A response to an identified security vulnerability that if exploited could allow unauthorized updates to meta-data about DIDs published on the ledger.

# Overall Activity in the Past Quarter

In the past quarter, ledger development has slowed as we focus on upgrading the CI/CD pipeline and defining the Indy DID Method. Some work has occurred in the indy-sdk and release planning has begun for that, with resources committed to the work. In doing the indy-sdk release, we'll work on (at least) documenting the process to enable modernizing the CI/CD pipeline for the project.

# Current Plans

There is little ledger activity occurring, so the current plans have not evolved significantly from the last report.

We've added a focus on interoperability across Indy deployments using the Indy DID Method as the driver for that work.

Previous work on "rich schemas" to support W3C VCs has been put on hold and will likely be replaced with a focus on BBS+ ZKPs, which likely has the benefit of eliminating (well, deprecating) features from Indy vs. adding.

Our focus for client libraries is to break LibIndy into separate components that can be evolved to fit the proposed Aries architecture. Isolated progress has been made on that effort, but the work is not had a large audience as yet.  We hope that will occur this quarter.

Work on an improved revocation has progressed slowly, delayed within the Ursa community.

# Maintainer Diversity

The weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. Interest in and attendence at the Indy Contributors meetings are rising.

# Contributor Diversity

We've had several organizations join the Indy Contributors call and some are doing the work on the upcoming release (code changes) and the CI/CD pipeline.

# Additional Information

- Key channels on Hyperledger Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

# Reviewed by

- Angelo De Caro
- Arnaud J Le Hors
- Arun S M
- Baohua Yang
- Bobbi Muscara
- Dave Enyeart
- Gari Singh
- Grace Hartley
- Danno Ferrin
- Hart Montgomery
- Mark Wagner
- María Teresa Nieto
- Nathan George
- Tracy Kuhrt
- Troy Ronda

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
