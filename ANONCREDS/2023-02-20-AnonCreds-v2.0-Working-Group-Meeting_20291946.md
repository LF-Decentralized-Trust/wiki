1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-02-20 AnonCreds v2.0 Working Group Meeting

Created by Stephen Curran, last modified on Feb 21, 2023

## Summary

- Getting Organized
- Goals of the Working Group
- What are we starting with?
- Open Discussion

## Recording of Call: [dummyfile.txt](#)

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

[Mike Lodder](https://lf-hyperledger.atlassian.net/wiki/people/557058:23b28066-a30e-4a6b-9b86-34dae49fd7f0?ref=confluence) &lt;redmike7@gmail.com&gt;

[Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence) (RootsID)&lt;alex.andrei@rootsid.com&gt;

[belsy yuen](https://lf-hyperledger.atlassian.net/wiki/people/557058:e119392d-95a0-402d-8442-6e4fcb3b5513?ref=confluence) (Nymlab)&lt;belsy@nymlab.it&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
- Updates to the Agenda

## Agenda

- [Presentation/Agenda Slides](https://docs.google.com/presentation/d/1RlZbId6EvOgIHQfndFDYtTb7zY_xjA3lyhE0vOU5hG0/edit?usp=sharing)
- Getting Organized
  
  - Bi-Weekly meetings on Mondays at 10:00 Pacific / 19:00 Central Europe starting Feb. 20, next meeting March 6
- Goals of the Working Group:
  
  - *The goal of AnonCreds v2.0 is to retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security.*
- What are we starting with?
  
  - Mike's proposal from the [AnonCreds Specification Working Group Meeting of 2022.11.28](https://lf-hyperledger.atlassian.net/wiki/display/ANONCREDS/2022-11-28+AnonCreds+Specification+Working+Group+Meeting)
    
    - Extends the definition of "Schema" to include a type of each claim based on how it can be used in a presentation
      
      - Extends the current AnonCreds (implicit) types of Integer, Hash and Scalar (blinded) to include:
        
        - Scalar defined by the issuer (not just the hidden blinded link secret)
        - Enumerated
        - Range (including negative)
        - Verified encrypted
      - Enables ZKPs on additional types of data, beyond the V1.0 predicates.
    - Covers issuer signing, presentation generation and verification.
    - Requires the same interactions as in the AnonCreds v1.0 specification
    - Enables the use of more signature schemes
      
      - Mike proposes we could choose to support:
        
        - CL Signatures
        - BBS+ Signatures
        - BLS Signatures
        - Pointcheval-Sanders (PS) - [https://eprint.iacr.org/2015/525](https://eprint.iacr.org/2015/525)
      - We agree there is a benefit to be opinionated on what to use, but will ideally make it easy to swap out what we choose to use.
  - Other things to consider:
    
    - What data model to use – e.g. can we support the W3C Verifiable Credentials Data Model Standard?
      
      - Approach could be similar to what we have proposed for AnonCreds v1.0 – e.g. using JSON-LD, but don't sign the RDF tuples – sign the encoded data values as per AnonCreds.
    - What presentation request data model to use?
      
      - Stick with AnonCreds or switch to Presentation Exchange?
    - Revocation
  - What will the V2.0 Spec contain?
    
    - Much like the V1.0 spec, with pointers to the cryptography to be used that is documented elsewhere.
- Next Steps:
  
  - Mike is creating a HackMD document to cover the Data Models he is proposing: [https://hackmd.io/@n3EfHQ0HR9-Gab\_iWRQZUA/B1b0h1MjI](https://hackmd.io/@n3EfHQ0HR9-Gab_iWRQZUA/B1b0h1MjI)
- Volunteers: We need additional people to lead this group. Step up, folks!

## Future Calls

## To Dos:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291946/20295103.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
