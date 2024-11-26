1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-04-27 Aries Working Group Call

Created by Stephen Curran, last modified by Philippe Foucault on May 09, 2022

## Summary:

- eContinued: Updating from unqualified DIDs to fully formed DIDs / Adoption of did:indy DIDs
- Present Proof 1 of N Problem

## Recording: [dummyfile.txt](#)

- Extraction: [Proposed RFC](https://hackmd.io/0PP3vrq7Qb2oD5wja8kLcQ?edit) Transition to use qualified DIDs - [dummyfile.txt](#)
- Extraction: Presentation Request for "1 of N Credentials" problem/solutions - [Slides](https://docs.google.com/presentation/d/1wKhGpkMuGtLGmxcr4-BqkFRK9ijqjXtUN25776uKeIo/edit?usp=sharing) - [dummyfile.txt](#)

## Date

27 Apr 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;

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

Continued Discussion:

- Updating from unqualified DIDs to fully formed DIDs - Timo 
  
  - Draft Community Coordinated Update RFC: [https://hackmd.io/0PP3vrq7Qb2oD5wja8kLcQ?edit](https://hackmd.io/0PP3vrq7Qb2oD5wja8kLcQ?edit)
- Adoption of did:indy DIDs - Stephen
  
  - CredX for the shared components
  - Also need updates for Indy SDK
    
    - Point about the did

AnonCreds Proof Request Challenge:

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

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496216/18516218.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496216/18516217.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496216/18516216.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
