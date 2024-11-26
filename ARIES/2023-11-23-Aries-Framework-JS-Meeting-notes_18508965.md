1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-11-23 Aries Framework JS Meeting notes

Created by Ariel Gentile, last modified by Alexander Shenshin on Nov 23, 2023

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) - DSR Corporation (alexander.shenshin@dsr-corporation.com)

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call [2023-11-08 Aries Working Group Call](2023-11-08-Aries-Working-Group-Call_18508719.html)
  
  - Unqualified DIDs
  - DIDComm V2 follow-up
  - LTS Policy

## Agenda

- Record the meeting
- Moving to OWF - proposal 
  
  - [https://github.com/openwallet-foundation/project-proposals/pull/26](https://github.com/openwallet-foundation/project-proposals/pull/26)
  - Working on a good name! agent.js? Something with trust? Use a custom scope (e.g. @trust.js/core, @trust-framework/core)
- 0.5.0 release
  
  - AnonCreds revocation (merged, but need to document)
  - Remove Indy SDK ([https://github.com/hyperledger/aries-framework-javascript/pull/1629](https://github.com/hyperledger/aries-framework-javascript/pull/1629))
  - Test wrappers in React Native. Release stable versions
  - Message Pickup V2 Live mode support
  - OpenID4VC
  - Unqualified DID Community Coordinated Update Step 1/2
    
    - Signature update in DID Exchange (1.1)
    - did:peer:4 support
    - DID Rotation (part of connections module)
- Tenants PR
  
  - How to store efficiently when using multi-tenancy. Separate sensitive data from not sensitive data that can be indexable/needs more performance

## Meeting Notes

- Moving to OWF - meeting notes from this week's Aries WG
  
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/1586](https://github.com/hyperledger/aries-framework-javascript/discussions/1586)
  - Org migrations should be done with a transfer of the repo
    
    - maintains links &amp; commit history
    - Move is far better than a fork.
  - Should discuss which components would be moved simultaneously
    
    - Probably at least Bifold and Askar
  - What to do with the RFCs?
  - Interoperability: are .Net and Go implementations still interoperable with the latest RFCs and interop suite?
    
    - .Net already moved to OWF
  - OWF policy: maintainers are in charge of the repositories and decisions (same as in Hyperledger)
  - AJF would probably be the most mature wallet framework, so OWF would have an incentive to promote and market it

## Recording / Slides

## Future topics

Future Topics:

- 0.5.0 release
- Separating the storage layer
  
  - Storing messages? All state should be derived from message exchange
    
    - User chooses whether to store the messages, but user needs to provide the current state of the protocol
  - Goal from Timo: More control over the database entities, how state is persisted.
  - Built in storage useful in a lot of cases as well
  - Discuss next time: current storage model
  - Splitting DIDComm in packages like:
    
    - @afj/didcomm-base
    - @afj/didcomm-credentials
    - @afj/didcomm-proofs
    - @afj/didcomm-mediation
- DIDComm v2
  
  - Discover Features V2 over DIDComm V2: [https://github.com/hyperledger/aries-framework-javascript/pull/1576](https://github.com/hyperledger/aries-framework-javascript/pull/1576)
  - Basic Messages V2:  [https://github.com/hyperledger/aries-framework-javascript/pull/1546](https://github.com/hyperledger/aries-framework-javascript/pull/1546)
  - Credentials protocols V3: [https://github.com/hyperledger/aries-framework-javascript/pull/1560](https://github.com/hyperledger/aries-framework-javascript/pull/1560)
  - Missing:
    
    - DID Rotation
    - Mediation / Pickup

<!--THE END-->

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Extracting parts of AFJ into generic libraries
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
