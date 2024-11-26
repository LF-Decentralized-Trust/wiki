1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-02-17 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Feb 21, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) &lt;timo@animo.id&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Animo has won eSSIF Lab Grant to build Aries Mobile SDK - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://drive.google.com/file/d/1t9_XljI9rvFrgvNVM7ymxFae3Xo0Nhvx/view?usp=sharing)
  
  - AIP 2.0
  - BBS+, JSON-LD
  - Shared components (Aries Askar, Indy CredX, Indy VDR)

## Agenda

- Record the meeting
- Hyperledger moved to Discord
  
  - Replaces rocket.chat
  - [https://discord.gg/N84Eg4z3](https://discord.gg/N84Eg4z3)
- Hyperledger Fabric ([Harsh Multani](https://lf-hyperledger.atlassian.net/wiki/people/712020:dc87604d-17c8-4baa-aece-b04d80c37a2a?ref=confluence))
- License headers ([Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence))
  
  - Sign-off / PGP signature
- Shared Components libraries ([Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence))
  
  - Three packages
    
    - Shared library for typing and utils method
    - Separate Node and React Native package
  - Having three static libraries increases the bundle size quite a lot
    
    - Possible to create a single binary to decrease bundle size?
  - React Native packages are focused on React Native
  - TS → C++ → libindyvdr
    
    - Not using a Swift / Kotlin wrapper
- Wallet Storage and querying ([Mike Richardson](https://lf-hyperledger.atlassian.net/wiki/people/5ff5d919f7ea2a0107b56eac?ref=confluence))
- AyanWorks contributions 
  
  - sidetree protocol for non-indy ledgers
    
    - still looking into which did methods
  - DIDComm v2
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
- BBS+ work
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

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
