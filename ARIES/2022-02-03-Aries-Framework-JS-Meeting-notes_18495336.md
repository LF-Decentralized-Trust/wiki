1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-02-03 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified on Feb 03, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)&lt;jakub.koci@gmail.com&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Animo has won eSSIF Lab Grant to build Aries Mobile SDK - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://drive.google.com/file/d/1t9_XljI9rvFrgvNVM7ymxFae3Xo0Nhvx/view?usp=sharing)
  
  - AIP 2.0
  - BBS+, JSON-LD
  - Shared components (Aries Askar, Indy CredX, Indy VDR)

## Agenda

- Record the meeting
- AFJ holder interoperability
- Issue Credential V2
- Out-of-band &amp; DID Exchange  ([Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)) 
  
  - update OOB API
  - interop with Aries Framework .NET as it doesn’t recognize DidDommService
  - If the `did` is resolvable (either an inline `peer:did` or a publicly resolvable DID), the `did_doc~attach` attribute should not be included. [https://github.com/hyperledger/aries-rfcs/blob/main/features/0023-did-exchange/README.md#request-message-attributes](https://github.com/hyperledger/aries-rfcs/blob/main/features/0023-did-exchange/README.md#request-message-attributes)
- Present proof directory structure
- Revocation ([James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence))
- Allow to support multiple versions of the same protocol
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/596](https://github.com/hyperledger/aries-framework-javascript/issues/596)
  - *We’ve also found a few agents that have already implemented the [Aries Out-of-Band 1.1 protocol](https://github.com/hyperledger/aries-rfcs/tree/4e78319e5f79df2003ddf37f8f497d0fae20cc63/features/0434-outofband) without implementing the previous versions of Out-of-Band. These agents also fail testing with try.connect.me*
- Open PRs
- AMA

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
- Monorepo dependencies
  
  - TypeScript types

![](plugins/servlet/confluence/placeholder/unknown-attachment)

**Meeting recording:**

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
