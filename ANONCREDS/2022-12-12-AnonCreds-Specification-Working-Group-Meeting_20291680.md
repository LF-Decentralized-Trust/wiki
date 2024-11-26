1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2022 Meetings: AnonCreds Working Group](20295016.html)

# Hyperledger AnonCreds : 2022-12-12 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Dec 12, 2022

## Summary

- Revocation Registry List Data Model
- Validation of Identifiers - specification vs. implementation
- What is the "prover\_did" data item?
- Checkin: anoncreds-rs implementation progress, requests
- Open Discussion

Recording of Call: [dummyfile.txt](#)

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

[Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

[Matteo Midena](https://lf-hyperledger.atlassian.net/wiki/people/712020:6d8efac9-b483-4b2e-a418-0b2e34e7aba4?ref=confluence) (Monokee) &lt;matteo.midena@monokee.com&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - Latex in the specification now enabled.
  - Meetings: Last one for 2022 next week, then 2 weeks hiatus.
    
    - First 2023 meeting: 2023.01.09
- Updates the Agenda

## Agenda

Open Issue

- [Issue 108](https://github.com/hyperledger/anoncreds-spec/issues/108): Revocation Registry List Data Model
  
  - This data model is sufficient for a holder to an AnonCreds implementation
  - Within the AnonCreds implementation, the calculation of the witness must be derived from that.
- [Issue 111](https://github.com/hyperledger/anoncreds-spec/issues/111): Validation of Identifiers - specification vs. implementation
  
  - Change the spec. to be MUST for a URI (which includes the legacy Indy format) and that validation is required.
- [Issue 107](https://github.com/hyperledger/anoncreds-spec/issues/107): What is the "prover\_did" data item?
  
  - From Chat:
    
    - From Timo Glastra : We also use that (the holder's DIDComm peer DID for the connection) in AFJ
      
      - Note: Interesting to know what is used when there is a connection-less issuance. ![(smile)](images/icons/emoticons/smile.png)
    - From Rodolfo Miranda : For object identifiers I like this DID-Linked Resources Specification that was proposed by cheqd on ToIP Utility Foundry WG: [https://wiki.trustoverip.org/display/HOME/DID-Linked+Resources+Specification](https://wiki.trustoverip.org/display/HOME/DID-Linked+Resources+Specification)
    - From Keith Kowal : So it sounds like Prover\_DID=Holder DID. So this would be the pairwise DID - which might cause problems in some recovery scenarios...
    - From Timo Glastra : Seems like an issue to solve on top of AnonCreds, not in AnonCreds
    - From Steve McCown : +1 for Timo’s comment
    - From Timo Glastra : We could deprecate it. Problem is that for legacy indy anoncereds this will be a breaking change, while until now we've been able to avoid breaking changes in the exchanged data models. I.e. an old legacy implementation could still interact with a system that follows the ledger agnostic anoncreds spec, as long as they use the legacy identifiers
      
      - Idea would that it would be optional, and if the holder did not provide it, the issuer would generate something suitable to replace it.  That would work since it seems in the cryptography, it doesn't matter what it's value is anyway...
    - From Timo Glastra : One thing to note, the prover\_did would need to be a did (legacy did) as ACA-Py validates the prover\_did value to be an unqualified indy did. So it can't be just a string
  - Seems to be used in generating the credential, but is not used anywhere in the verification process – not shared beyond that
  - Could be deprecated, with the issuer "creating" the value if not supplied
  - Seems like it was an afterthought addition to the specification, that was not documented
  - Second, related issue is the use of the nonce, and the fact that the nonce in the Cred Offer is different from the nonce in the Cred Request.
    
    - Expectation (to be confirmed by Belsy) is that:
      
      - The Issuer created CredOfferNonce is used by the holder in the CredRequest correctness\_proof and verified by the Issuer
      - The Holder created CredRequestNonce is used by the issuer in the Credential correctness\_proof and verified by the Holder
- Checkin: anoncreds-rs implementation progress, requests
- Open Discussion

## Future Calls

- [Issue 102](https://github.com/hyperledger/anoncreds-spec/issues/102): AnonCreds object signed by the key of the publisher
  
  - Which is related to [Issue 74](https://github.com/hyperledger/anoncreds-spec/issues/74): issuer\_did and schema\_issuer\_did should be IDs?

## To Dos:

- Issue to be added and further investigation into what happens to the nonce(s) by Belsy.
- Updates to the spec. re: revocation data model, prover\_did and nonces uses
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
- Ankur to add paragraph about philosophy of the AnonCreds API, styles
- Review the Issuing and Presentation sections to exclude Legacy Indy impacts, and to formalize the Abstract API for writing/reading published objects
- Cred Def Generation + PRIVATE\_CRED\_DEF -- non revocation, and plus revocation
- Normative/Non-normative references
  
  - Collect from documents mentioned below (under action items) and from previous meeting

## Action items

- Request from Stephen Curran -- I'd like to go through the `presentation` section of the spec to convert the specific implementation calls (e.g. `indy_prover_...` and the like) into content to be more about the data objects passed into AnonCreds/returned from AnonCreds for processing events.
- Suggestion made and supported that the group request to provide a presentation about AnonCreds to the W3C VC Working Group about the formatting of AnonCreds verifiable credential and presentation in W3C format and the processing implied.
- Issue -- should "encoded" generation be handled by the Issuer or within AnonCreds?
  
  - Formalize the encoding in the specification
  - Transition to "encoding in AnonCreds" ASAP
- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291680/20295067.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
