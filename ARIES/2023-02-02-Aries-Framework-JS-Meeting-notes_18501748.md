1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-02-02 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Feb 02, 2023

**Meeting recording**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (Petri Dish Development) &lt;amanji@petridish.dev&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Demoed the OCA updates in the wallet
  - PR in Bifold that conforms to this specification: [https://github.com/hyperledger/aries-rfcs/pull/755](https://github.com/hyperledger/aries-rfcs/pull/755)
- Aries Call [2023-01-18 Aries Working Group Call](2023-01-18-Aries-Working-Group-Call_18501202.html)
  
  - Not much updates. Short call
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
- AnonCreds Api, AnonCreds Records, etc..
  
  - [https://github.com/TimoGlastra/aries-framework-javascript/pull/18](https://github.com/TimoGlastra/aries-framework-javascript/pull/18)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/1193](https://github.com/hyperledger/aries-framework-javascript/issues/1193)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/1164](https://github.com/hyperledger/aries-framework-javascript/issues/1164)
- Storage of created did documents
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/1257](https://github.com/hyperledger/aries-framework-javascript/issues/1257)
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501748/18517498.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
