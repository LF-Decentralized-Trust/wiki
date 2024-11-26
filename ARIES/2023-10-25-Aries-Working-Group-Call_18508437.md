1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-10-25 Aries Working Group Call

Created by Sam Curren, last modified by Daniel Bluhm on Oct 25, 2023

## Summary:

- Mentor Report
- did:peer:2
- Direction, Energy, and speed

## Date

25 Oct 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Kimmo Hovi](https://lf-hyperledger.atlassian.net/wiki/people/712020:52956dda-a083-4ba5-85b9-3f1efd76f8c1?ref=confluence) (FindyNet) &lt;ext.kimmo.hovi@findy.fi&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    
    - Release 0.4.0-dev16
    - Release 0.5.0 will have breaking changes, including did:indy branch merged into main.
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - Release 0.2.9
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
    
    - Release 0.1.0
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
    
    - Release 0.3.3 Bugfix (bug was in the python wrapper)
      
    - Release 1.0.0 Embeds new AnonCreds CL Signatures library with fixes, performance improvements
- Frameworks:
  
  - Aries-CloudAgent-Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: https://aca-py.org
    
    - 0.10.4 Release – patch to address an interop issue with ACA-Py mediator and aries-framework-kotlin
    - 0.11 on deck with did rotate and did:peer:4
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - OWF - shared in OWF list and discord, giving more time for feedback.
    - 0.5 in the works
      
      - Dropping IndySDK
      - AnonCreds Revocation
      - Dropping Node 16 support (EOL)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Release 0.59.1 [https://github.com/hyperledger/aries-vcx/releases/tag/0.56.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.56.0)
    - Ongoing refactoring
    - finished migration to IndyVDR
    - Indy CredX up soon
    - issue and present v2 on deck
  - Picos as of pico-engine version 1.3.0 natively use DIDComm v2 ([https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md](https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md))
    
    - replacing ACA-Pico agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico)) which are now deprecated
    - protocols implemented so far: oob invitation, trust-ping, basicmessage (more to be added [https://github.com/Picolab/DIDComm-V2](https://github.com/Picolab/DIDComm-V2))
    - based on the SICPA didcomm NodeJS module
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native), Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
    
    - 0.4.0 in Bifold – including the shared components
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - Update to use SocketDock?
- [aries-endorser-service](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)

## Discussion Topics

- Aries marketing update - [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60da2fc7285656006a667081?ref=confluence) [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence)  
  
  - New draft Aries logos: [https://docs.google.com/document/d/1G5o24hw3fyBDoB5VdcELv8hjd4IH7cF-JYIcX7hSUt4/edit](https://docs.google.com/document/d/1G5o24hw3fyBDoB5VdcELv8hjd4IH7cF-JYIcX7hSUt4/edit)
  - Join our marketing working group meeting, last Tuesday of every month: [Aries Marketing Working Group](Aries-Marketing-Working-Group_18505802.html)
- Mentorship Review - Patrik
  
  - mentee: Naian [ng.p.ref@mailbox.org](mailto:ng.p.ref@mailbox.org)
  - [Project Plan - aries-vcx based message mediator service](https://lf-hyperledger.atlassian.net/wiki/spaces/INTERN/pages/21960090/Project+Plan+-+aries-vcx+based+message+mediator+service)
  - Current implementation: [https://github.com/hyperledger/aries-vcx/tree/main/agents/rust/mediator](https://github.com/hyperledger/aries-vcx/tree/main/agents/rust/mediator)
  - [Links: Useful research, analysis and general guide.](https://lf-hyperledger.atlassian.net/wiki/spaces/INTERN/pages/21960219/Links+Useful+research+analysis+and+general+guide.)
- Open Discussion about direction and energy spend
  
  - Unqualified DIDs?
  - DIDComm v2?
  - OID4VC Protocols?
    
    - EUDI compatibility
  - Next AIP?
- did:peer:2 Update - Daniel Bluhm
  
  - Ready to merge: [https://github.com/decentralized-identity/peer-did-method-spec/pull/62](https://github.com/decentralized-identity/peer-did-method-spec/pull/62)
- Unqualified DIDs
  
  - DID Rotation
    
    - [https://github.com/hyperledger/aries-rfcs/pull/794](https://github.com/hyperledger/aries-rfcs/pull/794)
  - did:peer:4
    
    - [https://github.com/decentralized-identity/peer-did-method-spec/pull/61](https://github.com/decentralized-identity/peer-did-method-spec/pull/61) (pr to method)
    - [https://github.com/decentralized-identity/peer-did-method-spec/issues/58](https://github.com/decentralized-identity/peer-did-method-spec/issues/58) (original post)
    - [Browser Resolver Demo](https://dbluhm.github.io/did-peer-4-ts/?did=did%3Apeer%3A4zQmd8CpeFPci817KDsbSAKWcXAE2mjvCQSasRewvbSF54Bd%3Az2M1k7h4psgp4CmJcnQn2Ljp7Pz7ktsd7oBhMU3dWY5s4fhFNj17qcRTQ427C7QHNT6cQ7T3XfRh35Q2GhaNFZmWHVFq4vL7F8nm36PA9Y96DvdrUiRUaiCuXnBFrn1o7mxFZAx14JL4t8vUWpuDPwQuddVo1T8myRiVH7wdxuoYbsva5x6idEpCQydJdFjiHGCpNc2UtjzPQ8awSXkctGCnBmgkhrj5gto3D4i3EREXYq4Z8r2cWGBr2UzbSmnxW2BuYddFo9Yfm6mKjtJyLpF74ytqrF5xtf84MnGFg1hMBmh1xVx1JwjZ2BeMJs7mNS8DTZhKC7KH38EgqDtUZzfjhpjmmUfkXg2KFEA3EGbbVm1DPqQXayPYKAsYPS9AyKkcQ3fzWafLPP93UfNhtUPL8JW5pMcSV3P8v6j3vPXqnnGknNyBprD6YGUVtgLiAqDBDUF3LSxFQJCVYYtghMTv8WuSw9h1a1SRFrDQLGHE4UrkgoRvwaGWr64aM87T1eVGkP5Dt4L1AbboeK2ceLArPScrdYGTpi3BpTkLwZCdjdiFSfTy9okL1YNRARqUf2wm8DvkVGUU7u5nQA3ZMaXWJAewk6k1YUxKd7LvofGUK4YEDtoxN5vb6r1Q2godrGqaPkjfL3RoYPpDYymf9XhcgG8Kx3DZaA6cyTs24t45KxYAfeCw4wqUpCH9HbpD78TbEUr9PPAsJgXBvBj2VVsxnr7FKbK4KykGcg1W8M1JPz21Z4Y72LWgGQCmixovrkHktcTX1uNHjAvKBqVD5C7XmVfHgXCHj7djCh3vzLNuVLtEED8J1hhqsB1oCBGiuh3xXr7fZ9wUjJCQ1HYHqxLJKdYKtoCiPmgKM7etVftXkmTFETZmpM19aRyih3bao76LdpQtbw636r7a3qt8v4WfxsXJetSL8c7t24SqQBcAY89FBsbEnFNrQCMK3JEseKHVaU388ctvRD45uQfe5GndFxthj4iSDomk4uRFd1uRbywoP1tRuabHTDX42UxPjz)
  - **DID Exchange with no DID Document / Signature** - [https://github.com/hyperledger/aries-rfcs/issues/717](https://github.com/hyperledger/aries-rfcs/issues/717)
    
    - [https://github.com/hyperledger/aries-rfcs/pull/795](https://github.com/hyperledger/aries-rfcs/pull/795)
  - Community Coordinated Update
    
    - [https://github.com/hyperledger/aries-rfcs/pull/793](https://github.com/hyperledger/aries-rfcs/pull/793)
  - Aries Agent Test Harness update for testing support
- Open Tasks
  
  - LTS Policy
    
    - Fabric starting point: ([https://hyperledger.github.io/fabric-rfcs/text/0005-lts-release-strategy.html](https://hyperledger.github.io/fabric-rfcs/text/0005-lts-release-strategy.html))
- Open Discussion

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- State-of-union of Aries projects
- decorator for redirection after proofs. - existing?
- in the [Aug 9 call](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2023-08-09+Aries+Working+Group+Call?src=contextnavpagetreemode) there was talk about EUDI compatibility. Maybe tracking the progress every now and then in these calls? Has there been any discussion about adding SD-JWT and OID4VC stuff to Aries Interop test suite?

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
