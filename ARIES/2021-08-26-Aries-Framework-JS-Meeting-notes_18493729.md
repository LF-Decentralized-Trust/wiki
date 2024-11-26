1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-08-26 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified by Stephen Curran on Sep 22, 2021

Planned Topics:

- Dependency between MediatorPickupStrategy and transport layer
- Multi-transport with both HTTP and WebSocket together
- Use smaller library for date parsing #439

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)(Absa)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call

## Agenda

- Dependency between MediatorPickupStrategy and transport layer
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/434/files](https://github.com/hyperledger/aries-framework-javascript/pull/434/files)
  - [https://github.com/hyperledger/aries-framework-javascript/pull/432](https://github.com/hyperledger/aries-framework-javascript/pull/432)
- Multi-transport with both HTTP and WebSocket together
- [Use smaller library for date parsing #439](https://github.com/hyperledger/aries-framework-javascript/issues/439)

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
  
  - Although it's not our focus right now, it should be possible in the long term.
  - First, we need to analyze if the following dependencies will work in Deno or what we need to do to make it work:
    
    - indy-sdk
    - native dependencies (file system, transport protocols like HTTP or WebSockets, ...)
    - other dependencies in package.json
- Monorepo dependencies
  
  - TypeScript types

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
