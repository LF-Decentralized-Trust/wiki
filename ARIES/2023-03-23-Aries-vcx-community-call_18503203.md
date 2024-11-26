1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-03-23 Aries-vcx community call

Created by Patrik Stas, last modified on Mar 23, 2023

### Meeting time: **09:00 am UTC** Zoom link:  [**https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09#success**](https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09#success)

![](attachments/18503203/18517769.jpg?height=250)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Agenda:**

- **Start meeting discussion** 
  
  - Mentorship program status update
    
    - Pending for TOC approval
  - Github "Good first issue" catching on! 
    
    - 2 new contributors
  - Work parallelization
    
    - Discussion about parallelizing work on messages2 integration and building state pattern based protocol state machines
    - Release 0.54.0 is expected to be based on the new `message2`  crate - the current `messages`  implementation will be deleted.
      
      - Minor changes to `aries-vcx`  rust API is expected
      - The upgrade completely opaque to `libvcx` , `vcx-napi-rs`  users

<!--THE END-->

- **Overview of recent work done**
  
  - Proof Verifier API changes: [https://github.com/hyperledger/aries-vcx/pull/769](https://github.com/hyperledger/aries-vcx/pull/769), [https://github.com/hyperledger/aries-vcx/pull/769](https://github.com/hyperledger/aries-vcx/pull/769)
  - Release 0.53.0 [https://github.com/hyperledger/aries-vcx/releases/tag/0.53.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.53.0)
- **Check on work in progress**
  
  - New contributor: styvane - encode\_attributes refactor [https://github.com/hyperledger/aries-vcx/pull/778](https://github.com/hyperledger/aries-vcx/pull/778)
  - New contributor: andy-waine - post\_message migration [https://github.com/hyperledger/aries-vcx/pull/777](https://github.com/hyperledger/aries-vcx/pull/777)
  - Messages2 crate - approaching completion [https://github.com/hyperledger/aries-vcx/pull/754](https://github.com/hyperledger/aries-vcx/pull/754)
- **Upcoming work**
  
  - Finish messages2 crate
  - Integrate messages2 crate into aries-vcx
  - Typestate pattern 
    
    - credential holder (started by George)
    - credential issuer
    - presentation verifier
    - presentation prover
  - \[ vdr-tools, DID parser, did-resolver ]

<!--THE END-->

- **End meeting discussion** (anything else that comes up to be discussed)
  
  - **Dependency flags**
    
    - WIP: Feature flags to opt out of `vdr-tools`  or modular dependencies - [https://github.com/hyperledger/aries-vcx/pull/763](https://github.com/hyperledger/aries-vcx/pull/763)
  - **Guidelines for re-implementing state machines**
    
    1. **No "Sent" states:** Do not use `<something>Sent`  states which serve as "marker" that some message has been sent to a counterparty.
    2. **Various final states:** Different variants of final state should be expressed by different rust state types - eg. `Success`  / `Fail`  /  `Declined`
    3. **Received aries messages change state:**Message from a counterparty always changes state - even if it's just `ack` . Finished state and "AlmostFinishedButWaitingForAck" in some protocol should be 2 different states.
    4. **Intermediate states:** Use intermediate states to enable separation of response processing and reply construction - for example `PresentationPrepared`  in ProofProver SM, `PresentationRequestSet` in ProofVerifier SM
       
       - The fact that the our "to be sent" message has been built/prepared/set (we should maybe unify the terminology there as well) means that we are expecting response (as per point 1. we do not track on state machine level whether that message has been sent, it's aries-vcx user's resposibility to deliver the message)
    5. **Linearization of transitions:** - each state machine transition method should either fail, or succeed and switch state deterministically.
       
       - [https://github.com/hyperledger/aries-vcx/pull/768#issuecomment-1461576585](https://github.com/hyperledger/aries-vcx/pull/768#issuecomment-1461576585)

Task backlog: 

- - Compile time protocol registry boundary
  - Apply state pattern for issuance, presentation state machines
  - Issuer with credx
  - Eliminate usage of MediatedConnection in tests (in favor of (non-mediated) Connection)
  - DDO as first class citizen
  - Create DID parser, DID type
  - Implement DID resolver [https://github.com/hyperledger/aries-vcx/issues/706](https://github.com/hyperledger/aries-vcx/issues/706)
  - Add more typing across codebase
    
    - use **did** type, use **url** type, and others
  - New protocols: DidExchange protocol, Presentation Protocol 2.0, Issuance Protocol 2.0
  - Aries mediator client (pick protocol V2)

Recording:

[https://youtu.be/msyBT0\_nhI8](https://youtu.be/msyBT0_nhI8)

[GMT20230323-085927\_RecordingnewChat.txt](attachments/18503203/18517830.txt)

## Attachments:

![](images/icons/bullet_blue.gif) [hyperledger\_antitrust\_policy.jpg](attachments/18503203/18517769.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [GMT20230323-085927\_RecordingnewChat.txt](attachments/18503203/18517830.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
