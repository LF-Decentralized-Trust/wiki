1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-09-28 Aries-vcx community call

Created by Patrik Stas, last modified on Sep 28, 2023

![](attachments/18507918/18518754.jpg?height=250)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Agenda:**

- **Start meeting discussion**
  
  - Agenda overview and ad-hoc additions ( you can add your discussion your point )
  - Community updates
    
    - DIF DIDComm Users Group Meets 2,3, and 4th Mondays: [https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md](https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md)
    - Loosening dependency versions in aries components
      
      - [https://github.com/hyperledger/anoncreds-rs/issues/240](https://github.com/hyperledger/anoncreds-rs/issues/240)
    - V2 issue-credential protocol discussion  started
      
      - [https://github.com/hyperledger/aries-rfcs/issues/796](https://github.com/hyperledger/aries-rfcs/issues/796)
    - Last Monday HL Anoncreds 2.0 call  
      
      - [2023-09-25 AnonCreds v2.0 Working Group Meeting](https://lf-hyperledger.atlassian.net/wiki/spaces/ANONCREDS/pages/20292602/2023-09-25+AnonCreds+v2.0+Working+Group+Meeting)
  - Mentorship updates
    
    - deploying mediator, simple relay, vcx-agency - data cleaned up daily
      
      - mediator: need docker container
      - relay: need docker container
      - vcx agency: to be deployed
    - mediator project project plan [aries-vcx based message mediator](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/aries-vcx+based+message+mediator) 
      
      - [https://github.com/nain-F49FF806/axum-test-server](https://github.com/nain-F49FF806/axum-test-server/pull/16)
    - uniffi aries-vcx wrapper project [Project Plan - Aries VCX Next-gen Mobile Wrapper (UniFFI)](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21960060)
      
      - [https://github.com/hyperledger/aries-vcx/tree/main/uniffi\_aries\_vcx](https://github.com/hyperledger/aries-vcx/tree/main/uniffi_aries_vcx)
- **Overview of recent work done**
  
  - Naian: unpack, refactoring
    
    - [https://github.com/hyperledger/aries-vcx/pull/992](https://github.com/hyperledger/aries-vcx/pull/992)
    - [https://github.com/hyperledger/aries-vcx/pull/1002](https://github.com/hyperledger/aries-vcx/pull/1002)
  - Completed lint fixes
  - Aries Messages: issue-credential v2 
    
    - [https://github.com/hyperledger/aries-vcx/pull/990](https://github.com/hyperledger/aries-vcx/pull/990)
- **Parked**
  
  - Demo aries-vcx [https://github.com/hyperledger/aries-vcx/pull/952](https://github.com/hyperledger/aries-vcx/pull/952)
  - did exchange [https://github.com/hyperledger/aries-vcx/pull/928](https://github.com/hyperledger/aries-vcx/pull/928)
    
    - AATH PR!! [https://github.com/hyperledger/aries-agent-test-harness/pull/723/files](https://github.com/hyperledger/aries-agent-test-harness/pull/723/files)
    - aath: did-exchange for acapy in progress
    - aath: did-exchange for AFJ blocked
      
      - afj: works with qualified identifiers
      - aath: works with unqualified identifiers
    - aath: moving to qualified identifiers, qualified DIDs
- **In review**
  
  - V2 for issuance/presentation protocols
  - Connection protocol: removed+added APIs
    
    - [https://github.com/hyperledger/aries-vcx/pull/982](https://github.com/hyperledger/aries-vcx/pull/982)
- **In progress**
  
  - Release 0.59.0
    
    - today/tomorrow
  - Repo re-org 
    
    - [https://github.com/hyperledger/aries-vcx/pull/1001](https://github.com/hyperledger/aries-vcx/pull/1001)
    - [https://github.com/hyperledger/aries-vcx/pull/998](https://github.com/hyperledger/aries-vcx/pull/998)
  - Preparing for vdr-tools anoncreds removal
    
    - expecting early next week
  - profiles: generics in favor of trait objects
- **Planned**
  
  - did:peer:4

<!--THE END-->

- **End meeting discussion**
  
  - Protocol: Presentation V2
  - try to upgrade sqlx after removing vdrtools anoncreds
- **Todos:**
  
  - Reject invites with invalid DIDs [https://github.com/hyperledger/aries-vcx/issues/963](https://github.com/hyperledger/aries-vcx/issues/963)
  - Repo org - we have a lot of directories now ![(smile)](images/icons/emoticons/smile.png) Can look a overwhelming for newcomers

## Attachments:

![](images/icons/bullet_blue.gif) [hyperledger\_antitrust\_policy.jpg](attachments/18507918/18518754.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
