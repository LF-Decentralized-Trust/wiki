1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Aries

Created by Stephen Curran, last modified by Angelo de Caro on Dec 09, 2021

Project

Hyperledger Aries

Project Health

Hyperledger Aries continues to garner a lot of activity from contributors and a lot of interest from those wanting to use Aries in various use cases. It has an extremely diverse and global community. There were significant milestones accomplished within Aries this past quarter, including the approval by the community of the Aries Interop Profile (AIP) 2.0, which extends the AIP 1.0 from 2020 to achieve Aries stated goal of being both ledger and verifiable credential format agnostic.

The new capabilities that are included in AIP 2.0 have been added to some of the Aries frameworks, allowing for opportunities to interoperate with products and tools from other verifiable credential ecosystems. A collaborative effort (called WACI-PEx) started at the Internet Identity Workshop is bringing together teams from the W3C, DIF and Hyperledger Aries communities.

# Questions/Issues for the TSC

None.

# Releases

The following releases occurred in the last quarter:

- Aries Interop Profile 2.0
- Aries Cloud Agent Python Release 0.7.0 (early July)
  
  - Major release adding support for W3C Standard BBS+ verifiable credentials, DIF Presentation Exchange, a pluggable DID Resolver, Indy Endorser handling
  - Adds support for running the new "shared components" (indy-vdr, indy-shared-rs and aries-askar), allowing operation without the Indy SDK.
- Aries Framework JavaScript – many regular "unstable" releases that are leading up to the 0.1.0 release
  
  - Now used as the basis for the new Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native)](https://github.com/hyperledger/aries-mobile-agent-react-native%29) open source wallet.
- Aries Askar 0.2.0, 0.2.1 (early July)
- Aries VCX Releases 0.17.0, 0.18.0, 0.19.0
- Aries Mobile Agent Xamarin (Aries-MAX) 0.1.0
  
  - Lots of activity on this open source wallet.

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). Aries Agent Test Harness extended to support testing W3C Standard Verifiable Credentials and DIF Presentation Exchange. In addition, work is underway for adding test agents based on three other frameworks, expanding the community of products that are verified to be interoperable.

The Hyperledger Labs "[Business Partner Agent](https://github.com/hyperledger-labs/business-partner-agent)" project is an application that is built on Aries (ACA-Py) that is extremely active and interesting. It forsees a future where organizations run Aries agents that allow for the secure interchange of authentic data between business partners – supply chain participants, customers, suppliers, etc. This includes a company sharing basic, public information (as verifiable credentials) about itself for all those that are interested. Instead of relying on Google-ing for information about a company, ask it and get back verifiable credentials; authentic data.

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-04-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-06-30T07%3A00%3A00.000Z%22%7D) for the first quarter of 2021, Aries codebases had 871 commits (up substantially from last quarter) from 49 contributors.

Community participation is extremely active in rocketchat channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

Coordination with the DIF DIDComm working group is healthy, with regular reports being shared.

Project work in main repos is healthy and active.

# Current Plans

- Most Aries teams are focused on adding the core capabilities of AIP 2.0 to their code bases.
- Work is active to extend Aries beyond support just Indy ledgers and Indy AnonCred verifiable credentials to supporting other ledgers and other verifiable credential formats – most notably BBS+ signatures, supporting ZKPs and selective disclosure.
  
  - ACA-Py and AF-Go have working code
- The Aries Mobile Agent React Native (aka Bifold) built on Aries Framework JavaScript has been extremely active is becoming the open source wallet a larger community rallied behind.
  
  - Aries Framework JavaScript is nearing AIP 1.0-complete, and once there, will quickly move on to replicating the AIP 2.0 features already part of other frameworks, especially support for W3C Standard BBS+ Verifiable Credentials.
- Interoperability testing continues to be a key focus.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration is increasing. For example, work is happening on interop testing capabilities across the Python, Go, .NET, Rust and JavaScript frameworks, with two developers of proprietary Aries implementations joining in as well.

As interest in verifiable credentials has increased with COVID-19 use cases (proof of testing, proof of immunization and mobile medical workforces), interest and attendance has increased, as have deployments of Aries-based implementations.

# Contributor Diversity

In addition to the code contribution statistics (above), here are a few indicators of our current diversity:

- We hold two community calls on Wednesdays: weekly at noon Pacific to cover US and Pacific contributors, and biweekly at 7am Pacific to cover US and European contributors.
- Call attendance for each is typically in the 15-20 range.
- Most organizations have only one attendee; it is rare for more than 3 to attend from the same organization.
- Cross codebase interoperability efforts indicate cross-organization cooperation.

# Additional Information

Related activity to Aries is occurring in [DIF](https://identity.foundation/) (Decentralized Identity Foundation), the [Trust over IP Foundation](https://trustoverip.org/), and especially in their [Good Health Pass](https://wiki.trustoverip.org/pages/viewpage.action?pageId=73790) initiative, and in [Linux Foundation Public Health](https://www.lfph.io/) (LFPH).

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Former user (Deleted)](https://lf-hyperledger.atlassian.net/wiki/people/712020:4f2bf4bc-35ef-43ea-bb8c-33564383f8ed?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:62746046-52ae-43bb-827b-6dfdde9f07d7?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
