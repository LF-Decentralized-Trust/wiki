1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-08-17 Aries Framework JS Meeting notes

Created by Ariel Gentile, last modified by Alexander Shenshin on Aug 31, 2023

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
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
  
  - Meetings suspended until September
- Aries Call [2023-08-16 Aries Working Group Call](2023-08-16-Aries-Working-Group-Call_18506887.html)
  
  - Discussion on peer did migration
    
    - Stephen gave a presentation about ACA-Py migration
    - Do we need to support unqualified DIDs for DIDExchange? Or just keep did:peer:1 and did:peer:2?
      
      - It seems to us better to keep DIDExchange without unqualified DID support (it would be an step backward for us), as ACA-Py will support receiving did:peer:2 from step 1 of the transition)

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- AnonCreds
  
  - Ursa replacement with anoncreds-clsignatures-rs [https://github.com/hyperledger/anoncreds-rs/pull/226](https://github.com/hyperledger/anoncreds-rs/pull/226)
    
    - A few changes in the API (tails file not required anymore for issuing/revoking credentials

## Agenda

- Record the meeting
- AFJ in Browser
  
  - "Aries with AnonCreds in the browser"
    
    - [https://github.com/kfsoftware/meetup-k8s-aries-july-2023](https://github.com/kfsoftware/meetup-k8s-aries-july-2023)
  - Serious performance issues with Anoncreds in WASM. For holder is fine, but issuing, creating objects, etc is very bad
- DIDComm v2
  
  - Discussion: [https://github.com/hyperledger/aries-framework-javascript/discussions/1539](https://github.com/hyperledger/aries-framework-javascript/discussions/1539)
  - Basic Message V2 protocol: [https://github.com/hyperledger/aries-framework-javascript/pull/1546](https://github.com/hyperledger/aries-framework-javascript/pull/1546/files)
  - It is possible to merge without breaking changes?
  - How to make protocols support both DIDComm V1 and V2 (e.g. Discover Features V2, Basic Messages V2)
- Look at open issues / PRs
- 0.5.0 release
  
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/1525](https://github.com/hyperledger/aries-framework-javascript/discussions/1525)
    
    - Create a 0.4.1 first. To not introduce Breaking Changes, merge first:
      
      - [https://github.com/hyperledger/aries-framework-javascript/pull/1427](https://github.com/hyperledger/aries-framework-javascript/pull/1427)
      - [https://github.com/hyperledger/aries-framework-javascript/pull/1542](https://github.com/hyperledger/aries-framework-javascript/pull/1542) (need a change to not break public field)
    - Drop node 16 support
    - Merge DIDComm V2 stuff

## Meeting Notes

## Recording / Slides

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Extracting parts of AFJ into generic libraries
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20230720-130043\_RecordingnewChat.txt](attachments/18506951/18518603.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [GMT20230720-130043\_Recording.transcript.vtt](attachments/18506951/18518604.vtt) (application/octet-stream)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
