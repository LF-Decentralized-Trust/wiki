1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-03-16 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Alexander Shenshin on Mar 16, 2023

**Meeting recording**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)  (Animo Solutions) &lt;timo@animo.id&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) (DSR Corporation) &lt;alexander.shenshin@dsr-corporation.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Short meeting
  - AFJ upgrade, removal of indy-sdk
  - Re-achitecture: [https://github.com/hyperledger/aries-mobile-agent-react-native/pull/641](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/641)
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
  
  - did peer and issues with legacy peer did
  - new did:peer:3 to move from legacy peer did
  - big updates presented on OCA and how bundles will be managed/retrieved
    
    - multiple options for resolving/storing (data on ledger, link to where stored on ledger with hash, big repo / well-known)
- Releases
  
  - AFJ 0.4.0-alpha releases (74)
- DIDComm v2
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
- Open Source Summit in Vancouver
  
  - [https://ossna2023.sched.com/event/1K58t?iframe=no](https://ossna2023.sched.com/event/1K58t?iframe=no)

## Agenda

- Record the meeting
- timezones / meeting time
  
  - ideal solution: hyperledger moves to UTC
  - for now: move to earlier/later
  - [https://www.worldtimebuddy.com/?qm=1&amp;lid=2759794,8,30&amp;h=2759794&amp;date=2023-3-16&amp;sln=15-17&amp;hf=0](https://www.worldtimebuddy.com/?qm=1&lid=2759794%2C8%2C30&h=2759794&date=2023-3-16&sln=15-17&hf=0)
- Update on AFJ 0.4.0
  
  - Bifold e2e flow working now
  - requirement for android API 30+ (Android 11+) is only for indy-vdr
    
    - Bifold currently supports Android SDK 21+ (Android 5+)
    - could use indy-vdr-proxy as an alternative ([Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) will give demo next week)
      
      - need to trust proxy
    - As of January 6th, 2023, Android Studio recommends targeting Android 7 (API 24) for 94.4% device coverage. Android 5 (API 21) gives 99.3% coverage
    - [https://hackmd.io/@blueberi/Bk50yEyJh](https://hackmd.io/@blueberi/Bk50yEyJh)
  - AFJ 0.4.0
    
    - Bug fixing, last releases, finishing touches
    - migration scripts (mostly done)
- Update on cheqd integration
  
  - Ask Daev to give a demo
- DIF presentation exchange format
  
  - [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) will update with latest changes, look at what's missing
  - [Mike Richardson](https://lf-hyperledger.atlassian.net/wiki/people/5ff5d919f7ea2a0107b56eac?ref=confluence) demo of the presentation exchange flow (in 1/2 weeks)
- prioritisation for 0.5.0
  
  - DIDComm v2
    
    - now that indy-sdk is gone, other libraries have DIDComm v2 support, main objective of AIP 3
    - Askar as backend for DIDComm v2? SICPA has implemented using didcomm v2 wasm library
    - support both libraries
  - Need to work on a new wallet api
    
    - focused on indy-sdk
    - still uses parameters for indy-sdk
    - way we are creating / opening the wallet is inherited from indy-sdk
  - Improving interfaces for message repository
    
    - fully support pickup v2 and v3 protocols
    - be a mediator without in memory message repository
  - Refactor basic message / trust ping to align with new way of doing things (support multiple versions of the protocol)
  - End user wallet perspective
    
    - key rotation
    - changing mediator
    - initialization, efficient way to check if the wallet key is valid

## Meeting Notes

- ...

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503227/18517783.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
