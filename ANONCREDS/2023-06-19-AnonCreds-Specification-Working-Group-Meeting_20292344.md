1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-06-19 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Jun 19, 2023

## Summary

- NEW ZOOM LINK!!!
- Celebration!! AnonCreds 0.1.0 Release finalized!
- AnonCreds Workshop Report
- Mentorship Update
- AnonCreds Specification: Mixing overview/flow information with cryptographic details
- New revocation approaches
- Open Discussion

## Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

## Recording:

- [https://youtu.be/sUcstipdEm8](https://youtu.be/sUcstipdEm8)
- [2023 06 19 Hyperledger AnonCreds Specification Working Group Chat.txt](attachments/20292344/20295165.txt)
- [2023 06 19 Hyperledger AnonCreds Specification Working Group.transcript.txt](attachments/20292344/20295166.txt)

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
  
  - AnonCreds 0.1.0 Rust Implementation officially released!
  - Welcome [Aritra Bhaduri](https://lf-hyperledger.atlassian.net/wiki/people/6369366711c69c741844e7c9?ref=confluence) a Hyperledger Mentor working on the AnonCreds Specification
    
    - Documenting the cryptography and aligning it with the implementation.
  - Update on the AnonCreds V2.0 Working Group
    
    - Last Week: How the model supports multiple underlying cryptographic signatures
    - Next Week: Presentation Data Models
- Any updates to the Agenda?

## Agenda

Open Issue

- NEW ZOOM LINK!!!
- Celebration!! AnonCreds 0.1.0 Release finalized!
- AnonCreds Workshop Report
- Mentorship Update
- Deferred: AnonCreds Specification: To Do List
- Deferred: AnonCreds Specification: Mixing overview/flow information with cryptographic details
- Presentation: [AnonCreds Revocation Options](https://docs.google.com/presentation/d/10Ns1hpeA6WRxGXCV-ofPDOcS-EzuQNVAuWi0g48RfVM/edit?usp=sharing)
  
  - [AnonCreds v1.0](https://github.com/hyperledger/indy-hipe/blob/main/text/0011-cred-revocation/README.md) — CKS Signature with tails file
  - [ALLOSAUR](https://eprint.iacr.org/2022/1362) — Revocation Managers contacted at presentation time
  - [LVVC](https://eprint.iacr.org/2022/1658.pdf) — Linked Validity Verifiable Credential -- Revocation Manager issues a VC about the revocation state of a credential.
  - [zk-SAM](https://hackmd.io/vTyqrJc9QoKgThqQpVtP3g?view) — Signed Accumulator Membership - publication of full revocation state
- Open Discussion

## Future Calls

## To Dos:

- Issue to talking about what AnonCreds verifies and what is left to the issuer to verify.
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

## Action items

- Adding support for W3C Format AnonCreds to the anoncreds implementation and the spec.
- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

## Attachments:

![](images/icons/bullet_blue.gif) [2023 06 05 AnonCreds Spec Chat.txt](attachments/20292344/20295153.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [2023 06 05 AnonCreds Spec Transcript.vtt](attachments/20292344/20295154.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [2023 06 19 Hyperledger AnonCreds Specification Working Group Chat.txt](attachments/20292344/20295165.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [2023 06 19 Hyperledger AnonCreds Specification Working Group.transcript.txt](attachments/20292344/20295166.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
