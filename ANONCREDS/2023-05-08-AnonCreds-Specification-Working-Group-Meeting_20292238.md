1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-05-08 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on May 08, 2023

## Summary

- Update on the AnonCreds V2.0 Working Group
- Unrevealed attributes
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

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@[anonyome.com](http://anonyome.com)&gt; 

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
  
  - Previous Meeting: Revisiting the Issuance data models – do we need an extra "attributes repository" object?
    
    - Same objects as AnonCreds 1 – Schema, Credential Definition, Credential
    - Schema adds types information on attributes – cryptographic types (string, numeric, scalar, enumeration, range)
    - Proposed addition of new "Schema Claims" object that is effectively a "repository of claims" to be shared across schemas
      
      - Name, type, validators defined at either the Schema Claims level or at the Schema level
  - Next week: Presentation Data Models
- [PRs](https://github.com/hyperledger/anoncreds-spec/pulls) for review and merging
- [Issues to Discuss](https://github.com/hyperledger/anoncreds-spec/labels/Discuss%20at%20Meeting) – None.
- **Unrevealed Attributes**, cryptographic vs. business-level verification, and related issues:
  
  - Core issue – cryptographic verification vs. business purpose verification. 
    
    - Where does the AnonCreds specification end, and the Present Proof protocol take over?
  - Clarification of the behaviour of unrevealed attributes. Based on recent [message on Discord](https://discord.com/channels/905194001349627914/1037471454775746580/1103892851789680680) – gmulhearn
    
    - Unrevealed attributes are the same as selective disclosure controlled by the holder.
    - Unrevealed attributes are not (as I had thought) a way to choose to disclose/not disclose an entire referent (group of claims from a credential).
      
      - This is a desirable feature: Being asked for multiple types of credentials (ORs), any of which are suitable, with the expectation the holder holds (will respond with) only one of them.
        
        - Referents for "Person" Credential from three different jurisdictions (3 credential types), where any one person would ever only have 1 of the 3.
        - The AnonCreds Presentation Request syntax has no mechanism to make this kind of request.
          
          - Note: DIF Presentation Exchange does support this kind of syntax.
  - In the "Ask for 3 when I only have 1" issue, the holder is (evidently) able act unilaterally, assuming what the verifier intended:
    
    - A holder may respond to a presentation request with only a subset of the referents (claim groups) and the presentation will verify.
    - The verifier must then decide what to do – accept the presentation as meeting the business need or not.
      
      - E.g., ACA-Py was been coded to detect what the developer called a "bait and switch" by the holder – being very firm on the presentation matching the presentation request.
        
        - However, this approach rejects both the use of "unrevealed attributes", and the "one of many" use case.
  - Another example:
    
    - Verifier presentation request asks for a "Proof of Degree" based on a common schema.
    - The presentation may verify.
    - Is the credential that was used for the presentation from a trusted source?
    - Being able to scale requires this capability.
  - Issue:
    
    - AnonCreds stops at the cryptographic verification.
      
      - The verification wrapper around AnonCreds verification may go further.  Should that be part of the spec or not?
    - The protocol around AnonCreds may or may not have a "business verification" response.
    - How do we combine the two?
    - For AnonCreds v1.0 we clarify what is possible.
    - For AnonCreds v2.0 we adjust the design.
  - To Do:
    
    - Issue to talking about what AnonCreds verifies and what is left to the issuer to verify.
- Dynamic Accumulator Revocation scheme
  
  - Proposal: To be presented two weeks from today.
- Checkin: anoncreds-rs implementation progress, requests
  
  - Seems to be pretty stable right now – most effort is in using the implementation in various frameworks.
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292238/20295144.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
