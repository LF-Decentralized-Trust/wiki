1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-07-15 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified on Jul 15, 2021

## Date

15 Jul 2021

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call

## Agenda

- Record the meeting
- RN Indy SDK Absa donation announcement :)
  
  - [https://github.com/hyperledger/indy-sdk-react-native/](https://github.com/hyperledger/indy-sdk-react-native/)
- Auto acceptation
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/336](https://github.com/hyperledger/aries-framework-javascript/pull/336)
- PR priority
- Mediation
  
  - Some issues to be resolved
  - [https://github.com/hyperledger/aries-framework-javascript/issues/381](https://github.com/hyperledger/aries-framework-javascript/issues/381)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/379](https://github.com/hyperledger/aries-framework-javascript/issues/379)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/378](https://github.com/hyperledger/aries-framework-javascript/issues/378)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/371](https://github.com/hyperledger/aries-framework-javascript/issues/371) (DID Resolver Interface discussion)
- Documentation overhaul
  
  - with help from Mostafa Youssef
  - [https://lucid.app/lucidchart/invitations/accept/inv\_f6076e23-cb5b-4fd7-9e9c-922fc6c3486d?viewport\_loc=-403,1232,1629,1056,0\_0](https://lucid.app/lucidchart/invitations/accept/inv_f6076e23-cb5b-4fd7-9e9c-922fc6c3486d?viewport_loc=-403%2C1232%2C1629%2C1056%2C0_0)
  - [https://lucid.app/lucidchart/52e02e25-ae09-469a-966e-bc99529f48f2/edit?shared=true&amp;page=0\_0#](https://lucid.app/lucidchart/52e02e25-ae09-469a-966e-bc99529f48f2/edit?shared=true&page=0_0)
- Monorepo dependencies
  
  - TypeScript types
- createProof RequestedCredentials
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/382](https://github.com/hyperledger/aries-framework-javascript/issues/382)
- Support for Deno
  
  - Although it's not our focus right now, it should be possible in the long term.
  - First, we need to analyze if the following dependencies will work in Deno or what we need to do to make it work:
    
    - indy-sdk
    - native dependencies (file system, transport protocols like HTTP or WebSockets, ...)
    - other dependencies in package.json

## Meeting Notes

## Future topics

- React Native testing

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
