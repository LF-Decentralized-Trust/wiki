1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-07-01 Indy Maintainers Call

Created by Richard Esplin, last modified on Jul 01, 2019

## Summary

- Update on June releases.
- Planned releases for July and August.
- Discussed call mechanics.
- Discussed documentation improvements.
- Discussed improvements to how transactions are endorsed.

## Timezone: US morning and Europe afternoon

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (organization) &lt;email&gt;
- Sam Curren (Sovrin Foundation) &lt;sam@sovrin.org&gt;
- Richard Esplin (Evernym) &lt;richard.esplin@evernym.com&gt;
- Samuel Smith (Sovrin Foundation) [sam@samuelsmith.org](mailto:sam@samuelsmith.org)
- Tomislav Markovski (Streetcred) [tomislav@streetcred.id](mailto:tomislav@streetcred.id)

Announcements

- Indy SDK call being cancelled

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

## Work Updates

- Documentation improvements: Michael B and Stephen C
  
  - Start with new developer path through Aries.
    
    - First draft in aries-cloudagent-python [from 0 to coding in Aries](https://github.com/bcgov/aries-cloudagent-python/blob/master/docs/GettingStartedAriesDev/README.md)
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Michael is working on Indy Agent walkthrough using C#
- SDK 2.0 architecture / Indy-Aries split (Sergey)
  
  - [http://jira.hyperledger.org/browse/IS-1285](http://jira.hyperledger.org/browse/IS-1285)
- Payment decorator (Sergey)
  
  - Tomislav has some feedback that should be incorporated
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

- Call mechanics:
  
  - Merge this call with the Indy SDK working group calls
  - Timing: move afternoon call later to pick up more of Asia
    
    - No change at this point
  - Frequency of the call: move to every week alternating timezones
    
    - No change at this point
  - Will begin recording the call
- Documentation improvements: (a conversation for the US / Europe group, already had it with US / Asia)
  
  - Where to document changes? HIPEs/Repo Docs/Jira Tickets
  - PR's should link back to Jira tickets / GitHub issues
    
    - Goal is for each PR to link to somewhere that includes additional context / underlying motivation
    - Exclude RFC and HIPE repos
    - Need to revisit Hyperledger's policy on GitHub issues
  - Rocket Chat questions should be pushed to Stack Overflow
- Recording transaction endorsers and INDY-1999
  
  - Error rendering macro 'jira' : null

## Next Week

## Action items

## Call Recording

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
