1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-11-25 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified on Nov 25, 2021

Planned Topics:

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Aries Mobile Summit
  
  - We decided on weekly 2 hour sessions, with agendas for each meeting created in advance. Meetings will be recorded. Summary information will be shared during the regular weekly Aries calls.
  - Areas of interest: mobile infrastructure, security, UX/UI of invitation, UX/UI of credential, mobile agent specific protocols
- Animo has won eSSIF Lab Grant to build Aries Mobile SDK - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://drive.google.com/file/d/1t9_XljI9rvFrgvNVM7ymxFae3Xo0Nhvx/view?usp=sharing)
  
  - AIP 2.0
  - BBS+, JSON-LD
  - Shared components (Aries Askar, Indy CredX, Indy VDR)

## Agenda

- Record the meeting
- Out of Band Updates ([Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence))
  
  - [Add support for RFC 0434: Out-of-Band](https://github.com/hyperledger/aries-framework-javascript/issues/344)
  - [https://github.com/hyperledger/aries-framework-javascript/compare/main...jakubkoci:out-of-band](https://github.com/hyperledger/aries-framework-javascript/compare/main...jakubkoci:out-of-band)
- DIDs ([Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence))
- Send message and update state
- PII inside log messages
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/551](https://github.com/hyperledger/aries-framework-javascript/issues/551)

## Open Issues

- [Finish getting started guides in documentation](https://github.com/hyperledger/aries-framework-javascript/issues/338) !!! Stephen &amp; Mostafa
- [Add support for receiving and proving revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/349) - James
- Loading ledger asynchronously - reduce the time it takes when receiving a credential
- How to handle the case without an internet connection
- [Add support for RFC 0035: Problem Report](https://github.com/hyperledger/aries-framework-javascript/issues/58) - both adopted into other protocols and initiating it as a standalone protocol
- [wallet import and export](https://github.com/hyperledger/aries-framework-javascript/issues/175)
- Add demos on how to use AFJ as issuer/holder/verifier (like sample mediator)
- Machine-readable governance frameworks
- Action menu
- [Add support for verifying revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/350)
- [Allow invitations to use public DID](https://github.com/hyperledger/aries-framework-javascript/issues/84)
- [Add support for RFC 0434: Out-of-Band](https://github.com/hyperledger/aries-framework-javascript/issues/344) - Priority (Connection reuse)
- [Add support for RFC 0023: DID Exchange](https://github.com/hyperledger/aries-framework-javascript/issues/345)
- [Add support for 0453: Issue Credential v2](https://github.com/hyperledger/aries-framework-javascript/issues/352)

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
- Monorepo dependencies
  
  - TypeScript types

**Meeting recording:**

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
