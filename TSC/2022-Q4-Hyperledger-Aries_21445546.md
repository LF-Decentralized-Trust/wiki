1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q4 Hyperledger Aries

Created by Stephen Curran, last modified by Jim Zhang on Dec 01, 2022

Project

Hyperledger Aries

Project Health

Hyperledger Aries continues to grow stronger in terms of number of contributors and in the interest from those using Aries in various use cases. It has an extremely diverse and global community. The Aries "Interopathon" held at the end of August 2022 and the Hyperledger Global Forum were very successful in both getting developers from different Aries Frameworks together and in introducing new developers to the Frameworks, increasing the contributor community.

The following are the highlights from this past quarter:

- Continued progress on ledger agnosticism in Aries, and a significant focus on ledger-agnostic AnonCreds, culminating in the proposal (later accepted) to create the Hyperledger AnonCreds project. This change, along with an ongoing investigation into changing the data format of AnonCreds into alignment with the W3C Verifiable Credentials Standard data model will expand both the AnonCreds and Aries communities. There will be a lot more to cover on that in the next Hyperledger Aries and Hyperledger AnonCreds reports.
- As expected, support for AnonCreds on ledgers other than Indy is at the proof-of-concept level within Aries Framework JavaScript, and that work will be the basis for transitioning all of the Aries Frameworks to support AnonCreds on ledgers other than Indy. We expect some interest as AnonCreds becomes ledger-agnostic from the other Hyperledger communities like Fabric and Besu in supporting the storage of AnonCreds objects on those platforms.
- Significant moves have been made in the three most active Aries Frameworks (ACA-Py, AFJ and Aries VCX) in completing all of AIP 2.0 and enabling key user experience features, such as OCA (below).
- Progress was made in the community on the use of [Overlays Capture Architecture](https://oca.colossi.network/) (OCA) to power the on-screen display of credentials, as mentioned in the previous report. Within Aries Bifold (open source wallet), OCA has been implemented and deployed in the newly launched BC Wallet (available on app stores now).
  
  - OCA allows a credential issuer to define the semantics of credential attributes, such as language translations for credential attribute labels and help text, what attributes contain personally identifiable information (PII), the data type and encoding of attributes, and the onscreen layout of credentials, including support for issuer icons and background images that can make a digital credential look like a physical credential.
- Speaking of Aries Bifold, substantial progress has been made. Perhaps the most significant advance of the quarter was the creation by the Wallet Team at BC Gov to make a pipeline that allows for the publication of fully customized Aries Bifold wallet via a patching process that minimizes the code outside of Aries Bifold. This has allowed that team to do ~90% of their code at the Aries Bifold level for the benefit of the entire community, while still producing a fully custom BC Wallet for publication to app stores. This is a FAR, FAR better model than a team forking Aries Bifold and then developing on the fork, with painful effort to give back contributions. This approach needs to be promoted and replicated by others wanting a publishable, high quality wallet. Key features added to Aries Bifold:
  
  - Wallet security features – PIN and Biometrics
  - Wallet initialization actions and screens easily customized for a specific deployment.
  - Configurable settings.
  - The addition of OCA handling for a better user experience.
- Must work was done on the Aries Endorser Service, a service that is commonly needed in Indy deployments of Aries agents, where a permissioned agent signs transactions to be written to an Indy ledger on behalf of an author.
- Rapid progress on Aries Framework JavaScript continues, with a release of several 0.2.x (current), and release 0.3.x (future) versions.
- Aries Framework Go's evolution continues with updated support for the Sidetree protocol, DIDs, and DIDComm.
- Both the [Aries Agent Test Harness](https://aries-interop.info/) (AATH) and especially the [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness) continue to evolve. AATH and AAMH were covered and used at the Aries Interopathon in August, and tests and test wrappers for Aries Agents continue to be expanded. The only concern in that area is that the Aries Framework Go team seems to no longer be using AATH.
- Attendance at the regular communities meetings is high across the board.

There continues to be lots of delivered, verified code and increases in participation and use of Aries.

The Indy/Aries stack continues to be the global leader in SSI/verifiable data solutions, with AnonCreds the most used credential format.

# Questions/Issues for the TSC

None.

# Releases

The following Aries releases occurred in the last quarter:

- Aries Cloud Agent Python – 1.0.0-rc0
- Aries Framework JavaScript – 0.2.2, 0.2.3 and 0.2.4
- Aries Askar
- Aries VCX Releases 0.37.0, 0.38.0, 0.39.0, 0.40.0, 0.41.0, 0.42.0
- Aries Framework Go

Interoperability status can be seen here: [https://aries-interop.info](https://aries-interop.info). 

# Overall Activity in the Past Quarter

Per the [Aries Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Faries/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-07-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-09-30T07%3A00%3A00.000Z%22%7D) for the third quarter of 2022 (July-September), Aries codebases had 412 PRs (down slightly) from 69 contributors (down slightly). Impressive, given this is over the summer holiday months in the northern hemisphere.

Community participation is extremely active in Discord channels, community calls, and repo PR reviews and issues. Email lists are less frequently used.

# Current Plans

- A continued focus on building common code for mobile wallet apps using both Aries Framework JavaScript and Aries VCX.
- Continuing the push to get AIP used – especially focused on establishing connections.
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
