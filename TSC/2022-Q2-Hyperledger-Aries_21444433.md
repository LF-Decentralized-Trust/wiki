1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q2 Hyperledger Aries

Created by Stephen Curran, last modified by Grace Hartley (Deactivated) on May 24, 2022

Project

Hyperledger Aries

Project Health

Hyperledger Aries continues to grow stronger in terms of activity by contributors and in the interest from those using Aries in various use cases. It has an extremely diverse and global community. In addition to the steady progress made in most of the sub-projects, a number of significant events occurred in the project including:

- Rapid progress on Aries Framework JavaScript continues, with key AIP v2.0 PRs merged (e.g. support for Credential Exchange V2 and W3C VC Standard credentials) or in process.
- Aries Bifold, the community-developed react native mobile Wallet App built on Aries Framework JavaScript, also continues to evolve rapidly, with impressive deployment-specific pipelines that allow going from Bifold, overlaying instance specific code and publishing the result to the iOS and Android stores. This powerful approach allows rapid iteration of published products with the changes being put in exactly the right place – AFJ, AFJ-Extension, Aries Bifold (all of which benefit the entire community) or to the deployment specific instance. This gets away from the "fork-and-forget" model, enabling proper open source development for a UX-focused project.
- The community is stress testing the Aries frameworks and some issues have been reported, and addressed, as you will see. The addition of an open source [Aries Load Generator](https://github.com/My-DIGI-ID/aries-cloudagent-loadgenerator) tool (which I think will be moving to Hyperledger) provides an amazing tool for exploring these issues. The combination of the load test generator and some focused work in [Aries Askar](https://github.com/hyperledger/aries-askar) both addressed the intermittent problems and boosted Askar performance by 11% in the process.  Very cool!
  
  - The load test generator also enables an easy way to do a direct comparison of the old IndySDK and the new Aries Askar and shared components. As seen by these results, Askar is far more stable than the Indy SDK (doesn't slow over time) and is about twice as fast as the Indy SDK – the differences are stark!  See the follow test run results for [ACA-Py 0.7.3+IndySDK](https://github.com/lissi-id/acapy-load-test-results/blob/main/AcaPy_0-7-3/Without%20Multitenancy/Revokable/Full%20Flow%20Constant%20Load/13%20AcaPy%200_7_3%20indy_wallet/report-test-results.pdf) and [ACA-Py 0.7.4+Askar](https://github.com/lissi-id/acapy-load-test-results/blob/main/AcaPy_0-7-4/Endurance_Test/0_7_4-200rpm/report-test-results-0-6.pdf)
- Both the [Aries Agent Test Harness](https://aries-interop.info/) and the [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness) continue to evolve with more contributions provided this past quarter in making them work together and in expanding the tests being run.
- Attendance at the regular communities meetings is up, with 35+ people at recent Aries Cloud Agent Python User Group meeting.
- Work has begun in integrating DIDComm V2 into the Aries frameworks – some design and some implementation work. We think this will progress slowly as interest is clearly in what people can do **today** but these proof-of-concepts demonstrate that Aries frameworks are well designed to enable such evolutions.

There continues to be lots of delivered, verified code, let alone the increases in participation and use of Aries.

As mentioned in the last report, the focus on making AnonCreds a standard vs. a de facto standard is gaining momentum. The standard drafting process is going will, producing [this work in progress spec](https://anoncreds-wg.github.io/anoncreds-spec/), with a strong contingent working regularly to evolve it.

The Indy/Aries stack continues to be the global leader in SSI/verifiable data solutions.

# Questions/Issues for the TSC

None.

# Releases

The following Aries releases occurred in the last quarter:

- Aries Cloud Agent Python Release 0.7.4-rc0, 0.7.4-rc1
- Aries Framework JavaScript – 0.2.0-alpha
- Aries Askar 0.2.5
- Aries VCX Releases 0.28.0 through 0.45.0

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). 

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-01-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-03-31T07%3A00%3A00.000Z%22%7D) for the first quarter of 2022 (Jan-March), Aries codebases had 1.37k commits (up significantly) from 60 contributors (up slightly).

Community participation is extremely active in Discord channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

Coordination with the DIF DIDComm working group is healthy, with regular reports being shared.

Project work in main repos is healthy and active. A potential concern raised last quarter was the lack of activity in the Aries Framework .NET repository, but even that had some activity this quarter, with a couple of interesting PRs completed and merged.

# Current Plans

- A continued focus on building common code for mobile wallet apps using both Aries Framework JavaScript and Aries VCX.
- Based on feedback from the community – a lot of effort has gone into stress testing Aries – especially Aries Cloud Agent Python, with good results.
- A split focus between deploying more production solutions and moving the Aries frameworks forward to use new protocols – AIP 2.0 and DIDComm v2.
- A focus on standardizing AnonCreds to provide increased comfort of the solid foundation in Aries and use beyond Aries.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration continues to increase through the use of the Aries Agent Test Harness. For example, interop tests are executed daily across the Python, Go, .NET, Rust (VCX) and JavaScript frameworks, plus two non-Hyperledger implementations of Aries.

# Contributor Diversity

In addition to the code contribution statistics (above), here are a few indicators of our current diversity:

- We hold community calls each Wednesday at 7am Pacific to cover (the mostly) US and European contributors.
- Call attendance for each is typically in the 15-20 range, up somewhat lately.
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
