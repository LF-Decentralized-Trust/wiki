1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-04-24 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Apr 24, 2023

## Summary

- Update on the AnonCreds V2.0 Working Group
- Hyperledger AnonCreds Workshop – May 31, 2023 8:00 Pacific / 17:00 Central Europe
- IIW Recap
- Discussion: AnonCreds in W3C VC and JWT formats
- Checkin: anoncreds-rs implementation progress, requests
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

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements
  
  - Presentation at VC-API Working Group
- Any updates to the Agenda?

## Agenda

Open Issue

- Update on the AnonCreds V2.0 Working Group
  
  - Previous Meeting: ALLOSAUR Revocation
  - Next week: Revisiting the Issuance data models
- Hyperledger AnonCreds Workshop - May 31
  
  - Proposed Agenda:
    
    - Introduction to AnonCreds and ZKPs
      
      - Set Context – VCs, issuer-holder-verifier
      - AnonCreds
      - ZKPs overview
      - Where ZKPs are used in AnonCreds
      - Exercise – issuing, holding, requesting, presenting
      - Revocation
    - AnonCreds Methods
      
      - AnonCreds on other than Indy Ledgers
      - Ideally an exercise using AnonCreds with other than Indy
      - What changes when using other ledgers?
    - Making AnonCreds Credential Beautiful
      
      - AnonCreds and the Overlays Capture Architecture (OCA)
    - Future AnonCreds Features
      
      - AnonCreds in W3C Format
      - AnonCreds v2.0 — what’s next?
- IIW
  
  - Revocation
  - OCA
  - AnonCreds AMA
  - Lots of OpenID4VCs
  - OWF presence but no new information
