1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-11-06 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Dec 15, 2023

## Summary

- PRs to the AnonCreds specification – current status
- Design and planning – AnonCreds v1.0 in the W3C Verifiable Credentials Data Model Standard format
- Open Discussion

## Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

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

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

[Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (DSR Corporation) &lt;alexander.sherbakov@dsr-corporation.com&gt;

[Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) (DSR Corporation) &lt;artem.ivanov@dsr-corporation.com&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  
  - Ledger Agnostic AnonCreds Project Page: [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
- Any updates no the Agenda?

## Agenda

Open Issues

- [PRs](https://github.com/hyperledger/anoncreds-spec/pulls) to Review
- Design and planning – AnonCreds v1.0 in the W3C Verifiable Credentials Data Model Standard format
  
  - The BC Gov Code With Us on AnonCreds Rust – [https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/d81f1bb4-4abb-4a4c-8b19-92904e0bd6a6](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/d81f1bb4-4abb-4a4c-8b19-92904e0bd6a6)
  - PR with a starting point for discussing the design: [https://github.com/hyperledger/anoncreds-rs/pull/266](https://github.com/hyperledger/anoncreds-rs/pull/266)
    
    - Questions Raised:
      
      - JSON-LD processing on the contexts?
      - Identifier within the `CredentialSubject` ?
      - Nested JSON and Arrays in AnonCreds credentials.
      - Encoding scheme – move into AnonCreds or leave for the issuer?
      - Time of Day for the \`IssuanceDate\` field
      - Use of the term "Data Integrity Proof" to differentiate AnonCreds and non-AnonCreds Data Integrity Proofs.
      - Simple vs. complex/size efficient encoding of the proof data into a single "proof" JSON item?
      - "mapping" of source VC attributes/predicates to the presentation request.
      - Using other than the AnonCreds presentation request model
      - Out of scope – support in the AnonCreds library for signing W3C VC/VP Format Data Integrity Proofs with other Proof Types.
        
        - There might be some "devil in the details" in this. Do we have to add extra values (notably `issuer` ) to have a second signature?
      - Altering the format/Data Model of the Credential Offer and Request format.
      - Proposed AnonCreds library API changes.
      - Using AnonCreds W3C format with OpenID4VCs.  Can OpenID4VCs support the necessary Offer-Request-Issuer flow?
  - Downstream Code With Us opportunities for [Aries Cloud Agent Python](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/7afcbd7c-2bbc-41ed-bf27-b6ba6e2903c5) and [Aries Framework JavaScript](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/6f08d6d5-7e3d-489a-a98f-d7c607309dc9)
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

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
