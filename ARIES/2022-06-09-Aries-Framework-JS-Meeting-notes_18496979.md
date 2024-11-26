1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-06-09 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Jun 10, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Hyperledger moved to Discord
  
  - Replaces rocket.chat
  - [https://discord.gg/hyperledger](https://discord.gg/hyperledger)
- Releases
  
  - Next release - 0.2.0
    
    - Issue Credential v2 indy
    - Present Proof v2 indy
    - Out of Band / DID Exchange - no public dids yet
    - Pickup v2
    - Holder/Verifier revocation and revocation notification
  - 0.3.0
    
    - Issue Credential v2 JSON-LD
    - Present Proof v2 JSON-LD
    - Shared Components?
    - Splitting up the framework

## Agenda

- Record the meeting
- Status updates
- Source of truth in records
  
  - process first message in exchange
  - process nth message in exchange
  - send message
  - separate proposal attribute?
  - method to get the latest attributes? record always stores our truth
- AFJ versions
  
  - with relation to AFJ-Ext
  - create afj-0.2.0. branch in AFJ-Ext ([Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence))
  - Release AFJ 0.2.0 without present proof v2 work.
- Interop between AIP 1.0 and AIP 2.0
  
  - AFJ will keep supporting AIP 1.0
  - Test with older version of AFJ
- Generic Credentials Module
  
  - raise issue in Aries WG for problem report when no formats are supported ([James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) )
  - [https://github.com/hyperledger/aries-framework-javascript/pull/841](https://github.com/hyperledger/aries-framework-javascript/pull/841)
- Multi tenancy updates
  
  - Updated design document: [https://hackmd.io/vGLVlxLvQR6jsEEjzNcL8g?view](https://hackmd.io/vGLVlxLvQR6jsEEjzNcL8g?view)
- AMA

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
- Monorepo dependencies
  
  - TypeScript types

**Meeting recording:**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
