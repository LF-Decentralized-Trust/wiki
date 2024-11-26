1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2022 Meetings: AnonCreds Working Group](20295016.html)

# Hyperledger AnonCreds : 2022-11-21 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Nov 21, 2022

## Summary

- IIW Update
- PRs and Backwards Compatibility
- Latest on AnonCreds in W3C VC Standard Data Model format
- Open Issues
- Open Discussion

Recording of Call: [dummyfile.txt](#)

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

[Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence)(RootsID) &lt;alex.andrei@rootsid.com&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;

[Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

[Matteo Midena](https://lf-hyperledger.atlassian.net/wiki/people/712020:6d8efac9-b483-4b2e-a418-0b2e34e7aba4?ref=confluence) (Monokee) &lt;matteo.midena@monokee.com&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - RootsID is working on deploying AnonCreds on the Cardano Network
- Updates the Agenda

## Agenda

- IIW Update
  
  - Session on Hyperledger AnonCreds
  - Discussions about JSON-LD usage
  - Lots of discussions of supporting AnonCreds in "other formats" – e.g. OWF, OID4VCs
  - BBS+ Predicates work that is happening - Dan Yamamoto
  - Aside: Mike Lodder presentation
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
- Creating/sharing AnonCreds verifiable credential and presentation objects in W3C VC Data Model format
  
  - Repository with code: [andrewwhitehead/anoncreds-w3c-mapping](https://github.com/andrewwhitehead/anoncreds-w3c-mapping)
  - Signing an AnonCreds VC with an LDSignature based on a static context
- Open PRs Review, Open Issues Review
  
  - PR #[80](https://github.com/hyperledger/anoncreds-spec/pull/80)
    
    - Ready to merge – need [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)to resolve conflicts with the PR
  - Issue #[100](https://github.com/hyperledger/anoncreds-spec/issue/100): Clarifying if the holder is the software agent acting on behalf of an entity or the entity itself
    
    - Agreed to update the issue and specification with a change to the definition of "holder", "issuer" and "verifier" to mean that software that acts on behalf of the controller entity. Any examples where (for example) the term "holder" implies the person will be adjusted appropriately. Possibly, we will add another term, such as "holder-entity", etc. or "controller" to mean the entity for which the "holder" (etc.) on behalf.
  - Issue #[84](https://github.com/hyperledger/anoncreds-spec/issues/84): Changing encoding to be in AnonCreds and NOT handled by the issuer
    
    - This issue has been referenced in the new "Issuance Update" PR that was submitted over the weekend.
- Open Discussion

## Future Calls

- No topics pending

## To Dos:

- Ankur to add paragraph about philosophy of the AnonCreds API, styles
- Review the Issuing and Presentation sections to exclude Legacy Indy impacts, and to formalize the Abstract API for writing/reading published objects
- Cred Def Generation + PRIVATE\_CRED\_DEF -- non revocation, and plus revocation
- Revocation data elements -- definition
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
- From Artur Philipp : Issue about raw/encoded values used in AnonCreds [https://jira.hyperledger.org/browse/IS-786](https://jira.hyperledger.org/browse/IS-786)
- Latex in Spec-Up / (Re)Discovery of [AnonCreds Protocols](https://github.com/hyperledger/indy-hipe/tree/main/text/0109-anoncreds-protocol) paper from Mike Lodder, Brent Zundel. There is a full latex version of the document -- that document uses images to get the calculations into the text.

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291584/20295049.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
