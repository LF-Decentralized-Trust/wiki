1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-07-29 Indy Maintainers Call

Created by Richard Esplin, last modified on Aug 27, 2019

## Summary

- Work and release updates
- Improvements to Indy Node including PBFT view change
- Schedule for future calls

## Timezone: Europe afternoon and US morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym)
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (SF) &lt;daniel.bluhm@sovrin.org&gt;

Announcements

## Summary of Prior Call

## Release Status

- Indy Node
  
  - Late July: 1.9.1
    
    - Bug fix release
      
      - Authors vs Endorsers (INDY-1999)
      - Public write access (INDY-2171)
  - August: 1.9.2
    
    - Bug fix release
  - September: 1.10.0
    
    - PBFT view change
- Indy SDK
  
  - Late July: 1.11.0
    
    - Usability improvements to Indy CLI and Payments (Sovrin Foundation and Evernym)
      
      - Requires concurrent release with libsovtoken
    - LibVCX without agency (Evernym)
    - Proof of possession of payment address – UNLIKELY
  - August:
    
    - Finish Authors vs Endorsers
    - Finish proof of possession of payment address
    - GitLab migration alongside Jenkins (Foundation)?
    - Platform Updates (Evernym?)
  - Future
    
    - Aries / Indy split
    - Anoncreds 2.0 (Sovrin Foundation, [BC.gov?](http://BC.gov))
- Ursa
  
  - July: 0.2.0
    
    - Refactor internal plumbing for anoncreds 2.0, shouldn't impact external interfaces
    - Multi-signature BLS instead of aggregated signature
- Aries
  
  - Agent from Indy Catalyst migrated to aries-cloudagent-python (BC.gov)
  - Initial code migration from Indy SDK repositories
- Indy Catalyst
  
  - Not migrated yet

## Work Updates

- Documentation improvements: Michael B and Stephen C
  
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Michael is working on Indy Agent walkthrough using C#
- SDK 2.0 architecture / Indy-Aries split (Sergey)
  
  - [Aries Working Group 2019-07-31-A](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/pages/18481614/2019-07-31-A+Aries+Working+Group+Call+US+morning)
  - [http://jira.hyperledger.org/browse/IS-1285](http://jira.hyperledger.org/browse/IS-1285)
- GitLab migration (Mike and Steve G)
  
  - Demo in the Identity Implementers call?
  - Issues with Jenkins machines because Rust builds run out of memory—workaround increased build time but is a temporary solution
- Advanced Schemas and W3C creds (Ken)
  
  - Can successfully write and retrieve the Context object from the node code. Will track through all layers up to Aries.
    
    - [https://github.com/ken-ebert/indy-node/commits/master](https://github.com/ken-ebert/indy-node/commits/master)
    - Once unit tests work, will commit back either to Master or in a Branch.
  - 5 additional objects need to be added.
- Warnings from rust cargo clippy (Mike)
  
  - IS-1270 through IS-1274
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - First draft is latex document in Ursa repo. Will be published as PDF and HTML.
    
    - [https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2](https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2)
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)

## Other Business

- Proposed improvements to Indy Node architecture and PBFT view change
  
  - [https://github.com/hyperledger/indy-plenum/blob/master/design/plenum\_2\_0\_architecture\_class.png](https://github.com/hyperledger/indy-plenum/blob/master/design/plenum_2_0_architecture_class.png)
  - [https://github.com/hyperledger/indy-plenum/blob/master/design/plenum\_2\_0\_architecture\_object.png](https://github.com/hyperledger/indy-plenum/blob/master/design/plenum_2_0_architecture_object.png)
  - [https://github.com/hyperledger/indy-plenum/blob/master/design/plenum\_2\_0\_communication.png](https://github.com/hyperledger/indy-plenum/blob/master/design/plenum_2_0_communication.png)
  - Relationship to long term "Ledger 2.0"
    
    - multi-process
    - ZMQ client communication vs DIDComm over HTTP
    - Modular architecture: "Micro-services" / actors
- 4 levels of tests in Indy Node
  
  - Unit
  - Integration
  - System
  - Simulation
- Schedule for future calls
  
  - Meeting every two weeks in this timezone

## Next Week

- Maintainership requirements for Indy Node and Indy SDK
- Ursa and AMCL
- New pack / unpack requires disclosure of recipient

## Action items

- Nathan (Richard)
  
  - Fix Hyperledger calendar invitation
- Nathan (Daniel)
  
  - Set up alternate meeting hosts to record
- Mike (Ken)
  
  - Address memory issues with current CI / CD pipelines
- Axel (Artem)
  
  - Dependency update of Backtrace slowed down build pipelines for Windows

## Call Recording

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
