1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2020 AFJ meetings](2020-AFJ-meetings_18513105.html)

# Hyperledger Aries : 2020-11-06 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Ajay Jadhav on Nov 10, 2020

## Date

06 Nov 2020

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Ajay Jadhav](https://lf-hyperledger.atlassian.net/wiki/people/557058:4c9b11a5-2616-4abe-af94-bbc11c984654?ref=confluence) (AyanWorks) &lt;ajay@ayanworks.com&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;
- [shonjs](https://lf-hyperledger.atlassian.net/wiki/people/557058:b2736d63-185c-457c-88a1-e84b63da434d?ref=confluence) (KBA) &lt;rush2shon@gmail.com)

## Status updates

- Issue credential protocol
  
  - Issue credential merged
  - Still needed:
    
    - Start with credential proposal
    - advanced threading
    - validate credential preview against actual credential
- Present proof protocol
  
  - First PR for presentation request message opened
- AFJ ↔ React Native
  
  - [https://github.com/TimoGlastra/aries-mobile-agent-javascript](https://github.com/TimoGlastra/aries-mobile-agent-javascript)
  - Errors thrown by rn-indy-sdk do not match errors thrown by indy-sdk for NodeJS ([https://github.com/AbsaOSS/rn-indy-sdk/issues/21](https://github.com/AbsaOSS/rn-indy-sdk/issues/21))
- Started work on \`@types/indy-sdk\`
  
  - DefinitelyType will be updated instantly, adding to indy-sdk repo limits us to their release cycle
  - I hope this would also allow us to reuse the types for rn-indy-sdk
  - [https://github.com/TimoGlastra/DefinitelyTyped/tree/%40types/indy-sdk/types/indy-sdk](https://github.com/TimoGlastra/DefinitelyTyped/tree/%40types/indy-sdk/types/indy-sdk)
  - [https://github.com/TimoGlastra/aries-framework-javascript/tree/feature/external-indy-sdk-types](https://github.com/TimoGlastra/aries-framework-javascript/tree/feature/external-indy-sdk-types)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/38](https://github.com/hyperledger/aries-framework-javascript/issues/38)

## Agenda

- Record the meeting
- Show how to run various kind of framework tests
- Reiterate toJSON approach
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/113](https://github.com/hyperledger/aries-framework-javascript/issues/113)
- Inconsistencies between connection and issue credential implementations
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/115](https://github.com/hyperledger/aries-framework-javascript/issues/115)
- Auto accept credentials (+connections)
  
  - More granular config? (Like ACA-Py with auto-accept-request / auto-accept-response)
  - Currently when you accept the credential request, you accept the whole credential. No option to control every step of the protocol.
    
    - How will this work with auto-accept credentials? [https://github.com/hyperledger/aries-framework-javascript/issues/116](https://github.com/hyperledger/aries-framework-javascript/issues/116)
- Decide on logger library to use
  
  - Create custom logger interface so library is abstracted away?
  - [https://github.com/hyperledger/aries-framework-javascript/issues/77](https://github.com/hyperledger/aries-framework-javascript/issues/77)
- Use new [https://didcomm.org](https://didcomm.org) prefix for agent message types
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/121](https://github.com/hyperledger/aries-framework-javascript/issues/121)
  - [https://github.com/hyperledger/aries-rfcs/blob/master/features/0348-transition-msg-type-to-https/README.md](https://github.com/hyperledger/aries-rfcs/blob/master/features/0348-transition-msg-type-to-https/README.md)
- Reiterate possible approaches for \`@types/indy-sdk\`

## Meeting Notes

## Future topics

- State machines
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion\_r517635298](https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion_r517635298)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18489314/18514347.txt "Download")

Nov 06, 2020 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
