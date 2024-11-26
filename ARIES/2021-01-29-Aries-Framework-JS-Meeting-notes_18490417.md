1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-01-29 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified on Jan 29, 2021

## Date

15 Jan 2021

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;

## Status updates

- Issue credential protocol
  
  - Issue credential merged
  - Still needed:
    
    - Start with credential proposal
    - advanced threading
    - validate credential preview against actual credential
    - storing messages
- Present proof protocol
  
  - Feature branch: [https://github.com/hyperledger/aries-framework-javascript/tree/feature/present-proof](https://github.com/hyperledger/aries-framework-javascript/tree/feature/present-proof)
- Mobile Agent
  
  - [https://github.com/animo/aries-mobile-agent-react-native](https://github.com/animo/aries-mobile-agent-react-native)
- First version of @types/indy-sdk released
  
  - [https://npmjs.org/package/@types/indy-sdk](https://npmjs.org/package/@types/indy-sdk)
  - [AFJ @types/indy-sdk dependency working branch](https://github.com/TimoGlastra/aries-framework-javascript/tree/feature/external-indy-sdk-types)
  - [@types/indy-sdk issue](https://github.com/hyperledger/aries-framework-javascript/issues/38)

## Agenda

- Record the meeting
- Update meeting calender event
- rename master to main
- did pr
- storing messages

## Meeting Notes

- ...

## Future topics

- Use record state values that match RFC
  
  - Easy for comparison, why not?
- Only storing message content (CredentialPreview, PresentationPreview, CredOffer) instead of complete didcomm message?
  
  - unnessacary base64 encoding / decoding
- IDs vs Objects
- find vs get
  
  - Error vs non-error
  - [https://github.com/hyperledger/aries-framework-javascript/issues/78](https://github.com/hyperledger/aries-framework-javascript/issues/78)
- Present Proof Progress
  
  - How to handle auto accept?
  - negotiate vs createXXXAsResponse
- State machines
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion\_r517635298](https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion_r517635298)

## File Modified No files shared here yet. Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif) Upload file File description
