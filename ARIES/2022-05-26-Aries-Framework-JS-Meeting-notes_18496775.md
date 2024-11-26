1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-05-26 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on May 26, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar / BC Gov) &lt;jason.leach@fullboar.ca&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Hyperledger moved to Discord
  
  - Replaces rocket.chat
  - [https://discord.gg/hyperledger](https://discord.gg/hyperledger)
- Releases
  
  - Next release - 0.2.0
    
    - Issue Credential v2 indy
    - Present Proof v2 indy
    - Out of Band / DID Exchange - no public dids yet
    - Pickup v2
    - Holder/Verifier revocation and revocation notification
  - 0.3.0
    
    - Issue Credential v2 JSON-LD
    - Present Proof v2 JSON-LD
    - Shared Components?
    - Splitting up the framework

## Agenda

- Record the meeting
- OOB / DID Exchange / Issue credential v2 fixes
- JSON-LD Credential support update
- Message queueing in mobile agents
- Splitting up the framework
  
  - With all the features being added we need to split up the framework
  - [https://hackmd.io/6eXZcMhdQR-QCNPMFYTvuA?view](https://hackmd.io/6eXZcMhdQR-QCNPMFYTvuA?view)
- AMA

## Meeting Notes

- Aries Agent Test Harness documentation for AFJ
- Message queueing in mobile agents
  
  - Context
    
    - using AFJ in mobile agent in bifold
    - using websockets to pick up messages from mediator
  - Problem: messages are not processed sequentially in order
  - Batch pickup already queues messages and processes in order
  - Websocket transport does not queue messages
  - Issue occurs because the credential offer is sent when the connection is still response, did exchange doesn't have this problem anymore because of required complete message.
  - How do we want to proceed with having ability to configure messages being processed sequentially or in parallel
  - Use sequential processing for pickup v1, v2 and implicit.  ([Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence))

## Future topics

- React Native testing
- Support for Deno
- Monorepo dependencies
  
  - TypeScript types

**Meeting recording:**

[meeting-recording](#)

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
