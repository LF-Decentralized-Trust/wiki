1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-01-22 Aries Framework JS Meeting notes

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
- Present proof protocol
  
  - Feature branch: [https://github.com/hyperledger/aries-framework-javascript/tree/feature/present-proof](https://github.com/hyperledger/aries-framework-javascript/tree/feature/present-proof)
- AFJ ↔ React Native
  
  - [https://github.com/animo/aries-mobile-agent-react-native](https://github.com/animo/aries-mobile-agent-react-native)
- Started work on \`@types/indy-sdk\`
  
  - [DefinitelyTyped @types/indy-sdk working branch](https://github.com/TimoGlastra/DefinitelyTyped/tree/%40types/indy-sdk/types/indy-sdk)
  - [AFJ @types/indy-sdk dependency working branch](https://github.com/TimoGlastra/aries-framework-javascript/tree/feature/external-indy-sdk-types)
  - [@types/indy-sdk issue](https://github.com/hyperledger/aries-framework-javascript/issues/38)

## Agenda

- Record the meeting
- Error after framework update
- WebSockets
  
  - How to get rid of polling?
  - Should an edge agent get just notification about new messages or should it get forwarded messages directly via WebSocket?
    
    - In both cases, the mediator needs to know how to forward an incoming message belonging to the given \`verkey\`. Should it store into storage for polling or send it (message, or notification message) directly via WebSocket.
    - How to pass such information?
- Architecture refactoring
  
  - agent
  - decorators
  - modules
    
    - basicmessage
    - connections + trustping
    - credentials
    - routing + coordinatemediation + messagepickup
  - storage
  - transport
  - utils
  - wallet
  - ...
- Module structure
  
  - api/index
  - handlers
  - services
  - messages

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
- State machines
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion\_r517635298](https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion_r517635298)

## File Modified Labels No labels [Edit Labels](# "Edit Labels") [Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true) Text File [chat.txt](attachments/18490295/18514701.txt "Download") Jan 29, 2021 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5) Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif) Upload file File description
