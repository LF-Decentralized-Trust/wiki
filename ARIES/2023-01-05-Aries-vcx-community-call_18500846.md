1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2023 VCX calls](2023-VCX-calls_18517247.html)

# Hyperledger Aries : 2023-01-05 Aries-vcx community call

Created by Patrik Stas, last modified by Ry Jones on Jan 05, 2023

![](attachments/18500846/18517248.png?height=250)

**PLEASE NOTE:**

- **If you are planning on attending aries-vcx call, feel free login to wiki and add your own points under the "Discussion" section!**
- **Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)** 
  

<!--THE END-->

- Free discussion

<!--THE END-->

- Overview of recent work done
  
  - Removal of PublicAgent API [https://github.com/hyperledger/aries-vcx/pull/715](https://github.com/hyperledger/aries-vcx/pull/715)
  - Minor refactoring PRs
- Check on work in progress
  
  - NodeJS: napi-rs based bindings for NodeJS wrapper [https://github.com/hyperledger/aries-vcx/pull/665](https://github.com/hyperledger/aries-vcx/pull/665)
  - Expanded support for (non-mediated) Connection ([https://github.com/hyperledger/aries-vcx/pull/717](https://github.com/hyperledger/aries-vcx/pull/717), [https://github.com/hyperledger/aries-vcx/pull/718](https://github.com/hyperledger/aries-vcx/pull/718))
  - Verifier using credx [https://github.com/hyperledger/aries-vcx/pull/708](https://github.com/hyperledger/aries-vcx/pull/708)

<!--THE END-->

- **2022 review and current state**
  
  - Modularization &amp; decoupling
    
    - DDO, Messages
    - libvcx split to api\_c, api\_vcx
    - Vcxagency mediator becoming optional
  - Simplifications and refactoring
  - Increased community focus
    
    - community calls
    - new contributors
  - Testing improvements
  - AATH integration
  - NodeJS Wrapper
- **2023 outlook**
  
  - crateification! ([https://github.com/hyperledger/aries-vcx/issues/712](https://github.com/hyperledger/aries-vcx/issues/712))
    
    - drive APIs and documentation quality
  - DDO resolver  ([https://github.com/hyperledger/aries-vcx/issues/706](https://github.com/hyperledger/aries-vcx/issues/706))
    
    - think about ledger agnosticity, at least in terms of didcomm
  - Migrating to modular credex libs ([https://github.com/hyperledger/aries-vcx/issues/699](https://github.com/hyperledger/aries-vcx/issues/699))
    
    - Credex libraries on issuer+verifier
    - Enable migration of vdr-tools issuer -→ credex issuer
    - Add support for Aries Askar wallet
  - Continue improving code quality
    
    - More traits, more typing
    - Faster test execution - parallelization, independence of tests, remove usage of msg mediator
    - Explore use of mocking libraries
  - Further increase community engagement
    
    - Improve documentation
    - Lower barriers getting started with aries-vcx
    - Aries-vcx based project examples
  - Enhance aries protocols support
  - Dicomm 2.0 exploration

<!--THE END-->

- Discussion

Parked work:

- AriesVCX-CLI POC [https://github.com/hyperledger/aries-vcx/pull/692](https://github.com/hyperledger/aries-vcx/pull/692)

Task backlog: 

- - Implement DDO resolver [https://github.com/hyperledger/aries-vcx/issues/706](https://github.com/hyperledger/aries-vcx/issues/706)
  - Decoupling: Extract `protocols`  crate [https://github.com/hyperledger/aries-vcx/issues/698](https://github.com/hyperledger/aries-vcx/issues/698)
  - Refactoring: Unify state machine interface approach [https://github.com/hyperledger/aries-vcx/issues/696](https://github.com/hyperledger/aries-vcx/issues/696)
  - Eliminate usage of PublicAgent [https://github.com/hyperledger/aries-vcx/issues/679](https://github.com/hyperledger/aries-vcx/issues/679)
  - Optimize codecov approach in CI  [https://github.com/hyperledger/aries-vcx/issues/677](https://github.com/hyperledger/aries-vcx/issues/677)
  - Split libvcx in 2 crates (no breaking changes for existing wrappers)
  - Enable OOB tests in AATH [https://github.com/hyperledger/aries-vcx/issues/678](https://github.com/hyperledger/aries-vcx/issues/678)
  - Eliminate usage of MediatedConnection in tests
  - DDO as first class citizen
  - Add more typing across codebase
  - New protocols: DidExchange protocol, Presentation Protocol 2.0, Issuance Protocol 2.0

### Current architecture diagrams 1.1.2023 LibVCX: ![](attachments/18500846/18517250.png?height=250)

### 1.1.2023 Aries-vcx

## ![](attachments/18500846/18517251.png?height=250)

#### Comparison - Old Q3 2021 diagram ![](attachments/18500846/18517252.png?height=250)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

PNG File [image-2023-1-4\_17-56-24.png](attachments/18500846/18517248.png "Download")

Jan 04, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

PNG File [ariesvcx\_architecture\_now\_040123\_libvcx.drawio.png](attachments/18500846/18517250.png "Download")

Jan 04, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true)

PNG File [ariesvcx\_architecture\_now\_040123\_aries\_vcx.drawio.png](attachments/18500846/18517251.png "Download")

Jan 04, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true)

PNG File [ariesvcx\_architecture\_now\_180821.png](attachments/18500846/18517252.png "Download")

Jan 04, 2023 by [Patrik Stas](/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true&isFromPageView=true)

File [GMT20230105-090143\_Recording.transcript.vtt](attachments/18500846/18517276.vtt "Download")

Jan 05, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description

[Download All](/wiki/download/all_attachments?pageId=18500846 "Download all the latest versions of attachments on this page as single zip file.")

## Attachments:

![](images/icons/bullet_blue.gif) [image-2023-1-4\_17-56-24.png](attachments/18500846/18517248.png) (image/png)  
![](images/icons/bullet_blue.gif) [ariesvcx\_architecture\_now\_040123\_libvcx.drawio.png](attachments/18500846/18517250.png) (image/png)  
![](images/icons/bullet_blue.gif) [ariesvcx\_architecture\_now\_040123\_aries\_vcx.drawio.png](attachments/18500846/18517251.png) (image/png)  
![](images/icons/bullet_blue.gif) [ariesvcx\_architecture\_now\_180821.png](attachments/18500846/18517252.png) (image/png)  
![](images/icons/bullet_blue.gif) [GMT20230105-090143\_Recording.transcript.vtt](attachments/18500846/18517276.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18500846/18517275.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18500846/18517277.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
