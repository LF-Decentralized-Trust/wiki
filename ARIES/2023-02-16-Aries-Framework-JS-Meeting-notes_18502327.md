1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-02-16 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Feb 16, 2023

**Meeting recording**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
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
- Releases
  
  - AFJ 0.4.0-alpha releases (30)
- DIDComm v2
  
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
- OWF
  
  - OWF is interested in 'wallet engine components' so viewing AFJ as a wallet engine will be a good frame.
  - we'll talk about common components before, so askar will be explained already. probably an architecture diagram?
  - the 'features' list will be similar to the other projects, but noting things like Bluetooth and OpenID4vc progress will be interesting.
  - OpenWallet Foundation presentation from Aries community - **February 20th 8PM CET**
    
    - What do we have in the Aries community, and what are we working on
    - Not interested in UI pieces
    - OWF Aries Presentation: [https://hackmd.io/suQXbYWNRp2eow2XJ9xqAA](https://hackmd.io/suQXbYWNRp2eow2XJ9xqAA)
  - Topics / Ideas
    
    - Future plans regarding OpenID (e.g. verification side)
    - Multi-credential format support
    - Non-Indy specific / Ledger Agnostic (core + specific components)
    - Multi-platform (Node.JS / React Native)
- Shared Components React Native / Bifold integration
  
  - Remove support for Indy SDK?
    
    - Need migration script from Indy SDK to Aries Askar
    - Need clear communication, no versioning for Bifold at the moment
    - Need good documentation on how to migrate
    - Keep it simple, just do it
    - Keeping separate branches is complex, the faster we get it done the better
    - Create a tag for the commit that includes the migration
    - I'd surface the issue and allow anybody in the community to raise their voice if they want to keep IndySDK. (We'll ask the community in the Bifold Discord)
  - Lowest Android  version?
    
    - Indicio: As of mid 2022 support Android 9+ (80% of devices), since recent on a project Android 10+
    - Android NDK=r25b and SDK=28 are being used.
    - Need to build custom cross images
    - [https://github.com/cross-rs/cross/issues/1195](https://github.com/cross-rs/cross/issues/1195)
    - [https://github.com/cross-rs/cross/issues/1155](https://github.com/cross-rs/cross/issues/1155)
    - iOS 12/13 (80% already) lowest version (current 16)
      
      - [https://iosref.com/ios-usage](https://iosref.com/ios-usage)
  - Migration Script support version?
    
    - Prompt the user to open the wallet and upgrade
    - Complexity: have to upgrade from any version to any version
    - Optional module
    - The app vendor can decide how long to keep the migration script in. People can update the migration script as long as there's a need for it.
    - As per iOS — “Use the BackgroundTasks framework to keep your app content up to date and run tasks requiring minutes to complete while your app is in the background. Longer tasks can optionally require a powered device and network connectivity.”
    - [https://developer.apple.com/documentation/backgroundtasks](https://developer.apple.com/documentation/backgroundtasks)
- Module bundles
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/1297](https://github.com/hyperledger/aries-framework-javascript/issues/1297)
- AFJ as a mediator. Thoughts and conversation on High Availability (HA) support. Anyone who runs a mediator in prod will probably want HA (3 pods, 3 servers, etc) ([Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) / [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence))
- Open Issues / Pull Requests

## Meeting Notes

- ...

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18502327/18517601.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
