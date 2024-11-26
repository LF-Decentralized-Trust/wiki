1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2020 AFJ meetings](2020-AFJ-meetings_18513105.html)

# Hyperledger Aries : 2020-08-28 Aries Framework JS Meeting notes

Created by shonjs, last modified by Jakub Koci on Sep 04, 2020

## Date

28 Aug 2020

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence)  (Animo) &lt;karim@animo.id&gt;
- [Ajay Jadhav](https://lf-hyperledger.atlassian.net/wiki/people/557058:4c9b11a5-2616-4abe-af94-bbc11c984654?ref=confluence) (AyanWorks) &lt;ajay@ayanworks.com&gt;

## Agenda

- Record the meeting
- Don't use indy-sdk types as globals, but import them explicitly
- Update about credential exchange (Jakub)
- Encode/decode library vs Buffer (Jakub)
- Serialization/deserialization of data stored into db and send via transport layer (Jakub)

## Meeting Notes

- Current thoughts on Serialization/deserialization of data stored into db and send via transport layer:
  
  - Transform class instance to JSON string just before storing
  - Directly after retrieving transform to class instance again
  - [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) Will think more about it
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) started using the framework inside a react native app
  
  - Will give insights on the consumer side of the framework.
  - For now only Android. Working on iOS
  - Current issues:
    
    - OutboundPackage not exposed from index of framework
    - IndySDK is needed (because of devDependency) even when using framework in React Native app

## Action items

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Remove global Indy type definitions. Make type imports explicit.
- We need to document and be aware of packages and globals that are native to NodeJS
  
  - buffer → [https://www.npmjs.com/package/buffer](https://www.npmjs.com/package/buffer)
  - events → [https://www.npmjs.com/package/events](https://www.npmjs.com/package/events)
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) Replace base64 NPM package with buffer

## Future topics

- State machines

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
