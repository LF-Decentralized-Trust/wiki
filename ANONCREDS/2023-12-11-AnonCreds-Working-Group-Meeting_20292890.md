1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-12-11 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Dec 15, 2023

## Summary

- Project Update/Discussion: AnonCreds v1.0 in the W3C Verifiable Credentials Data Model Standard format
  
  - Wrap up!!!
  - Exposed APIs
- Aries Issue Credential and Present Proof attachment formats
- Eliminating the need for an AnonCreds JSON-LD `@context`
- Open Discussion

## Time: 7:00 Pacific / 16:00 Central Europe Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

## Recording:

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

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
- Any updates to the Agenda?

## Agenda

Open Issues

- Design and planning – AnonCreds v1.0 in the W3C Verifiable Credentials Data Model Standard format
  
  - Exposed APIs – walkthrough
  - Remaining questions:
    
    - VC 1.1 vs. 2.0 spec. – what would have to change?
    - Given this [Email](https://lists.w3.org/Archives/Public/public-credentials/2023Nov/0080.html) From Manu Sporny:
      
      - "and if Anoncreds needs to define new properties (which I'd very strongly advise against), your VC ends up w/ this context:..."
      - What is in the [AnonCreds context](https://github.com/hyperledger/anoncreds-spec/pull/185/files#diff-ea0357e70bdcf951a1648a8a1b1c66579c14f6de118434248912894c871e5b88)?
      - [Example](https://github.com/hyperledger/anoncreds-spec/pull/185/files#diff-a24b365b118aeaf7ac017372e01bb201967b2f27efa43362d3fa4e8210804638) use
      - Follow up questions for JSON-LD experts
- Aries Issue Credential / Present Proof Attachments
  
  - Current: [Indy](https://github.com/hyperledger/aries-rfcs/tree/main/features/0592-indy-attachments), [JSON-LD](https://github.com/hyperledger/aries-rfcs/tree/main/features/0593-json-ld-cred-attach) - which do we use, or should we define another that (also) handles JWTs?
- Eliminating having a special \`@context\` for AnonCreds
  
  - What do we do about the AnonCreds `@type` values?
  - Can/should we move more into the `proof`  sections?
    
    - Downside is you can't look at the proof and see the IDs for the CredDef or Schema.
- Open discussion

## Future Calls

## To Dos:

- Issue to talking about what AnonCreds verifies and what is left to the issuer to verify.
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

## W3C AnonCreds + AFJ Demo

- Aries Framework JavaScript repo: [https://github.com/DSRCorporation/aries-framework-javascript/tree/w3c-demo-poc](https://github.com/DSRCorporation/aries-framework-javascript/tree/w3c-demo-poc)
- Anoncreds-RS library, Anoncreds-NodeJs, and Anoncreds-Shared are built from the branch: [https://github.com/DSRCorporation/anoncreds-rs/tree/anoncreds-wc3-wrappers](https://github.com/DSRCorporation/anoncreds-rs/tree/anoncreds-wc3-wrappers)
  
  - Use main implementation (not included, dropping of `mapping`  and `encoding`  changes)
- Update AFJ `@hyperledger/anoncreds-nodejs`  and \`@hyperledger/anoncreds-shared\` dependencies to use locally built packages

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
