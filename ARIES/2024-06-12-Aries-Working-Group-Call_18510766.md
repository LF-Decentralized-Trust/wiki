1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-06-12 Aries Working Group Call

Created by Sam Curren, last modified by Stephen Curran on Jun 13, 2024

## Summary:

- Catching Up
- Prioritizing Topics

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

## Date

12 Jun 2024 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

move ![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Instnt) &lt;james@jamesebert.dev&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Implementations:
  
  - Aries Cloud Agent Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: [https://aca-py.org](https://aca-py.org)
  - Credo [https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts/discussions/1586#discussioncomment-7815973), Meetings: [Credo Meetings](https://wiki.openwallet.foundation/display/CREDO/Meeting+notes)
  - Bifold Wallet -- [https://github.com/openwallet-foundation/bifold-wallet](https://github.com/openwallet-foundation/bifold-wallet) Meetings: [Bifold Meetings](https://wiki.openwallet.foundation/display/BIFOLD/Meeting+notes)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
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

- Pickup Protocol Review - James E.
  
  - [https://github.com/decentralized-identity/didcomm.org/pull/110](https://github.com/decentralized-identity/didcomm.org/pull/110)
- Draft abilities of DIDComm protocol versions
  
  - [https://hackmd.io/49ZNhgIHQ1Kn7DAmsQlHhw](https://hackmd.io/49ZNhgIHQ1Kn7DAmsQlHhw)
  - possibly full semver in next version?
  - not targeted before next major version of DIDComm
- Unqualified DIDs 
  
  - [https://hyperledger.github.io/aries-rfcs/latest/features/0793-unqualfied-dids-transition/](https://hyperledger.github.io/aries-rfcs/latest/features/0793-unqualfied-dids-transition/)
  - Progress?
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
  - PRs for adoption status welcome
- VDR Proxy
  
  - PR: [https://github.com/hyperledger/aries-rfcs/pull/832/files?short\_path=7976275#diff-797627530cc29d5c4aa7372d33251b624cdcf3133c2d666f47f961996967ce48](https://github.com/hyperledger/aries-rfcs/pull/832/files?short_path=7976275#diff-797627530cc29d5c4aa7372d33251b624cdcf3133c2d666f47f961996967ce48)
  - Team in Brazil has a solution?
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
