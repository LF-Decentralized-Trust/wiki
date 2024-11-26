1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-02-23 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Feb 23, 2023

**Meeting recording**

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Simon Henriksen](https://lf-hyperledger.atlassian.net/wiki/people/712020:23306fb2-e990-49b4-b9c6-9ef1a17f038b?ref=confluence) (Hyphen) &lt;simon@hyphenapp.xyz&gt;
- [Philip Essy-Ehsing](https://lf-hyperledger.atlassian.net/wiki/people/712020:493a701d-81ff-40c3-9ecd-d35e2f937163?ref=confluence) (Hyphen) &lt;philip@hyphenapp.xyz&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Went over a few PRs
  - Compatibility with upgrade from 0.2.x to 0.3.x in interoperability (mediator not supporting did:key for mediation messages)
  - Moved from NPM to Yarn - more consistent with AFJ.
    
    - But also some issues NPM when using bifold as module
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
  
  - did:legacypeer RFC - [https://github.com/hyperledger/aries-rfcs/pull/768](https://github.com/hyperledger/aries-rfcs/pull/768)
  - Consensus: do not implement did:legacypeer, but rather transform between the legacy dids and already existing did methods (did:peer:1, did:peer:2, did:keri lite)
  - Create a table to compare the different did methods
- Releases
  
  - AFJ 0.4.0-alpha releases (30)
- DIDComm v2
  
  - Great presentation by Nessus/Tom Diesler at the Aries DIDComm v2 WG showing DIDComm v1 comms with Aca-py and DIDComm v2 comms with another Nessus agent. Recording here [https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Aries+DIDCommV2+Working+Group+2023-02-20+meeting](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Aries+DIDCommV2+Working+Group+2023-02-20+meeting)
  - [https://github.com/hyperledger/aries-framework-javascript/pull/1141](https://github.com/hyperledger/aries-framework-javascript/pull/1141)
  - The PR above was started by SICPA but they currently don't have the resources to finish it, so we're looking for someone who would like to take over the effort.
  - We discussed:
    
    - [Aries DIDCommV2 Working Group 2023-02-06 meeting](Aries-DIDCommV2-Working-Group-2023-02-06-meeting_18501798.html)
      
      Picos and their usage in IoT.
    - Aries RFCs and DIDComm v2/AIP3.
    - sub-protocols for things like issue credential, etc.
  - Nice guide for the difference (improvements) between DIDComm v1 and v2 [https://didcomm.org/book/v2/whatsnew](https://didcomm.org/book/v2/whatsnew)
  - DIDComm being discussed at the Feb 13 OWF meeting [https://github.com/openwallet-foundation/architecture-task-force/blob/main/meeting-details.md](https://github.com/openwallet-foundation/architecture-task-force/blob/main/meeting-details.md)
- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- Shared Components
  
  - Indy VDR 0.1.0-dev.4
    
    - React Native &amp; Node.JS
  - Aries Askar 0.2.8-dev.1
    
    - React Native &amp; Node.JS
    - Some issues with broken build pipeline
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1211](https://github.com/hyperledger/aries-framework-javascript/pull/1211)
    - ACA-Pug Call talking about Askar profiles: [2023-01-24 Aries Cloud Agent - Python Users Group Community Meeting](2023-01-24-Aries-Cloud-Agent---Python-Users-Group-Community-Meeting_18501358.html)
  - AnonCreds 0.1.0-dev.4
    
    - Node.JS
    - React Native (only iOS)
  - Berend made a demo: [https://www.loom.com/share/8497e12cb1c64383aa01768ac2551078](https://www.loom.com/share/8497e12cb1c64383aa01768ac2551078)

## Agenda

- Record the meeting
- Cardano AnonCreds implementation in AFJ demo
- AnonCreds &amp; Shared Components
  
  - Update on Migration Script
    
    - Redoing the implementation the in Rust
  - Update on Shared Components
    
    - Askar, Indy VDR, AnonCreds Rust
    - Starting to test in React Native
      
      - several issues discovered with the integration
      - Pointer issues in C++
      - Couldn't run in Android emulators even if Android 12
        
        - Works in ARM, but not in x86
        - Issues with symbols/ndk version
      - Error messages different in React Native
      - Errors related to fetching keys
    - Issues in AFJs implementation
      
      - e.g. freeing objects
    - Tests running on test harness
      
      - AFJ-AFJ works well
      - AFJ-ACA-Py where AFJ is issuer/verifier also works well
      - ACA-Py-AFJ where AFJ is holder does not work well
  - Update on Aries Bifold integration
    
    - Updated to latest alpha, now starting to integrate the shared components
- AFJ 0.4.0 - What's changed, what's new?
- How to integrate other ledgers into AFJ
  
  - Did Resolver
  - Did Registrar
  - AnonCreds Method

<!--THE END-->

- Module bundles
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/1297](https://github.com/hyperledger/aries-framework-javascript/issues/1297)

## Meeting Notes

- ...

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
