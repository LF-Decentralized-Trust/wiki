1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q4 Hyperledger Indy

Created by Stephen Curran, last modified by Jim Zhang on Dec 01, 2022

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

The road to a new pipeline and OS platform for Indy showed its promise while overcoming some dependency pain this quarter. In upgrading Indy to run on Ubuntu 20.04, we found a key piece of code that caused a pretty fundamental blockchain type issue was broken on the Ubuntu 20.04 Indy. A cryptographic signature was created and verified on across what amounted to an unordered array ![(sad)](images/icons/emoticons/sad.png). When the code was changed to newer versions of Python, the underlying array handling (C code) produced a different ordering for the array, and hence a different signature. Great work in the community by [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)and [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)resulted in a couple of iterations to a solution that all were happy with (including the signatures). The effort showed the power of the new CI/CD pipeline for indy-node, as where creating a new release artifact previously took weeks of effort (don't ask!), it is now just a couple of hours. This sped up the process and enabled substantially more testing to occur. Note that although the move right now is to Ubuntu 20.04, the pipeline makes all future updates to the OS platform and Indy itself MUCH easier.

A deployment hold up for production Indy instances in the community is because there are still CI/CD and Ubuntu upgrade work in the downstream implementations of Indy. The CI/CD issues in Indy were also in the Sovrin repos, and so the CI/CD work continues there.

The two vulnerabilities reported in the previous quarter where addressed by the community in all of the (known) test and production instances of Indy. An excellent concerted effort by the community in reporting, understanding, implementing and deploying in a timely fashion the fixes.

The migration of AnonCreds out of Indy and into its own higher-profile project will, we think, have a net positive impact on Indy. While a portion of the code for AnonCreds leaves the project, the anticipated expanded use of AnonCreds will result in a corresponding increase in the use of Indy as a publishing platform for AnonCreds objects. Note that as the migration of AnonCreds occurs, there is still the need for likely two AnonCreds Methods code instances within Indy repos – one for the legacy Indy identifiers, and another for did:indy identifiers. These are important for two reasons – the smooth transition of the new library structure for Aries Frameworks, and for the vast set of automated tests involving AnonCreds based on Indy instances.

The production CANdy Network, an instance of Indy for governments and broader public sector entities in Canada was launched this quarter. Interest in deploying instances of Indy continues to be strong, with lots of questions on Hyperledger Discord from people learning to run their own instances. 

Per the [Indy Activity Dashboard (2022-07 to 2022-09)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-07-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-09-30T07%3A00%3A00.000Z%22%7D), there were 56 commits from 12 contributors. both of which are down from last quarter. Knowing the importance of the work done this quarter around the vulnerabilities and the correcting of the dependency challenges in moving to Ubuntu 20.04 (described above), there is not a reason to be concerned about that number. ![(warning)](images/icons/emoticons/warning.png) *Checking to see if all Indy repos are accounted for in the Dashboard.*

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: The Ubuntu upgrade is complete, producing releases and compatibility with the Ubuntu 16.04 instance has been tested.

### **Diversity of Contributor Community**

**Update**: Little change this quarter in contributor community. Lots of interest, but the core maintainers continue to do most of the work.

# Releases

- indy-node (Ubuntu 16.04) – 1.12.5, 1.12.6
- indy-node (Ubuntu 20.04) – v1.13.2-rc3

# Overall Activity in the Past Quarter

In the past quarter (as in the previous quarter), ledger code development focused on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04. There was also much work done on testing of the new release, and addressing the identified vulnerabilities that were published during the quarter. Much was done on AnonCreds in Indy.

# Current Plans

With the new CI/CD Indy Node and Plenum pipelines complete, and the Ubuntu 20.04 indy-node upgrade available, the core maintainers are focused on their downstream releases.

The creation of the Hyperledger AnonCreds project means that the indy-shared-rs has been duplicated (new instance called "anoncreds-rs"), and the "cred-x" part of indy-shared-rs will be removed, while in the other repo, all but "cred-x" will be removed. Work to make those two repositories independent and aligned is a top priority in the Indy/Aries/AnonCreds community.

The community is starting the move towards deprecating the indy-sdk by enabling the use of indy-vdr, indy-shared-rs and aries-askar across all Aries Frameworks. There are a couple of tools still needed for that (a migration tool from indy-wallet to Aries Askar, and an Aries Askar/Indy VDR-based CLI for Indy) and it's overdue for that work to happen. Once that is done, documentation and getting started material will need to be updated.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on larger changes. Topics and attendance has increased recently, with more and more interested parties showing up, and new contributors weighing in on the conversations.

# Contributor Diversity

From the last report: The "Indy Contributors" course was presented in early 2022 and was extremely well received. The edX course about Indy, Aries, AnonCreds and Ursa ([here](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)) was updated recently with a new version scheduled to be out in late 2022.

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
