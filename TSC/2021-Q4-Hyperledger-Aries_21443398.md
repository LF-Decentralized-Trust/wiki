1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Aries

Created by Stephen Curran, last modified by Angelo de Caro on Dec 09, 2021

Project

Hyperledger Aries

Project Health

Hyperledger Aries continues increase quarter-on-quarter, in terms of activity by contributors and in the interest from those wanting to use Aries in various use cases. It has an extremely diverse and global community. In addition to the steady progress made in all the sub-projects, a number of significant events occurred in the project including:

- Substantial progress on Aries Framework JavaScript and its capability as the foundation of an Bifold, and Aries React Native mobile wallet.
- An "Aries Mobile Summit" is planned this month (organized by the Aries Working Group) to increase mobile and web wallet delivery velocity.
- Substantial progress on the Aries VCX framework, a Rust-based framework suitable for use in a number of server-side and mobile use cases.
- The addition of a new non-Hyperledger, but still complete open source implementation of the Aries Interop Profile RFCs by the FIndy (Finland) project.
- Three new frameworks (including Aries VCX and Findy) added to the [Aries Agent Test Harness](https://aries-interop.info/), and a significant increase in the number of passing tests across all frameworks. The Test Harness has become the go to way to achieve and prove interoperability.
- Aries Interop v2.0 implementations in Aries Framework Go and Aries Cloud Agent Python, including passing Aries Agent Test Harness test cases using most AIP 2.0 protocols, including exchanging W3C Standard Verifiable Credentials.

There is probably a more to talk about in terms of delivered, verified code, let alone the increases in participation and use of Aries.

Another highlight in the community – Aries contributing to solutions for Climate Change.  The Hyperledger Labs "[Business Partner Agent](https://github.com/hyperledger-labs/business-partner-agent)" project continues to be an exemplar application built on Aries (ACA-Py). As mentioned in the last quarterly report, BPA forsees a future where organizations run Aries agents that allow for the secure interchange of authentic data between business partners – supply chain participants, customers, suppliers, etc. A collaboration based on BPA by BC Gov (Mines), IBM, the Open Earth Foundation and others was highlighted at the ongoing COP26 Conference on Climate Change. The following videos talk about what is possible using verifiable data to enable trust amongst parties sharing crucial data about Climate Change.

- BC’s Mines Digital Trust video presented at COP26 [https://www.youtube.com/watch?v=q0Jml3isSh8](https://www.youtube.com/watch?v=q0Jml3isSh8)
- Reactions at COP26:
  
  - “Such systems can be really effective if it is adopted world wide, do you think the UNFCCC Global Innovation Hub can support in that aspect by promoting such type of approach for carbon footprint so that it can be used globally.”
    
    - Massamba Thioye, Project Executive, UNFCCC Global Innovation Hub [https://youtu.be/8Jo8PhhouGQ?t=27119](https://youtu.be/8Jo8PhhouGQ?t=27119) -
  - “What we just showed is extremely relevant to what’s happening across this conference… how do we have transparency alongside data privacy… to have a subnational government not only very excited to test it but also fully focused on open source and open standards - which is also something I would like to see a lot more jurisdictions focusing on.”
    
    - Martin Wainstein, Executive Director, Open Earth Foundation [https://youtu.be/8Jo8PhhouGQ?t=27659](https://youtu.be/8Jo8PhhouGQ?t=27659) –
  - “Thank you so much for blowing my mind… we aren’t just talking about how to start, you are already hard at work.”
    
    - Catherine Atkin, Director, Stanford Centre for Legal Informatics (CodeX) Climate Data Policy Initiative [https://youtu.be/8Jo8PhhouGQ?t=29863](https://youtu.be/8Jo8PhhouGQ?t=29863)
  - “Really impressed with the work you are doing and what is happening in the public and private sector can come together.”
    
    - Anna Stanley, Manager, Climate Action, World Business Council for Sustainable Development [https://youtu.be/8Jo8PhhouGQ?t=30287](https://youtu.be/8Jo8PhhouGQ?t=30287)
- IBM Media Release: [Building a digital trust ecosystem for mining in British Columbia IBM Supply Chain and Blockchain Blog](https://www.ibm.com/blogs/blockchain/2021/11/building-a-digital-trust-ecosystem-for-mining-in-british-columbia/)

# Questions/Issues for the TSC

None.

# Releases

The following Aries releases occurred in the last quarter:

- Aries Cloud Agent Python Release 0.7.1, 0.7.2Rc0
- Aries Framework JavaScript – many regular "unstable" releases that are leading up to the 0.1.0 release
  
  - New, related repo Aries Framework JavaScript Extensions that supports React Native components for use in Aries RN Mobile Wallets.
- Aries Askar 0.2.2
- Aries VCX Releases 0.20.0, 0.21.0, 0.22.0, 0.23.0
- Aries Framework Go Release 0.17.0

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). Aries Agent Test Harness (again) extended to support testing more W3C Standard Verifiable Credentials and DIF Presentation Exchange. In addition. three new frameworks were added to the daily interop runs, and a fourth was in work.

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-07-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-09-30T07%3A00%3A00.000Z%22%7D) for the second quarter of 2021, Aries codebases had 1000 commits from 68 contributors. Both numbers are up substantially from last quarter, 28% and 39% respectively.

Community participation is extremely active in rocketchat channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

Coordination with the DIF DIDComm working group is healthy, with regular reports being shared.

Project work in main repos is healthy and active.

# Current Plans

- There has been a significant growth in building common code for mobile wallet apps using both Aries Framework JavaScript and Aries VCX.
  
  - The "Current Plans" mentioned in the last quarterly report saw implementation this quarter – with much more work planned.
- Most Aries teams are focused on adding the core capabilities of AIP 2.0 to their code bases.
- Work is active to extend Aries beyond support just Indy ledgers and Indy AnonCred verifiable credentials to supporting other ledgers and other verifiable credential formats – most notably BBS+ signatures, supporting ZKPs and selective disclosure.
  
  - ACA-Py and AF-Go have working code, including executing test cases.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration continues to increase through the use of the Aries Agent Test Harness. For example, interop tests are executed daily across the Python, Go, .NET, Rust (VCX) and JavaScript frameworks, plus two non-Hyperledger implementations of Aries.

# Contributor Diversity

In addition to the code contribution statistics (above), here are a few indicators of our current diversity:

- We hold community calls each Wednesday at 7am Pacific to cover (the mostly) US and European contributors.
- Call attendance for each is typically in the 20-25 range.
- Most organizations have only one attendee; it is rare for more than three to attend from the same organization.
- Cross codebase interoperability efforts indicate cross-organization cooperation.

# Additional Information

Related activity to Aries is occurring in [Decentralized Identity Foundation](https://identity.foundation/) (DIF), the [Trust over IP Foundation](https://trustoverip.org/), and especially in their [Good Health Pass](https://wiki.trustoverip.org/pages/viewpage.action?pageId=73790) initiative, and in [Linux Foundation Public Health](https://www.lfph.io/) (LFPH).

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

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
