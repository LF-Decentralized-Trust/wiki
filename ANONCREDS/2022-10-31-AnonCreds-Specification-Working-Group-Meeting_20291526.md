1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2022 Meetings: AnonCreds Working Group](20295016.html)

# Hyperledger AnonCreds : 2022-10-31 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Nov 02, 2022

Recording: [https://youtu.be/7mIUJBqLV7Y](https://youtu.be/7mIUJBqLV7Y)

## Summary

- IIW Plans
- Transition to Hyperledger
- Iterations on AnonCreds in W3C VC Standard format
- Converting AnonCreds VC to W3C VC Standard format and adding other signature types (e.g. LD-Signature/NIST/ed25519/BBS+)
- Open Discussion

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- Proposal: Start an AnonCreds Code Development Working Group driven by this [Roadmap](https://github.com/orgs/hyperledger/projects/16)

## Release Status and Work Updates

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Preliminaries

- Start Recording
- Reminder: [Community Specification License v1.0](https://github.com/AnonCreds-WG/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md) and [Working Group Code of Conduct](https://github.com/AnonCreds-WG/anoncreds-spec/blob/main/8._Code_of_Conduct.md)
- Welcome and Introductions
- Announcements:
  
  - IIW -- Nov 15-17, Mountain View, Calif.
    
    - Suggestions for what to do at IIW
      
      - Ledger-agnostic AnonCreds
      - AnonCreds in W3C Format
      - Sam:
        
        - Governance, Aries for other than AnonCreds
    - Proposed that Hyperledger publish a Press Release about AnonCreds the first morning of IIW

## Main Agenda

- Tasks in moving this group into Hyperledger
  
  - Move the repos from this group into HL, get new URL
  - Create new replacement repos in this organization and publish a redirector to the new location
  - PR to update the references to the home of the specifications as being in Hyperledger
  - PR to review and update the Community License V1.0 documents.
  - Create a Meetings page off the [Hyperledger AnonCreds home page](https://lf-hyperledger.atlassian.net/wiki/display/ANONCREDS/)
  - Move all meeting agendas to the new Meetings page
  - All the other work in establishing the Hyperledger AnonCreds project: [Checklist](https://lf-hyperledger.atlassian.net/wiki/display/CA/Hyperledger+AnonCreds+New+Project+Checklist)
- Creating/sharing AnonCreds verifiable credential and presentation objects in W3C VC Data Model format
  
  - Repository with code: [andrewwhitehead/anoncreds-w3c-mapping](https://github.com/andrewwhitehead/anoncreds-w3c-mapping)
  - Review the inputs and outputs
  - AnonCreds Presentation as a W3C VC or a VP?
  - Issue being argued within the W3C VC Working Group: Is JSON-LD a MAY or a MUST?
    
    - Whether `@context` is optional or not.
    - Whether a Verifiable Credential MUST be signed with an LD-Signature (aka DataIntegrityProof).
      
      - Positioning chat on issue: [VCWG Issue #](https://github.com/hyperledger/anoncreds-spec/wiki/WG-2022-10-31)
      - Why LD? Global root of all schema semantics.
      - Alternative to a full `@context`: you can use an `@vocab` item to inline the context for attributes.
    - Any other comments/ideas/suggestions on the mapping?
    - Presentation - an option for AnonCreds verifiable credentials -- convert to W3C and add other signatures -- notably DataIntegrityProof
      
      - Example given of an AnonCreds VC with ed25519, NIST and BBS+ credentials.
- [Open PRs Review](https://github.com/AnonCreds-WG/anoncreds-spec/pulls), [Open Issues Review](https://github.com/AnonCreds-WG/anoncreds-spec/issues)
  
  - Next week: Issue [#86](https://github.com/AnonCreds-WG/anoncreds-spec/issues/86): Should we allow the possibility of an Issuer using only a subset of a schema?
  - Next week: Issue [#92](https://github.com/AnonCreds-WG/anoncreds-spec/issues/92): Does AnonCreds support in the Presentation Request / Presentation flow the concept of presenting any one of N verifiable credentials?

## Future Topics:

- RevReg Object updates -- enabling AnonCreds Methods to support both deltas and "full state" RevReg storage
  
  - Proposal: Make the RevRegEntry data model that the AnonCreds method must present to the AnonCreds NRP generation code two primary elements, the accumulator itself (needed? or do we provide the tails file contents?), and the array listing the revoked credentials. No compression will be applied to the list of revoked credentials.
  - An AnonCreds Method must produce the format. How it stores the data on ledger is up to the Method.

## What's left?

- To Dos:
  
  - Request from Stephen Curran -- I'd like to go through the `presentation` section of the spec to convert the specific implementation calls (e.g. `indy_prover_...` and the like) into content to be more about the data objects passed into AnonCreds/returned from AnonCreds for processing events.
  - Ankur to add paragraph about philosophy of the AnonCreds API, styles
  - Review the Issuing and Presentation sections to exclude Legacy Indy impacts, and to formalize the Abstract API for writing/reading published objects
  - Cred Def Generation + PRIVATE\_CRED\_DEF -- non revocation, and plus revocation
  - Revocation data elements -- definition
  - Normative/Non-normative references
    
    - Collect from documents mentioned below (under action items) and from previous meetings

## Action Items From Previous Meetings:

- Suggestion made and supported that the group request to provide a presentation about AnonCreds to the W3C VC Working Group about the formatting of AnonCreds verifiable credential and presentation in W3C format and the processing implied.
- Issue -- should "encoded" generation be handled by the Issuer or within AnonCreds?
  
  - Formalize the encoding in the specification
  - Transition to "encoding in AnonCreds" ASAP
- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)
- From Artur Philipp : Issue about raw/encoded values used in AnonCreds [https://jira.hyperledger.org/browse/IS-786](https://jira.hyperledger.org/browse/IS-786)
- Latex in Spec-Up / (Re)Discovery of [AnonCreds Protocols](https://github.com/hyperledger/indy-hipe/tree/main/text/0109-anoncreds-protocol) paper from Mike Lodder, Brent Zundel. There is a full latex version of the document -- that document uses images to get the calculations into the text.

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
