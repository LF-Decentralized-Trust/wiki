1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q2 Hyperledger FireFly

Created by Ray Chen, last modified by Jim Zhang on Aug 25, 2022

Project Health

We achieved a significant milestone this quarter with the release of Hyperledger FireFly 1.0.  In case you missed it, check out the [launch blog](https://www.hyperledger.org/hyperledger-firefly/2022/04/13/introducing-hyperledger-firefly-1-0-the-supernode-for-enterprise-web3-applications).  Here is a quick recap of the 1.0 stack from the launch webinar:

The FireFly SuperNode: a complete stack for enterprises to build and scale secure Web3 applications. 

![](attachments/21444743/21456277.png?height=250)

The 1.0 release includes a rich set of functionality that is hardened for production use and represents a major step in the development of the complete FireFly stack:

- **FireFly Core -** Support for multiple protocols across public and private chains with a powerful orchestration engine backed by a scalable event bus. Manage private data, on-chain data, and shared storage. Track state across networks, chains, and internal back office systems.
- **Apps** - Accelerate development with tools that make building on Web3 familiar to any Web2 developer, including an API Gateway, Event Streams, and the Smart Contract API Generator.
- **Flows** - Coordinate how data, value, and processes flow both on-chain and off-chain in decentralized networks, while maintaining privacy and security.
- **Digital Assets** - Manage tokens at institutional scale with APIs that simplify the creation, transfer, and tracking of fungible and non-fungible tokens. Simplify custody with robust wallet and key management integration capabilities.
- **Tools** - Monitor transactions, messages, and events in the FireFly Explorer. Test out key FireFly functionality and generate example code snippets in the FireFly Sandbox. Run apps with a rich set of DevOps tools on modern, scalable cloud architecture.

We hosted 2 webinars and 3 meetups on Hyperledger FireFly that had over 1,000 registrants and generated over 14,500 views on their recordings.  

We've also seen an uptick in new community members this quarter participating in discussions in Discord with 71 people versus 23 the previous quarter.

Contributors are very active in the project and in the month of May, excluding merges, we’ve had 8 authors push 144 commits to main.

There are currently 370K lines of code for Hyperledger FireFly across 11 repositories, with a total of 4.6K commits to date.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo. Yes
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? No
   

# Questions/Issues for the TSC

No questions for the TSC

# Releases

April:

[FireFly 1.0](https://github.com/hyperledger/firefly/releases/tag/v1.0.0)

May:

[FireFly 1.](https://github.com/hyperledger/firefly/releases/tag/v1.0.1)[0.1](https://github.com/hyperledger/firefly/releases/tag/v1.0.1)

[FireFly 1.](https://github.com/hyperledger/firefly/releases/tag/v1.0.2)[0.2](https://github.com/hyperledger/firefly/releases/tag/v1.0.2)

The full list of releases can be found at: [https://github.com/hyperledger/firefly/releases](https://github.com/hyperledger/firefly/releases)

# Overall Activity in the Past Quarter

The Discord is very active and project maintainers answer questions regularly. Some metrics for the last 90 days of activity.

**Dimension**

**Link to Insights**

PR Activities

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=pull-request-management%2Fgithub-pr%2Foverview](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=pull-request-management%2Fgithub-pr%2Foverview)

Contributor Strength

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;quicktime=time\_filter\_3M](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;quicktime=time_filter_3M)

Commit Activities

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=source-control%2Fcommits%2Foverview](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=source-control%2Fcommits%2Foverview)

# Current Plans

- Active: Enhanced connector framework structure
- - active development on new public chain connectors for Ethereum and Bitcoin

<!--THE END-->

- Active: Namespace isolation
- - Allows single FireFly SuperNode to talk to multiple blockchains
  - Major step towards multi-tenancy support
- Active: New operation modes for Gateway and Consortium
- - Explicit multi-chain support
- Active: Revamped docs site
- - Major updates throughout for v1.0
  - Top level version toggle
  - Multi-language support starting with Chinese
  - Automated API and object reference sections
- Queued: Enhanced API Security model

Please see the GitHub project board for our most updated plans: [https://github.com/orgs/hyperledger/projects/4/views/7](https://github.com/orgs/hyperledger/projects/4/views/7)

# Maintainer Diversity

No new maintainers in this quarter.

# Contributor Diversity

Contributions in Q2 including code, documentation, or other contributions:

Active contributors from Kaleido: 10

Active contributors from other organizations: 1 (Built Technologies)

# Additional Information

Various enterprises are already using FireFly for their business products and live deployments. 

These include the following:

**Riskstream** - The largest enterprise-level blockchain consortium in risk management and insurance uses Hyperledger FireFly for First Notice of Loss (FNOL) data sharing between companies, Mortality Monitor which offers a single source of digital decedent information required to process life insurance claims, Surety Bond Verification for Power of Attorney, and Licensing and Appointments micro credentialing.

**Synaptic Health Alliance** - A coalition of US healthcare leaders leveraged Hyperledger FireFly to create a blockchain-based decentralized Provider Data Directory. This directory tackles the challenge of providing access to care via accurate provider data.

**TradeGo** - A global commodity trading consortium that uses Hyperledger FireFly to get its Digital Presentation product to production much quicker and lower cost than initially expected. Digital Presentation enables highly efficient and transparent sharing of original, confidential trade documents in a digital format. 

**AscendBit** - AscendBit is a company owned by CP Group that is using Hyperledger FireFly to launch initiatives in Supply Chain as well as its own company coin.

The leaders of the Riskstream and Synaptic consortiums spoke at our FireFly [launch](https://www.youtube.com/watch?v=j3IXHE-vyNI) and the CEO of TradeGo and CTO of AscendBit recently spoke at our FireFly 1.0 AP [webinar](https://www.youtube.com/watch?v=Yw6SRWCULMg&t=325s).

Technical metrics from March 15, 2022 to June 15, 2022 may be found [here](https://tinyurl.com/25v49uzt)

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

## Attachments:

![](images/icons/bullet_blue.gif) [FireFly Diagram.png](attachments/21444743/21456277.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
