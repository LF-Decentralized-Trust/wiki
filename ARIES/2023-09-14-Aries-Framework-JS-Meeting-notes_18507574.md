1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-09-14 Aries Framework JS Meeting notes

Created by Ariel Gentile, last modified by Timo Glastra on Sep 14, 2023

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Meetings suspended until September
- Aries Call [2023-08-30 Aries Working Group Call](2023-08-30-Aries-Working-Group-Call_18507105.html)
  
  - Discussion on peer did migration
    
    - Proposed did:peer:4 to replace all previous methods
    - [https://github.com/dbluhm/did-peer-4](https://github.com/dbluhm/did-peer-4)
  - DID Rotate protocol
- New Code With Us from BC Gov
  
  - [https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/51d7c289-51a8-4307-939c-5a4271c7b2b6](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/51d7c289-51a8-4307-939c-5a4271c7b2b6)
  - Create a Load Generator for Testing BC Gov Issuers, Verifiers, and DIDComm Mediator

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)

## Agenda

- Record the meeting
- DIDComm v2
  
  - Supporting multiple versions of DIDComm WIP by [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence)
- 0.5.0 release
  
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/1525](https://github.com/hyperledger/aries-framework-javascript/discussions/1525)
    
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1427](https://github.com/hyperledger/aries-framework-javascript/pull/1427)
    - Drop node 16 support
  - Releasing new wrapper versions (for dropping support for Node 16)
    
    - [https://github.com/hyperledger/aries-askar/pull/179](https://github.com/hyperledger/aries-askar/pull/179)
    - Need to update Indy VDR React Native wrapper: [https://github.com/hyperledger/indy-vdr/issues/216](https://github.com/hyperledger/indy-vdr/issues/216)
    - Need to create AnonCreds version update PR
    - Mark the indy-sdk as deprecated
  - DIDComm V2 moved to 0.6.x
  - Message repository updates?
    
    - Does not support filtering by key/id
- Keeping http socket open, when using implicit invitations
  
  - delay the closing of the http session?
  - Have a interface to override session closing handling? If not registered it will auto close if no response internally. Otherwise you get control over it
    
    - could be solved using middleware?
    - [https://github.com/hyperledger/aries-framework-javascript/issues/97](https://github.com/hyperledger/aries-framework-javascript/issues/97)
    - feels a bit hacky? Requires you to implement custom logic, but there's probably more people that need to solve this issue → accepting request based on implicit invitation from an agent without an endpoint
  - Add option to auto accept requests to implicit invitations for certain dids?
    
    - DidRecord.metadata.allowImplicitInvitations = true
    - config: { autoAcceptImplicitInvitationsForDids: \["did:web:mediator.animo.id"] }
- Support ~timing decorator natively in AFJ
- Separating the storage layer
  
  - Storing messages? All state should be derived from message exchange
    
    - User chooses whether to store the messages, but user needs to provide the current state of the protocol
  - Goal from Timo: More control over the database entities, how state is persisted.
  - Built in storage useful in a lot of cases as well
  - Discuss next time: current storage model

## Meeting Notes

## Recording / Slides

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Extracting parts of AFJ into generic libraries
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
