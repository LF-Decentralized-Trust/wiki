1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-03-02 Aries-vcx community call

Created by Patrik Stas, last modified on Mar 02, 2023

![](attachments/18502496/18517664.jpg?height=250)

### Meeting time: **Thursday 2023-02-23, 09:00UTC** Zoom link:  [**https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09#success**](https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09#success)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Agenda:**

- Start meeting discussion 
  
  - **feel free to add your discussion point here** (you need to login)

<!--THE END-->

- Overview of recent work done
  
  - oob serialization/deserialization fix [https://github.com/hyperledger/aries-vcx/pull/762](https://github.com/hyperledger/aries-vcx/pull/762)
  - libvcx split, updated documentation [https://github.com/hyperledger/aries-vcx/pull/759](https://github.com/hyperledger/aries-vcx/pull/759)
  - aath results conclusion
    
    - aath oob tests are often using connectionless proof presentation [https://github.com/hyperledger/aries-rfcs/blob/main/features/0496-transition-to-oob-and-did-exchange/README.md](https://github.com/hyperledger/aries-rfcs/blob/main/features/0496-transition-to-oob-and-did-exchange/README.md)
- Check on work in progress
  
  - messages rework update [https://github.com/hyperledger/aries-vcx/pull/754](https://github.com/hyperledger/aries-vcx/pull/754)
- Upcoming work
  
  - vdr-tools as feature flag [https://github.com/hyperledger/aries-vcx/pull/763](https://github.com/hyperledger/aries-vcx/pull/763)
  - removal of legacy did:sov implementation ( `parse_legacy_endpoint_attrib` , `write_endpoint_legacy`  )
    
    - [https://github.com/hyperledger/aries-vcx/blob/3feb5fa32e632c6a8beb3ca6ec1fe845dcf987ad/aries\_vcx/src/common/ledger/transactions.rs#L198](https://github.com/hyperledger/aries-vcx/blob/3feb5fa32e632c6a8beb3ca6ec1fe845dcf987ad/aries_vcx/src/common/ledger/transactions.rs#L198)

<!--THE END-->

- End meeting discussion
  
  - release 0.53.0
  - Mentorship program [Mentorship Projects](https://lf-hyperledger.atlassian.net/wiki/spaces/INTERN/pages/21954604/Mentorship+Projects)
  - protocol threading behaviour [https://github.com/hyperledger/aries-vcx/issues/761](https://github.com/hyperledger/aries-vcx/issues/761)
  - **feel free to add your discussion point here** (you need to login)

Task backlog: 

- - Compile time protocol registry boundary
  - Apply state pattern for issuance, presentation state machines
  - Issuer with credx
  - Eliminate usage of MediatedConnection in tests (in favor of (non-mediated) Connection)
  - DDO as first class citizen
  - Create DID parser, DID type
  - Implement DID resolver [https://github.com/hyperledger/aries-vcx/issues/706](https://github.com/hyperledger/aries-vcx/issues/706)
  - Add more typing across codebase
    
    - use **did** type, use **url** type, and others
  - New protocols: DidExchange protocol, Presentation Protocol 2.0, Issuance Protocol 2.0
  - Aries mediator client (pick protocol V2)

### Recording

[https://youtu.be/hbjEPAdbXxo](https://youtu.be/hbjEPAdbXxo)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

JPEG File [hyperledger\_antitrust\_policy.jpg](attachments/18502496/18517664.jpg "Download")

Feb 23, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [GMT20230302-085905\_RecordingnewChat.txt](attachments/18502496/18517700.txt "Download")

Mar 02, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description

[Download All](/wiki/download/all_attachments?pageId=18502496 "Download all the latest versions of attachments on this page as single zip file.")

## Attachments:

![](images/icons/bullet_blue.gif) [hyperledger\_antitrust\_policy.jpg](attachments/18502496/18517664.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [GMT20230302-085905\_RecordingnewChat.txt](attachments/18502496/18517700.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
