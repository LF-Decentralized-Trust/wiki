1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-02-27 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Feb 27, 2023

## Summary

- Update on the AnonCreds V2.0 Working Group
- AnonCreds on Cardano - Presentation by [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence)
- AnonCreds, JSON-LD, W3C Verifiable Credentials Data Model Standard and the VCWG
- PRs
- Issues to discuss
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

[Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

[Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;

[Matteo Midena](https://lf-hyperledger.atlassian.net/wiki/people/712020:6d8efac9-b483-4b2e-a418-0b2e34e7aba4?ref=confluence) (Monokee) &lt;matteo.midena@monokee.com&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - [AnonCreds V2.0 Working Group](/wiki/pages/createpage.action?spaceKey=ANONCREDS&title=Meetings%3A%20AnonCreds%20v2.0%20Working%20Group&linkCreation=true&fromPageId=20291970) meetings started last week, and will meet every second Monday (next meeting is next Monday, March 6 at 10:00 Pacific / 19:00 Central Europe)
  - This meeting will now be every second Monday as will, but at this time of 7:00 Pacific / 16:00 Central Europe.
- Any updates to the Agenda?

## Agenda

Open Issue

- Update on the AnonCreds V2.0 Working Group
  
  - *The goal of AnonCreds v2.0 is to retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security.*
  - Next week's meeting: Data Model proposals from Mike Lodder
- AnonCreds on Cardano - Presentation by [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) 
  
  - From Timo Glastra : I was wondering after your last demo. Even if it would support any did as issuerId, I think we should still limit the identifier of the anoncreds object to be specific to the cardano registry. That could for example mean prepending it with \`did:cardano\` or it could mean prefixing it with something like \`anoncreds:cardano:&lt;identifier&gt;\`. As otherwise we're going to have conflicts I assume with an anoncreds object having e.g. an \`did:example\` identifier, which should be reserved for the \`did:example\` method.
  - Links:
    
    - [https://wiki.trustoverip.org/display/HOME/DID-Linked+Resources+Specification](https://wiki.trustoverip.org/display/HOME/DID-Linked+Resources+Specification)
    - [https://github.com/roots-id/cardano-anoncreds/blob/main/cardano-anoncred-methods.md](https://github.com/roots-id/cardano-anoncreds/blob/main/cardano-anoncred-methods.md)
    - [https://hyperledger.github.io/anoncreds-methods-registry/#cardano-anoncreds-method](https://hyperledger.github.io/anoncreds-methods-registry/#cardano-anoncreds-method)
    - [https://github.com/roots-id/cardano-anoncreds/tree/main/reference-implementations](https://github.com/roots-id/cardano-anoncreds/tree/main/reference-implementations)
  - From Alex Andrei : I was talking to the side tree guys and they mentioned that using IPNS is also a good use case for anoncreds objects
- Migrating to did:indy – can just happen?
  
  - Credentials issued to old identifiers - proof request has old identifiers, either unqualified or "did:sov" – there is an equivalent "did:indy"
  - Add to spec – unqualified and map them to "did:indy" automagically, or require the verifier to ask for both representations explicitly.
  - [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) to do a test to see the effort is supporting all flavours on receipt of a proof request and in verifying.  How painful is that to support?
  - Link to Indy DID Networks repo: [https://github.com/hyperledger/indy-did-networks](https://github.com/hyperledger/indy-did-networks)
    
    - Discord: [https://discord.com/channels/905194001349627914/941708981825576960/1036580808196116481](https://discord.com/channels/905194001349627914/941708981825576960/1036580808196116481)
- AnonCreds, JSON-LD, W3C Verifiable Credentials Data Model Standard and the VCWG
  
  - On step further in aligning with JSON-LD – signing the hash of the `@context`  RDF tuple WITHOUT credential data.  Good idea?
  - The VCWG Miami F2F – the resolution to the "Big Tent" issue.
- [PRs](https://github.com/hyperledger/anoncreds-spec/pulls) for review and merging
  
  - AnonCreds Rust [102](https://github.com/hyperledger/anoncreds-rs/pull/102) – handling combinations of Revoked/Non-Revoked presentations
    
    - Timestamp
    - Handling of both revocable and non-revocable credentials in a single presentation in all cases (bug in older implementation).
  - ANDs and ORs in the spec. are wrong – need to update the specification.
- [Issues to Discuss](https://github.com/hyperledger/anoncreds-spec/labels/Discuss%20at%20Meeting) – notably, issues that are ready to be closed.
- Checkin: anoncreds-rs implementation progress, requests
  
  - NodeJs wrapper performance issue: [https://github.com/hyperledger/aries-askar/issues/76](https://github.com/hyperledger/aries-askar/issues/76)
- Open Discussion:
  
  - Ideas on how to link from the specification to the cryptographic operations?
  - Discussion from several weeks ago – having an intermediary collect presentations from holders and then share them with the final verifier.
    
    - Use Case:
      
      - A bus is visiting a secure site for which all visitors must present ID.
      - Site sends the bus operator a nonce.
      - The bus operator uses the nonce in a presentation request flow with each passenger.
      - Bus operator verifies all of the presentations.
      - The Bus operator forwards all of the presentations to the site for verification.
    - Questions:
      
      - Is there value in the use of the nonce in this way?
      - Does this alter the cryptography in any way?
      - Terms of use of the data received by the bus operator?
    - Discussion to be carried forward to next week.
  - Proposal: Should we move attribute encoding into the specification and out of the hands of the issuer?
    
    - Approach:
      
      - Deprecate the inclusion of encoded values from the "sign credential" process
      - If passed, recalculate and error if they don't match the canonicalization algorithm
        
        - If integer or string integer - leave as is
        - Else stringify and hash
      - In presentation – recalculate on use, as needed.

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
- Issue -- should "encoded" generation be handled by the Issuer or within AnonCreds?
  
  - Formalize the encoding in the specification
  - Transition to "encoding in AnonCreds" ASAP
- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291970/20295110.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
