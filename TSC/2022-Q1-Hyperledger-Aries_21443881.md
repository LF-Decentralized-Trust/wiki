1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Aries

Created by Stephen Curran, last modified by Angelo de Caro on Mar 23, 2022

Project

Hyperledger Aries

Project Health

Hyperledger Aries continues to grow stronger in terms of activity by contributors and in the interest from those using Aries in various use cases. It has an extremely diverse and global community. In addition to the steady progress made in most of the sub-projects, a number of significant events occurred in the project including:

- Progress on Aries Framework JavaScript in implementing Aries Interop v2.0 (AIP 2.0), and its capability as the foundation of an Bifold, an Aries React Native mobile wallet.
- An "Aries Mobile Summit" was held and significant progress as been made in open source mobile wallet delivery velocity. There are now Aries React Native mobile wallets being deployed by various groups into the App Stores.
- A new repo "aries-mediator-service" has been created that can be used by mobile Wallet providers as an Aries Mediator to enable communication between the mobile wallet and all other Aries agent. The repo is built on the latest ACA-Py release configured to act as an Aries mediator.
- Continued progress on the Aries VCX framework toward AIP 2.0, a Rust-based framework suitable for use in a number of server-side and mobile use cases.
- Continued evolution of the open source implementation of the Aries Interop Profile RFCs by the FIndy (Finland) project.
- The [Aries Agent Test Harness](https://aries-interop.info/), continues to be a focal point for the community in verifying interoperability, with ongoing adjustments based on test results as the various frameworks evolve.
- A new [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness) was added for automating the testing of Aries Mobile Wallets.

There continues to be lots of delivered, verified code, let alone the increases in participation and use of Aries.

This quarter has also seen an increased focus on the use of the verifiable credentials mechanism found in Hyperledger Indy–AnonCreds as a "long term" approach versus the plan this time last year of moving to the W3C VC 1.x data model. After a lot of effort in moving to the W3C VC data model, practical limitations have meant that for those wanting to deploy solutions today, AnonCreds has been found by many to be the better approach. In response to that, a number in the Aries community have started the process of making AnonCreds not just open source, but also an open standard, and to remove a perception by some of it being proprietary. We expect that a v1.0 specification will be produced fairly quickly that (more or less) documents what we have today, and in parallel or soon after, we'll work on an AnonCreds v2.0 that retains all the capabilities of AnonCreds, but based on "newer" approaches, such as replacing CL-Signatures with BBS+ Signatures.  Note that although AnonCreds is currently a part of Hyperledger Indy, AnonCreds itself is more relevant at the higher levels of the Trust over IP stack, and thus is more of a concern of Aries contributors and those using the Aries in building and deploying real world applications.

# Questions/Issues for the TSC

None.

# Releases

The following Aries releases occurred in the last quarter:

- Aries Cloud Agent Python Release 0.7.2, 0.7.3
- Aries Framework JavaScript – a transition from "unstable" tags, to "alpha" tags, and version 0.1.0
  
  - [Aries Framework JavaScript Extensions](https://github.com/hyperledger/aries-framework-javascript-ext) was tagged multiple times by feature
- Aries Askar 0.2.3, 0.2.4
- Aries VCX Releases 0.24.1 through 0.29.0

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). 

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-10-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-12-31T07%3A00%3A00.000Z%22%7D) for the fourth quarter of 2021 (Oct-Dec), Aries codebases had 900 commits from 58 contributors. Both numbers are slightly down from last quarter, about 10% each – most likely a reflection of the holiday season vs. interest.

Community participation is extremely active in rocketchat channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

Coordination with the DIF DIDComm working group is healthy, with regular reports being shared.

Project work in main repos is healthy and active. A potential concern is the lack of activity in the Aries Framework .NET repository, which has gone largely dormant. It was a popular Aries framework in the beginning, and was the basis for the well known Aries Wallets in the market. This is likely due to a combination of factors, including the focus on React Native (and hence Aries Framework JavaScript) over Xamarin by mobile app developers, the use of Aries Cloud Agent Python and Aries VCX on the server side, and the focus of the main contributor to Aries Framework .NET shifting to other products.

# Current Plans

- There has been a significant growth in building common code for mobile wallet apps using both Aries Framework JavaScript and Aries VCX.
  
  - This is the same as in the last quarterly report – it was correct this past quarter and will continue to be so as Aries Framework JavaScript implements Aries Interop Profile 2.0 and mobile wallets are released.
- Most Aries teams are focused on adding the core capabilities of AIP 2.0 to their code bases. the work is nearing completion in Aries VCX, Aries Framework JavaScript and Aries Cloud Agent Python.
- A focus on standardizing AnonCreds to provide increased comfort of the solid foundation in Aries and use beyond Aries.
- The ACA-Py team is looking at what more needs to be done to jump to an ACA-Py 1.0.0 release.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration continues to increase through the use of the Aries Agent Test Harness. For example, interop tests are executed daily across the Python, Go, .NET, Rust (VCX) and JavaScript frameworks, plus two non-Hyperledger implementations of Aries.

# Contributor Diversity

In addition to the code contribution statistics (above), here are a few indicators of our current diversity:

- We hold community calls each Wednesday at 7am Pacific to cover (the mostly) US and European contributors.
- Call attendance for each is typically in the 10-12 range, down somewhat lately. However, in the quarter there was the very well-attended Aries Mobile Summit (5 weekly 2 hour sessions) and other Aries framework specific calls.
- Most organizations have only one attendee; it is rare for more than three to attend from the same organization.
- Cross codebase interoperability efforts indicate cross-organization cooperation.

# Additional Information

Nothing

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
