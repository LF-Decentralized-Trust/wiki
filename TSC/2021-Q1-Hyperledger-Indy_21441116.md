1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Indy

Created by Stephen Curran, last modified by Gari Singh on Mar 17, 2021

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

Indy is a healthy project, particularly at the deployments and business interest level, but continues to be short on contributors.  Interest has increased in the quarter, with more contributors on the specific initiatives of the team, and a lot more participation as the bi-weekly the Contributors meeting. The current work focuses on modernizing the CI/CD process to use GitHub Actions (and eliminate reliance on specific people and infrastructure) for indy-node, indy-plenum and indy-sdk, and upgrading the dependencies for indy-node artifacts to run on Ubuntu 20.04. Coming soon will be a code-focused effort to add support for the new "did:indy" DID Method that will align Indy with the pending W3C DID Core Specification.

A new repository was added to indy, contributed by the Government of British Columbia – indy-shared-rs – which is a client library that provides in Rust a set of utilities for interacting with an Indy ledger. It is part of the process of breaking up the indy-sdk.

Per the [Indy Activity Dashboard (2020-11 to 2021-01)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard?time=%7B%22from%22%3A%222020-11-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-01-31T08%3A00%3A00.000Z%22%7D), there were 52 commits from 15 contributors. which is in line with the last quarter. I don't think those statistics include the indy-shared-rs library.

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: Good progress is being made on converting the CI/CD pipelines from Jenkins to GitHub Actions, for indy-node, indy-plenum and indy-sdk. This has been the focus of the community during this period as without this, the ability to release products is extremely limited.

### **Diversity of Contributor Community**

**Update**: This remains a top of mind issue with the maintainers.  On the last Indy Contributors call, we are considering a "Contributor Campaign" in conjunction with Hyperledger Staff to build attention to both Indy and the new "did:indy" DID Method.

# Releases

### None.

# Overall Activity in the Past Quarter

In the past quarter, ledger code development has slowed as we focus on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04.  The main code related activity was done by a team focused on being able to remove ledger plugins from a running instance of Indy.

Work continues on defining the Indy DID Method, with some good progress being made.  We're nearing completion of that work – and nearing a need for some new ledger code development efforts, particularly in Indy Node.

A release of the Indy SDK has been prepared and will be released shortly. As well, the Indy SDK CI/CD pipelines have been migrated to GitHub Actions and the existing pipelines will soon be retired.  As well, the Verifiable Credential Exchange (VCX) component of the Indy SDK has been pulled from the Indy SDK and moved to it's own repo in Aries. The code was focused on Aries protocols, and so the move makes a lot of sense.  This continues to the trend towards Indy just being a ledger for decentralized identity and the Trust over IP stack vs. covering the Agent and above layers of the stack.

As noted above, a new component, indy-shared-rs was contributed to better support agents that want to interact with Indy ledgers without depending on the entire Indy SDK.

# Current Plans

The push will continue this quarter to complete the new CI/CD Indy Node and Plenum pipelines, and the Ubuntu 20.04 upgrade. In parallel, we'll try to wrap up the "did:indy" DID Method specification and generate a backlog of work to be added to Indy Node.  We anticipate that next quarter, with the ability to easily release code, addressing the DID Method backlog will be the focus.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. The core maintainers are in close contact, and the new maintainers are gaining experience and confidence with the components.

# Contributor Diversity

We've had several organizations join the Indy Contributors call and some are doing the work on the upcoming release (code changes) and the CI/CD pipeline. Interest in Indy has been rising because of the demand for verifiable credentials related to the various COVID-19 use cases, such as travel and back to work plans.

# Additional Information

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
