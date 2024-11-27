1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-06-17 Indy Maintainers Call

Created by Richard Esplin, last modified on Jun 17, 2019

## Summary

- Release planning for next three months
- Restructuring Indy calls now that we have Aries
  
  - Combine some of the calls?
  - Focused on getting work done: work streams and release planning
- Plans for improving documentation
  
  - Focus for new developer experience should be Aries

## Timezone: US afternoon and Asia morning

## [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

NameOrganizationEmailRichard EsplinEvernymrichard.esplin@evernym.com

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

Cloud Compass Computing/BC Govswcurran@cloudcompass.ca

Mike

Sam

Michael

## Announcements

## Agenda

SubjectWhoNotesSummary of Prior callEverybody  
Calls focused on getting work done: Indy SDK WG best practicesRichard

Documentation: (a conversation for the US / Europe group, already had it with US / Asia)

- Where to document changes? HIPEs/Repo Docs/Jira Tickets
- PR's should link back to Jira tickets
- Rocket Chat questions should be pushed to Stack Overflow

## Release Status

- Indy Node
  
  - June: 1.9.0 Pluggable Request Handlers
    
    - Testing is at risk for June
  - July: 1.9.1
    
    - Bug fix release
  - August: 1.9.2
    
    - Bug fix release
  - September: 1.10.0
    
    - PBFT view change
- Indy SDK
  
  - June: Indy SDK 1.10.0
    
    - Flexible Credential Attribute Tagging ([BC.gov](http://BC.gov))
    - Bugfixes
  - July:
    
    - GitLab migration alongside Jenkins (Foundation)?
      
      - Linux should be ready, maybe Windows.
      - Need a plan for mobile devices.
      - Could run it right after the release.
  - August
    
    - Platform Updates (Evernym?)
    - Aries / Indy split (Evernym will help with architecture)
    - Anoncreds 2.0 (Sovrin Foundation, [BC.gov?](http://BC.gov))
- Ursa
  
  - June: 0.1.2
    
    - Exposing the existing functionality over a C-API for the Aroha team.
  - July: 0.2.0
    
    - Refactor internal plumbing for anoncreds 2.0, shouldn't impact external interfaces
    - Multi-signature BLS instead of aggregated signature
- Aries
  
  - Initial code migration

## Work Updates

- Documentation improvements: Michael B and Stephen C
- SDK 2.0 architecture (Sergey)
- Payment decorator (Sergey)
- GitLab migration (Mike and Steve G)
- Warnings from rust cargo clippy (Mike)
  
  - IS-1270 through IS-1274
  - Will look at again in July
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
    
    - First draft is latex document in Ursa repo. Will be published as PDF and HTML.
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)

## Notes

- Status of Indy / Aries split:
  
  - Should discuss in an Aries WG call, but not this week. Evernym is working on a proposal to start the discussion, this shouldn't stop others from putting together their own proposals.
  - Sam added README / Migration Notice to Aries repos.
- Aries should be the starting point for most new developers. Need to focus on documentation for new developers. Stephen getting started.
- Daniel has been adding notes to Indy HIPE informing people when they are superseded by Aries. More of this needs to be done.
- Concerns about losing the branding work we have done with Indy. How can we transfer this branding goodness to Aries?
  
  - We can emphasize that Aries was incubated in Indy, but we also need to be welcoming to the non-Indy people to achieve the Aries vision.
- What is the role of this call post-Aries?
  
  - Merge this call with the Indy SDK working group?
    
    - Cancel the Wednesday call and just use the Monday slot?
    - Do we need an afternoon slot? How interested are the AU / NZ people in Indy vs Aries?
  - Give room for an Aries Maintainers call?
- Documentation questions:
  
  - Need to discuss with NA / EU
  - Benefits of Stack Overflow
  - Need to review and prune out-of-date documentation
    
    - Alice / Faber treatment of pairwise DIDs is a key pain point
    - Start with the "new developer on Aries" path, and then decide what developers need to know about Indy?
  - Michael is working on Indy Agent walkthrough using C#
  - Would love to see a point and click demo walkthrough
    
    - Need to have a high enough level for new developers
- Note: Richard hates Confluence tables in meeting agendas, as they don't copy / paste.

## Next Week

## Action items

## Call Recording

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
