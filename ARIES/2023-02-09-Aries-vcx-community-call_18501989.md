1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-02-09 Aries-vcx community call

Created by Patrik Stas, last modified on Feb 09, 2023

![](attachments/18501989/18517531.png?height=250)

**PLEASE NOTE:**

- **If you are planning on attending aries-vcx call, feel free login to wiki and add your own points under the "Discussion" section!**
- **Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)** 
  

<!--THE END-->

- Start meeting discussion

<!--THE END-->

- Overview of recent work done
  
  - ✅ Connection rewrite using state pattern  - [https://github.com/hyperledger/aries-vcx/pull/739](https://github.com/hyperledger/aries-vcx/pull/739)
  - ✨ \[New contributor PR] - libvcx ios wrapper fix [https://github.com/hyperledger/aries-vcx/pull/747](https://github.com/hyperledger/aries-vcx/pull/747)
- Check on work in progress
  
  - POC: UniFFI - [https://github.com/hyperledger/aries-vcx/pull/737](https://github.com/hyperledger/aries-vcx/pull/737), notes:
    
    - George explained how UniFFI prototype works, demoed actual Android application in emulator utilizing UniFFI wrapper (the PR)
    - We've discussed the approach to async functions with the uniffi
- Upcoming work
  
  - Finish polishing Connection rewrite (#739)
  - Messages crate refactor

<!--THE END-->

- End meeting discussion
  
  - State machine serialization approach and philosophy
    
    - [https://github.com/hyperledger/aries-vcx/issues/742](https://github.com/hyperledger/aries-vcx/issues/742)
    - [https://github.com/hyperledger/aries-vcx/issues/745](https://github.com/hyperledger/aries-vcx/issues/745)
    - question: should serialized format be considered opaque to users?
  - Discussion conclusion:
    
    - **Serialized state machines should be considered opaque - users should not rely on the serialization structure, it might change in the future**.
    - However, users can rely on ability to deserialize state machine from previous version of vcx, even if change in serialization format occurs
    - We will include `from_parts`  , `to_parts`  type of API on state machines, as it existed on `MediatedConnection`

Task backlog: 

- - Reduce cloning in `messages, diddoc`  crates
  - Replace some of macros (for example `threadlike_optional`) with traits instead
  - Apply State pattern for issuance, presentation state machines
  - Issuer with credx
  - Decoupling: Extract `protocols`  crate [https://github.com/hyperledger/aries-vcx/issues/698](https://github.com/hyperledger/aries-vcx/issues/698)
  - Refactoring: Unify state machine interface approach [https://github.com/hyperledger/aries-vcx/issues/696](https://github.com/hyperledger/aries-vcx/issues/696)
  - Enable OOB tests in AATH [https://github.com/hyperledger/aries-vcx/issues/678](https://github.com/hyperledger/aries-vcx/issues/678)
  - Eliminate usage of MediatedConnection in tests
  - DDO as first class citizen
  - Add more typing across codebase
  - New protocols: DidExchange protocol, Presentation Protocol 2.0, Issuance Protocol 2.0

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

PNG File [image-2023-2-8\_18-54-51.png](attachments/18501989/18517530.png "Download")

Feb 08, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

PNG File [HyperledgerFoundationAntiTrust.png](attachments/18501989/18517531.png "Download")

Feb 08, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true)

File [GMT20230209-085946\_Recording.transcript.vtt](attachments/18501989/18517541.vtt "Download")

Feb 09, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true)

Text File [GMT20230209-085946\_RecordingnewChat.txt](attachments/18501989/18517543.txt "Download")

Feb 09, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true)

PNG File [image-2023-2-9\_17-19-20.png](attachments/18501989/18517544.png "Download")

Feb 09, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
