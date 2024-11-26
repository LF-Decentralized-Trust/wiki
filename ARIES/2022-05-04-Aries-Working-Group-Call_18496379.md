1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-05-04 Aries Working Group Call

Created by Sam Curren on May 04, 2022

## Summary:

- IIW Review
- Continued: Updating from unqualified DIDs to fully formed DIDs / Adoption of did:indy DIDs
- Present Proof 1 of N Problem

## Date

04 May 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Shared Components - Indy SDK replacements
  
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs,)
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr,)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - 0.2.5 release - performance/load work and testing – specific load errors reduced (down to 0.05% error rate), performance up 11%
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - Working on 0.2.0 release
      
      - Issue Credential / Present Proof v2
      - OOB / DIDExchange
      - Merged: Holder revocation with revocation notifications support
    - PR open to support lower versions of a protocol
    - Started working on JSON-LD and BBS+ credential support
    - Started working on writing a wrapper for Indy VDR for React Native – Almost ready now
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html)) 
    
    - Working on support for DIDComm v2, Credential Manifest, OOB v2 and v3 credential protocols (for DIDComm v2)
    - [RFC 700](https://github.com/hyperledger/aries-rfcs/pull/700) to enable web wallets
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-service-mediator](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries-Toolbox
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Notes:

## Discussion Topics

- IIW Review
  
  - Verified Connections - James Ebert
  - Machine Readable Governance
    
    - New working group
  - JSON-LD Credential Profiles
    
    - "How do we make JSON-LD Credentials suck less?"
    - [https://github.com/decentralized-identity/interoperability/discussions/63](https://github.com/decentralized-identity/interoperability/discussions/63)
  - DIDComm
    
    - Control Channel concept well received
    - Work 'started' to provide action integration with GNAP with Justin Richter
  - Interoperability
    
    - Labeling Interoperability (Sam): [https://indicio.tech/wp-content/uploads/2022/04/Indicio\_Report\_TrustVerifiableCredentialsInteroperability\_040622.pdf](https://indicio.tech/wp-content/uploads/2022/04/Indicio_Report_TrustVerifiableCredentialsInteroperability_040622.pdf)
    - What phase of interop/community development are we in?
  - Not all good news
    
    - Continued False Perception about Aries interop only based on universal libIndy use.
    - Circulating false perceptions about predicates not working on dates.
- Fully Qualified DIDs Transition
  
  - Summary
  - Community Coordiated RFC?
  - Draft Community Coordinated Update RFC: [https://hackmd.io/0PP3vrq7Qb2oD5wja8kLcQ?edit](https://hackmd.io/0PP3vrq7Qb2oD5wja8kLcQ?edit)
- Adopting did:indy - Stephen
  
  - CredX for the shared components
  - Also need updates for Indy SDK
    
    - Point about the did
- AnonCredsProve 1 of N
  
  - Summary of last week

AnonCreds Proof Request Challenge: (last week notes)

- Holder has one of N credentials with different schema, issuers
- Is there a single AnonCreds proof request that allows the holder to construct and proof that can be verified for that scenario?
- Assuming you can't - what can we do?
  
  - Present Proof [Negotiation](https://github.com/hyperledger/aries-rfcs/tree/main/features/0454-present-proof-v2#negotiation-and-preview)
  - Modification to the Present Proof "[request-presentation](https://github.com/hyperledger/aries-rfcs/tree/main/features/0454-present-proof-v2#request-presentation)" message semantics to allow multiple proof requests
  - Use DIF Presentation Exchange with AnonCreds
  - Other ideas?

## Other Business

## Future Topics

- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

  File Modified

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
