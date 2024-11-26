1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-10-05 Aries-vcx community call

Created by Patrik Stas, last modified on Oct 05, 2023

![](attachments/18508132/18518804.jpg?height=250)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Agenda:**

- **Start meeting discussion**
  
  - Agenda overview and ad-hoc additions ( you can add your discussion your point )
  - Community updates
    
    - DIF DIDComm Users Group Meets 2,3, and 4th Mondays: [https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md](https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md)
    - Loosening dependency versions in Aries components
      
      - [https://github.com/hyperledger/anoncreds-rs/issues/240](https://github.com/hyperledger/anoncreds-rs/issues/240)
    - V2 issue-credential protocol discussion  started
      
      - [https://github.com/hyperledger/aries-rfcs/issues/796](https://github.com/hyperledger/aries-rfcs/issues/796)
  - Mentorship updates
    
    - mediators deployments:
      
      - vcx agency: deployed at [https://agency.indyscan.io](https://agency.indyscan.io)
      - mediator: need docker container
      - relay: need docker container
    - mediator project project plan [aries-vcx based message mediator](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/aries-vcx+based+message+mediator) 
      
      - [https://github.com/nain-F49FF806/axum-test-server](https://github.com/nain-F49FF806/axum-test-server/pull/16)
    - uniffi aries-vcx wrapper project [Project Plan - Aries VCX Next-gen Mobile Wrapper (UniFFI)](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21960060)
      
      - [https://github.com/hyperledger/aries-vcx/tree/main/uniffi\_aries\_vcx](https://github.com/hyperledger/aries-vcx/tree/main/uniffi_aries_vcx)
- **Overview of recent work done**
  
  - Release 0.59.0 [https://github.com/hyperledger/aries-vcx/releases/tag/0.59.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.59.0)
  - Release 0.59.1 [https://github.com/hyperledger/aries-vcx/releases/tag/0.59.1](https://github.com/hyperledger/aries-vcx/releases/tag/0.59.1)
    
    - Sunsetting vdrtools based anoncreds implementation in favor of credx, yay!!!
  - Naian: refactoring
    
    - [https://github.com/hyperledger/aries-vcx/pull/992](https://github.com/hyperledger/aries-vcx/pull/992) - unpack\_message return type
    - [https://github.com/hyperledger/aries-vcx/pull/1002](https://github.com/hyperledger/aries-vcx/pull/1002) - refactoring, remove function from aries-vcx
    - [https://github.com/hyperledger/aries-vcx/pull/1007](https://github.com/hyperledger/aries-vcx/pull/1007) - tweak EncryptionEnvelope API
  - Bogdan: Refactoring &amp; cleanups
    
    - [https://github.com/hyperledger/aries-vcx/pull/1003](https://github.com/hyperledger/aries-vcx/pull/1003) -  Use generics in favor of trait objects
    - [https://github.com/hyperledger/aries-vcx/pull/1005](https://github.com/hyperledger/aries-vcx/pull/1005) - Removal of old-style mocking, removal of settings.rs global state
  - Patrik: Connection protocol: removed+added APIs
    
    - [https://github.com/hyperledger/aries-vcx/pull/982](https://github.com/hyperledger/aries-vcx/pull/982)
- **Parked**
  
  - Demo aries-vcx [https://github.com/hyperledger/aries-vcx/pull/952](https://github.com/hyperledger/aries-vcx/pull/952)
  - Repo re-org 
    
    - [https://github.com/hyperledger/aries-vcx/pull/998](https://github.com/hyperledger/aries-vcx/pull/998)
  - did exchange [https://github.com/hyperledger/aries-vcx/pull/928](https://github.com/hyperledger/aries-vcx/pull/928)
    
    - AATH PR!! [https://github.com/hyperledger/aries-agent-test-harness/pull/723/files](https://github.com/hyperledger/aries-agent-test-harness/pull/723/files)
    - aath: did-exchange for acapy in progress
    - aath: did-exchange for AFJ blocked
      
      - afj: works with qualified identifiers
      - aath: works with unqualified identifiers
    - aath: moving to qualified identifiers, qualified DIDs
- **In review**
  
  - V2 for issuance/presentation protocols
    
    - [https://github.com/hyperledger/aries-vcx/pulls](https://github.com/hyperledger/aries-vcx/pulls)
- **In progress**
  
  - Drop vdrtools anoncreds from CI, features - [https://github.com/hyperledger/aries-vcx/pull/1008](https://github.com/hyperledger/aries-vcx/pull/1008)
  - libvcx\_core refactoring - generics in favor of trait objects - [https://github.com/hyperledger/aries-vcx/pull/1011](https://github.com/hyperledger/aries-vcx/pull/1011)
- **Planned**
  
  - Release 0.60.0
    
    - Removed vdrtools (only keep wallet - perhaps in separate workspace to enable Askar wallet contribution?)
  - did:peer:4
  - Upgrade vdrtools wallet sqlx dependency
  - V2 issuance/presentation protocols

<!--THE END-->

- **End meeting discussion**
  
  - **Patrik:** Integration testing approach - revisiting issues pointed out by Miro upon test refactoring
    
    - Many integration tests belong to aries-vcx-core
    - In many cases, 1 test per aries protocol should suffice
  - **Patrik: Long/medium term goals:**
    
    - anoncreds-rs, support for did:web anoncreds methods
    - didcomm v2 (start with messaging, unrelying protocols like issuance/presentation later)
      
      - FYI: V3 issuance/presentation protocols exists - accomodated to didcomm v2

<!--THE END-->

- **Todos:**
  
  - Reject invites with invalid DIDs [https://github.com/hyperledger/aries-vcx/issues/963](https://github.com/hyperledger/aries-vcx/issues/963)

## Attachments:

![](images/icons/bullet_blue.gif) [hyperledger\_antitrust\_policy.jpg](attachments/18508132/18518804.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
