1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-09-25 Aries Working Group Call

Created by Stephen Curran, last modified on Sep 27, 2024

## Summary:

- Update on the move of ACA-Py and other Aries Repos to OWF
- PR to RFC 0721 Revocation Notification to support "Unrevoke"
- Action Menu Demonstration and Protocol Improvement Proposals – Dave McKay
- Open Discussion

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

![antitrust-policy-notice.png](https://github.com/LF-Decentralized-Trust/governance/blob/845bf277e246fa2be73be260f57b645b8aa84838/tac/meeting-minutes/images/antitrust-policy-notice.png?raw=true)

![](https://raw.githubusercontent.com/LF-Decentralized-Trust/governance/717c2020287a32594adff365c898b6bfe90d630a/tac/meeting-minutes/images/all-are-welcome.png)

LF Decentralized Trust is committed to creating a safe and welcoming

community for all. For more information

please visit the [LFDT Code of Conduct](https://lf-decentralized-trust.github.io/governance/governing-documents/code-of-conduct.html).

## Attendees:

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio.tech) &lt;sam@indicio.tech&gt;

## Welcome / Introductions

## Announcements

- [Aries BBS Go](https://github.com/hyperledger/aries-bbs-go) has been created, and a [VC-DI-BBS Go implementation has been added as a Hyperledger Lab](https://labs.hyperledger.org/labs/jsonld-vc-bbs-go.html)
- did:tdw - Moved to DIF. Regular meetings are happening – tomorrow for second one.
  
  - Meeting Agenda and Zoom link: [https://hackmd.io/k4cIK9vQSlaeg2pdHE51IQ?view](https://hackmd.io/k4cIK9vQSlaeg2pdHE51IQ?view)

Release Status and Work Updates

- Implementations:
  
  - Aries Cloud Agent Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: [https://aca-py.org](https://aca-py.org)
  - Credo [https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts/discussions/1586#discussioncomment-7815973), Meetings: [Credo Meetings](https://wiki.openwallet.foundation/display/CREDO/Meeting+notes)
  - Bifold Wallet -- [https://github.com/openwallet-foundation/bifold-wallet](https://github.com/openwallet-foundation/bifold-wallet) Meetings: [Bifold Meetings](https://wiki.openwallet.foundation/display/BIFOLD/Meeting+notes)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Proposal to move Aries VCX to the Open Wallet Foundation - [https://github.com/hyperledger/aries-vcx/discussions/1285](https://github.com/hyperledger/aries-vcx/discussions/1285)
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

- Future of Aries Discussion--Project Proposals accepted by OWF
  
  - Updates
  - Execution
    
    - Meeting adjustments
    - Actually Moving Repos
    - Pipeline adjustments
    - Marketing - Sam to drive prep
      
      - ACA-Py 1.0/Move to OWF announcement
- PR Review
  
  - Unrevoke
    
    - [https://github.com/hyperledger/aries-rfcs/pull/851](https://github.com/hyperledger/aries-rfcs/pull/851)
- Action Menu Demonstration and Protocol Improvement Proposals – Dave McKay
- Open Discussion

## Future Topics

- Mid-Transition Work Items
  
  - Continued project advancement
    
    - No need to adjust code contributions
  - Community Coordinated Updates

<!--THE END-->

- - - Unqualified DIDs 
      
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
- In person offline presentation
  
  - Transport
    
    - BLE DIDComm transport
    - ISO/mDL
  - Caching Strategies
    
    - Knowing what to cache
      
      - Credential Trust Establishment spec
    - Keeping things cached, and use cached state
      
      - verifier decides if it's new enough
    - revocation check
    - don't include proof of non-revocation if not asked
      
      - can't be ignored?
  - don't do indy edits on cred defs and schemas
    
    - is this already a rule? if not, it should be.
    - edit rule does exist. but why?
- Interopathon?
  
  - Discuss post EIC
  - Virtual
  - potential target end of july
  - participants
    
    - Aries /  ACA-Py
    - Credo
    - Veramo
    - Identus
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

## Other Business

## Future Topics

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
