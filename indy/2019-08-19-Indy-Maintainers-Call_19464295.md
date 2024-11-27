1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-08-19 Indy Maintainers Call

Created by Richard Esplin, last modified on Aug 19, 2019

## Summary

- Release updates
- Rich schemas HIPE
- Proposal to improve performance of the Indy SDK CI test pipeline

## Timezone: US afternoon and Asia morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Evernym) &lt;richard.esplin@evernym.com&gt;

Announcements

## Summary of Prior Call

## Release Status

- Indy Node
  
  - August: 1.9.2
    
    - Bug fix release
  - September: 1.10.0
    
    - PBFT view change
- Indy SDK
  
  - August:
    
    - Finish Authors vs Endorsers
    - Finish proof of possession of payment address
    - Platform Updates: Ubuntu 18.04
  - Future
    
    - Platfrom Updates: MacOS, CentOS
    - GitLab migration alongside Jenkins (Foundation)?
    - Aries / Indy split
    - Anoncreds 2.0 (Sovrin Foundation, [BC.gov?](http://BC.gov))
- Ursa
  
  - Working on release of 0.2.0
    
    - ZKP  / ZKLang improvements
    - Debian packages
    - Refactor internal plumbing for anoncreds 2.0, shouldn't impact external interfaces
    - Refactor multi-signature BLS in addition to aggregated signature
- Aries
  
  - Agent from Indy Catalyst migrated to aries-cloudagent-python (BC.gov)
  - Initial code migration from Indy SDK repositories
- Indy Catalyst
  
  - Migrated

## Work Updates

- Documentation improvements: Michael B and Stephen C
  
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Michael is working on Indy Agent walkthrough using C#
  - Finishing work on ReadTheDocs (2 more weeks?)
- SDK 2.0 architecture / Indy-Aries split (Sergey)
- GitLab migration (Mike and Steve G)
  
  - Demos in the Identity Implementers WG calls
  - Issues with Jenkins machines because Rust builds run out of memory—workaround increased build time but is a temporary solution
- Advanced Schemas and W3C creds (Ken)
  
  - Can successfully write and retrieve the Context object from the node code. Will track through all layers up to Aries.
    
    - [https://github.com/ken-ebert/indy-node/commits/master](https://github.com/ken-ebert/indy-node/commits/master)
  - 5 additional objects need to be added.
- Warnings from rust cargo clippy (Mike and Axel)
  
  - IS-1270 through IS-1274
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - First draft is latex document in Ursa repo. Will be published as PDF and HTML.
    
    - [https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2](https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2)
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)

## Other Business

- Accepting HIPE PR #138, Issue #144
- Improving the performance of the Indy SDK CI pipeline: 
  
  Error rendering macro 'jira' : null
- Close PR [https://github.com/hyperledger/indy-sdk/pull/1048](https://github.com/hyperledger/indy-sdk/pull/1048) as something that will be replaced by the advanced schema work?
  
  - Ken will review the work to see what we can learn.

## Future Calls

- Proposal for Fully Qualified DIDs
  
  - [IS-451](https://jira.hyperledger.org/browse/IS-451)
  - [IS-1358](http://I)
  - Breaking change in order to go faster and avoid duplicated code?
- New pack / unpack requires disclosure of recipient
  
  - Cannot hide the receiver of the message like we could with msg\_pack
  - Allows having multiple recipients of the same message
  - Should list the drawback in the Aries-RFC? Is there an alternative way that preserves the capability to selectively disclose the recipient?
- Ursa and AMCL
- Architecture questions for Indy SDK:
  
  ![](plugins/servlet/confluence/placeholder/unknown-macro)
- PostgreSQL wallet to graduate from "experimental" status?
- Maintainership requirements for Indy Node and Indy SDK
- How to handle old pull requests that failed DCO Checks? Close?
- How to handle pull requests for IOS / Swift wrappers? Close and encourage the move to Aries?
- How to handle pull requests for LibVCX? Deprecate?
- HIPE pull requests: [https://github.com/hyperledger/indy-hipe/pulls](https://github.com/hyperledger/indy-hipe/pulls)

## Action items

- Nathan (Daniel)
  
  - Set up alternate meeting hosts to record
- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC

## Call Recording

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
