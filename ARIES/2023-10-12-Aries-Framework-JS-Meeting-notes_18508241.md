1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-10-12 Aries Framework JS Meeting notes

Created by Karim Stekelenburg on Oct 12, 2023

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) - Animo Solutions (karim@animo.id)
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) (DSR Corporation) &lt;artem.ivanov@[dsr-corporation.com](http://dsr-corporation.com)&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call [2023-09-27 Aries Working Group Call](2023-09-27-Aries-Working-Group-Call_18507826.html)
  
  - Unqualified DIDs
  - Credential Protocols
  - AFJ OWF Proposal

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)

## Agenda

- Record the meeting
- Moving to OWF
  
  - Interest on moving Bifold as well and Askar. ACA-Py not yet but probably in a future
  - Repositories to move:
    
    - Aries JS Docs
    - Aries Framework JS
    - Aries Framework JS Extensions
  - Pre-IIW F2F OWF event: [https://www.eventbrite.com/e/openwallet-pre-iiw-developers-face-to-face-tickets-722252636077](https://www.eventbrite.com/e/openwallet-pre-iiw-developers-face-to-face-tickets-722252636077)
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
- 0.4.2 release
  
  - Add fix for [https://github.com/hyperledger/aries-framework-javascript/issues/1587](https://github.com/hyperledger/aries-framework-javascript/issues/1587)
  - Fix in implicit invitations: [https://github.com/hyperledger/aries-framework-javascript/pull/1592](https://github.com/hyperledger/aries-framework-javascript/pull/1592)
- 0.5.0 release
  
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/1525](https://github.com/hyperledger/aries-framework-javascript/discussions/1525)
    
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1427](https://github.com/hyperledger/aries-framework-javascript/pull/1427)
    - Drop node 16 support
  - Releasing new wrapper versions (for dropping support for Node 16)
    
    - Problem releasing Indy VDR wrapper. Hopefully fixed by: [https://github.com/hyperledger/indy-vdr/pull/222](https://github.com/hyperledger/indy-vdr/pull/222)
  - DIDComm V2 moved to 0.6.x
  - Message repository updates?
    
    - Does not support filtering by key/id

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

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Extracting parts of AFJ into generic libraries
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
