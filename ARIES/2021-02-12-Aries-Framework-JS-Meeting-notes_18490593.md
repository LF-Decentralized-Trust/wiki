1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-02-12 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified by Timo Glastra on Feb 12, 2021

## Date

12 Feb 2021

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

## Status updates

- Issue credential protocol
  
  - Still needed:
    
    - Start with credential proposal
    - advanced threading
    - validate credential preview against actual credential
    - storing messages
- Present proof protocol
  
  - Feature branch: [https://github.com/hyperledger/aries-framework-javascript/tree/feature/present-proof](https://github.com/hyperledger/aries-framework-javascript/tree/feature/present-proof)

## Agenda

- Record the meeting
- Update meeting calendar event
- WebSockets

## Meeting Notes

- Move to bi-weekly meeting (for a while)
  
  - 2021-02-12
  - 2021-02-26
  - ...
- Import / Export
- Use record state values that match RFC
  
  - PROPOSAL\_RECEIVED → proposal-received
- Store complete didcomm message, but add util methods to make it easier to work it.
  
  - next version: Add option to remove the history of messages (like in ACA-Py, auto-remove option)
- Modules will have ids that reference records as input, Services will use the actual record objects as input
- find vs get
  
  - findXXX → can return null
  - getXXX → will throw error if not found
  - Create dedicated error class for RecordNotFound
  - [https://github.com/hyperledger/aries-framework-javascript/issues/78](https://github.com/hyperledger/aries-framework-javascript/issues/78)
  - findAll vs getAll
- Response messages
  
  - negotiate vs createXXXAsResponse
  - module will use negotiate
  - service will use createXXXAsResponse
- Auto accept present proof
  
  - Auto send ack message? ([https://github.com/hyperledger/aries-rfcs/issues/471](https://github.com/hyperledger/aries-rfcs/issues/471))
- State machines
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion\_r517635298](https://github.com/hyperledger/aries-framework-javascript/pull/130#discussion_r517635298)
  - Aries Framework .NET → [https://github.com/hyperledger/aries-framework-dotnet/blob/a18bef91e5b9e4a1892818df7408e2383c642dfa/src/Hyperledger.Aries/Features/IssueCredential/Records/CredentialRecord.cs#L164](https://github.com/hyperledger/aries-framework-dotnet/blob/a18bef91e5b9e4a1892818df7408e2383c642dfa/src/Hyperledger.Aries/Features/IssueCredential/Records/CredentialRecord.cs#L164)
  - Implement ourselves rather than use a library to implement state machines
  - Make it smarter than Aries protocols
    
    - Transition state according to message type

## Future topics

## File Modified No files shared here yet. Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif) Upload file File description
