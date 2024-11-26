1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-01-26 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Jan 26, 2023

**Meeting recording**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) (Instnt, Inc) &lt;alberto@instnt.org&gt;

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
  
  - Discussion on AIP 3
    
    - What if someone supports a smaller part of the protocol
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
  - Mostly talking about AIP 3 – how to support the effort
- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- Shared Components
  
  - Indy VDR 0.1.0-dev.2
    
    - React Native &amp; Node.JS
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1160](https://github.com/hyperledger/aries-framework-javascript/pull/1160)
  - Aries Askar 0.2.8-dev.1
    
    - React Native &amp; Node.JS
    - Some issues with broken build pipeline
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1211](https://github.com/hyperledger/aries-framework-javascript/pull/1211)
    - ACA-Pug Call talking about Askar profiles: [2023-01-24 Aries Cloud Agent - Python Users Group Community Meeting](2023-01-24-Aries-Cloud-Agent---Python-Users-Group-Community-Meeting_18501358.html)
  - AnonCreds 0.1.0-dev.1
    
    - Node.JS
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1232](https://github.com/hyperledger/aries-framework-javascript/pull/1232)

## Agenda

- Record the meeting
- OpenID4VCI Demo ([Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence))
- Legacy did sov prefix
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/1245](https://github.com/hyperledger/aries-framework-javascript/pull/1245)
- Open Issues / Pull Requests

## Meeting Notes

- ...

## Future topics

Next Week:

- .devcontainers demo ([Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence))
- AFJ as a mediator. Thoughts and conversation on High Availability (HA) support. Anyone who runs a mediator in prod will probably want HA (3 pods, 3 servers, etc) ([Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) / [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence))

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501534/18517442.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
