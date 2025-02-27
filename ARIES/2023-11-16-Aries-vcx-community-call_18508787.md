1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-11-16 Aries-vcx community call

Created by Patrik Stas, last modified on Nov 30, 2023

![](attachments/18508787/18518881.png?height=250)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Announcements:**

- **Schedule change: starting from today - November 16th 2023, aries-vcx community calls are happening bi-weekly (next meeting on November 30th)**

### **Agenda:**

- **Start meeting discussion**
  
  - Agenda overview and ad-hoc additions ( you can add your discussion your point )
  - Community updates
    
    - DIF DIDComm Users Group Meets 2,3, and 4th Mondays: [https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.m](https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md)
  - Heads up: 
    
    - yesterdays November 15th 2023 aries-wg call was interesting! Talk about the future of Aries RFCs, what belongs them and what not going forward.
  - Mentorship updates
    
    - uniffi aries-vcx wrapper project [Project Plan - Aries VCX Next-gen Mobile Wrapper (UniFFI)](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21960060)
    - [https://github.com/hyperledger/aries-vcx/tree/main/uniffi\_aries\_vcx](https://github.com/hyperledger/aries-vcx/tree/main/uniffi_aries_vcx)
    - Mentee presentation expect on 29th November on Aries-WG call
- **Overview of recent work done**
  
  - Mediator agent refactoring: variety of PRs ([https://github.com/hyperledger/aries-vcx/pull/1061](https://github.com/hyperledger/aries-vcx/pull/1061), [https://github.com/hyperledger/aries-vcx/pull/1056](https://github.com/hyperledger/aries-vcx/pull/1056), [https://github.com/hyperledger/aries-vcx/pull/1041](https://github.com/hyperledger/aries-vcx/pull/1041))
  - Testing: allow running aries\_vcx integration tests in parallel [https://github.com/hyperledger/aries-vcx/pull/1057](https://github.com/hyperledger/aries-vcx/pull/1057)
  - Fix: graceful base64 padding/no-padding decoding [https://github.com/hyperledger/aries-vcx/pull/1055](https://github.com/hyperledger/aries-vcx/pull/1055)
  - Feature: mediation coordination messages data model [https://github.com/hyperledger/aries-vcx/pulls?q=is%3Apr+is%3Aclosed](https://github.com/hyperledger/aries-vcx/pulls?q=is%3Apr%20is%3Aclosed)
  - Onboarding: add readme/examples for did\_parser [https://github.com/hyperledger/aries-vcx/pull/1051](https://github.com/hyperledger/aries-vcx/pull/1051)
  - Cleanup: deleted unused/obscure methods for OOB: [https://github.com/hyperledger/aries-vcx/pull/1039](https://github.com/hyperledger/aries-vcx/pull/1039)
- **In review**
  
  - did-exchange revival [https://github.com/hyperledger/aries-vcx/pull/1046](https://github.com/hyperledger/aries-vcx/pull/1046) of the original PR [https://github.com/hyperledger/aries-vcx/pull/928](https://github.com/hyperledger/aries-vcx/pull/928)
  - repo structure reorg [https://github.com/hyperledger/aries-vcx/pull/1059](https://github.com/hyperledger/aries-vcx/pull/1059)
    
    - this is important to reflect what aries-vcx repo represents - and this possible hints eventual renaming the repository itself (not of the particular \`aries\_vcx\` crate)
  - issue/presentation V2 protocols implementaiton
    
    - [https://github.com/hyperledger/aries-vcx/pull/987](https://github.com/hyperledger/aries-vcx/pull/987)
- **In progress**
  
  - aries-askar wallet implementation
- **Planned**
  
  - separate CIs for non-aries crates in the repo? did\_parser, did\_document, did\_resolver etc.
    
    - could be versioned separately as well
  - changes to did\_document - removal of generics
    
    - also impacts to did\_sov crate and
    - subsequently implementation of did:peer:4 [https://identity.foundation/peer-did-method-spec/](https://identity.foundation/peer-did-method-spec/)
  - didcomm v2 POC

<!--THE END-->

- **End meeting discussion**
  
  - potential brainstorming: ?? new repository name ??

## Attachments:

![](images/icons/bullet_blue.gif) [image-2023-11-8\_0-22-30.png](attachments/18508787/18518881.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
