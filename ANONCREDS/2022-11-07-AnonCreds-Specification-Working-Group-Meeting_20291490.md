1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2022 Meetings: AnonCreds Working Group](20295016.html)

# Hyperledger AnonCreds : 2022-11-07 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Nov 07, 2022

## Summary

- Logos!
- Transition to Hyperledger
- RevReg Objects between AnonCreds and AnonCreds Methods
- Iterations on AnonCreds in W3C VC Standard format
- Open Issues and PRs
- Open Discussion

Recording of Call: [dummyfile.txt](#)

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

[Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

[Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - IIW -- Nov 15-17, Mountain View, Calif.
    
    - Suggestions for what to do at IIW
      
      - Ledger-agnostic AnonCreds
      - AnonCreds in W3C Format
      - Sam:
        
        - Governance, Aries for other than AnonCreds
- Updates the Agenda

## Agenda

- Logos – selecting the Hyperledger AnonCreds project logo. [Link to survey](https://forms.gle/hATicchHPoRPvZSWA).
  
  - Finalize - Concept 1, colors TBD (likely Greens 7 votes vs. 4 for each of Blues and Red/Grey)
  - Sent to Hyperledger and the designer
- Transition into Hyperledger AnonCreds
  
  - Tasks in moving this group into Hyperledger
  - Move the repos from AnonCreds-WG organizations into HL, get new URL [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
  - Create new replacement repos in existing organization and publish a redirector to the new location - [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)
  - PR to update the references to the home of the specifications as being in Hyperledger and update the Community License V1.0 documents.
    
    - [Summary of PR](https://github.com/hyperledger/anoncreds-spec/pull/97) for the specification
    - To Do - Method Registry – need [PRs approved](https://github.com/hyperledger/anoncreds-methods-registry/pulls)
  - Create a Meetings page off the Hyperledger AnonCreds home page
  - Move all meeting agendas to the new Meetings page
  - All the other work in establishing the Hyperledger AnonCreds project: [Checklist](https://lf-hyperledger.atlassian.net/wiki/display/CA/Hyperledger+AnonCreds+New+Project+Checklist)
- RevReg Object updates -- enabling AnonCreds Methods to support both deltas and "full state" RevReg storage [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)
  
  - Discussion starts at 18:49 of the recording.
  - Initial proposed revocation list data model: [https://hackmd.io/@animo/Sys3SqUri](https://hackmd.io/@animo/Sys3SqUri)
  - In short – in creating the presentation, the invoking process must pass an object with this structure, plus (at least) the tails file:
    
    - `{ "revocation_list": [0,1,0,1....], "current_accumulator": "xxx", "timestamp": "xxx" }`
    - That will enable the AnonCreds presentation generator to produce the Proof of Non Revocation.
    - The invoker must get from the AnonCreds Method the data in that format, regardless of how the data is stored on ledger.
  - Next step is to put this into the specification as part of the presentation section – assigned to Stephen Curran to write (he should get on it...Soon!!)
- Creating/sharing AnonCreds verifiable credential and presentation objects in W3C VC Data Model format
  
  - Repository with code: [andrewwhitehead/anoncreds-w3c-mapping](https://github.com/andrewwhitehead/anoncreds-w3c-mapping)
  - Keep an eye on the repo – a context has been developed that should work for this.
- Open PRs Review, Open Issues Review
  
  - Issue #86: Should we allow the possibility of an Issuer using only a subset of a schema?
    
    - Discussed at the 37:26 mark of the recording.
    - Short answer is no – it's a bad idea for holders and verifiers, as it eliminates the expectation of what claims are in a credential. As noted in the ACA-Py discussion, the issuer has options for not using attributes (such as putting "NULL" into the credential). Such a change would be very complicated.
  - Issue #92: Does AnonCreds support in the Presentation Request / Presentation flow the concept of presenting any one of N verifiable credentials?
    
    - Discussed at the 47:04 mark of the recording.
    - It may, using unrevealed attributes.
    - If it does not work, the path to follow to "fix" this would mostly likely be to go to DIF Presentation Exchange, and not to
  - Issue #100: Clarifying if the holder is the software agent acting on behalf of an entity or the entity itself
    
    - Request for others to review and discuss at the next meeting
- Open Discussion

## Future Calls

- None pending

## To Dos:

- Request from Stephen Curran -- I'd like to go through the `presentation` section of the spec to convert the specific implementation calls (e.g. `indy_prover_...` and the like) into content to be more about the data objects passed into AnonCreds/returned from AnonCreds for processing events.
- Ankur to add paragraph about philosophy of the AnonCreds API, styles
- Review the Issuing and Presentation sections to exclude Legacy Indy impacts, and to formalize the Abstract API for writing/reading published objects
- Cred Def Generation + PRIVATE\_CRED\_DEF -- non revocation, and plus revocation
- Revocation data elements -- definition
- Normative/Non-normative references
  
  - Collect from documents mentioned below (under action items) and from previous meeting

## Action items

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291490/20295034.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
