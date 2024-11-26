1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-09-27 Aries Working Group Call

Created by Sam Curren, last modified by Sean Bohan on Sep 27, 2023

## Summary:

- Unqualified DIDs
- Credential Protocols
- AFJ OWF Proposal

## Date

27 Sep 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Samuel Rinnetmäki](https://lf-hyperledger.atlassian.net/wiki/people/712020:b4cba51f-8e9c-44db-9269-a7d19161f716?ref=confluence) (Findynet) &lt;samuel.rinnetmaki@findy.fi&gt;
- Kimmo Hovi (Findynet) &lt;ext.kimmo.hovi@findy.fi&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (OPS) &lt;tim.bloomfield@ontario.ca&gt;
- [John Jordan](https://lf-hyperledger.atlassian.net/wiki/people/557058:1368af8b-9c11-4aa7-9519-52fcc6683f1f?ref=confluence) (BCGov) &lt;john.jordan@gov.bc.ca&gt;
- [Sean Bohan](https://lf-hyperledger.atlassian.net/wiki/people/634eef0301c2ff842c15f9e7?ref=confluence) (Hyperledger Foundation) &lt;sbohan@linuxfoundation.org&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) (Animo Solutions) &lt;karim@animo.id&gt;
- [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) (Entidad) (jorge@entidad.io)

## Welcome / Introductions

## Announcements

- Oct 10-12 IIW
- HL Member Summit Oct 23 in SF and Tokyo

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
    
    - Patch Release 0.10.2 is about to be released. A couple of regression fixes that might impact some deployments.
      
      - 0.10.2 has been released
      - 0.10.3 in process for one more tweak
    - SD-JWT support merged - 0.11 as target
    - DID Rotate in PR (WIP)
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - Version 0.4.0 released! - [https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0](https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0) - HUGE!
    - 0.4.1 released
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Release 0.56.0 [https://github.com/hyperledger/aries-vcx/releases/tag/0.56.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.56.0)
    - Ongoing refactoring
    - finished migration to IndyVDR
    - Indy CredX up soon
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
  
  - Longer description added to Aries landing page on Hyperledger website: [https://www.hyperledger.org/projects/aries](https://www.hyperledger.org/projects/aries)
  - New Wiki page going live shortly: [New Hyperledger Aries Draft](/wiki/pages/createpage.action?spaceKey=ARIES&title=New%20Hyperledger%20Aries%20Draft&linkCreation=true&fromPageId=18507826)
  - We are exploring resource for short Aries introductory animated video
  - Join our marketing working group meeting, last Tuesday of every month (so next Tuesday!): [Aries Marketing Working Group](Aries-Marketing-Working-Group_18505802.html)
- Patrik: Issue Credential Protocol V2
  
  - multiple credential formats
  - supporting negotiation of credential types?
- AFJ OWF Proposal
  
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/1586](https://github.com/hyperledger/aries-framework-javascript/discussions/1586)
  - Org migrations should be done with a transfer of the repo
    
    - maintains links &amp; commit history
    - Move is far better than a fork.
  - Should discuss which components would be moved simultaneously
    
    - Probably at least Bifold and Askar
  - What to do with the RFCs?
  - Interoperability: are .Net and Go implementations still interoperable with the latest RFCs and interop suite?
    
    - .Net already moved to OWF
  - OWF policy: maintainers are in charge of the repositories and decisions (same as in Hyperledger)
  - AJF would probably be the most mature wallet framework, so OWF would have an incentive to promote and market it
- Unqualified DIDs
  
  - DID Rotation
    
    - [https://github.com/hyperledger/aries-rfcs/pull/794](https://github.com/hyperledger/aries-rfcs/pull/794)
  - did:peer:4
    
    - [https://github.com/decentralized-identity/peer-did-method-spec/pull/61](https://github.com/decentralized-identity/peer-did-method-spec/pull/61) (pr to method)
    - [https://github.com/decentralized-identity/peer-did-method-spec/issues/58](https://github.com/decentralized-identity/peer-did-method-spec/issues/58) (original post)
  - DID Exchange with no DID Document / Signature - [https://github.com/hyperledger/aries-rfcs/issues/717](https://github.com/hyperledger/aries-rfcs/issues/717)
    
    - [https://github.com/hyperledger/aries-rfcs/pull/795](https://github.com/hyperledger/aries-rfcs/pull/795)
  - Community Coordinated Update
    
    - [https://github.com/hyperledger/aries-rfcs/pull/793](https://github.com/hyperledger/aries-rfcs/pull/793)
  - Aries Agent Test Harness update for testing support
- Beta v2 mediator with websocket support.
  
  - [https://indicio-tech.github.io/mediator/beta](https://indicio-tech.github.io/mediator/beta)
- DIDComm V2 Demo: [https://indicio-tech.github.io/didcomm-demo/](https://indicio-tech.github.io/didcomm-demo/) ([Github Repo](https://github.com/Indicio-tech/didcomm-demo))
- Open Tasks
  
  - LTS Policy
    
    - Fabric starting point: ([https://hyperledger.github.io/fabric-rfcs/text/0005-lts-release-strategy.html](https://hyperledger.github.io/fabric-rfcs/text/0005-lts-release-strategy.html))
- Open Discussion

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- |State-of-union of Aries projects
- decorator for redirection after proofs. - existing?
- in the [Aug 9 call](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2023-08-09+Aries+Working+Group+Call?src=contextnavpagetreemode) there was talk about EUDI compatibility. Maybe tracking the progress every now and then in these calls? Has there been any discussion about adding SD-JWT and OID4VC stuff to Aries Interop test suite?

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
