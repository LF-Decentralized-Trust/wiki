1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-01-13 Indy Contributors Call

Created by Richard Esplin, last modified on Jan 13, 2020

## Summary

- Work updates
- Results from performance testing LibIndy
- INDY-2305 and outbound IP address

## Timezone: Europe afternoon / America morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) &lt;[alexander.shcherbakov@evernym.com](mailto:alexander.shcherbakov@evernym.com)&gt;
- [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence) (Sovrin Foundation) &lt;ken@sovrin.org&gt;
- [Camilo Parra](https://lf-hyperledger.atlassian.net/wiki/people/5ade0ac99fcb1f22f34ccae2?ref=confluence) (Kiva) &lt;camilop@kiva.org&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Sovrin Foundation) &lt;daniel.bluhm@sovrin.org&gt;

## Related Calls and Announcements

- Previous Indy Contributors call was cancelled
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.
- Recording and slides are posted for the [SSI Meetup webinar on Indy and Plenum](https://ssimeetup.org/hyperledger-indy-public-blockchain-node-alexander-shcherbakov-webinar-43/).

## Release Status and Work Updates

- Indy Node
  
  - December: 1.12.1
    
    - Improvements to the TAA behavior
    - Roll-out to Sovrin Network delayed: Post-release identified corner cases related to View Change, and weirdness seen during Builder Net upgrade. Investigation is ongoing.
  - January:
    
    - Additional rich schemas objects: schema object (Sovrin Foundation)
      
      - Just posted Indy HIPE
        
        [https://github.com/hyperledger/indy-hipe/pull/149](https://github.com/hyperledger/indy-hipe/pull/149)
      - Aries RFC
        
        [https://github.com/hyperledger/aries-rfcs/pull/281](https://github.com/hyperledger/aries-rfcs/pull/281)
      - PR of schema object in progress for December
      - Making progress on other RFCs for objects and one that shows how all the objects fit together.
      - Next: encoding object, then mapping object
    - Replacing Indy Crypto with Ursa (Kiva)
      
      - Debian packages for Ursa-0.3.0 are uploaded to [repo.sovrin.org](http://repo.sovrin.org)
  - Future
    
    - Ubuntu 18.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
    - Remove replicas (Aardvark BFT) ?
    - Anoncreds 2.0 (Sovrin Foundation)
- Indy SDK
  
  - December: 1.14.0 / 1.14.1
    
    - LibVCX support for Aries Interop v1
    - Improvements to the TAA behavior
  - January:
    
    - Bugfixes
  - Future
    
    - Deprecating some docs (IS-1425: Getting Started Guides) and wrappers (IS-1423: Python and DotNet)
    - Deprecate  additional wrappers (IS-1424) and LibVCX (IS-1416)
    - GitLab migration alongside Jenkins (Foundation)?
    - Warnings from rust cargo clippy (Mike and Axel), epic: IS-1401
- Indy Catalyst
  
  - Plan is to moving to aries-verified-credential-registry
  - [https://github.com/bcgov/indy-catalyst](https://github.com/bcgov/indy-catalyst)
  - Production deployment testing: volume loads.
    
    - Happy with performance now.
  - Not yet migrated to Hyperledger. Needs more documentation.
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)
    - BC.gov will implement the existing revocation capability in ACA-Py for use in constrained cases
      
      - Looking to build against Anoncreds 2.0 as soon as it is available.
      - Unable to contribute to the Anoncreds 2.0 revocation capability at this time - no resources for that work.
- Aries Shared Libraries
  
  - indy-aries-vdr ([Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence))

## Main Business

- Kiva update:
  
  - test networks is running Indy Node 1.8
    
    - Seeing some compatibility issues
  - created 5 million test wallets with citizen data
- Non-secrets in the Indy Wallet
  
  - Cam is working on pluggable crypto. The wallet shouldn't decide what encryption you should be using.
    
    - [https://github.com/mac-arrap/aries-rfcs/tree/master/concepts/0276-key-management-service](https://github.com/mac-arrap/aries-rfcs/tree/master/concepts/0276-key-management-service)
    - Indy wallet currently forces encryption to avoid mistakes in the ecosystem, specifically around searching
  - Best practices with Indy today
    
    - Indy wallet wasn't designed for general storage, but people are using it because there aren't alternatives.
  - Shared goals for Aries
    
    - Aries-KMS is key specific
      
      - link secret should be treated the same as a key
    - Separate storage for connections, credentials, and protocol state
    - Need an additional storage for larger items
- Use cases where we would want to move keys between wallets
- - We receive requests for moving the link secret / credential data from one device to another (synchronized storage)
    
    - Concerns with private keys ever leaving the wallet. If it can be done for any use case, how can it be protected against malicious use cases?
    - But wallet portability requires migration: export from one wallet, and import into a different wallet
      
      - migration between vendors
      - some types of upgrades
    - Preferred approach is to create a protocol for migrating credentials between wallets: move data and rotate to new private keys.
      
      - How do we handle the link secret?
  - Related use cases
    
    - backup and restore: storage layer backup
    - Debug use cases: unencrypted wallet plugin?
    - Delegation and guardianship: DID Doc
    - Enterprise use case:  pre-signing, signing API for arbitrary data.
  - Work-around with the web-crypto API

## Future Calls

- Results from performance testing LibIndy ([BC.gov](http://BC.gov))
- Requirements questions:
  
  - INDY-2305: Add IP address range for outbound TCP connections from validator nodes
    
    - Changes the way nodes are represented in the Pool Ledger
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

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464339/19464348.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