- **Discussion**: AnonCreds in W3C VC and JWT format
  
  - Importance?
    
    - Open discussion
      
      - Issue date / validity date
    - Verifiable Credential - Data Model 2.0
      
      - Research needed: What changes from 1.0, 1.1 to 2.0?
      - `@vocab` usage
  - Anyone know about the W3C to JWT transformation mechanism?
    
    - Can that be used with AnonCreds?
      
      - [https://github.com/w3c/vc-test-suite/blob/gh-pages/test/vc-data-model-1.0/50-jwt.js](https://github.com/w3c/vc-test-suite/blob/gh-pages/test/vc-data-model-1.0/50-jwt.js)
    - Can we extend this to generate a JWT: [https://github.com/andrewwhitehead/anoncreds-w3c-mapping](https://github.com/andrewwhitehead/anoncreds-w3c-mapping)
      
      - How to do a JWS with AnonCreds.
  - AnonCreds RS:
    
    - Consuming a credential/presentation in another format should be easy
      
      - Sniff the format and convert to "internal" format.
        
        - Receipt of Credential
        - Receipt of Presentation
    - Production of Credential/Presentation in different formats?
      
      - Add a parameter to indicate the type?
      - Add a call to convert the type?
      - Produce multiple formats?
    - Revocation – how to manage?
      
      - Not StatusList2021, how to use the "W3C Format StatusList"
  - Other questions from Discord:
    
    - The process of issuance in this context, more specifically, what does a AnonCreds credential request would look like in w3c format. Is the `AnonCreds in W3C VC formats` feature only limited to a representation of the already signed and issued credential?
    - To sign a json-ld VC you apply a signature to the Credential, transforming it into a VC without a need to communicate with the holder. With AnonCreds there is an exchange between the issuer and holder to introduce the secret link before the credential is signed.
- Demo: IDLab AnonCreds Flows demo–very cool!  By [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) 
  
  - Recording from the call: [dummyfile.txt](#)
  - Links to Flow:
    
    - [https://api.anoncreds.idlab.app/openapi/rapidoc](https://api.anoncreds.idlab.app/openapi/rapidoc)
    - [https://flows.dtt.idlab.app/](https://flows.dtt.idlab.app/)
- [PRs](https://github.com/hyperledger/anoncreds-spec/pulls) for review and merging
- [Issues to Discuss](https://github.com/hyperledger/anoncreds-spec/labels/Discuss%20at%20Meeting) – None.
- Checkin: anoncreds-rs implementation progress, requests
  
  - Wrapping up wrappers, documentation
  - Official release coming soon!  Working in test deployments of Bifold
  - Status of ASCA-Py implementation
- Open Discussion:

## Future Calls

## To Dos:

- [Issue #137](https://lf-hyperledger.atlassian.net/wiki/display/~swcurran/) added regarding further investigation into what happens to the issuance data flow nonce(s) by Belsy – definition completed, to be added to the spec. [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Issue #140](https://github.com/hyperledger/anoncreds-spec/issues/140) should WQL be allowed in a Presentation Request?
  
  - WQL is supported currently in the Indy SDK, but not in the Aries Frameworks
  - Should it be in the specification?
  - If so, in what form. From [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) — don't call it WQL if we do include it – just describe it.
  - Not used and it is not clear there is a good reason to support it.
  - Complicates the specification and the implementation.
  - Decision:
    
    - Not supported in the specification – let's keep it out in this version
- Revocation Interval
  
  - Approach to determine if the holder used an acceptable RevRegistry – see [this Issue comment](https://github.com/hyperledger/anoncreds-spec/issues/132#issuecomment-1400856502)
  - Who calls the AnonCreds method to get the Revocation Registry from the ledger for verification
    
    - Verifier or AnonCreds?
  - To set "validation" to true/false based on the RevRegEntry timestamp in relation to the revocation interval?  [Presentation](https://docs.google.com/presentation/d/11hXNz_BKOx-ljEGj6cXB1dwnEgEBg3ocqoyR7lgZW1I/edit?usp=share_link)
  - Key points:
    
    - 1\. an RevRegEntry is “current” from the time it is written, to the time of the next RevRegEntry
    - 2\. “within the interval” is based on when a RevRegEntry is “current” (see 1.), not its timestamp.
    - 3\. AnonCreds or the Verifier (calling AnonCreds) should calculate “within interval” (using 2.) and mark verification true if the RevRegEntry used by the Prover is within the interval, else false.
      
      - Dangers:
        
        - False-Negatives: If a strict "timestamp used is between from, to" and not based on when a RevReg is "current" (per 2.), we will get "not verified" incorrectly.
        - False-Positives: If we don't do any checking of the timestamp and the interval, the holder could incorrectly use an old RevRegEntry.
    - 4\. General point: AnonCreds should return both a summary (true/false) and if false, additional data about why it was false.
  - Decision – add an optional \`at\_from\_ts\` set of entries, one per NRP, that AnonCreds can use for determining if the holder\_ts is within the Presentation Request interval.
- Backwards Compatibility
  
  - PRs in (#[82](https://github.com/hyperledger/anoncreds-spec/pull/82), #[105](https://github.com/hyperledger/anoncreds-spec/pull/105)) that seem to change public data structures – ones that are handled outside of AnonCreds and/or by two or more participants (issuer, holder, verifier)
  - We want to retain compatibility with existing data – credentials that have been issued and the published AnonCreds objects on which they rely.
  - That extends to business logic – e.g. the handling of the objects not just by AnonCreds, AnonCreds Methods and Aries Frameworks, but also by business applications built on Aries.
  - Suggestion:
    
    - Include in the specification a statement about backward compatibility
      
      - Perhaps this is what Ankur had planned to do?
    - Formalize what data structures will be expected by AnonCreds
      
      - This is being done throughout the specification and verified against the current implementation.
    - As needed support sending and receiving data in "old" and "new" formats, but (for now) always sending "old" formats.
      
      - TBD if there are any such cases.

## Action items

- Adding support for W3C Format AnonCreds to the anoncreds implementation and the spec.
- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292172/20295136.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292172/20295135.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
