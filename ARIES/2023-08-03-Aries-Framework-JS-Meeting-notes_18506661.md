1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-08-03 Aries Framework JS Meeting notes

Created by Ariel Gentile, last modified by Alexander Shenshin on Aug 03, 2023

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Zdravko Iliev](https://lf-hyperledger.atlassian.net/wiki/people/712020:63aec7b4-ed57-4567-add1-9c4f1eef670c?ref=confluence) - Vereign AG (zdravko.iliev@vereign.com)
- @Kalin Canov - Vereign AG (kalin.canov@[vereign.com](http://vereign.com))
  
- Alexey Lunin - Vereign AG ([alexey.lunin@vereign.com](mailto:alexey.lunin@vereign.com))
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) (DSR Corporation) &lt;alexander.shenshin@dsr-corporation.com&gt;
- [Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) (DSR Corporation) &lt;artem.ivanov@dsr-corporation.com&gt;

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
- Aries Call [2023-08-02 Aries Working Group Call](2023-08-02-Aries-Working-Group-Call_18506518.html)
  
  - Discussion on peer did migration
    
    - Use Discover Features to know if the other party supports did:peer:3

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- AnonCreds
  
  - Ursa replacement with anoncreds-clsignatures-rs [https://github.com/hyperledger/anoncreds-rs/pull/226](https://github.com/hyperledger/anoncreds-rs/pull/226)
    
    - A few changes in the API (tails file not required anymore for issuing/revoking credentials
    - Will be good to wait for a new release including this before merging [https://github.com/hyperledger/aries-framework-javascript/pull/1427](https://github.com/hyperledger/aries-framework-javascript/pull/1427)

## Agenda

- Record the meeting
- Unqualified DID migration and DID:peer:3 support
  
  - Aries RFC proposal: [https://github.com/hyperledger/aries-rfcs/pull/793](https://github.com/hyperledger/aries-rfcs/pull/793)
  - Some updates to be reviewed for transformation script [https://github.com/TimoGlastra/legacy-did-transformation/pull/4](https://github.com/TimoGlastra/legacy-did-transformation/pull/4)
  - A few notes for AFJ implementation:  [https://hackmd.io/sz0xbL9MTxeB3qDht3ClrQ](https://hackmd.io/sz0xbL9MTxeB3qDht3ClrQ)
  - See hackmd for notes from the WG Call
- JFF Plugfest 3: support for DIDComm V2/WACI-Pex? OIDC4VP?
  
  - Probably no DIDComm tests for Plugfest 3
  - Most parties using DIDComm v2 (makes sense to use that) → so we need DIDComm v2
    
    - Issue Credential v3, Present Proof v3
    - PEX attachment format for present proof
  - Implementation of OpenID4VP for AFJ: [https://github.com/animo/paradym-wallet/tree/main/packages/openid4vc-client/src/presentations](https://github.com/animo/paradym-wallet/tree/main/packages/openid4vc-client/src/presentations)
- DIDComm v2
  
  - Discussion: [https://github.com/hyperledger/aries-framework-javascript/discussions/1539](https://github.com/hyperledger/aries-framework-javascript/discussions/1539)
  - Should be able to create oob v1.1 message and receive didcomm v2 message (using `accept` [https://github.com/hyperledger/aries-rfcs/blob/main/features/0044-didcomm-file-and-mime-types/README.md#defined-profiles](https://github.com/hyperledger/aries-rfcs/blob/main/features/0044-didcomm-file-and-mime-types/README.md#defined-profiles))
  - OOB v2: [https://identity.foundation/didcomm-messaging/spec/v2.0/#out-of-band-messages](https://identity.foundation/didcomm-messaging/spec/v2.0/#out-of-band-messages)
- Look at open issues / PRs
- 0.5.0 release
  
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/1525](https://github.com/hyperledger/aries-framework-javascript/discussions/1525)
- Deprecating the Indy SDK
  
  - deprecate indy-sdk in 0.6.0?
  - 0.5 will be last version with indy-sdk support, or should we already deprecate/remove it in 0.5?
  - add deprecation warning to the framework already?
  - need to coordinate with stephen

## Meeting Notes

## Recording / Slides

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Extracting parts of AFJ into generic libraries
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20230720-130043\_Recording.transcript.vtt](attachments/18506661/18518540.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [GMT20230720-130043\_RecordingnewChat.txt](attachments/18506661/18518541.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
