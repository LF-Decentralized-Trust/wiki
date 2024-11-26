1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2022 Meetings: AnonCreds Working Group](20295016.html)

# Hyperledger AnonCreds : 2022-12-05 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Dec 05, 2022

## Summary

- Open Issues
- Discussion of Mike Lodder's proposals from last week and paper posted this week
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

[Matteo Midena](https://lf-hyperledger.atlassian.net/wiki/people/712020:6d8efac9-b483-4b2e-a418-0b2e34e7aba4?ref=confluence) (Monokee) &lt;matteo.midena@monokee.com&gt;

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
- Updates the Agenda

## Agenda

- Open PRs Review, Open Issues Review
- Request for work on the specification – especially the cryptographic elements
- Discussion of what an AnonCreds 2.0 might look like based on the work Mike has done.
- Open Discussion

## Future Calls

- No topics pending

## To Dos:

- Issue #[100](https://github.com/hyperledger/anoncreds-spec/issue/100): Clarifying if the holder is the software agent acting on behalf of an entity or the entity itself
  
  - Agreed to update the issue and specification with a change to the definition of "holder", "issuer" and "verifier" to mean that software that acts on behalf of the controller entity. Any examples where (for example) the term "holder" implies the person will be adjusted appropriately. Possibly, we will add another term, such as "holder-entity", etc. or "controller" to mean the entity for which the "holder" (etc.) on behalf.
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291650/20295060.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
