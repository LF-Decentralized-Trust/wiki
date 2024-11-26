1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-04-03 AnonCreds v2.0 Working Group Meeting

Created by Stephen Curran, last modified on Apr 03, 2023

## Summary

- Revocation Scheme Proposal ALLOSAUR - Presentation - Mike Lodder
- Request: Support for Arrays and Nested data in AnonCreds
- Open Discussion

## Recording of Call: [dummyfile.txt](#)

Mike Lodder Presentation on ALLOSAUR Revocation: [dummyfile.txt](#)

Mike Lodder Q&amp;A on ALLOSAUR Revocation: [dummyfile.txt](#)

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Repositories:

- Mike Lodder's proposed Data Models: [https://hackmd.io/ZlsnLoclSveePJOZljgMfA](https://hackmd.io/ZlsnLoclSveePJOZljgMfA)
- AnonCreds v2.0 Specification Repository: [https://github.com/hyperledger/anoncreds-spec-v2/](https://github.com/hyperledger/anoncreds-spec-v2/)
- AnonCreds v1.0 Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Goals of the Working Group:

The goal of AnonCreds v2.0 is to retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security.

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - IIW – April 18-20 – Let's plan some presentations.
  - Next AnonCreds V2.0 Meeting will be **cancelled** because of IIW
  - AnonCreds Workshop presented by Hyperledger is planned for May 31, 2023, 8:00 Pacific / 17:00 Central Europe. Details to be shared.
  - I'll be talking at the Linux Foundation Open Source Summit, Metaverse Conference about Hyperledger AnonCreds and ZKPs.
- Updates to the Agenda?

## Agenda

- [Mike Lodder](https://lf-hyperledger.atlassian.net/wiki/people/557058:23b28066-a30e-4a6b-9b86-34dae49fd7f0?ref=confluence)  will continue the discussion of his proposal for AnonCreds v2.0, this time talking about the proposed [ALLOSAUR accumulator/ZKP revocation scheme](https://eprint.iacr.org/2022/1362).
- Request: Support for Arrays and Nested data in AnonCreds – [Kyle Robinson](https://lf-hyperledger.atlassian.net/wiki/people/60e73ed74134aa0069502ec1?ref=confluence) - Presentation: [BC Digital Trust AnonCreds April 3 2023.pptx](attachments/20292148/20295129.pptx)
  
  - Supported needed for arrays and nested data.
  - Suggestion is to use Data URLs (e.g., "`data: application/json,...")` – Aries RFC being posted Real Soon Now: 
    
    - Holder, verifier would at least know that the Attribute contained a string that was (in this case) JSON data, and could process it accordingly.
    - However – would lose ability to selectively disclose (all or nothing) or use predicates on such data.
    - Same approach is going to be used for images in attributes – "`data: image/png,...")`
- Plans for IIW?
- Next Meeting (two weeks):
  
  - Cancelled for IIW

## Future Calls

- Collect some use case specific examples and continue the discussions:
  
  - Applying the data structures to a real use case or two
    
    - Take an existing AnonCreds Schema (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/13)) and Credential Definition (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/14)) and define what it would be using Mike's proposed data models.
      
      - Where would the data models exist, such as on ledger, in the AnonCreds specification?
  - What concrete uses other than link-secret is there for blinded data in a credential?

## To Dos:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [BC Digital Trust AnonCreds April 3 2023.pptx](attachments/20292148/20295129.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292148/20295132.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292148/20295131.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20292148/20295130.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
