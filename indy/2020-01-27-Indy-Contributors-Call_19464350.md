1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-01-27 Indy Contributors Call

Created by Richard Esplin, last modified on Jan 27, 2020

## Summary

- Proposed changes to the CI / CD pipeline
- Work on indy-aries-vdri
- Discussing Rich Schemas

## Timezone: Europe afternoon / America morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- [Sergey Minaev](https://lf-hyperledger.atlassian.net/wiki/people/557058:f3eb01c9-c402-4ddf-8eb0-18eff9f16aa2?ref=confluence) (Evernym)
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (Evernym)
- Name (Organization) &lt;email&gt;

## Related Calls and Announcements

- Aries Working Group: Performance Testing LibIndy and ACA-Py
  
  - Presentation: [2020-01-22-B Aries Working Group Call](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/pages/18484534/2020-01-22-B+Aries+Working+Group+Call+US+afternoon) (starting ~65 minutes in)
  - Participate in the follow-up Q&amp;A: [2020-01-27-A Aries Working Group Call](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/pages/18484474/2020-01-29-A+Aries+Working+Group+Call+AMER+morning)
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.

## Release Status and Work Updates

- Indy Node
  
  - January:
    
    - Bugfix-release for edge cases in consensus protocol
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
    - Anoncreds 2.0 (Sovrin Foundation)
- Indy SDK
  
  - January:
    
    - Bugfixes 1.14.2
  - Future
    
    - Deprecating some docs (IS-1425: Getting Started Guides) and wrappers (IS-1423: Python and DotNet)
    - Deprecate  additional wrappers (IS-1424) and LibVCX (IS-1416)
    - GitLab migration alongside Jenkins (Foundation)?
    - Warnings from rust cargo clippy (Mike and Axel), epic: IS-1401
- Indy Catalyst
  
  - [https://github.com/bcgov/indy-catalyst](https://github.com/bcgov/indy-catalyst)
  - Migrating to Hyperledger Aries: plan is to moving to aries-verified-credential-registry
    
    - Needs more documentation
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Need a plan for changes to Indy Node
    
    - Design: [https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2](https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2)
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)
    - BC.gov will implement the existing revocation capability in ACA-Py for use in constrained cases, starting with extracting anoncreds from libindy into indy-aries-anoncreds
  - Comparison of Anoncreds 1.0 and 2.0: [https://docs.google.com/presentation/d/18aqk5q1sqRI\_UhOEuXWAS46-Oltsu\_HNk\_JtKfDVBGc/edit#slide=id.g790163706e\_0\_0](https://docs.google.com/presentation/d/18aqk5q1sqRI_UhOEuXWAS46-Oltsu_HNk_JtKfDVBGc/edit#slide=id.g790163706e_0_0)
- Aries Shared Libraries
  
  - indy-aries-vdr ([Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)) [https://github.com/andrewwhitehead/indy-ledger-client](https://github.com/andrewwhitehead/indy-ledger-client)
    
    - Rust API is almost completed
    - No FFI
    - HTTP proxy
  - Next is indy-aries-anoncreds with anoncreds 1 (ready to add anoncreds 2)

## Main Business

- Proposed changes to the Indy CI / CD pipeline ([Steven Gubler](https://lf-hyperledger.atlassian.net/wiki/people/712020:424ad11d-3863-4e88-9881-3aa563ebaac1?ref=confluence))
  
  - [https://github.com/hyperledger/indy-sdk/pull/2048](https://github.com/hyperledger/indy-sdk/pull/2048)
- Work on Indy-Aries-VDR ([Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)and [Sergey Minaev](https://lf-hyperledger.atlassian.net/wiki/people/557058:f3eb01c9-c402-4ddf-8eb0-18eff9f16aa2?ref=confluence))
- Rich Schema discussions ([Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence) [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence))
  
  - [https://github.com/hyperledger/aries-rfcs/issues/398](https://github.com/hyperledger/aries-rfcs/issues/398)
  - [https://github.com/hyperledger/indy-hipe/pull/151](https://github.com/hyperledger/indy-hipe/pull/151)
  - [https://github.com/hyperledger/indy-hipe/pull/152](https://github.com/hyperledger/indy-hipe/pull/151)

## Future Calls

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464350/19465270.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
