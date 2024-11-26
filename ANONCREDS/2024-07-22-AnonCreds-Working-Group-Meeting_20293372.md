1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-07-22 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Jul 23, 2024

## Summary

- Proposed scheme for unlinkability with ZKPs using hardware based holder key
- AnonCreds Project Charter
- Project status updates – Revocation Manager for ALLOSAUR, BBS, auditing
- Open Discussion

## Time: 15:00 Pacific / 16:00 Mountain / Super Late Central Europe (Midnight...) / 10:00 Auckland/Wellington Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

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
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

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
- Any updates to the Agenda?

## Agenda

- Proposal from Dfinity / Google / Jan Camenisch for using ZKPs with Hardware Keys
  
  - Follows:
    
    - Feedback from Cryptographers on the European ARF
      
      - GitHub Issue: [https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/66](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/66)
      - Paper: [https://github.com/user-attachments/files/15904122/cryptographers-feedback.pdf](https://github.com/user-attachments/files/15904122/cryptographers-feedback.pdf)
  - Proposal: [EUDI\_Follow\_up-2.pdf](attachments/20293372/20295316.pdf)
  - Presentation about the proposal: [https://docs.google.com/presentation/d/1uuPzP7yqXWhePDKloaQx3pbY4r-PrNUy2plbSR\_kjkw/edit?usp=sharing](https://docs.google.com/presentation/d/1uuPzP7yqXWhePDKloaQx3pbY4r-PrNUy2plbSR_kjkw/edit?usp=sharing)
- AnonCreds Project Charter:
  
  - Stems from the recent "intent to form" [announcement](https://www.linuxfoundation.org/press/linux-foundation-announces-intent-to-form-lf-decentralized-trust) from the Linux Foundation and Hyperledger Foundation about LF Decentralized Trust.
  - Proposed Charter: [https://docs.google.com/document/d/1UiUv2H\_xOHxV\_rXfTSlsPu2TdQjgxNlVhU67RtqbMlM/edit?usp=sharing](https://docs.google.com/document/d/1UiUv2H_xOHxV_rXfTSlsPu2TdQjgxNlVhU67RtqbMlM/edit?usp=sharing)
  - No objections to the changes were raised at the meeting
- Status updates from current work:
  
  - Revocation Manager for ALLOSAUR Project – Hyperledger Mentorship project being executed by [VictorH2208](https://lf-hyperledger.atlassian.net/wiki/people/712020:a4e736ac-f0a4-4270-ae8b-ef76cebf844d?ref=confluence)[Project plan](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Project+Plan+-+AnonCreds+v2+Credential+Revocation+Manager+Implementation)
  - BBS Signatures
  - Audit Updates from Mike Lodder: 
    
    - blsful - audit complete and published in Agora
    - Audit complete: Genaro to be contributed
    - Audits wrapping up: verifiable-secret-sharing (overview meeting this Thursday)
    - Being audited: threshold-mpc libraries
- Open Discussion

## To Dos:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [EUDI\_Follow\_up-2.pdf](attachments/20293372/20295316.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
