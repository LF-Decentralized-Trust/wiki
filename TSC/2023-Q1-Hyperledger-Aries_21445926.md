1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2023 Project Updates](2023-Project-Updates_21445803.html)

# Technical Oversight Committee : 2023 Q1 Hyperledger Aries

Created by Stephen Curran, last modified by David Enyeart on Feb 02, 2023

Project

Hyperledger Aries

Project Health

Hyperledger Aries has seen a lot of activity overall, and especially in the [Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript), [Aries Bifold](https://github.com/hyperledger/aries-mobile-agent-react-native) (mobile wallet) and [Aries VCX](https://github.com/hyperledger/aries-vcx) communities. Lots of progress being made in those projects!

The following are the highlights from this past quarter:

- Work on Hyperledger AnonCreds is increasing with the goal of moving to all of the Aries Frameworks moving towards being ledger-agnostic. Lots of progress in the AnonCreds repository and particularly in Aries Framework JavaScript. Issue created in ACA-Py to start the work of switching to use the AnonCreds Rust implementation.
- The Aries projects that have a dependency on the Indy SDK are making a concerted effort towards moving off of that and onto the "Shared Components" – [Aries Askar](https://github.com/hyperledger/aries-askar) (secure storage and key management), [anoncreds-rs](https://github.com/hyperledger/anoncreds-rs), or its predecessor – [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) (AnonCreds implementation) and [Indy VDR](https://github.com/hyperledger/indy-vdr) (integration with Indy Node).
  
  - BC Gov posted 5 separate "Code With Us" funded opportunities for deliverables around the elimination of the Indy SDK in favor of the Shared Components.
  - [Animo](https://animo.id), [Indicio](https://indicio.tech) and [DSR](https://dsr-corporation.com) (x3) were awarded the opportunities and are all making progress.
- Discussions began on Aries Interop Profile (AIP) v3.0, which extend AIP 2.0 to be based on DIDComm V2.
- Improvements in the ACA-Py pipelines for producing both artifacts supporting multiple versions of Python and container images with Python and ACA-Py included.
  
  - Looking to see if there are tools available to Hyperledger projects for container vulnerability scanning.
- Important releases from the AFJ team to enable AIP 2.0 support for W3C Format verifiable credential using LD-Signature and BBS+ Signature for JSON-LD and DIF's presentation exchange.
- Lots of work in Aries VCX in moving to AIP 2.0 and moving away from an Indy SDK basis.
- Continued good progress was made in the community on the use of [Overlays Capture Architecture](https://oca.colossi.network/) (OCA) to power the on-screen display of credentials, as mentioned in the previous report. An Aries RFC has been proposed and gone through a couple of iterations, with good feedback – [OCA for Aries RFC PR](https://github.com/hyperledger/aries-rfcs/pull/755), [OCA for Aries RFC (proposed)](https://github.com/swcurran/aries-rfcs/tree/oca4aries/features/0755-oca-for-aries) and [OCA for Aries Style Guide (proposed)](https://github.com/swcurran/aries-rfcs/tree/oca4aries/features/0756-oca-for-aries-style-guide).
  
  - OCA allows a credential issuer to define the semantics of credential attributes, such as language translations for credential attribute labels and help text, what attributes contain personally identifiable information (PII), the data type and encoding of attributes, and the onscreen layout of credentials, including support for issuer icons and background images that can make a digital credential look like a physical credential.
- Continued progress on Aries Bifold, with support for OCA added, a number of iterations on the functionality, and a substantial build out on the [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness).
- Attendance at the regular communities meetings is high across the board.

There continues to be lots of delivered, verified code and increases in participation and use of Aries.

The Indy/Aries stack continues to be the global leader in SSI/verifiable data solutions, with AnonCreds the most used credential format.

# Questions/Issues for the TSC

None.

# Releases

The following Aries releases occurred in the last quarter:

- Aries Cloud Agent Python – 0.7.5-rc0, 0.7.5-rc1, 0.7.5, 1.0.0-rc1
- Aries Framework JavaScript – 0.2.5, 0.3.0, 0.3.1, 0.3.2, 0.3.3
- Aries Askar
- Aries VCX Releases 0.43.0, 0.44.0, 0.45.0, 0.46.0, 0.47.0, 0.48.0, 0.49.0, 0.50.0
- Aries Framework Go

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). 

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-10-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-12-31T07%3A00%3A00.000Z%22%7D) for the fourth quarter of 2022 (October-December), Aries codebases had 397 PRs (down slightly) from 67 contributors (down slightly).

Community participation is extremely active in Discord channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

# Current Plans

- Aggressive work on eliminating the use of the Indy SDK in favor of the Aries Askar/Indy VDR/anoncreds-rs.
- Expanding features in mobile wallet apps, including adding support for OCA to enable beautifully displayed credentials.
- Work on ledger agnostic AnonCreds support in Aries Frameworks and the standardization of AnonCreds.
- Work on Overlays Capture Architecture (OCA) published by issuers.

# Maintainer Diversity

Aries is a multi-codebase effort, and each codebase has its own set of maintainers. The diversity of maintainers closely matches contributors, with notes below.  Cross framework collaboration continues to increase through the replacement of the Indy SDK/use of the Shared Components, and in the work on ledger agnostic AnonCreds.

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

- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [Marcus Brandenburger](https://lf-hyperledger.atlassian.net/wiki/people/5d6cd4bb3803ee0db6cedaaf?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Venkatraman Ramakrishna](https://lf-hyperledger.atlassian.net/wiki/people/6124c28b45f75300691e9f16?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
