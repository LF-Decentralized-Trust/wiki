1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-07-15 Indy Maintainers Call

Created by Richard Esplin, last modified by Nathan George on Jul 16, 2019

## Summary

- Discussed release status of various dependent components
- GitLab migration still in progress
- What to do about IndySDK→AriesSDK+IndyResolver migration
  
  - C Callable Wrappers and Rust
  - Anoncreds 2.0
  - Schema 2.0
- Documentation updates
  
  - Call to contribute or deprecate out of date documentation
- Discussion on Indy WG call becoming an Identity WG Implementers call

## Timezone: US afternoon and Asia morning

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence) (Sovrin Foundation) &lt;nage@sovrin.org&gt;
- [Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)  (Mattr) &lt;kyle.denhartog@mattr.global&gt;
- [Tobias Looker](https://lf-hyperledger.atlassian.net/wiki/people/712020:6b4b9e75-c537-4af4-b498-bd8e8b96dc37?ref=confluence)  (Mattr) &lt;tobias.looker@mattr.global&gt;
- [Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)  (Sovrin Foundation) &lt;adam@sovrin.org&gt;
- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Sovrin Foundation) &lt;sam@sovrin.org&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass/BC Gov) &lt;swcurran@cloudcompass.ca&gt;
- [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence) (Sovrin Foundation) &lt;ken@sovrin.org&gt;
- [Camilo Parra](https://lf-hyperledger.atlassian.net/wiki/people/5ade0ac99fcb1f22f34ccae2?ref=confluence) (Kiva) &lt;camilop@kiva.org&gt;
- [Alan Krassowski](https://lf-hyperledger.atlassian.net/wiki/people/712020:a23c820f-82e4-44ea-bc08-98f77b9e38ca?ref=confluence) (Kiva) &lt;alank@kiva.org&gt;
- Name (organization) &lt;email&gt;

Announcements

## Summary of Prior Call

## Release Status

- Indy Node
  
  - Early July: 1.9.0 Pluggable Request Handlers
    
    - CI / CD problems left us broken for days. Release is likely to be next week.
  - July: 1.9.1
    
    - Bug fix release
    - Still trying for late July
  - August: 1.9.2
    
    - Bug fix release
  - September: 1.10.0
    
    - PBFT view change
- Indy SDK
  
  - Early July: Indy SDK 1.10.0
    
    - Flexible Credential Attribute Tagging ([BC.gov](http://BC.gov))
    - Bugfixes
    - CI / CD problems left us broken for days. Release is likely to be late this week.
  - Late July:
    
    - Usability improvements to Indy CLI and Payments (Sovrin Foundation and Evernym)
      
      - Requires concurrent release with libsovtoken
    - GitLab migration alongside Jenkins (Foundation)?
      
      - Linux should be ready, maybe Windows.
      - Need a plan for mobile devices.
      - Could run it right after the release.
    - LibVCX without agency (Evernym)
  - August
    
    - Platform Updates (Evernym?)
    - Aries / Indy split
    - Anoncreds 2.0 (Sovrin Foundation, [BC.gov?](http://BC.gov))
- Ursa
  
  - June: 0.1.2
    
    - Exposing the existing functionality over a C-API for the Aroha team.
    - Not tagged in GitHub
  - July: 0.2.0
    
    - Refactor internal plumbing for anoncreds 2.0, shouldn't impact external interfaces
    - Multi-signature BLS instead of aggregated signature
- Aries
  
  - Agent from Indy Catalyst migrated to aries-cloudagent-python (BC.gov)
  - Initial code migration from SDK repositories
- Indy Catalyst
  
  - Migration from BC repos this week.
- Indy WG call - proposal to rebrand to Identity WG or Sovrin call to cover cross-project concerns (keep it every week and report on various project WG status and talk about cross-project issues and end-to-end integrations).

## Work Updates

- Documentation improvements: Michael B and Stephen C
  
  - Start with new developer path through Aries.
    
    - First draft in aries-cloudagent-python [from 0 to coding in Aries](https://github.com/bcgov/aries-cloudagent-python/blob/master/docs/GettingStartedAriesDev/README.md)
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Michael is working on Indy Agent walkthrough using C#
- SDK 2.0 architecture / Indy-Aries split (Sergey)
  
  - [http://jira.hyperledger.org/browse/IS-1285](http://jira.hyperledger.org/browse/IS-1285)
- GitLab migration (Mike and Steve G)
  
  - Evaluated Circle CI, but it doesn't support Windows
  - Blocking various platform updates and CI / CD improvements
- Warnings from rust cargo clippy (Mike)
  
  - IS-1270 through IS-1274
  - Will look at again in July
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - First draft is latex document in Ursa repo. Will be published as PDF and HTML.
    
    - [https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2](https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2)
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)

## Other Business

## Next Week

## Action items

## Call Recording

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
