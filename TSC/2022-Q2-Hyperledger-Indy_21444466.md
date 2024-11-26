1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q2 Hyperledger Indy

Created by Stephen Curran, last modified by Grace Hartley (Deactivated) on May 24, 2022

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
- [indy-did-method](https://github.com/hyperledger/indy-did-method) - "did:indy" [DID Method specification](https://hyperledger.github.io/indy-did-method/)
- [indy-node-container](https://github.com/hyperledger/indy-node-container) ![(plus)](images/icons/emoticons/add.png) NEW!

Project Health

In a change from the previous quarters, contributions to Indy ticked up this quarter – a good thing!  The project is getting a lot of external attention and that is (finally!) changing into contributor interest.  Attendance is up significantly at community meetings, a new repo was added ([indy-node-container](https://github.com/hyperledger/indy-node-container) – a containerized instance of Indy Node for easier deployment). As well, the first major addition to Indy in some time was added – an implementation of did:indy in [indy-node](https://github.com/hyperledger/indy-node), with the following features:

- Indy clients (e.g. Aries Agents) can add full DID Standard DIDDocs to an Indy DID published on the ledger. This had not been supported in Indy prior to this because Indy pre-dated the DID Standard.
- A client can indicate a new DID is self-certifying, with the ledger verifying that the DID (the identifier) was derived from the initial verkey (public key) of the key pair associate with the DID
- The [did-indy-method](https://github.com/hyperledger/indy-did-method) repository and [published spec](https://hyperledger.github.io/indy-did-method/) have been updated to match the implementation.
- Changes were added to indy-vdr to implement the "network of networks" support so that a DID will contain an extra "namespace" element indicating on which Indy network the object is to be found.
- A mechanism has been defined based on the concept of DID URLs as a mechanism for providing identifiers for other AnonCred objects beyond DIDs: schemas, CredDefs and Revocation Registries.
- The use of the ATTRIB transaction was deprecated in favour of the (somewhat) less arbitrary DIDDoc feature of DIDs. The use of ATTRIBs may be used for other purposes in the future, but we'd like to stop the "wild, wild west" days of using ATTRIB for anything.

A BC Gov "Code With Us" challenge for $CDN70k was create to get work on the "did:indy" method done. The challenge was won last quarter and implemented this quarter by two respondents – [Indicio](https://indicio.tech/) for the Indy Node/Plenum work and [Dominic Wörner](https://lf-hyperledger.atlassian.net/wiki/people/557058:cd48c258-308c-45bc-828f-909cf9284982?ref=confluence) for the Indy VDR (Client) work. They completed the plan worked and their changes have been merged into the relevant code bases. Kudos to all of the participants and the progress it represents!

On the less good news front, the CI/CD upgrade and Ubuntu 20.04 effort moved forward, but is still not complete.  Just as was stated in the last quarterly report, there is still work to do, but progress was made – including some significant updates.  The big items to complete remain the same:

- Investigation of a potential intermittent bug on a network with a mix of Ubuntu 16.04 and 20.04 nodes (likely something in libsodium).
- Automation of a tagged release to produce published artifacts.

As mentioned in the last report, the focus on making AnonCreds a standard vs. an open source implementation de facto standard is gaining momentum. The standard drafting process is going will, producing this work in progress [spec](https://anoncreds-wg.github.io/anoncreds-spec/), with a strong contingent working regularly to evolve it.

Work continues this quarter on the new client-side Indy library indy-vdr, and on indy-shared-rs, although no new releases were tagged. The Aries Cloud Agent Python project has made the use of the shared components (along with [Aries Askar](https://github.com/hyperledger/aries-askar)) as the recommended default for ACA-Py. The stability and performance results are much better than with Indy SDK.

The interest in deploying instances of Indy continues to be strong, with lots of questions on Hyperledger Chat from people learning to run their own instances. There are no significant bugs that are pending action, and little demand for new functionality (beyond the "did:indy" method) from the user base. Indy "just works". 

Per the [Indy Activity Dashboard (2022-01 to 2022-03)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-01-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-03-31T07%3A00%3A00.000Z%22%7D), there were 135 commits from 20 contributors. both of which are double the numbers from last quarter.

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: Steady progress, with GHAs implemented, the test automation process updated and the Ubuntu upgrade nearing completion.

### **Diversity of Contributor Community**

**Update**: Contributor community diversity remains a top of mind issue with the maintainers. We're seeing improvements beginning as more deployments begin (notably Aries deployments) and the importance of the underlying ledger utility is understood. We need more, but in this quarter, there was improvement seen.

# Releases

- indy-did-method (completed)

# Overall Activity in the Past Quarter

In the past quarter (as in the previous quarter), ledger code development focused on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04.  Unlike previous quarters, there was also work completed on the did:indy DID Method and effort put into providing stable indy-node containers.

# Current Plans

The push will be to complete the new CI/CD Indy Node and Plenum pipelines, the Ubuntu 20.04 upgrade.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. Topics and attendance has increased recently, with more and more interested parties showing up, and new contributors weighing in on the conversations.

# Contributor Diversity

The "Indy Contributors" course was presented in early 2022 and was extremely well received. The edX course about Indy, Aries and Ursa ([here](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)) was updated early in 2021 (this was missed in the last Quarterly report – even though the author of the quarterly report was the course creator...).

# Additional Information

- Key channels on Hyperledger Discord: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

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
