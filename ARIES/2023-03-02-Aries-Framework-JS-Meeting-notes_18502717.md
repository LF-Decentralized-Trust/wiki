1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-03-02 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Mar 16, 2023

**Meeting recording**

[dummyfile.txt](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Short call to discuss some updates to the wallet
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
  
  - legacy did peer, finding a good peer did
  - swift wrapper around the shared components, auto generating wrappers in Rust (UniFFI)
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

<!--THE END-->

- Presentation on AFJ 0.4.0
