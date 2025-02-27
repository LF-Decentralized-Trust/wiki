1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-09-14 Aries-vcx community call

Created by Patrik Stas, last modified on Sep 14, 2023

![](attachments/18507527/18518693.png?height=250)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Agenda:**

- **Start meeting discussion**
  
  - Agenda overview and ad-hoc additions ( you can add your discussion your point )
  - Community updates
    
    - DIF DIDComm Users Group Meets 2,3, and 4th Mondays: [https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md](https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md)
  - Mentorship updates
    
    - mediator project project plan [aries-vcx based message mediator](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/aries-vcx+based+message+mediator)
      
      - [https://github.com/nain-F49FF806/axum-test-server](https://github.com/nain-F49FF806/axum-test-server/pull/16)
    - uniffi aries-vcx wrapper project [Project Plan - Aries VCX Next-gen Mobile Wrapper (UniFFI)](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21960060)
      
      - [https://github.com/hyperledger/aries-vcx/tree/main/uniffi\_aries\_vcx](https://github.com/hyperledger/aries-vcx/tree/main/uniffi_aries_vcx)
- **Overview of recent work done**
  
  - Message builders [https://github.com/hyperledger/aries-vcx/pull/972](https://github.com/hyperledger/aries-vcx/pull/972)
  - Test refactoring
    
    - pt1. [https://github.com/hyperledger/aries-vcx/pull/967](https://github.com/hyperledger/aries-vcx/pull/967)
    - pt2. [https://github.com/hyperledger/aries-vcx/pull/974](https://github.com/hyperledger/aries-vcx/pull/974)
    - Among many other improvements: Removed dependency on agency\_client in tests. People don't anymore need to run vcxagency-node to execute integration tests
  - Uniffi demo QR scanning [https://github.com/hyperledger/aries-vcx/pull/954](https://github.com/hyperledger/aries-vcx/pull/954)
- **Parked**
  
  - Demo aries-vcx [https://github.com/hyperledger/aries-vcx/pull/952](https://github.com/hyperledger/aries-vcx/pull/952)
  - did exchange [https://github.com/hyperledger/aries-vcx/pull/928](https://github.com/hyperledger/aries-vcx/pull/928)
    
    - AATH PR!! [https://github.com/hyperledger/aries-agent-test-harness/pull/723/files](https://github.com/hyperledger/aries-agent-test-harness/pull/723/files)
    - aath: did-exchange for acapy in progress
    - aath: did-exchange for AFJ blocked
      
      - afj: works with qualified identifiers
      - aath: works with unqualified identifiers
    - aath: moving to qualified identifiers, qualified DIDs
- **In progress**
  
  - More test refactoring
  - Preparing for vdr-tools anoncreds removal
  - Fix the lints
- **Planned**
  
  - V2 for issuance/presentation protocols

<!--THE END-->

- **End meeting discussion**
  
  - &lt;this can be your topic&gt; - let us know at the beginning of session
- **Todos:**
  
  - Reject invites with invalid DIDs [https://github.com/hyperledger/aries-vcx/issues/963](https://github.com/hyperledger/aries-vcx/issues/963)
  - Repo org - we have a lot of directories now ![(smile)](images/icons/emoticons/smile.png) Can look a overwhelming for newcomers
  - Lint fix needed too!

## Attachments:

![](images/icons/bullet_blue.gif) [hl-antitrust.png](attachments/18507527/18518693.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
