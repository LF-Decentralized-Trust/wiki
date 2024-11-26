1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-02-24 Aries Framework JS Meeting notes

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
- Hyperledger Fabric ([Harsh Multani](https://lf-hyperledger.atlassian.net/wiki/people/712020:dc87604d-17c8-4baa-aece-b04d80c37a2a?ref=confluence))
- BBS+ work
- Non-indy based ledgers ([Sai Ranjit Tummalapalli](https://lf-hyperledger.atlassian.net/wiki/people/5f620f169109170076f8dc96?ref=confluence) )
- Ongoing work
- - Issue Credential V2
  - Present Proof v2
    
    - Where to locate e2e tests?
      
      - option: locate in module / protocol directory. Indicate test is e2e test using .e2e.test.ts
      - locating tests in the protocol directory makes it easy to run tests for a specific protocol version
  - Revocation
    
    - Revocation has been merged into main, tests for holder are passing in AATH with ACA-Py
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

Text File [chat.txt](attachments/18495570/18515970.txt "Download")

Feb 24, 2022 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
