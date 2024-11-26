1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-04-01 Aries Framework JS Meeting notes

Created by Jakub Koci on Mar 31, 2021

## Date

01 Apr 2021

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))

## Agenda

- Record the meeting
- Websockets
  
  - [Support multiple transporters at the same time](https://github.com/hyperledger/aries-framework-javascript/issues/101)
  - [Add HTTP and WebSocket default transporters to the framework](https://github.com/hyperledger/aries-framework-javascript/issues/102)
  - [Add transport into message context](https://github.com/hyperledger/aries-framework-javascript/issues/81)
- Revocation Notification
- [Rename \`CredentialRecord\` and \`ProofRecord\` to \`CredentialExchangeRecord\` and \`PresentationExchangeRecord\`](https://github.com/hyperledger/aries-framework-javascript/issues/199)
- Suggestions for DI framework/library - must work with React-Native
  
  - Inversify - need to investigate
  - NestJs - mostly server side - but it's worth investigating for RN
  - Tsyringe - [https://github.com/microsoft/tsyringe/issues/124](https://github.com/microsoft/tsyringe/issues/124)
- Features required for Aries Bifold
  
  - Full support for mediator Coordination protocol
    
    - [Store mediation messages inside the framework](https://github.com/hyperledger/aries-framework-javascript/issues/103)
    - [Mediator coordination protocol](https://github.com/hyperledger/aries-framework-javascript/issues/63)
    - [Mediation for Edge Agents in Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript/issues/40)
  - Multiple transports / WebSocket support
  - Revocation
    
    - [Add support for revocation in issue credential and present proof protocols](https://github.com/hyperledger/aries-framework-javascript/issues/112)
  - [Credentials have no easy way to access its attributes](https://github.com/hyperledger/aries-framework-javascript/issues/187)
  - rn-indy-sdk: [Error: Wallet already opened during development](https://github.com/AbsaOSS/rn-indy-sdk/issues/41)
  - rn-indy-sdk: [prover search credentials for iOS](https://github.com/AbsaOSS/rn-indy-sdk/pull/42)
  - rn-indy-sdk: Create AAR and Pod for Android respective iOS for easier distribution of the libindy library
  - rn-indy-sdk: Compile libindy library also for iOS Simulator and Android Emulator
- Version 1.0
  
  - Export/Import
  - Revocations
  - Full mediator support
    
    - Internalize the handling of mediation messages
  - Support multiple transport mechanisms,
    
    - Add two default transporters for WebSockets and HTTP
  - Libindy storage plugin?

## Meeting Notes

## Future topics

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18491667/18515053.txt "Download")

Apr 01, 2021 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
