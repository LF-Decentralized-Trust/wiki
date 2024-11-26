1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-03-03 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Philippe Foucault on Mar 31, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) &lt;timo@animo.id&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Hyperledger moved to Discord
  
  - Replaces rocket.chat
  - [https://discord.gg/N84Eg4z3](https://discord.gg/N84Eg4z3)

## Agenda

- Record the meeting
- Non-Indy ledger support finding the correct approach ([Sai Ranjit Tummalapalli](https://lf-hyperledger.atlassian.net/wiki/people/5f620f169109170076f8dc96?ref=confluence))
- OOB/DID-exchange
- 0.2.0 release of AFJ
  
  - Target release date march 15th. Can we make it? What are the bottlenecks?
  - Target date to have everything merged by March 15th
  - [https://github.com/hyperledger/aries-framework-javascript/discussions/622](https://github.com/hyperledger/aries-framework-javascript/discussions/622)
  - Done:
    
    - [Add support for receiving and proving revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/349)
    - [Add support for verifying revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/350)
  - In Review:
    
    - [Add support for 0453: Issue Credential v2](https://github.com/hyperledger/aries-framework-javascript/issues/352)
    - [Add support for RFC 0183 Revocation Notification Protocol](https://github.com/hyperledger/aries-framework-javascript/issues/493)
      
      - Support only v2?
      - ACA-Py has not implemented v1 according to the RFC
      - The AFJ PR conforms to the ACA-Py implementation, not the RFC
  - In Progress:
    
    - [Add support for RFC 0023: DID Exchange](https://github.com/hyperledger/aries-framework-javascript/issues/345)
    - [Add support for RFC 0434: Out-of-Band](https://github.com/hyperledger/aries-framework-javascript/issues/344)
      
      - Current changes are mainly about refactoring
      - Update the old connection invitation to the new OOB invitation
    - [Add support for 0454: Present Proof v2](https://github.com/hyperledger/aries-framework-javascript/issues/353)
      
      - Implementation is complete
      - v1 tests are complete
      - Working on v2 tests
    - [Adopt RFC 0592: Indy Attachment Format](https://github.com/hyperledger/aries-framework-javascript/issues/494)
      
      - Issuer side done as part of Issue Credential v2 PR
      - Verifier side will be done as part of Present Proof v2 PR
    - [Need strategy for handling breaking changes in storage records](https://github.com/hyperledger/aries-framework-javascript/issues/305)
      
      - Logic in place to import/export wallets for NodeJS, React Native WIP
      - Logic in place to apply the needed upgrades
      - Will need some time to add migration scripts for the breaking changes introduced after the respective PRs are merged
      - Let [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)which fields have changed.
- [Unable to accept credential offer as of 0.2.0-alpha.20](https://github.com/hyperledger/aries-framework-javascript/issues/647)
- Storing revocation status in CredentialRecord
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/579](https://github.com/hyperledger/aries-framework-javascript/pull/579)
- Fabric Support ([Harsh Multani](https://lf-hyperledger.atlassian.net/wiki/people/712020:dc87604d-17c8-4baa-aece-b04d80c37a2a?ref=confluence))
- Ongoing work
- - Issue Credential V2
  - Present Proof v2
  - Revocation
  - OOB / DIDExchange (routing keys, roles and states, get rid of did doc and verkey)
  - Shared Components
- Open PRs
- AMA

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
- Monorepo dependencies
  
  - TypeScript types

**Meeting recording:**

**![](plugins/servlet/confluence/placeholder/unknown-attachment)**

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18495584/18515992.txt "Download")

Mar 03, 2022 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
