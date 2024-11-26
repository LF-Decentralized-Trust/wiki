1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-03-16 Aries-vcx community call

Created by Patrik Stas, last modified by Ry Jones on Mar 16, 2023

### Meeting time: **09:00 am UTC** Zoom link:  [**https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09#success**](https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09#success)

![](attachments/18503085/18517743.jpg?height=250)

### **Note:**

- If you are planning on attending aries-vcx call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### **Agenda:**

- **Start meeting discussion** 
  
  - **feel free to add a topic/question here** (you just need to login to edit this page)
  - Mentorship program [Mentorship Projects](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Mentorship+Projects) 
    
    - [aries-vcx based message mediator](https://lf-hyperledger.atlassian.net/wiki/spaces/INTERN/pages/21954879/aries-vcx+based+message+mediator)
    - [aries-vcx next-gen mobile wrapper](https://lf-hyperledger.atlassian.net/wiki/spaces/INTERN/pages/21954874/aries-vcx+next-gen+mobile+wrapper)
  - Onboarding new contributors - "Good first issue" Github issues
    
    - New issues has been created
      
      - [https://github.com/hyperledger/aries-vcx/issues/772](https://github.com/hyperledger/aries-vcx/issues/772)
      - [https://github.com/hyperledger/aries-vcx/issues/773](https://github.com/hyperledger/aries-vcx/issues/773)
      - [https://github.com/hyperledger/aries-vcx/issues/774](https://github.com/hyperledger/aries-vcx/issues/774)
      - [https://github.com/hyperledger/aries-vcx/issues/775](https://github.com/hyperledger/aries-vcx/issues/775)
      - [https://github.com/hyperledger/aries-vcx/issues/776](https://github.com/hyperledger/aries-vcx/issues/776)
    - "Good first issue" guidelines

<!--THE END-->

- **Overview of recent work done**
  
  - Proof Verifier API changes [https://github.com/hyperledger/aries-vcx/pull/770](https://github.com/hyperledger/aries-vcx/pull/770)
    
    - Discussion: Other state machines changes
      
      - Final Success/Success non-acked/Failure state - separate state structure, or shared and derive Aries status from .getState()?
      - Intermediate states (CredentialBuilt)
        
        - How should `.getState()`  behave when residing in an intermediate state?
      - Transition linearization
  - feature flag for VdrToolsLess [https://github.com/hyperledger/aries-vcx/pull/763](https://github.com/hyperledger/aries-vcx/pull/763)
- **Check on work in progress**
  
  - Messages2 crate [https://github.com/hyperledger/aries-vcx/pull/754](https://github.com/hyperledger/aries-vcx/pull/754)
  - Typestate pattern: Cred. Holder [https://github.com/hyperledger/aries-vcx/pull/768](https://github.com/hyperledger/aries-vcx/pull/768)
    
    - Update from George: *I’ve mostly paused work on the holder state pattern and will continue after messages crate is merged. Will also review messages crate if/when it’s ready*
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

- End meeting discussion
  
  - **anything else that comes up to be discussed**

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

Recording

[https://youtu.be/ku1NZudkZiY](https://youtu.be/ku1NZudkZiY)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

JPEG File [hyperledger\_antitrust\_policy.jpg](attachments/18503085/18517743.jpg "Download")

Mar 14, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [GMT20230316-085819\_RecordingnewChat.txt](attachments/18503085/18517781.txt "Download")

Mar 16, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description

[Download All](/wiki/download/all_attachments?pageId=18503085 "Download all the latest versions of attachments on this page as single zip file.")

## Attachments:

![](images/icons/bullet_blue.gif) [hyperledger\_antitrust\_policy.jpg](attachments/18503085/18517743.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [GMT20230316-085819\_RecordingnewChat.txt](attachments/18503085/18517781.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
