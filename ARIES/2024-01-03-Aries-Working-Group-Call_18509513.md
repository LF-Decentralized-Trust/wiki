1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-01-03 Aries Working Group Call

Created by Sam Curren, last modified on Jan 03, 2024

## Summary:

- 2024 Aries Roadmap

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

## Date

03 Jan 2024 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (Petri Dish Development) &lt;amanji@petridish.dev&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;picolabs@sanbachs.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Welcome / Introductions

## Announcements

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
    
    - [0.10.5](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.10.5) Adds an important JSON-LD VC verification update
    - [0.11.0](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.11.0) has a full set of updates (includes 0.10.5 fix)
    - Addition of AnonCreds Rust library into ACA-Py now in main, using new wallet-type "askar-anoncreds"
      
      - Moving to ledger agnostic AnonCreds
    - Traction Sandbox now available - [https://traction-sandbox-tenant-ui.apps.silver.devops.gov.bc.ca](https://traction-sandbox-tenant-ui.apps.silver.devops.gov.bc.ca)
      
      - [Workshop Tutorial for using Traction, AnonCreds and Aries](https://docs.google.com/document/d/1QomkhJ6hDdxdDcYLA6wn-2VLBocotNp00xSQVwIriAE/edit?usp=sharing)
      - Repo - [https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo](https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo)
  - Agent-Framework-JavaScript  [https://github.com/openwallet-foundation/agent-framework-javascript](https://github.com/openwallet-foundation/agent-framework-javascript/discussions/1586#discussioncomment-7815973), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - Accepted by TAC in OWF, repository has moved. See initial announcement here: [https://github.com/openwallet-foundation/agent-framework-javascript/discussions/1586#discussioncomment-7815973](https://github.com/openwallet-foundation/agent-framework-javascript/discussions/1586#discussioncomment-7815973)
    - Looking for a new name, feel free to weigh in here: [https://github.com/openwallet-foundation/agent-framework-javascript/discussions/1668](https://github.com/openwallet-foundation/agent-framework-javascript/discussions/1668)
    - 0.5 in the works
      
      - Dropping IndySDK
      - AnonCreds Revocation
      - Dropping Node 16 support (EOL)
    - Continuing working on SD-JWT and OpenID4VC support
    - Started work on W3C issuance and verification of AnonCreds credentials
    - PR open for did:peer:4 support and did rotate protocol
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

- 2023 What Happened?
  
  - Unexpected potholes?
    
    - Expected faster progress on AIP 2
  - OWF emergence
    
    - Alignment / difference discovery
  - What progress was made?
    
    - Rework within projects
    - library work
    - dependency cleanup  - more involved than anticipated
    - Tuning given deployment experience
- 2024 Aries Roadmap
  
  - Annual Report due end of Jan, meeting early feb
    
    - [Overview of the Annual Report process](https://toc.hyperledger.org/governing-documents/project-annual-review.html) from the Hyperledger TOC
    - (More attendees than normal at the presentation to the TOC)
    - Aries, AnonCreds, and Indy all on the same schedule
  - Complete Unqualified DIDs CCU
  - Awareness / Marketing
    
    - Publishing a scalability report
    - Visibility for implementations and deployments
    - Bhutan - Verity
  - Alignment / Interop Efforts
    
    - JFF PlugFest
    - Aries Interopathon
    - OWF
    - Open Agent Framework
    - Etc.
  - AIP 2 completion
  - AIP 3 definition
    
    - DIDComm v2 / Trust Spanning Layer
  - Ledger Agnostic AnonCreds support within Aries projects
  - OID4VC Protocol support
  - LTS Efforts
  - Aries RFC
    
    - Aries RFC Status Review
    - Aries RFC Publishing in nice format
    - Better 'Start Here' Documentation
  - Cloud Reaching Ideas
    
    - Let's discuss next week
    - Mobile fragmentation (protocol/format/crypto/versions of all)
- WG Changes for 2024?
  
  - DIDComm related work
    
    - inclusion of (instead of linking) externally defined RFCs
    - possible code updates / replacement for didcomm.org
    - DIDComm UG needs better input on time slots for meeting
  - Alignment
    
    - DIDComm UG
    - OWF
      
      - AFJ has moved and might be renamed.
    - Open Enterprise Agent Framework – [https://github.com/hyperledger-labs/open-enterprise-agent](https://github.com/hyperledger-labs/open-enterprise-agent)
  - Cross org checkins on a monthly(?)/quarterly basis?
- Open Discussion

## Other Business

## Future Topics

- State of the Aries
  
  - What have we accomplished
  - What is on deck for next year?
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

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
