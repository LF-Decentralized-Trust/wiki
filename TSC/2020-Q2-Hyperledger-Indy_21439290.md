1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q2 Hyperledger Indy

Created by Lynn Gray Bendixsen, last modified by Gari Singh on Jun 11, 2020

# Projects

##### **Distributed Ledger**

- [indy-node](https://github.com/hyperledger/indy-node)
- i[ndy-plenum](https://github.com/hyperledger/indy-plenum)

##### **Client Tool**

- i[ndy-sdk](https://github.com/hyperledger/indy-sdk)
- [indy-vdr](https://github.com/hyperledger/indy-vdr)
- [indy-credx](https://github.com/andrewwhitehead/indy-credx) (to be transitioned to Hyperledger)
- [indy-shared-rs](https://github.com/andrewwhitehead/indy-shared-rs) (to be transitioned to Hyperledger)

##### **Shared Components**

- I[ndy-hipe](https://github.com/hyperledger/indy-hipe)
- [Indy-test-automation](https://github.com/hyperledger/indy-test-automation)

# Project Health

Indy is a healthy project. Indy’s codebase has 26582 commits from 189 unique contributors. This represents an increase of 7 contributors this quarter and about 696 additional commits. Forums and chat channels are monitored and a variety of participants are contributing helpful responses to questions.

A recent focus has been on breaking up the single indy-sdk client tool into separate components:

- indy-vdr for ledger interactions
- indy-credx for anonymous verifiable credential exchange
- indy-shared-rs for shared client tool utilities

These new libraries provide an easier, more modular integration for Aries Agents (the primary consumers of indy client artifacts) and are more accessible for developers wanting to contribute to the project and use the artifacts of the project. Work has started on an Aries Secure Storage repository that on completion will enable the depreciation of the indy-sdk in favour of these new components.

Work has also begun on the number one request from the Indy community—a “jurisdiction-scale” verifiable credential revocation mechanism.

As well, a plan has been formulated (but not yet executed) for migrating the Indy (especially the indy-sdk) CI/CD pipelines from their current Jenkins-basis to GitHub Actions.

# Questions/Issues for the TSC

We continue to track some of the same issues as in [previous quarters](https://lf-hyperledger.atlassian.net/wiki/display/HYP/2019+Q4+Hyperledger+Indy).

### **Measuring the size and make-up of our user community**

Update:

Modest progress with this effort in the past quarter.

- Moved from JIRA to GitHub Issues for issue tracking, making easier to measure the size of the community engagement.

Future work planned:

- Work with Hyperledger to get analytics about web sites, and Rocket Chat usage.
- Generate standardized statistics on GitHub Issue tracking.

### **Build Issues**

Update:

A [plan](https://lf-hyperledger.atlassian.net/wiki/display/CICD/Sovrin+resource+migration) was formulated for transitioning from the current Jenkins-based pipeline to GitHub Actions with the option of tactical deployment of Azure Pipelines.  The necessity to get off of Jenkins has increased because of the current reliance on Sovrin Foundation’s AWS resources that are at risk because of the financial status of the Foundation. Resources from BC Gov have been identified for the first part of the work, but it’s not their highest priority, and little progress has been made to date. Access to resources from other teams have decreased for the next few months because of COVID-19 related projects.

Future work planned:

- Getting resources for the project that can make it their highest priority.

### **Diversity of Contributor Community**

Update:

As agent implementers have moved to the Aries project, Indy was left with few contributors to the ledger, mostly from a single organization. The health of the project requires broadening this list. Progress on that goal was made this quarter as many of the contributions have come in from new core developers and project leads from other organizations (notably, BC Gov, Kiva and Mattr Global).  The transition off of Jira and onto GitHub Issues was a step in trying to expand contributions by making it easier to see where contributions would be welcomed.  The first GitHub issues raised have attracted some attention, so initial feedback on the change is positive.

Future work planned:

- Current initiatives are being led by different organizations, which we hope will become consistent contributors in the future.

# Releases

**February 2020:**

##### None

### **March 2020:**

##### **Indy SDK 1.14.3**

- LibVCX:
- - Removed connection\_handle from functions to get protocol messages.
  - Added ability to accept a duplicate connection by redirecting to the already existing one instead of forming a duplicate connection.
  - Added a new function vcx\_disclosed\_proof\_decline\_presentation\_request to explicitly reject a presentation request.
  - Added a new function vcx\_connection\_info to get information about connection.
- Bugfixes
- - Fix proof verification in case of credential attribute encoded value contains leading zeros (IS-1491).
  - Fix artifacts at [repo.sovrin.org](http://repo.sovrin.org) for Ubuntu 18.04
  - others minor bugfixes

##### **Indy SDK 1.15.0**

- Correction for Fix proof verification in case of credential attribute encoded value contains leading zeros (IS-1491). Indy 1.14.3 changes "0" to "" which leads to proof rejection.
- LibVCX: Supported protocol\_version: 3.0 which actually is an alternative to combination of settings: protocol\_version: 2.0 and communication\_method: aries.
- LibVCX: Fixed compatibility between proprietary (protocol\_version: 2.0/1.0) and aries communication protocols (protocol\_version: 3.0).
- Bugfixes

### **April 2020:**

##### **None**

# Overall Activity in the Past Quarter

In the past quarter, efforts have been largely focused on creating replacement components for the indy-sdk, enabling its depreciation of favour of several separate components. Verifiable Credential Revocation 2.0 work has started, building on the cryptography built into Ursa. A preliminary design has been defined and tech spikes started to evaluate the feasibility of that plan. Plans for migrating from Jenkins to GitHub Actions-based CI/CD have been formulated but not executed.

# Current Plans

Revocation, continued working on breaking up the indy-sdk, and the migration of CI/CD pipelines will be the primary focus of efforts this quarter. Most of the work will have to be done with limited input from the previous core team (who are busy on other projects in the space), which will be an interesting experiment. That said, Indy is very stable right now, and there is not a pressing need from the community for a lot more than is being planned.

# Maintainer Diversity

The bi-weekly Indy Maintainers call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. A recent increase in the number of participants on the call has been encouraging, although that has yet to translate into more commits from outside developers.

# Contributor Diversity

COVID-19 efforts have restricted Evernym from being able to contribute significantly to the code base in recent weeks and that is anticipated to go on for the next few months. The Sovrin Foundation was forced to let go of their paid staff (including Indy contributors) and is operating on a volunteer basis.  While that has slowed down efforts on the project, the current highest priority items (mentioned earlier - revocation, the break-up of the indy-sdk and the CI/CD migration) continue to move forward through the efforts of other contributors and key guidance from the Evernym team.

# Additional Information

- Key channels on Hyperledger Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

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
