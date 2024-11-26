1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-05-01 AnonCreds v2.0 Working Group Meeting

Created by Stephen Curran, last modified on May 01, 2023

## Summary

- Reviewing the proposed data models for AnonCreds v2.0 - [https://hackmd.io/ZlsnLoclSveePJOZljgMfA](https://hackmd.io/ZlsnLoclSveePJOZljgMfA)
- Revocation using zk-SAM
- Open Discussion

## Recording of Call:  [dummyfile.txt](#)

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Related Repositories:

- Mike Lodder's proposed Data Models: [https://hackmd.io/ZlsnLoclSveePJOZljgMfA](https://hackmd.io/ZlsnLoclSveePJOZljgMfA)
- AnonCreds v2.0 Specification Repository: [https://github.com/hyperledger/anoncreds-spec-v2/](https://github.com/hyperledger/anoncreds-spec-v2/)
- AnonCreds v1.0 Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Goals of the Working Group:

The goal of AnonCreds v2.0 is to retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security.

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - AnonCreds Workshop presented by Hyperledger is planned for May 31, 2023, 8:00 Pacific / 17:00 Central Europe. Details to be shared.
  - I'll be talking at the Linux Foundation Open Source Summit, Metaverse Conference about Hyperledger AnonCreds and ZKPs.
- Updates to the Agenda?

## Agenda

- Proposed data models discussion given what [Mike Lodder](https://lf-hyperledger.atlassian.net/wiki/people/557058:23b28066-a30e-4a6b-9b86-34dae49fd7f0?ref=confluence) has presented and documented here: [https://hackmd.io/ZlsnLoclSveePJOZljgMfA](https://hackmd.io/ZlsnLoclSveePJOZljgMfA)
  
  - Issuing AnonCreds v1.0:
    
    - Schema – simple list of attribute names, schema name, version
      
      - Attribute type is dynamically implied by the data in the credential – string or integer
    - Credential Definition – a signing key for each attribute, an extra field that is the link secret
    - Credential
      
      - Raw and encoded claims
      - Signature is added
  - Issuing v2.0
    
    - From document – items:
      
      - Claims – Schema, Validators, Data
      - Credential Schema, Credential Definition
      - Credential
    - Proposal that types are defined in the AnonCreds specification
    - Claims Schema Repository
      
      - Name, ID, type, validators
      - QUESTION: Do we want to add the complexity/overhead of adding this element vs. keeping all of the information encapsulated in the Credential Schema Object
        
        - Could have an optional "ClaimsSchemaId" as optional in the "Credential Schema Object":
          
          - When included, only the Claims Name/ID need be included in the Credential Schema Object
          - When not included, the full Claims information (type, validators) must be included in the Credential Schema Object.
    - Credential Schema Object:
      
      - Name, Description (should also have version?)
      - Blindly Signed Claims Schema
        
        - Attribute name/ID from Claims Schema
      - Ordered List: Claims Schema
        
        - Attribute name/ID from Claims Schema, or
        - Attribute Name, ID, type, validators
    - Credential Definition Object
      
      - Keys necessary to sign credentials
        
        - Parameters per attribute – could be derived when using some signature schemes
      - ID of Schema Object
      - Revocation Registry – keys
    - Credential:
      
      - Claims
      - Signature
      - Revocation Registry Handle
      - Credential Definition ID
  - Signature Schemes
    
    - CL
    - BLS - doesn't support selective disclosure
    - BBS+ - IETF submitted version can be used
      
      - PQ unlikely – none known at this time.
    - PS - Mike, et. al (potentially including "S" in "PS") is taking this to IETF
      
      - Has a post-quantum version, but slower and bigger
        
        - Calculation for 5 claims – in the Credential Definition: Public Key 912 bytes, PQ version: 6KB, increasing linearly (6x bigger)
          
          - Proof: 300-400 bytes, PQ version: 24kb (50x bigger)
        - Could be public key could be fixed size 192b and then derive a per claim data parameter (tradeoff size vs. time)

## Future Calls

- Collect some use case specific examples and continue the discussions:
  
  - Applying the data structures to a real use case or two
    
    - Take an existing AnonCreds Schema (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/13)) and Credential Definition (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/14)) and define what it would be using Mike's proposed data models.
      
      - Where would the data models exist, such as on ledger, in the AnonCreds specification?
  - What concrete uses other than link-secret is there for blinded data in a credential?

## To Dos:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292216/20295140.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
