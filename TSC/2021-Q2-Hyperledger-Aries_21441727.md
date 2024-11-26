1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q2 Hyperledger Aries

Created by Stephen Curran, last modified by Tracy Kuhrt on May 25, 2021

Project

Hyperledger Aries

Project Health

The Aries Project transitioned to "Active" in the last quarter, reflecting the project's current community state. Lots of active discussion, activity and growth internally, and a lot of external interest in the project and artifacts from the deliverables.

# Questions/Issues for the TSC

A discussion is happening email with [Brian Behlendorf (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/616ecf50702bd0006a5a7c6b?ref=confluence)and leaders in the Ursa community about how to get an audit report on Ursa and it's use in Aries and Indy. That is progressing, but it's a tricky subject, so any help from the TSC on moving the effort forward would be appreciated.

# Releases

The following releases occurred in the last quarter:

- Aries Cloud Agent Python Release 0.6.0
- Aries Framework Go Release 0.1.6
- Aries Framework JavaScript – multiple "unstable" releases that are leading up to the 0.0.1 release
- Aries Askar 0.1.3
- Aries VCX Releases 0.16.0, 0.17.0, 0.17.1

We expect that we'll get to designated "1.0.0" releases in the next few months for some of the sub-projects.

The Aries Agent Test Harness continued to evolve with the launch of a status page about the state of Aries interoperability – [https://aries-interop.info](https://aries-interop.info). As well, a mechanism was added to allow for the testing of mobile agents using the Aries Agent Test Harness, so that interop between frameworks as issuers and verifiers and mobile agents as holders.

![](attachments/21441727/21453505.png?height=400)

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard?time=%7B%22from%22%3A%222021-01-01T00%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-03-31T23%3A59%3A59.254Z%22%7D) for the first quarter of 2021, Aries codebases had 696 commits in 549 PRs from 53 contributors.

Community participation is extremely active in rocketchat channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

Coordination with the DIF DIDComm working group is healthy, with regular reports being shared.

Project work in main repos is healthy and active.

# Current Plans

- AIP 2.0 is very (very!) close to completion, with key additions to make Aries ledger agnostic and to add the use of new verifiable credential formats in W3C Standard format.
  
  - Lots of work is proceeding as the discussions about AIP 2.0 continue.
- Work is active to extend Aries beyond support just Indy ledgers and Indy AnonCred verifiable credentials to supporting other ledgers and other verifiable credential formats – most notably BBS+ signatures, supporting ZKPs and selective disclosure.
  
  - AF-Go has working code
  - ACA-Py has works in progress (as of the end of 2021-Q1) on multi-ledger resolution and verifiable credential formats.
- The Aries Mobile Agent React Native (aka Bifold) built on Aries Framework JavaScript has gained some traction and could be the open source wallet a larger community rallied behind.
- Interoperability testing continues to be a key focus.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration is increasing. For example, work is happening on interop testing capabilities across the Python, Go, .NET and JavaScript frameworks.

As interest in verifiable credentials has increased with COVID-19 use cases (proof of testing, proof of immunization and mobile medical workforces), interest and attendance has increased, as have deployments of Aries-based implementations.

# Contributor Diversity

In addition to the code contribution statistics (above), here are a few indicators of our current diversity:

- We hold two community calls on Wednesdays: weekly at noon Pacific to cover US and Pacific contributors, and biweekly at 7am Pacific to cover US and European contributors.
- Call attendance for each is typically in the 15-20 range.
- Most organizations have only one attendee; it is rare for more than 3 to attend from the same organization.
- Cross codebase interoperability efforts indicate cross-organization cooperation.

# Additional Information

Related activity to Aries is occurring in [DIF](https://identity.foundation/) (Decentralized Identity Foundation), the [Trust over IP Foundation](https://trustoverip.org/), and especially in their [Good Health Pass](https://wiki.trustoverip.org/pages/viewpage.action?pageId=73790) initiative, and in [Linux Foundation Public Health](https://www.lfph.io/) (LFPH).

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

## Attachments:

![](images/icons/bullet_blue.gif) [image2021-4-30\_8-23-54.png](attachments/21441727/21453505.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
