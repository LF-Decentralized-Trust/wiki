1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-12-06 Aries Working Group Call

Created by Sam Curren, last modified by Stephen Curran on Dec 15, 2023

## Summary:

- RPC / App Attestation Protocol
- Unqualified DID Checkin
- RFC Merge Review

## Recording: [https://youtu.be/sq5\_kFjlURE](https://youtu.be/sq5_kFjlURE)

## Date

06 Dec 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;picolabs@sanbachs.com&gt;
- [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) (Entidad) &lt;jorge@entidad.io&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) (2060.io) &lt;a@2060.io&gt;

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
    
    - [0.10.5](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.10.5) Adds an important JSON-LD VC verification update
    - [0.11.0](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.11.0) has a full set of updates (includes 0.10.5 fix)
    - Addition of AnonCreds Rust library into ACA-Py now in main, using new wallet-type "askar-anoncreds"
      
      - Moving to ledger agnostic AnonCreds
    - Traction Sandbox now available - [https://traction-sandbox-tenant-ui.apps.silver.devops.gov.bc.ca](https://traction-sandbox-tenant-ui.apps.silver.devops.gov.bc.ca)
      
      - [Workshop Tutorial for using Traction, AnonCreds and Aries](https://docs.google.com/document/d/1QomkhJ6hDdxdDcYLA6wn-2VLBocotNp00xSQVwIriAE/edit?usp=sharing)
      - Repo - [https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo](https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo)
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - OWF - shared in OWF list and discord, giving more time for feedback.
    - 0.5 in the works
      
      - Dropping IndySDK
      - AnonCreds Revocation
      - Dropping Node 16 support (EOL)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - aries-vcx as repository now contains 2 project families:
      
      - aries
      - didcore
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
- Aries Akrida - Load Testing DIDComm based protocols
  
  - AFJ 0.4.x upgrade in progress
  - Prepping for transition to Hyperledger (expected move later this week)
  - Shifting to TypeScript from Javascript

## Discussion Topics

- Aries marketing update - [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60da2fc7285656006a667081?ref=confluence) [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence)  
  
  - Logo complete
  - Marketing working group meeting yesterday
  - Next meeting is last Tuesday of January: [Aries Marketing Working Group](Aries-Marketing-Working-Group_18505802.html)
  - Q1 Interop event? - Discussion next week
- RPC / App attestation - Stephen
  
  - [https://github.com/hyperledger/aries-rfcs/pull/804](https://github.com/hyperledger/aries-rfcs/pull/804)
- Unqualified DIDs Checkin
  
  - Next Goal - Software Support (2023-12-17)
  - Issues?
- RFC Review
  
  - [0795](https://github.com/hyperledger/aries-rfcs/pull/795) - Add DID rotation signature to 0023
  - [0794](https://github.com/hyperledger/aries-rfcs/pull/794) - DID Rotate Protocol
  - [0793](https://github.com/hyperledger/aries-rfcs/pull/793) - Unqualified DID Community Coordinated Update
  - [0798](https://github.com/hyperledger/aries-rfcs/pull/798) - Fix Type in OCA RFC
  - [0799](https://github.com/hyperledger/aries-rfcs/pull/799) - LTS
  - [0801](https://github.com/hyperledger/aries-rfcs/pull/801) - Update unresolved questions in please ack

<!--THE END-->

- Open Discussion

## Other Business

## Future Topics

- Next Week - Mentee Demo on VCX/Traction
- State of AF-GO - New Maintainers or Archive?
- in Q1, projects are asked to do an annual report, review past year, plans for next year
  
  - More back and forth conversation. Multiple members need to attend presentation.
- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- State-of-union of Aries projects
- decorator for redirection after proofs. - existing?
- in the [Aug 9 call](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2023-08-09+Aries+Working+Group+Call?src=contextnavpagetreemode) there was talk about EUDI compatibility. Maybe tracking the progress every now and then in these calls? Has there been any discussion about adding SD-JWT and OID4VC stuff to Aries Interop test suite?

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
