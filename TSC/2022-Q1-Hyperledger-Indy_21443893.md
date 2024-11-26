1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Indy

Created by Stephen Curran, last modified by Angelo de Caro on Mar 23, 2022

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

Project Health

As with the previous quarter, work on the Indy DLT (indy-node and indy-plenum) continued slowly this quarter with a focus only on the CI/CD capabilities and upgrading to Ubuntu 20.04. Good progress was made and on the project and we (think we) can see the light at the end of the tunnel.  Accomplishments:

- All three of the relevant repos (indy-node, indy-plenum and indy-test-automation) have been updated to support GitHub Actions CI/CD and Jenkins. Jenkins will be dropped once we have a fully tested artifacted generated.
- A circular dependency in indy-test-automation with indy-node and code in the Sovrin Foundation r epos has been broken.
- A working Ubuntu 20.04 artifact has been produced and deployed as a node on the IdUnion Indy network test instance.
- Documentation has been updated for how to deploy a network and how to deploy a new node on a running network.
- Quick start Indy developer environments have been defined for Indy using containers and on GitPod.

Left to do:

- Investigation of a potential intermittent bug on a network with a mix of Ubuntu 16.04 and 20.04 nodes (likely something in libsodium).
- Automation of a tagged release to produce published artifacts.

As noted last report, work on the CI/CD and OS Upgrade has prevented progress on new features – blocking most notably the upgrade to the new "did:indy" DID Method. However, the new documentation and containerized developer environments will be a huge help for developers.

A course put on by Hyperledger and Indicio aimed at getting new developers started on Indy happened today (2022.02.03) and interest was high – there was a waiting list to attend. We're hoping that translates into developers working on the project.

BC Gov launched a "Code With Us" challenge for $CDN70k to get work on the  "did:indy" method started. The challenge was won by two respondents – Indicio for the Indy Node/Plenum work and [Dominic Wörner](https://lf-hyperledger.atlassian.net/wiki/people/557058:cd48c258-308c-45bc-828f-909cf9284982?ref=confluence) for the Indy VDR (Client) work. They have started their work by evaluating the specification and the existing code base to see if there "code-friendly" adjustments needed to the spec ([https://github.com/hyperledger/indy-did-method](https://github.com/hyperledger/indy-did-method)) to map out the changes to be made to the code. From there, let the coding begin! A team of interested parties are now meeting weekly to watch (and hopefully) help with the progress and to discuss the specification.

This quarter has also seen an increased focus on the use of the verifiable credentials mechanism found in Hyperledger Indy–AnonCreds as a "long term" approach versus the plan this time last year of moving to the W3C VC 1.x data model. After a lot of effort in moving to the W3C VC data model, practical limitations have meant that for those wanting to deploy solutions today, AnonCreds has been found by many to be the better approach. In response to that, a number in the Indy/Aries community have started the process of making AnonCreds not just open source, but also an open standard, and to remove a perception by some of it being proprietary. We expect that a v1.0 specification will be produced fairly quickly that (more or less) documents what we have today, and in parallel or soon after, we'll work on an AnonCreds v2.0 that retains all the capabilities of AnonCreds, but based on "newer" approaches, such as replacing CL-Signatures with BBS+ Signatures. Note that although AnonCreds is currently a part of Hyperledger Indy, AnonCreds itself is more relevant at the higher levels of the Trust over IP stack, and thus is more of a concern of Aries contributors and those using the Aries in building and deploying real world applications.

Work continues this quarter on the new client-side Indy library indy-vdr, with 1 tagged releases (0.3.4), and on indy-shared-rs (0.3.1). More teams are deploying that code and contributing to the code base. The indy-sdk CI/CD process was blocked for a period of time this quarter, but that was recently fixed and PRs continue to trickle in, but no release was completed.

The interest in deploying instances of Indy continues to be strong, with lots of questions on Hyperledger Chat from people learning to run their own instances. There are no significant bugs that are pending action, and little demand for new functionality (beyond the "did:indy" method) from the user base. Indy "just works". 

Per the [Indy Activity Dashboard (2021-10 to 2021-12)](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Findy/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-10-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-12-31T07%3A00%3A00.000Z%22%7D), there were 68 commits from 9 contributors. which is about the same as last quarter.

# Questions/Issues for the TSC

## Issues from previous reports:

### Build Pipelines

**Update**: Steady progress, with GHAs implemented, the test automation process updated and the Ubuntu upgrade nearing completion.

### **Diversity of Contributor Community**

**Update**: Contributor community diversity remains a top of mind issue with the maintainers. The Hyperledger Staff (particularly [David Boswell](https://lf-hyperledger.atlassian.net/wiki/people/70121:0a14f738-3039-421f-a6a9-a83d19f23227?ref=confluence) and [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) – thanks!) and Indicio worked on getting an "Indy Contributors" course in place that was run today.. We have also had a number of new contributors joining Aries projects that have a reliance on Indy.  As noted, interest and contributions to indy-vdr continues to increase.

# Releases

- indy-did-method (first draft)
- indy-vdr 0.3.4
- indy-shared-rs 0.3.1

# Overall Activity in the Past Quarter

In the past quarter (as in the previous quarter), ledger code development focused on code management – upgrading the Indy Node and Plenum CI/CD pipeline and upgrading Indy Node to run on Ubuntu 20.04.  

There has been some progress on the new Indy DID Method, but not code. The work left at the end of the last two quarters remains (albeit now as a repo vs. HackMD doc): wrapping up the specification and defining the backlog of work for indy-node, indy-sdk and indy-vdr. With the CI/CD work blocking progress on indy-node, it's been difficult to convince contributors in the community to work on the DID Method if it is so hard to test and impossible to release.

# Current Plans

The push will be to complete the new CI/CD Indy Node and Plenum pipelines, the Ubuntu 20.04 upgrade, and tools to make it easier to do Indy Node development. In parallel, we expect coding to begin on the "did:indy" method.

# Maintainer Diversity

The bi-weekly Indy Contributors call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. Topics and attendance has dropped recently, mostly because of the lack of topics other than "how is the CI/CD work coming along?"

# Contributor Diversity

Work has begun on putting together an "Indy Contributors" course for presentation in early 2022. The edX course about Indy, Aries and Ursa ([here](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)) was updated early in 2021 (this was missed in the last Quarterly report – even though the author of the quarterly report was the course creator...).

# Additional Information

- Key channels on Hyperledger Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
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
