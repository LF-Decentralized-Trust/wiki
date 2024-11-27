1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-12-09 Indy Contributors Call

Created by Richard Esplin, last modified on Dec 10, 2019

## Summary

- Work updates
- Update from the Aries Connect-a-thon
- Plans for migration of LibIndy to Aries

## Timezone: Americas afternoon / APAC morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Employer) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass/BC Gov) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- Note the updated calendar invitation on the Hyperledger Calendar
- Call schedule
  
  - December 16 (US+EMEA): normal
  - December 23: cancelled
  - December 30: cancelled
  - January 6 (US+APAC): cancel
  - January 13 (US+EMEA): normal
- [ssimeetup.org](http://ssimeetup.org) webinars
  
  - December 17: Deep dive into the Plenum Ledger
- Hyperledger edX course - [Introduction to Hyperledger Sovereign Identity Blockchain Solutions: Indy, Aries &amp; Ursa](https://www.edx.org/course/identity-in-hyperledger-aries-indy-and-ursa)
- Previous Indy Contributors call
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.

## Release Status and Work Updates

- Indy Node
  
  - November: 1.12.1
    
    - Bug fixes
  - December / January: 1.23.0
    
    - Additional rich schemas objects: schema object (Sovrin Foundation)
      
      - Just posted Indy HIPE
        
        [https://github.com/hyperledger/indy-hipe/pull/149](https://github.com/hyperledger/indy-hipe/pull/149)
      - Aries RFC
        
        [https://github.com/hyperledger/aries-rfcs/pull/281](https://github.com/hyperledger/aries-rfcs/pull/281)
      - PR of schema object in progress for November
      - Making progress on other RFCs for objects and one that shows how all the objects fit together.
      - Next: encoding object
  - Future
    
    - Ubuntu 18.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
    - Replacing Indy Crypto with Ursa (Kiva)
    - Remove replicas (Aardvark BFT) ?
    - Anoncreds 2.0 (Sovrin Foundation)
- Indy SDK
  
  - November 1.13.0
    
    - Issue reported by BC.gov:
      
      [https://github.com/hyperledger/indy-sdk/pull/1893](https://github.com/hyperledger/indy-sdk/pull/1893)
    - Need to include a manual release of iOS artifacts
    - LibVCX support for some Aries protocols
    - Bug fixes
  - Future
    
    - Deprecating some docs (IS-1425: Getting Started Guides) and wrappers (IS-1423: Python and DotNet)
    - Deprecate  additional wrappers (IS-1424) and LibVCX (IS-1416)
    - GitLab migration alongside Jenkins (Foundation)?
    - Warnings from rust cargo clippy (Mike and Axel), epic: IS-1401
- Indy Catalyst
  
  - Production deployment testing: volume loads.
    
    - Happy with performance now.
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

- Migrating LibIndy to Aries
  
  [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1sGm1_5OWZ_OMh4qzc8R_Pgb0p6lDHsr-qeuT4K6py4o/edit)
  
  - Indy Resolver becomes Indy-Aries-VDRI
    
    - Can wait to follow the DID-resolution spec, because the spec doesn't have enough detail today.
  - Indy Anoncreds becomes Aries-Shared-Creds-Anoncreds or Indy-Aries-Anoncreds
    
    - We prefer keeping it as a separate repo in Indy until another ledger shows interest.
  - Indy Wallet becomes Aries-Shared-KMS
    
    - Includes plugin interface
    - Aries-Shared-KMS-PostgreSQL
    - Aries-Shared-KMS-SQLite
- Other themes from the Aries Connect-a-thon
- Evernym can assist with:
  
  - Consensus
  - Revocation
  - Rich Schemas
  - DID Doc

## Future Calls

- January 13: Indy performance analysis ([BC.gov](http://BC.gov))
- Requirements question: IS-1099, should we allow duplicate credentials from the same issuer?
- Non-secrets in the Indy Wallet
  
  - Cam is working on pluggable crypto. The wallet shouldn't decide what encryption you should be using.
  - Use cases where we would want to move keys between wallets
    
    - Moving the link secret / credential data from one device to another (synchronized storage).
    - Debug use cases
    - Richard's hit other uses cases that were better solved with DID Doc,  pre-signing, signing API.
  - Work-around with the web-crypto API
- Migration of Indy-SDK to Aries-Core

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464333/19464337.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
