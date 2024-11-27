1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-12-02 Indy Contributors Call

Created by Richard Esplin, last modified on Dec 05, 2019

## Summary

- Work updates
- Update on LibVCX support for Aries

## Timezone: Europe afternoon / US morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Employer) &lt;email&gt;
- [Sergey Minaev](https://lf-hyperledger.atlassian.net/wiki/people/557058:f3eb01c9-c402-4ddf-8eb0-18eff9f16aa2?ref=confluence) (Evernym) sergey.minaev@evernym.com

## Related Calls and Announcements

- Aries Workshop/Connectathon December 3-5 in Provo, Utah
  
  - [https://www.meetup.com/Utah-Sovrin-Meetup/events/265714942/](https://www.meetup.com/Utah-Sovrin-Meetup/events/265714942/)
- [ssimeetup.org](http://ssimeetup.org) webinars
  
  - Peer DIDs Nov 21 at 1 PM MST,
  - December 17: Deep dive into the Plenum Ledger
- Hyperledger edX course - [Introduction to Hyperledger Sovereign Identity Blockchain Solutions: Indy, Aries &amp; Ursa](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)
- Previous Indy Contributors call
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.

## Release Status and Work Updates

- Indy Node
  
  - November: 1.12.1
    
    - Bug fixes
    - Ubuntu 18.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
    - Replacing Indy Crypto with Ursa (Kiva)
    - Additional rich schemas objects: schema object (Sovrin Foundation)
      
      - Just posted Indy HIPE
        
        [https://github.com/hyperledger/indy-hipe/pull/149](https://github.com/hyperledger/indy-hipe/pull/149)
      - Aries RFC
        
        [https://github.com/hyperledger/aries-rfcs/pull/281](https://github.com/hyperledger/aries-rfcs/pull/281)
      - PR of schema object in progress for November
      - Making progress on other RFCs for objects and one that shows how all the objects fit together.
  - December / January: 1.23.0
    
    - Remove replicas (Aardvark BFT) ?
    - Rich Schema progress: encoding object
  - Future
    
    - Anoncreds 2.0 (Sovrin Foundation)
- Indy SDK
  
  - November 1.13.0
    
    - Issue reported by BC.gov:
      
      [https://github.com/hyperledger/indy-sdk/pull/1893](https://github.com/hyperledger/indy-sdk/pull/1893)
    - Need to include a manual release of iOS artifacts
    - LibVCX support for some Aries protocols
    - Deprecating some docs (IS-1425: Getting Started Guides) and wrappers (IS-1423: Python and DotNet)
    - Bug fixes
  - Future
    
    - Deprecate  additional wrappers (IS-1424) and LibVCX (IS-1416)
    - GitLab migration alongside Jenkins (Foundation)?
    - Warnings from rust cargo clippy (Mike and Axel), epic: IS-1401
- Indy Catalyst
  
  - Production deployment testing: volume loads.
    
    - Trying to identify performance bottlenecks. Currently think it's calls to the database.
    - Performance problems is preventing going to production.
  - Not yet migrated to Hyperledger. Needs more documentation.
- Documentation improvements: Michael B and Stephen C
  
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Cloud Compass is building the Linux Foundation EdX courses for Indy and Aries
    
    - Overview launch date: November 21st
    - More content will follow
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)
    - BC.gov will implement the existing revocation capability in ACA-Py for use in constrained cases
      
      - Looking to build against Anoncreds 2.0 as soon as it is available.
      - Unable to contribute to the Anoncreds 2.0 revocation capability at this time - no resources for that work.

## Main Business

- Update on LibVCX support for Aries
  
  - [Evernym Sprint Demos](Evernym-Sprint-Demos_19464929.html) EV 19.22 and 19.23 - testing libVCX against ACA-Py and Aries Tests Suite
  - Available in master, will be part of 1.13.0 stable
- Aardvark discussions update

## Future Calls

- Requirements question: IS-1099, should we allow duplicate credentials from the same issuer?
- Non-secrets in the Indy Wallet
  
  - Cam is working on pluggable crypto. The wallet shouldn't decide what encryption you should be using.
  - Use cases where we would want to move keys between wallets
    
    - Moving the link secret / credential data from one device to another (synchronized storage).
    - Debug use cases
    - Richard's hit other uses cases that were better solved with DID Doc,  pre-signing, signing API.
  - Work-around with the web-crypto API
- Migration of Indy-SDK to Aries-Core
- Indy performance analysis ([BC.gov](http://BC.gov))

## Action items

- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC
- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Richard and Sergey will close old pull requests with a descriptive comment.
- Mike wants to review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464331/19465209.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
