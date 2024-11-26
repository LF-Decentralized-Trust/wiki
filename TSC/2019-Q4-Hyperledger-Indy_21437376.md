1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q4 Hyperledger Indy

Created by Lynn Gray Bendixsen, last modified by Angelo de Caro on Nov 13, 2019

# Projects

##### **Distributed Ledger**

- I[ndy-node](https://github.com/hyperledger/indy-node)
- I[ndy-plenum](https://github.com/hyperledger/indy-plenum)

##### **Client Tool**

- I[ndy-sdk](https://github.com/hyperledger/indy-sdk)

##### **Shared Components**

- I[ndy-hipe](https://github.com/hyperledger/indy-hipe)
- [Indy-test-automation](https://github.com/hyperledger/indy-test-automation)

Project Health

Indy is a healthy project. Indy’s codebase has 23962 commits from 177 unique contributors. This represents an increase of 7 contributors this quarter and about 2,000 additional commits. We had commits from 41 different authors in the last three months. Forums and chat channels are monitored and a variety of participants are contributing helpful responses to questions.

# Questions/Issues for the TSC

We continue to track the same issues as in [previous quarters](2019-Q3-Hyperledger-Indy_21431404.html).

### Incompatible agent implementations

Update:

The launch of project Aries had the intended effect of focusing attention on standards for agent implementations. We will continue to support that effort as we migrate portions of Indy SDK into Aries core libraries. We will not be tracking this as an issue in our future quarterly reports.

### Measuring the size and make-up of our user community

Update:

We played a bit with tools for counting contributors, but no other significant progress.

Future work planned:

- We expect that the Indy contributor community will continue to shrink as much of the attention shifts to Aries.
- Work with Hyperledger to get analytics about web sites, and Rocket Chat usage.
- Begin measuring usage of the Sovrin forums: new contributors, questions asked, and questions answered
- We will also explore the use of Github's contributor tool.

### Build Issues

Update:

Our transition to the GitLab CI build pipeline managed by the Sovrin Foundation is going slower than expected. The Indy SDK pipeline is complex, and GitLab's integration with GitHub is not yet mature. We have found credible solutions to the problems we have seen, but the project has not had sufficient developer focus to come to completion. We are still relying on the Jenkins instance managed by the Sovrin Foundation for our production CI / CD pipeline.

Future work planned:

- We need a new commitment from the various teams who have expressed interest.

# Releases

**August 2019:**

##### **Indy SDK 1.11.0**

- Enhancements and bugfixes added for TAA and Endorser txns
- Updated Indy-SDK CI/CD pipelines to test, to build and to publish Android artifacts for Libvcx.
- Improved state proof verification to support pagination.
- Bugfixes

##### **Indy SDK 1.11.1**

- Supported endorsing of transactions in Indy-CLI and Libvcx.
- Added new functions to Anoncreds API to rotate credential definition.
- Added sign/verify with payment address functions to Libvcx.
- Supported state proof verification for GET\_TXN request.
- Extended config parameter of indy\_open\_pool\_ledger function.
- Extended Libvcx initialization config to accept pool configuration.
- Supported new platforms Ubuntu 18.04 and Centos:
- Bugfixes

##### **Indy Node 1.9.1**

- New DIDs can be created without endorsers
- Transaction authors don't need to be endorsers
- TAA acceptance should use date, not time
- Bug fixes

##### **Indy Node 1.9.2**

- Stability fixes
- Endorser support fixes and improvements
- Improving GET\_TXN to be able to query just one node the same way as for other GET requests

### **September 2019:**

- No Releases

### **October 2019:**

##### **Indy SDK 1.12.0**

- Minimal *EXPERIMENTAL* support of Fully-Qualified identifiers:
  
  - omit or set "1.0" to use unqualified identifiers.
  - set "2.0" to use fully qualified identifiers.
  
  <!--THE END-->
  
  - added correspondent did qualify command to Indy-CLI.
  
  <!--THE END-->
- - general format of fully-qualified identifier is &lt;prefix&gt;:&lt;method&gt;:&lt;value&gt;.
  - extended did\_info parameter of indy\_create\_and\_store\_my\_did function to accepts optional method\_name filed. This field should be used to create fully qualified DID.
  - all functions can work with fully-qualified identifiers (new way) as well as with unqualified.
  - added a new function -- indy\_to\_unqualified -- that gets unqualified form of a fully qualified identifier.
  - proof requests now support versioning (ver field) -- now it specifies whether restrictions are full qualified or not.
  - The same format of identifiers will be used in generated proof and must be used for proof verification.
  - added a new function -- indy\_qualify\_did -- that updates DID stored in the wallet to make it fully qualified, or to do other DID maintenance.
  - all functions in Ledger API can accept fully-qualified identifiers but always return results in an unqualified form.
  - extended VCX provisioning config to accept optional did\_method filed. This field should be used to create fully qualified DIDs.
- Migrated Android onto the API v21 and NDK 20.
- Supported MacOS builds for Indy CLI.
- The default value of Protocol Version was changed on 2. Henceforth indy\_set\_protocol\_version function should be called if you are going to work with Indy-Node 1.3 and less.
- Bugfixes

##### **Indy Node 1.10.0**

- PBFT View Change implementation (not enabled yet) and corresponding code improvements
- BLS multi-signature fixes and improvements
- The latest version of ZMQ library support
- Stability fixes

# Overall Activity in the Past Quarter

Key activity over the past quarter:

- Migrating large parts of indy-agent, indy-hipe and indy-sdk to Aries, including infrastructure such as Jira issues.
- Improving the ledger to make it more stable, performant, provably correct, and easy to maintain. We made a lot of progress and are really pleased with Plenum.

Our contributor community collaborates a lot on Jira issues, in pull requests, using Rocket Chat, and in weekly meetings. But we don't use the mailing list very much. We do not have clear analytics, but the majority of questions appear to receive answers within a few days.

# Current Plans

- We are increasingly pushing contributors who want to add new features to the Indy SDK to focus instead on the Aries libraries. This impacts the language wrappers the most.
- However, we are continuing to maintain Indy SDK and wrappers for existing users to allow them a smooth transition, including adding compatibility for Aries protocols to LibVCX.
- The next round of ledger work will remove the RBFT replicas, instead implementing Aardvark BFT. This addresses a number of issues we see with replicas, and should significant improve performance and scalability giving us headroom in the adoption of production Indy networks for some time to come.
- Other initiatives include improving CI / CD (as described above), adding support for W3C DID and Verifiable Credential primitives, and adopting the new approach to revocation provided by Ursa's anoncreds 2.

# Maintainer Diversity

The weekly Indy Maintainers call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. In the past quarter, the teams at the Sovrin Foundation and at Kiva have been much more involved in maintaining Indy. There is a proposal to start cross-organizational reviews of pull requests in order to increase knowledge sharing, but we don't yet have commitments from sufficient organizations.

# Contributor Diversity

Fewer people work on Indy now that many contributors focus instead on Ursa and Aries. Evernym still sponsors the majority of development, but the developers at the Sovrin Foundation are confident in the code base. Developers from the government of British Columbia, Deutsche Telekom, and Kiva are increasingly familiar with the code base on a deep level.

**POCs, Pilots, Projects**

There are now too many Indy projects to list them all here. Recent public disclosures include:

- [Onfido](https://sovrin.org/use-case-spotlight-onfido-to-provide-self-sovereign-identity-verification-services/) and [UK FinTech ecosystem](https://www.evernym.com/blog/teaming-up-with-b-social-curve-monese-and-seedrs-to-test-decentralized-identity/)
- [esatus](https://sovrin.org/use-case-spotlight-enterprise-identity-access-with-esatus-self/)
- [CULedger and Desert Financial](https://www.cubroadcast.com/episodes/corelation-forum-interviews-desert-financials-amstutz-and-culedgers-ainsworth-leverage-blockchain-for-cus)
- [Farmer Connect](https://farmerconnect.com/2019/09/18/farmer-connect-sa-announces-blockchain-collaboration/)

# Additional Information

- Key channels on Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
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
