1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-03-04 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Mar 04, 2024

## Summary

- Updates on the AnonCreds in W3C VCDM from the Credo and ACA-Py groups (if available)
- Data organization in the AnonCreds v2 Presentation flow
- Pluggable Signatures in AnonCreds v2
- AnonCreds Hyperledger Mentorship Program ideas

## Time: 7:00 Pacific / 16:00 Central Europe Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

## Recording:

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

cifi![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- 9 others

## Related Specifications and Repositories:

- AnonCreds v1.0:
  
  - The v1.0 specification is published here: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
  - The Working Group uses this GitHub repository to manage the specification: [https://github.com/hyperledger/anoncreds-spec](https://github.com/hyperledger/anoncreds-spec)
  - The AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
  - The v1.0 implementation in Rust is here: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - The v1.0 implementation is dependent on this Rust CL Signatures implementation: [https://github.com/hyperledger/anoncreds-clsignatures-rs](https://github.com/hyperledger/anoncreds-spec-v2)
- AnonCreds v2.0
  
  - The initial framework for the v2.0 specification repository is here: [https://github.com/hyperledger/anoncreds-spec-v2](https://github.com/hyperledger/anoncreds-spec-v2)
  - The v2.0 implementation in Rust is here: [https://github.com/hyperledger/anoncreds-v2-rs](https://github.com/hyperledger/anoncreds-v2-rs)
  - Underlying AnonCreds v2.0 are cryptographic libraries in Hyperledger Labs Agora

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - Workshop Wed. April 24th: [Zero Knowledge Proofs and ZK Programming in Blockchain Application Development](https://zoom.us/meeting/register/tJYkfuyhpjsqGd1FCs-ZeFzD90EyqFy18IMt)
  - IIW – April 16-18, 2024
- Any updates to the Agenda?

## Agenda

- AnonCreds in W3C VCDM Format - Status/Updates
  
  - Test Vectors Repo: [https://github.com/TimoGlastra/anoncreds-w3c-test-vectors](https://github.com/TimoGlastra/anoncreds-w3c-test-vectors)
  - Credo / Bifold Progress:
    
    - PR is merged into Credo, 0.5.0 Alpha is available
    - Working on the Bifold – update agent to 0.5.0
  - ACA-Py Progress:
    
    - Progress and work on it.  Difficulty in getting tests to run.
    - ACA-Pug meeting tomorrow for a demo.
- Data organization in the AnonCreds v2 Presentation flow – [presentation](https://docs.google.com/presentation/d/1YqmfGwdm20wOoCgDw8CgQblCigC4W234B0Qpy5W5hbQ/edit?usp=sharing)
  
  - For ZKPs in a presentation, make the "claim" item a complex data structure, with one or more ZKPs listed with type and value.
    
    - Consider how best to handle multiple of the same type – e.g. multiple memberships on the same claim
    - TBD: The exact data format for each type (predicate, range proof, membership, etc.)
  - Revocation to be "automatic" based on whether or not the issuer decides to issue a revocable or non-revocable credential.
    
    - TBD: the flow of that during issuance
    - TBD: What about the W3C VCDM concept of "credentialStatus" and the possiblity of multiple status types on a credential.
  - Link secret to be likewise automatic – in the schema, in the credential, and always disclosed in a presentation.
  - To Do: formalize the list.
- Pluggable Signatures in AnonCreds v2 – PR submitted/merged – commits pushed to get the PR accepted.
- AnonCreds [Hyperledger Mentorship Program](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Hyperledger+Mentorship+Program) ideas – suggestion of ideas:
  
  - **A "revocation manager" implementation that can receive sharded requests and send back responses.**
  - BBS+ Implementation.
  - Rust coding to work on AnonCreds objects so that they can be published/spec'd.
  - Rust coding to do Post Quantum signatures -- a plugin to the existing library.
  - Other ideas?
- Open Discussion

## To Dos:

## Action items

- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
