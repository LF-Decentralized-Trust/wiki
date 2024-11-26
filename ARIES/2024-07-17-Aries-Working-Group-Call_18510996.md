1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-07-17 Aries Working Group Call

Created by Sam Curren, last modified on Jul 17, 2024

## Summary:

- Aries Charter Review

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

## Date

17 Jul 2024 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

move ![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Consultant) &lt;james@jamesebert.dev&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio) &lt;kim@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/712020:fa274eca-d9bb-44bf-868a-fe2ab12d850f?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Implementations:
  
  - Aries Cloud Agent Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: [https://aca-py.org](https://aca-py.org)
  - Credo [https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts/discussions/1586#discussioncomment-7815973), Meetings: [Credo Meetings](https://wiki.openwallet.foundation/display/CREDO/Meeting+notes)
  - Bifold Wallet -- [https://github.com/openwallet-foundation/bifold-wallet](https://github.com/openwallet-foundation/bifold-wallet) Meetings: [Bifold Meetings](https://wiki.openwallet.foundation/display/BIFOLD/Meeting+notes)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Are you using the Indy SDK for Aries VCX, please let us know, as we're looking to remove support from Aries VCX - [https://github.com/hyperledger/aries-vcx/issues/1250](https://github.com/hyperledger/aries-vcx/issues/1250)
  - Picos as of pico-engine version 1.3.0 natively use DIDComm v2 ([https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md](https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md))
- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
- [aries-endorser-service](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries Akrida](https://github.com/Indicio-tech/aries-akrida) - Load Testing DIDComm based protocols

## Discussion Topics

- Charter Review:
  
  - LFDT: [https://www.linuxfoundation.org/press/linux-foundation-announces-intent-to-form-lf-decentralized-trust](https://www.linuxfoundation.org/press/linux-foundation-announces-intent-to-form-lf-decentralized-trust)
  - Charter Draft: [https://docs.google.com/document/d/1F6RbR7xDaBt5CDJhqLJzR4c1pDJtyPGshp9fy6eVtSM/edit](https://docs.google.com/document/d/1F6RbR7xDaBt5CDJhqLJzR4c1pDJtyPGshp9fy6eVtSM/edit)\\
    
    - Changes in suggest mode
  - LF Charter: [https://www.hyperledger.org/about/charter](https://www.hyperledger.org/about/charter)
  - Discussion Topics:
    
    - Stated Purpose of Project
      
      - "create shared, reusable, interoperable, and scalable agents for developing critical decentralized trust solutions, including the use of verifiable credentials and communication technologies."
      - intent is to be DID method, credential type, and communication protocol agnostic. ledgers are acceptable but not required
      - we expect these agents to represent organizations, people, and things, and take action by direct subject interaction and also subject approved automation
      - From ChatGPT based on the above:
        
        - \### Stated Purpose of the Hyperledger Aries Project
          
          The Hyperledger Aries Project aims to create shared, reusable, interoperable, and scalable agents for developing critical decentralized trust solutions, including verifiable credentials and communication technologies. It is designed to be agnostic regarding DID methods, credential types, and communication protocols, with ledgers being optional. These agents will represent organizations, people, and things, capable of taking actions through direct interaction or subject-approved automation, fostering robust and flexible decentralized trust solutions.
    - TSC membership and chair
      
      - Membership is currently MAINTAINERS documented
        
        - [https://github.com/hyperledger/aries-rfcs/blob/main/MAINTAINERS.md](https://github.com/hyperledger/aries-rfcs/blob/main/MAINTAINERS.md)
        - [https://github.com/hyperledger/aries/tree/main](https://github.com/hyperledger/aries/tree/main) (no MAINTAINERS file)
          
          - current list is NOT in the file?
            
            - yaml files all in a single repo?
              
              - [https://github.com/hyperledger/governance/blob/main/access-control.yaml](https://github.com/hyperledger/governance/blob/main/access-control.yaml)
            - stephen to talk to Ry about how this is expected to work in the new org.
      - How is membership determined?
        
        - Start with who is there (where is there)
        - any person on any team with maintainer or above on any aries repository
          
          - code to generate this
          - TSC members approve the PRs that add them as a maintainer.
        - maintainers of the Aries (main / RFCs) repo
          
          - Simpler than ALL repos
        - added/removed
      - Chair is primary contact with LFDT
        
        - Who steps backwards the slowest.
      - Meetings?
        
        - Regular meeting functions as the TSC meeting.
    - IP/License
      
      - Apache 2

<!--THE END-->

- Unqualified DIDs 
  
  - [https://hyperledger.github.io/aries-rfcs/latest/features/0793-unqualfied-dids-transition/](https://hyperledger.github.io/aries-rfcs/latest/features/0793-unqualfied-dids-transition/)
  - Progress?
    
    - ACA-Py working on 1.0, this will be the SECOND major release (0.12.1) of ACA-Py that has accomplished step 1
    - Ongoing successful testing with Credo.
  - did:indy handling
    
    - unqualified anoncreds objects being rejected
    - did:indy changes the unique identifier within the DID. both the old method and the new method *should* work.
    - Credo is using did:indy only, cannot resolve unqualified asset identifiers.
    - Rushed work to address within [AnonCreds RS](https://github.com/hyperledger/anoncreds-rs/pull/335) ( ? ) and ACA-Py.
    - quicker fix in Credo, longer fix in everything.
  - PRs for adoption status welcome
- OOB Invitation / DID Exchange CCU
  
  - [https://hyperledger.github.io/aries-rfcs/latest/features/0496-transition-to-oob-and-did-exchange/](https://hyperledger.github.io/aries-rfcs/latest/features/0496-transition-to-oob-and-did-exchange/)
  - Step 1 (Accept OOB Invitations) needs confirmation - Please Do This.
    
    - Bifold using OOB, but then connections (allowed for transitions)
  - Step 2 - use OOB and implement DID Exchange
  - Known systems possibly still using Connection Invitations
    
    - Lissi
    - Dock
    - GlobalID
    - Trinsic
  - PRs for adoption status welcome
- DIDComm v2 adoption
  
  - ACA-Py progress shared last week
    
    - PR made for initial support. first round trip support.
  - Any other updates?
  - Credo has the beginnings of DIDComm v2, but does need some attention.
- Interopathon?
  
  - Discuss post EIC
  - Virtual
  - potential target end of july
  - participants
    
    - Aries /  ACA-Py
    - Credo
    - Veramo
  - scope
    
    - unqualified DIDs gone
      
      - did rotation
      - v1 - v2
    - DIDComm v2
      
      - trust ping?
      - discover features?
      - basicmessage?
      - did rotation after connection
      - didcomm demo interaction
    - advanced tasks
      
      - credential issuance / presentation
- Open Discussion
  
  - Validation of printed OOB Invitations
    
    - DID must be present in governance file?
    - Proof provided according to matching governance files.
    - prove well known dids other than the current connection.
  - JSON-LD creds impl within ACA-Py no longer working with Credo 0.5.0
    
    - Sphereon library using for Presentation Exchange objects is not expecting quite the same things, additional fields.
    - Daniel working through and testing, will report / create issues on the appropriate repos.
    - Updates?
    - Fix merged into ACA-Py. 
      
      - funny interactions between the speheron libraries and credo about presentation exchange. - issues raised to Timo et. al.
  - Protocol RFC
    
    - Harmonize Chat
      
      - [https://github.com/decentralized-identity/didcomm.org/pull/106/files](https://github.com/decentralized-identity/didcomm.org/pull/106/files)
    - Sub connection-Ariel
      
      - new DID for the connection.
  - QR code short URLs / redirect to large invitations / deep linking in a way that works with iOS and Android
    
    - [https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0700-oob-through-redirect/README.md](https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0700-oob-through-redirect/README.md)
    - BCGov working on something similar.
- Mediator Reconfig revisit
  
  - (from last week)
  - 3 new messages
    
    - updatedconfig - new routing DID
      
      - note about timing or avoiding causing a traffic stampede as a result.
    - ack- received by
    - updated downstream (keylist updates as alternative?)
  - need for this:
    
    - anytime a mediator needs to change the routing DID
    - static DID, but also other cases.
  - loss of data at the mediator
    
    - all routes lost.

## Other Business

## Future Topics

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
