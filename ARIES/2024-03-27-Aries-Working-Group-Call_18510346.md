1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-03-27 Aries Working Group Call

Created by Sam Curren, last modified by Stephen Curran on Apr 02, 2024

## Summary:

- Aries RFC MkDocs
- DIDComm v2 Credential protocol updates
- Basis for common identifiers

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

## Date

27 Mar 2024 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) (2060.io) &lt;a@2060.io&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/712020:fa274eca-d9bb-44bf-868a-fe2ab12d850f?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- @Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;picolabs@sanbachs.com&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio) &lt;kim@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Welcome / Introductions

## Announcements

- IIW - April 16-18
- There had been a number of BCovrin (dev, test, greenlight, etc.) Indy ledgers, all now point to BCovrin Test (e.g. genesis files all point to the same ledger).
  
  - BCovrin Test is the one that many Mobile Wallets use for testing. It will remain available indefinitely.

Release Status and Work Updates

- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    
    - PR merged for caching in Indy VDR of Pool Transactions - Aries Frameworks should be adding that to
    - Release 0.4.0
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
    
    - [0.12.0rc0](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.12.0rc0) – Peer DID support, many enhancement/fixes, nothing breaking yet but at least one will be made before finalized.
    - [Release 1.0.0 Checklist](https://github.com/hyperledger/aries-cloudagent-python/issues/2753) has been created and is being worked on.
    - Traction Sandbox now available - [https://traction-sandbox-tenant-ui.apps.silver.devops.gov.bc.ca](https://traction-sandbox-tenant-ui.apps.silver.devops.gov.bc.ca)
      
      - [Workshop Tutorial for using Traction, AnonCreds and Aries](https://docs.google.com/document/d/1QomkhJ6hDdxdDcYLA6wn-2VLBocotNp00xSQVwIriAE/edit?usp=sharing)
      - Repo - [https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo](https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo)
  - Credo (Agent-Framework-JavaScript)  [https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts/discussions/1586#discussioncomment-7815973), Meetings: [Credo Meetings](Framework-JS-Meetings_18482467.html)
    
    - 0.5 shipped!
      
      - Dropping IndySDK
      - AnonCreds Revocation
      - Dropping Node 16 support (EOL)
      - W3C issuance and verification of AnonCreds credentials
      - did:peer:2 and  did:peer:4 support and did rotate protocol
    - Continuing working on SD-JWT and OpenID4VC support
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
- [Aries Akrida](https://github.com/Indicio-tech/aries-akrida) - Load Testing DIDComm based protocols
  
  - Added module support for different Issuer and Verifiers

## Discussion Topics

- Aries RFC MkDocs Demo and Feedback - Stephen
- VCX Update - Patrik Stas
  
  - Rust implementation of Aries/DIDComm
  - Absa leaving the SSI space - will impact VCX development.
  - contact on Hyperledger discord: patrikstas
  - More discussion next week on the agenda (5+ min)
- DIDComm v2 conversion
  
  - (Notes from previous weeks)
    
    - Smaller changes may mean faster adoption
    - negotiation pulled out into a sibling protocol - (nobody using negotation? Subhasis referenced use.)
      
      - propose message moves to different family.
    - Document the short-circuted use of the protocol that starts at issuance directly, depending on needs of credential type.
    - we need to be careful not to match protocol to UX human steps on a 1 to 1 basis
    - abandoned state - if a user declines to present, what should happen between the holder and verifier?
      
      - problem report sent (or no message, see below) on decline - should be documented
    - explicit 'no' messages instead of a problem report when it's an explicit no, instead of an error.
    - document use of timeout for offers (didcomm v2 friendly, perhaps a field within the protocol.Credential Protocols for DIDComm v2
  - Any Volunteers?
- Basis for common identifiers
  
  - Long time since discussion
  - Governance has come a long way: [https://github.com/decentralized-identity/credential-trust-establishment](https://github.com/decentralized-identity/credential-trust-establishment)
  - [530](https://github.com/hyperledger/aries-rfcs/pull/530) - human readable verifiable identifier
  - [535](https://github.com/hyperledger/aries-rfcs/pull/535) - email access governance framework
  - building blocks
    
    - did that represents a web resource such as a document.
    - did has aka web uri
    - VC as used as a signed document.

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- decorator for redirection after proofs. - existing?
- in the [Aug 9 call](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2023-08-09+Aries+Working+Group+Call?src=contextnavpagetreemode) there was talk about EUDI compatibility. Maybe tracking the progress every now and then in these calls? Has there been any discussion about adding SD-JWT and OID4VC stuff to Aries Interop test suite?

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
