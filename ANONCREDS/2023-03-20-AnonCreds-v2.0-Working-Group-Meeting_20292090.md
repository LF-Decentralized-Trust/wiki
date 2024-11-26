1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-03-20 AnonCreds v2.0 Working Group Meeting

Created by Stephen Curran, last modified on Mar 20, 2023

## Summary

- Proposed AnonCreds v2.0 Data Models - Presentation - Mike Lodder
- Open Discussion

## Recording of Call: [dummyfile.txt](#)

Segment – Awesome Presentation by Mike Lodder: [dummyfile.txt](#)

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
  
  - IIW – April 18-20 – Let's plan some presentations.
  - New v2.0 Specification Repository created.
- Updates to the Agenda

## Agenda

- Mike Lodder will continue a discussion of the Data Models he is proposing for AnonCreds v2.0, this time talking about Presentations
  
  - Data Models HackMD document:  [https://hackmd.io/ZlsnLoclSveePJOZljgMfA](https://hackmd.io/ZlsnLoclSveePJOZljgMfA)
  - Notes from Meeting:
    
    - Contents of the Issued Credential – easily mapped into other formats, such as the W3C VC Data Model.
      
      - Open question on where encoding occurs – within AnonCreds (better interoperability, less data to store, more computation) or by the Issuer.
    - PresentationSchema
      
      - A possibly published data structure used by the Verifier to ask for data from the Holder.
      - Atomic – when requested, a Proof based on a PresentationSchema is either proven or not.
      - Can use something like DIF Presentation exchange to AND/OR a set of PresentationSchemas in to a Presentation Request – plus adding an ID and a nonce.
      - Different types of proofs were covered – from plain signatures to range-proofs.
      - Different crypto can be used.
    - From Chat:
      
      - Is bulletproof more efficient than schnorr proofs?
        
        - Different purposes – Schnorr: Prove you know the hidden value, Bullet: Proof hidden value is in range.
      - Discussion of revocation scalability – details to be covered in a future meeting.
- Plans for IIW?
- Next Meeting (two weeks):
  
  - Suspension vs./as well as revocation?
  - Collect some use case specific examples and continue the discussions:
    
    - Applying the data structures to a real use case or two
      
      - Take an existing AnonCreds Schema (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/13)) and Credential Definition (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/14)) and define what it would be using Mike's proposed data models.
        
        - Where would the data models exist, such as on ledger, in the AnonCreds specification?
    - What concrete uses other than link-secret is there for blinded data in a credential?
  - ALLOSAUR Revocation

## Future Calls

## To Dos:

- Plan session for IIW on AnonCreds.

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292090/20295122.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292090/20295121.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
