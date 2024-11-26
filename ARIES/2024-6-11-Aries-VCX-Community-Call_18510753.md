1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries-vcx Rust](Aries-vcx-Rust_18499431.html)
5. [Community calls](Community-calls_18499459.html)
6. [2024 VCX Calls](2024-VCX-Calls_18519103.html)

# Hyperledger Aries : 2024-6-11 Aries VCX Community Call

Created by James Ebert, last modified on Jun 12, 2024

![](attachments/18510753/18519428.png?height=250)

**Note:**

- If you are planning on attending Aries VCX Community Call, **feel free login to wiki and update the agenda below to include your discussion topic / question**
- Alternatively you can simply join the call and we can discuss your questions and concerns ![(smile)](images/icons/emoticons/smile.png)

### Zoom: [https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09](https://zoom.us/j/97759680284?pwd=VytRRlJSd3c5NXJ1V25XbUxNU0Jndz09)

### Recording

# Announcements

- Timing adjustment - Aries VCX community call to bi-weekly at Tuesday 11:00 PM UTC | Tuesday 4:00 PM PT | Wednesday 9 AM AEST
- Release 0.64.0 - [https://github.com/hyperledger/aries-vcx/releases/tag/0.64.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.64.0)
  
  - Lots of refactoring, fixes, and dependency updates. did:peer:4 support was added, as well as the move to using upstream anoncreds-rs releases. Release 0.64.0 includes the last of the major contributions supported by the Absa team--major thanks to all of the Absa contributors for all their hard work and contributions to Aries VCX!
- Absa presence in aries-vcx officially ending by the end of April
  
  - Overview of repo presented at the AriesWG call [2024-04-03 Aries Working Group Call](2024-04-03-Aries-Working-Group-Call_18510389.html)
- Vision for future:
  
  - DF.RS
  - Go-to user friendly, efficient, feature complete implementation of DidCore - DID, DidDocuments. Become \`url\` crate of DIDs and DidDocuments
  - Didcomm V2
  - Mediator with web sockets
  - Mediation client
  - New credential types
  - ?Mobile/Browser secure storage options?
- Cool blogpost from our ex-mentee and current co-maintainer Naian
  
  - [https://www.hyperledger.org/blog/hyperledger-mentorship-spotlight-aries-vcx-based-message-mediator](https://www.hyperledger.org/blog/hyperledger-mentorship-spotlight-aries-vcx-based-message-mediator "https://www.hyperledger.org/blog/hyperledger-mentorship-spotlight-aries-vcx-based-message-mediator")

## Overview of recent work done

- Reduce unnecessary dependencies - [https://github.com/hyperledger/aries-vcx/pull/1217](https://github.com/hyperledger/aries-vcx/pull/1217)
- Update to upstream anoncreds-rs 0.2 - [https://github.com/hyperledger/aries-vcx/pull/1213](https://github.com/hyperledger/aries-vcx/pull/1213)
- Loosen Presentation Request version restriction - [https://github.com/hyperledger/aries-vcx/pull/1212](https://github.com/hyperledger/aries-vcx/pull/1212)

## Overview of work in progress

- Update Aries Agent Test Harness (AATH) Aries VCX backchannel to use an image and update to version 0.64.0
  
  - [https://github.com/hyperledger/aries-vcx/pull/1221](https://github.com/hyperledger/aries-vcx/pull/1221)
  - [https://github.com/hyperledger/aries-agent-test-harness/pull/833/files](https://github.com/hyperledger/aries-agent-test-harness/pull/833/files)
- Fix Indy DID Generation from seed (secret bytes) - [https://github.com/hyperledger/aries-vcx/pull/1224](https://github.com/hyperledger/aries-vcx/pull/1224)

# Agenda:

- Aries Agent Test Harness updates (~looks really good)
  
  - [https://github.com/hyperledger/aries-vcx/pull/1221](https://github.com/hyperledger/aries-vcx/pull/1221)
  - [https://github.com/hyperledger/aries-agent-test-harness/pull/833/files](https://github.com/hyperledger/aries-agent-test-harness/pull/833/files)
- Aries VCX Modularity Discussion - [https://github.com/hyperledger/aries-vcx/pull/1212#issuecomment-2151083288](https://github.com/hyperledger/aries-vcx/pull/1212#issuecomment-2151083288)
  
  - Removing credx, indyvdrtools, legacy?
    
    - Only concern is other people using these dependencies
      
      - Absa built a whole bunch of migration tools for them
      - Find out if other people are out there using these features/wallets
      - Communicating deprecating/removing of features/crates from Aries VCX
        
        - Indy wallet, wallet migrator, Credx, indy-sdk(in legacy directory)
  - anoncreds-rs types
    
    - Bit of a maintenance issue - in particular with new major versions of AnonCreds RS
    - Allows us to not compile AnonCreds RS if someone doesn't want to.
    - Dream solution getting AnonCreds RS making a standalone anoncreds-types crate. Thinned down crate.
      
      - Maybe we should approach the anoncreds-rs maintainers
      - How difficult is it to make a switch here? - depends on how good you are with your IDE ![(wink)](images/icons/emoticons/wink.png)
      - How urgent?
        
        - Could wait until Anoncreds-rs 0.3 is released
        - We temporarily ignore the special use cases and use upstream immediately
          
          - could reduce code base complexity
        - May want to determine how heavy the existing crate is
      - Long term make a request for a thinner crate - anoncreds-rs - George to voice to GH issues.
- Any Ad hoc discussion topics (feel free to add items)
  
  - VCX Record storage / state machines - James question

![](attachments/18510753/18519427.jpg?height=250)

## Attachments:

![](images/icons/bullet_blue.gif) [aries-framework-rust.jpg](attachments/18510753/18519427.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [image-2024-4-4\_17-37-54.png](attachments/18510753/18519428.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
