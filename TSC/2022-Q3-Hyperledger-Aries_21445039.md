1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Aries

Created by Stephen Curran, last modified by artem on Sep 01, 2022

Project

Hyperledger Aries

Project Health

Hyperledger Aries continues to grow stronger in terms of number of contributors and in the interest from those using Aries in various use cases. It has an extremely diverse and global community.

The following are the highlights from this past quarter:

- The Aries Architecture is proving out as ledger agnostic implementations are coming out with relatively little effort. For some time, Aries Frameworks have supported pluggable DID resolvers, allowing DIDs to be resolved on any ledger.  This quarter, contributors are showing that AnonCreds ZKP-powered verifiable credentials can easily be made ledger agnostic with Aries, with 3 demonstrations implemented using Hyperledger Fabric (see recording of [presentation here](https://lf-hyperledger.atlassian.net/wiki/download/attachments/18497648/video1974150021.mp4?api=v2)), [cheqd](https://cheqd.io) and a simple database (unpublished PoC at this point) as the ledgers. This is a significant evolution as it moves the use of AnonCreds beyond use only with Hyperledger Indy. Expect that by the next report we will have support for this capability in at least one Aries Framework.
- Work in the community has begun on using [Overlays Capture Architecture](https://oca.colossi.network/) (OCA) to power the on-screen display of credentials. OCA allows a credential issuer to define the semantics of credential attributes, such as language translations for credential attribute labels and help text, what attributes contain personally identifiable information (PII), the data type and encoding of attributes, and the onscreen layout of credentials, including support for issuer icons and background images that can make a digital credential look like a physical credential. This powerful capability is being enabled across Aries frameworks, including in the Aries mobile wallet implementations.
- An Aries "Interopathon" event is planned for the end of August 2022 with a goal of having all Aries implementers verify support for key AIP 2.0 protocols – especially establishing connections.
- Additional repos are being added to the Aries ecosystem to make deployment easier, such as the [Aries Mediator Service](https://github.com/hyperledger/aries-mediator-service) that enables spinning up a fit-for-purpose Aries mediator based on configured deployment Aries Cloud Agent Python. A similar Aries Endorser Service is in the works for authorizing transactions for writing to Hyperledger Indy network instances.
- Rapid progress on Aries Framework JavaScript continues, with a release (0.2.x) including some AIP 2.0 support, progress on completing AIP 2.0 support (in upcoming release 0.3.x). PRs this quarter added support for credentials in Aries Framework JavaScript for using the W3C VC Data Model (issue in 0.20, presentation in 0.3.0) and an excellent new documentation site [https://aries.js.org/](https://aries.js.org/).
- Aries Framework Go's evolution continues with updated support for the Sidetree protocol, DIDs, and DIDComm.
- Both the [Aries Agent Test Harness](https://aries-interop.info/) (AATH) and especially the [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness) continue to evolve. The [IDLab](https://www.idlab.org/en/) presented ([recording here](https://wiki.hyperledger.org/display/ARIES/2022-07-13+Aries+Working+Group+Call?preview=%2F71698196%2F71698287%2F20220713%20Aries%20Working%20Group%20Call%20Recording.mp4) – starting at 8:28) on an interesting tool they had developed on top of Aries Agent Test Harness to make it easy for Aries Wallet developers to test their app using the AATH tests.
- Attendance at the regular communities meetings is up across the board.

There continues to be lots of delivered, verified code and increases in participation and use of Aries.

As mentioned in the previous reports, the focus on making AnonCreds a ledger agnostic standard vs. a de facto standard is gaining momentum. The standard drafting process is going well, producing [this work in progress spec](https://anoncreds-wg.github.io/anoncreds-spec/), with a strong contingent working regularly to evolve it.

The Indy/Aries stack continues to be the global leader in SSI/verifiable data solutions.

# Questions/Issues for the TSC

None.

# Releases

The following Aries releases occurred in the last quarter:

- Aries Cloud Agent Python – 0.7.4
- Aries Framework JavaScript – 0.2.0
- Aries Askar 0.2.6, 0.2.7
- Aries VCX Releases 0.35.0, 036.0
- Aries Framework Go 0.1.8

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). 

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-04-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-06-30T07%3A00%3A00.000Z%22%7D) for the second quarter of 2022 (April-June), Aries codebases had 463 PRs (up about 12%) from 77 contributors (almost 30%).

Community participation is extremely active in Discord channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

# Current Plans

- A continued focus on building common code for mobile wallet apps using both Aries Framework JavaScript and Aries VCX.
- A push to get AIP used – especially focused on establishing connections.
- Work on ledger agnostic AnonCreds support in Aries Frameworks and the standardization of AnonCreds.
- Work on Overlays Capture Architecture (OCA) (see above) to enable beautifully displayed credentials.
- A split focus between deploying more production solutions and moving the Aries frameworks forward to use new protocols – AIP 2.0 and DIDComm v2.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration continues to increase through the use of the Aries Agent Test Harness. For example, interop tests are executed daily across the Python, Go, .NET, Rust (VCX) and JavaScript frameworks, plus two non-Hyperledger implementations of Aries.

# Contributor Diversity

In addition to the code contribution statistics (above), here are a few indicators of our current diversity:

- We hold community calls each Wednesday at 7am Pacific to cover (the mostly) US and European contributors.
- Call attendance for each is typically in the 20-25 range, up somewhat lately.
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
