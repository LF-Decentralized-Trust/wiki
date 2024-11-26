1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-05-05 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on May 06, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Sai Ranjit Tummalapalli](https://lf-hyperledger.atlassian.net/wiki/people/5f620f169109170076f8dc96?ref=confluence)(AyanWorks) &lt;sairanjit.tummalapalli@ayanworks.com&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Hyperledger moved to Discord
  
  - Replaces rocket.chat
  - [https://discord.gg/hyperledger](https://discord.gg/hyperledger)

## Agenda

- Record the meeting
- Merging Issue Credential v2
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/649](https://github.com/hyperledger/aries-framework-javascript/pull/649)
- Dropping support for Node 12
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/734](https://github.com/hyperledger/aries-framework-javascript/issues/734)
- Security and handling of data in AFJ – [Lance Byrd opened an issue](https://github.com/hyperledger/aries-framework-javascript/issues/740)
  
  - [https://github.com/hyperledger/aries-mobile-agent-react-native/blob/main/docs/design/OS-specific-security-settings.md](https://github.com/hyperledger/aries-mobile-agent-react-native/blob/main/docs/design/OS-specific-security-settings.md)
  - [https://hyperledger-indy.readthedocs.io/projects/sdk/en/latest/docs/design/003-wallet-storage/README.html](https://hyperledger-indy.readthedocs.io/projects/sdk/en/latest/docs/design/003-wallet-storage/README.html)
  - [https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0051-dkms/dkms-v4.md](https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0051-dkms/dkms-v4.md)
- Make it possible to use AFJ with a subset of credential formats
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/730](https://github.com/hyperledger/aries-framework-javascript/issues/730)
- Most needed features for using AFJ on the server
  
  - Message queuing (persistent queue, outbound and inbound) – Ariel will create an issue
  - Hosting multiple AFJ instances next to each other that are connected to the same database
  - Multi tenancy support to AFJ
- Division of projects
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
