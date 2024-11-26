1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-04-07 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Apr 07, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) &lt;timo@animo.id&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) &lt;berend@animo.id&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Hyperledger moved to Discord
  
  - Replaces rocket.chat
  - [https://discord.gg/N84Eg4z3](https://discord.gg/N84Eg4z3)
- 0.2.0 release of AFJ
  
  - Target to have all PRs merged by march 15th
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/622](https://github.com/hyperledger/aries-framework-javascript/discussions/622)
  - Done:
    
    - [Add support for receiving and proving revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/349)
    - [Add support for verifying revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/350)
  - In Review:
    
    - [Add support for 0453: Issue Credential v2](https://github.com/hyperledger/aries-framework-javascript/issues/352)
    - [Add support for 0454: Present Proof v2](https://github.com/hyperledger/aries-framework-javascript/issues/353)
    - [Add support for RFC 0183 Revocation Notification Protocol](https://github.com/hyperledger/aries-framework-javascript/issues/493)
    - [Need strategy for handling breaking changes in storage records](https://github.com/hyperledger/aries-framework-javascript/issues/305)
  - In Progress:
    
    - [Add support for RFC 0023: DID Exchange](https://github.com/hyperledger/aries-framework-javascript/issues/345)
    - [Add support for RFC 0434: Out-of-Band](https://github.com/hyperledger/aries-framework-javascript/issues/344)

## Agenda

- Record the meeting
- 0.2.0 Release
  
  - Issue Credential v2 - Working on W3C credentials and comments from PR
  - Present Proof v2 - Working on fixing e2e tests
  - Revocation Notification - ?
  - DIDExchange / OOB
    
    - did:key to for recipientKeys, routingKeys
    - transforming service into did:peer
    - starting work on handshake reuse
- Split up working group
- Aries CLI Demo
  
  - [https://aries-cli.animo.id](https://aries-cli.animo.id)
  - [https://github.com/animo/aries-cli](https://github.com/animo/aries-cli)
- Update Assistant
- AMA

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
- Monorepo dependencies
  
  - TypeScript types

**Meeting recording:**

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18496046/18516132.txt "Download")

Apr 07, 2022 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
