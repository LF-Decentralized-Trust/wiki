1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2022 VCX calls](2022-VCX-calls_18516878.html)

# Hyperledger Aries : 2022-12-22 Aries-vcx community call

Created by Patrik Stas, last modified by Ry Jones on Dec 29, 2022

![](attachments/18500652/18517205.png?height=250)

**PLEASE NOTE:**

- **If you are planning on attending aries-vcx call, feel free login to wiki and add your own points under the "Discussion" section!**
- **Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)**

<!--THE END-->

- Free discussion 
  
  - Agenda additions and review

<!--THE END-->

- Overview of recent work done
  
  - refactoring: simplify messages crate [https://github.com/hyperledger/aries-vcx/issues/697](https://github.com/hyperledger/aries-vcx/issues/697)
  - error handling refactoring: [https://github.com/hyperledger/aries-vcx/issues/582](https://github.com/hyperledger/aries-vcx/issues/582)
  - Use `bs58`  instead `rust-base58`  [https://github.com/hyperledger/aries-vcx/issues/694](https://github.com/hyperledger/aries-vcx/issues/694)
- Check on work in progress
  
  - Error handling refactoring [https://github.com/hyperledger/aries-vcx/pull/702](https://github.com/hyperledger/aries-vcx/pull/702)
  - Messages/diddoc refactoring [https://github.com/hyperledger/aries-vcx/pull/704](https://github.com/hyperledger/aries-vcx/pull/704)
  - CI: Cargo fmt check [https://github.com/hyperledger/aries-vcx/pull/703](https://github.com/hyperledger/aries-vcx/pull/703)
  - CI: Clippy checks [https://github.com/hyperledger/aries-vcx/pull/705](https://github.com/hyperledger/aries-vcx/pull/705)
  - AriesVCX-CLI POC [https://github.com/hyperledger/aries-vcx/pull/692](https://github.com/hyperledger/aries-vcx/pull/692)
  - Support for Aries Askar wallet
  - NodeJS: New FFI [https://github.com/hyperledger/aries-vcx/pull/665](https://github.com/hyperledger/aries-vcx/pull/665)
- New tasks
  
  - Decoupling: Extract `protocols`  crate [https://github.com/hyperledger/aries-vcx/issues/698](https://github.com/hyperledger/aries-vcx/issues/698)
  - Refactoring: Unify state machine interface approach [https://github.com/hyperledger/aries-vcx/issues/696](https://github.com/hyperledger/aries-vcx/issues/696)
  - Eliminate usage of PublicAgent [https://github.com/hyperledger/aries-vcx/issues/679](https://github.com/hyperledger/aries-vcx/issues/679)
  - Optimize codecov approach in CI  [https://github.com/hyperledger/aries-vcx/issues/677](https://github.com/hyperledger/aries-vcx/issues/677)
  - Implement issuer/verifier for modular profiles [https://github.com/hyperledger/aries-vcx/issues/699](https://github.com/hyperledger/aries-vcx/issues/699)
  - Spit libvcx in 2 crates (no breaking changes for existing wrappers)
  - Update docs, diagrams
- Discussion
  
  - Reduction of error kinds? Do we have too many? What's the experience of consuming aries-vcx from a different crate?
  - JSON-LD credential support?

Task backlog: 

- - Enable OOB tests in AATH [https://github.com/hyperledger/aries-vcx/issues/678](https://github.com/hyperledger/aries-vcx/issues/678)
  - Eliminate usage of MediatedConnection in tests
  - DDO as first class citizen
  - Add more typing across codebase
  - New protocols: DidExchange protocol, Presentation Protocol 2.0, Issuance Protocol 2.0

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

PNG File [image-2022-12-21\_9-42-59.png](attachments/18500652/18517205.png "Download")

Dec 21, 2022 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

File [GMT20221222-085917\_Recording.transcript.vtt](attachments/18500652/18517228.vtt "Download")

Dec 29, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description

[Download All](/wiki/download/all_attachments?pageId=18500652 "Download all the latest versions of attachments on this page as single zip file.")

## Attachments:

![](images/icons/bullet_blue.gif) [image-2022-12-21\_9-42-59.png](attachments/18500652/18517205.png) (image/png)  
![](images/icons/bullet_blue.gif) [GMT20221222-085917\_Recording.transcript.vtt](attachments/18500652/18517228.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18500652/18517226.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18500652/18517227.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
