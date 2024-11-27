1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-03-09 Indy Contributors Call

Created by Richard Esplin, last modified on Mar 11, 2020

## Summary

- Work updates and collaboration on projects
  
  - VDR
  - CredX
  - Rich Schemas
- CI / CD
- Update from the Hyperledger Global Forum

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;

## Related Calls and Announcements

- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.
- Results from [call to discuss techniques for supporting an Indy Network](19464360.html)

## Release Status and Work Updates

- Indy Node
  
  - February:
    
    - No formal release of Indy Node
    - New items available
      
      - Tool for detecting ZMQ network problems
      - Troubleshooting guide
  - March:
    
    - Replacing Indy Crypto with Ursa (Kiva)
    - More "rich schema" objects
  - Future
    
    - Ubuntu 18.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
- Indy SDK
  
  - February:
    
    - Cancelled at the last minute because we found a bug.
  - March: 
    
    - 1.15.0:
      
      - LibVCX improvements to reject proof and connection redirect
      - Bug fixes
- Indy Catalyst
  
  - [https://github.com/bcgov/indy-catalyst](https://github.com/bcgov/indy-catalyst)
  - Still working on performance improvements
  - Being deployed at Government of Canada
  - Migrating to Hyperledger Aries: plan is to moving to aries-verified-credential-registry
    
    - Needs more documentation
- Anoncreds 2.0
  
  - Mike: Creating a development plan in the Indy section of the wiki
  - Mike: Aries-Credx
  - Andrew: Indy-Credx
- Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - Remaining work: Design doc, FFI, testing, CI / CD
        
        - PR for using GitHub actions to run unit tests for CI.
          
          - Mike can help review.
          - Mike and Artem can help with CD artifacts for the various platforms.
      - As an Aries interface becomes standardized, will add that API layer
      - Split out an Indy-Util to contain common components between Indy-VDR and Indy-Credx
        
        - Need to check that duplicate copies of the util library doesn't cause trouble.
    - indy-credx / aries-credx
      
      - [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
        
        - 6 most common attribute encodings
        - Does not yet have anoncreds 1 attribute encoding.
      - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
        
        - Can make a non-revocable credential and create proofs.
        - Tagging will be moved to the KMS.
        - Mike will be working on revocation registry 2.0
    - Aries-Shared-Util
      
      - Pack / Unpack
      - Not started yet
    - Aries-KMS
      
      - Mike working on documentation and architecture as an Aries RFC (KMS architecture) and Ursa RFC (API)
        
        - PR is submitted: [https://github.com/hyperledger/aries-rfcs/pull/440](https://github.com/hyperledger/aries-rfcs/pull/440)
      - Mike and Cam's aries-core-rs → aries-kms-mayaguez
        
        [https://github.com/sovrin-foundation/aries-kms-rs](https://github.com/sovrin-foundation/aries-kms-rs)
        
        - Persistence work allows plugging in any database engine.
        - Focus is using an external enclave.
      - Indy wallet crate might move to start another aries-kms implementation → aries-kms-vostok
- Ursa 0.3.2
  
  - To replace libsodium, need to have a replacement for the anoncrypt / authcrypt sealed box for pack / unpack.
    
    - Can be done in Ursa with two steps, but might add as a single function call.

## Main Business

- Issue with encoding stripping leading zeros. (IS-1492?)
- Experimenting with the PyO3 buffer:
  
  - Using on Indy Credx because it improves security.
  - Not needed on Indy-VDR: would complicate the code without providing any security benefit.
- Want to do more multi-organizational PR reviews (Mike and Andrew W can work together).
- CI / CD Aries shared libraries
  
  - Prefer GitHub Actions.
    
    - Use GitHub Actions Runner for iOS and Android hosted by the Sovrin Foundation.
    - Can easily migrate to Azure Pipelines or Circle CI if needed.
  - Reduce number of CD pipelines:
    
    - Will build the FFI wrapper, but not other language wrappers
    - We can reduce the number of architectures for mobile. Won't support old devices.
      
      - OSX, Windows, Ubuntu, CentOS, Android 64bit, iOS
        
        - Should we drop mobile? (People can put the proxy in their mediator.)
      - If people want other architectures, they should build it themselves.
  - Plan for indy-vdr
- Do we want a single Rust library that combines all the Indy shared libraries for easy consumption by Aries?
  
  - At least as an example? (Similar to LibVCX?)
  - Would it be needed if people are starting with the Aries framework tiers?
  - We need solutions to assist framework developers in getting onboarded and staying current as Indy and Aries evolves
    
    - But we still want to keep protocol code high in the stack, near business logic and easy to evolve.
- Need to think about where to serialize / decrypt to ensure security and ease-of-use. Configuration options: automatically decrypt attachments
- Update from the Hyperledger Global Forum
  
  - Absa contributed an agency.
  - Lots of challenges in getting started (but other projects are even worse).
  - Indy was a major force at the conference.
  - The Identity Problem is universal, and Indy needs to be part of these integrated solutions. People know they need help.
  - Fabric community is also adapting: IBM releasing more scalable engine, Secure Key contributing Aries compatibility.

## Future Calls

Next call:

- Pick an issue reported against the Sovrin networks, and show how we found the problem in the logs. [Sergey Khoroshavin](https://lf-hyperledger.atlassian.net/wiki/people/5b5607f3e288ee2d9b4b9cb9?ref=confluence)

Future:

- Requirements questions:
  
  - IS-1099: anoncreds.prover\_get\_credentials\_for\_proof\_req should return per-credential timestamp
    
    - Should we allow duplicate credentials from the same issuer?

## Action items

- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC
- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Richard and Sergey will close old pull requests with a descriptive comment.
- Mike wants to review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

We attempted to record the call, but did not succeed.

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
