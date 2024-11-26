1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-01-19 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Ariel Gentile on Jan 19, 2023

**Meeting recording**

[dummyfile.txt](#)

[dummyfile.txt](#)

[dummyfile.txt](#)

[dummyfile.txt](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Simon Henriksen](https://lf-hyperledger.atlassian.net/wiki/people/712020:23306fb2-e990-49b4-b9c6-9ef1a17f038b?ref=confluence) (Hyphen) &lt;simon@hyphenapp.xyz&gt;
- [Philip Essy-Ehsing](https://lf-hyperledger.atlassian.net/wiki/people/712020:493a701d-81ff-40c3-9ecd-d35e2f937163?ref=confluence) (Hyphen) &lt;philip@hyphenapp.xyz&gt;
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) (2060.io) &lt;gentilester@gmail.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - [Bifold Summit 2023](Bifold-Summit-2023_18500878.html)
- Aries Call [2023-01-18 Aries Working Group Call](2023-01-18-Aries-Working-Group-Call_18501202.html)
  
  - Still OCA discussion, lot of excitement about this
  - Bifold supports OCA - BC Showcase
  - Currently hardcoded in the wallet
- Releases
  
  - AFJ 0.3.3 Released
    
    - Release: [https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.3.3](https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.3.3)
    - Changelog: [https://github.com/hyperledger/aries-framework-javascript/blob/main/CHANGELOG.md#033-2023-01-18](https://github.com/hyperledger/aries-framework-javascript/blob/main/CHANGELOG.md#033-2023-01-18)
  - React Hooks 0.4.0 Released
    
    - Works with AFJ 0.3.2+
    - Changelog: [https://github.com/hyperledger/aries-framework-javascript-ext/blob/main/packages/react-hooks/CHANGELOG.md#040-2023-01-19](https://github.com/hyperledger/aries-framework-javascript-ext/blob/main/packages/react-hooks/CHANGELOG.md#040-2023-01-19)
- DIDComm v2
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/1141](https://github.com/hyperledger/aries-framework-javascript/pull/1141)
  - The PR above was started by SICPA but they currently don't have the resources to finish it, so we're looking for someone who would like to take over the effort.
  - In the meantime, Timo will create a new branch where we keep the work that has been done in the PR and that we can keep up to date with the main to some extent.
  - AFJ Feature branch: [https://github.com/hyperledger/aries-framework-javascript/tree/feat/didcomm-v2](https://github.com/hyperledger/aries-framework-javascript/tree/feat/didcomm-v2)
- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)

## Agenda

- Record the meeting
- Ledger Agnostic AnonCreds Update
  
  - [https://github.com/hyperledger/anoncreds-spec](https://github.com/hyperledger/anoncreds-spec)
  - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - [https://github.com/orgs/hyperledger/projects/16](https://github.com/orgs/hyperledger/projects/16)
  - Cardano anoncreds method work by RootsID [https://github.com/roots-id/cardano-anoncreds](https://github.com/roots-id/cardano-anoncreds)
    
    - And if you are interested we meet Bi-weekly to discuss AnonCreds on Cardano as part of the Cardano SSI Alliance: [https://github.com/roots-id/cardano-anoncreds/blob/main/meeting-notes.md](https://github.com/roots-id/cardano-anoncreds/blob/main/meeting-notes.md)
  - Stephen Curran gave presentation about Ledger AnonCreds at DIF Interop WG: &lt;todo: add link&gt; 
    
    - great podcast from Northern Block about AnonCreds with Stephen Curran [https://northernblock.io/anoncreds-anonymous-credentials-with-stephen-curran/](https://northernblock.io/anoncreds-anonymous-credentials-with-stephen-curran/)
- OpenID4VCI Update
  
  - Targeting interop with [https://launchpad.mattrlabs.com/](https://launchpad.mattrlabs.com/)
  - [https://openid.net/specs/openid-4-verifiable-credential-issuance-1\_0.html](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html)
  - [https://daniel-hardman.medium.com/sentries-confessionals-vaults-and-envelopes-4a58cf4f8a5a](https://daniel-hardman.medium.com/sentries-confessionals-vaults-and-envelopes-4a58cf4f8a5a)
  - > All of [#IIW](https://twitter.com/hashtag/IIW?src=hash&ref_src=twsrc%5Etfw) is starting to heat up for the end of day [#deathmatch](https://twitter.com/hashtag/deathmatch?src=hash&ref_src=twsrc%5Etfw) between [#OIDC4VC](https://twitter.com/hashtag/OIDC4VC?src=hash&ref_src=twsrc%5Etfw) and [#DIDComm](https://twitter.com/hashtag/DIDComm?src=hash&ref_src=twsrc%5Etfw). Blows are already being struck in the first session about where [#OIDC4VC](https://twitter.com/hashtag/OIDC4VC?src=hash&ref_src=twsrc%5Etfw) fits in the [#ToIP](https://twitter.com/hashtag/ToIP?src=hash&ref_src=twsrc%5Etfw) [#stack](https://twitter.com/hashtag/stack?src=hash&ref_src=twsrc%5Etfw). [pic.twitter.com/ql7YupwoZ7](https://t.co/ql7YupwoZ7)
    > 
    > — Drummond Reed (@drummondreed) [November 16, 2022](https://twitter.com/drummondreed/status/1592947135385055234?ref_src=twsrc%5Etfw)
  - > Final session of [#IIW](https://twitter.com/hashtag/IIW?src=hash&ref_src=twsrc%5Etfw) Day 2: the [#deathmatch](https://twitter.com/hashtag/deathmatch?src=hash&ref_src=twsrc%5Etfw) between the [#DIDComm](https://twitter.com/hashtag/DIDComm?src=hash&ref_src=twsrc%5Etfw) V2 and [#OIDC4VC](https://twitter.com/hashtag/OIDC4VC?src=hash&ref_src=twsrc%5Etfw) [#protocols](https://twitter.com/hashtag/protocols?src=hash&ref_src=twsrc%5Etfw) begins with [@TelegramSam](https://twitter.com/TelegramSam?ref_src=twsrc%5Etfw) and [@tlodderstedt](https://twitter.com/tlodderstedt?ref_src=twsrc%5Etfw) squaring off before a record-breaking IIW crowd. Everyone is desperate to find out: will there be a knockout??? ;-) [pic.twitter.com/cghx9H40v0](https://t.co/cghx9H40v0)
    > 
    > — Drummond Reed (@drummondreed) [November 16, 2022](https://twitter.com/drummondreed/status/1593027015707619328?ref_src=twsrc%5Etfw)
- Shared Components Update
  
  - Opportunity: [https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/b454a434-69fd-42fa-a90d-3ce614d5523b](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/b454a434-69fd-42fa-a90d-3ce614d5523b)
  - Indy VDR: [https://github.com/hyperledger/aries-framework-javascript/pull/1160](https://github.com/hyperledger/aries-framework-javascript/pull/1160)
  - Aries Askar: [https://github.com/hyperledger/aries-framework-javascript/pull/1211](https://github.com/hyperledger/aries-framework-javascript/pull/1211)
    
    - Most functionality there, will skip import/export for now
    - perfomance issues – supposed to be faster than indy
      
      - problem with garbage collection (spends ~80% of time on this)
      - solution found, only working in node 18 (not 14 &amp; 16)
        
        - [https://github.com/nodejs/release#release-schedule](https://github.com/nodejs/release#release-schedule)
      - Might also be an issue with indy-vdr &amp; anoncreds
  - AnonCreds Rs
  - Extracting Indy SDK, migration script to update indy wallet to Askar
- Multi-tenancy for Aries Framework JavaScript
  
  - Video tutorial:

## Meeting Notes

- ...

## Future topics

Next Week:

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501284/18517389.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501284/18517388.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501284/18517387.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501284/18517386.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
