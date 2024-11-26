1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-02-06 AnonCreds Specification Working Group Meeting

Created by Stephen Curran, last modified on Feb 06, 2023

## Summary

- Back to prover\_did – not optional/not issuer generated?
- WQL in Presentation Request?
- PRs
- Progress on the anoncreds\_rs implementation
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

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

[Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) (2060.io) &lt;gentilester@gmail.com&gt;

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

Open Issue

- [Issues to Discuss](https://github.com/hyperledger/anoncreds-spec/labels/Discuss%20at%20Meeting)
  
  - [Issue #137](https://github.com/hyperledger/anoncreds-spec/issues/137) added regarding further investigation into what happens to the issuance data flow nonce(s) by Belsy – definition completed, to be added to the spec. [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
  - [Issue #107](https://github.com/hyperledger/anoncreds-spec/issues/107) what happens to prover\_did?  Decisions made:
    
    - Rename the item to `entropy`
    - Update the spec and implementation (again) to make the item required from the holder
    - Describe how the item is combined with the `rev_idx` (if available) and hashed to produce the `credential_context` and put in the VC as `m2`
    - `m2` can be checked by the holder to ensure it is based the provided `entropy` value.
  - [Issue #140](https://github.com/hyperledger/anoncreds-spec/issues/140) should WQL be allowed in a Presentation Request?
    
    - WQL is supported currently in the Indy SDK, but not in the Aries Frameworks
    - Should it be in the specification?
    - If so, in what form. From [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) — don't call it WQL if we do include it – just describe it.
    - Not used and it is not clear there is a good reason to support it.
    - Complicates the specification and the implementation.
    - Decision:
      
      - Not supported in the specification – let's keep it out in this version
- [PRs](https://github.com/hyperledger/anoncreds-spec/pulls) for review and merging
  
  - Merged one of the two PRs in progress.
- Checkin: anoncreds-rs implementation progress, requests
  
  - NodeJs wrapper performance issue: [https://github.com/hyperledger/aries-askar/issues/76](https://github.com/hyperledger/aries-askar/issues/76)
  - Discussion about what to do about wrappers, especially if there is a need to drop the napi-js library to overcome this issue.  Various options were discussed, and links provided:
    
    - UniFFI Library for Mozilla to generate wrappers.  Describe the interface in a DSL, and then generate the wrappers thereafter.
      
      - From Steve McCown : [https://firefox-source-docs.mozilla.org/writing-rust-code/uniffi.html](https://firefox-source-docs.mozilla.org/writing-rust-code/uniffi.html)
      - From Stephen Curran : [https://mozilla.github.io/uniffi-rs/Overview.html](https://mozilla.github.io/uniffi-rs/Overview.html)
      - From Steve McCown : Here’s a link to the “Uniffi” tutorials that I wrote.  There have been a few updates to the tool, since I wrote these, so they might need some updating themselves.  I’ll take a look at that…
        
        [https://github.com/mccown/ffi-tutorials](https://github.com/mccown/ffi-tutorials)
      - From Ariel Gentile : Thanks for the link Steve! I'll check it out to see if we can give a try using it
      - From Timo Glastra : Yeah UniFFI looks interesting
    - State of React Native wrapper
      
      - From Timo Glastra : The RN wrappers are already done and working! [https://github.com/hyperledger/anoncreds-rs/tree/main/wrappers/javascript/anoncreds-react-native](https://github.com/hyperledger/anoncreds-rs/tree/main/wrappers/javascript/anoncreds-react-native)
      - From Timo Glastra : As Ariel mentioned, It's written in C++ (so no Swift / Kotlin)
      - From Alex Andrei : [https://www.npmjs.com/package/@hyperledger/anoncreds-react-native](https://www.npmjs.com/package/@hyperledger/anoncreds-react-native)
      - From Timo Glastra : We use a new React Native JSI (JavaScript Interface) [https://github.com/hyperledger/anoncreds-rs/blob/main/wrappers/javascript/anoncreds-react-native/cpp/anoncreds.cpp#L96-L122](https://github.com/hyperledger/anoncreds-rs/blob/main/wrappers/javascript/anoncreds-react-native/cpp/anoncreds.cpp#L96-L122)
    - C++ Wrappers – why and where?
      
      - From pasquale : For Ariel and Timo: do turboModules work also with Rust libs? Or just C++? Cause I see cpp files in the anoncreds wrapper
      - From Ariel Gentile : Yeah we need to add a CPP layer in the middle. That's what we tried to avoid in NodeJs by using the node-ffi-napi / ref-napi (whose advantage is exactly that)
      - From pasquale : Ok I see, you use C++ in order to write an adapter layer in one single language instead of creating two (one in java and one in swift), am I correct?
      - From Ariel Gentile : Yes!
      - From pasquale : Gotcha, thanks
- Discussion: Mike Lodder has proposed that a group start on "Next Gen" AnonCreds based on his [this recorded presentation](https://lf-hyperledger.atlassian.net/wiki/download/attachments/20291620/20221128%20Mike%20Lodder%20Presentation%20on%20a%20Proposed%20Future%20AnonCreds.mp4?version=1&modificationDate=1669667589000&api=v2) at out [2022-11-28 meeting](https://lf-hyperledger.atlassian.net/wiki/display/ANONCREDS/2022-11-28+AnonCreds+Specification+Working+Group+Meeting)
  
  - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) to find times that work for Mike and propose times for the group.
- Discussion – having an intermediary collect presentations from holders and then share them with the final verifier.
  
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

## Future Calls

## To Dos:

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291846/20295092.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
