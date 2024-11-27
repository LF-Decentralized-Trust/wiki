1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-11-18 Indy Contributors Call

Created by Richard Esplin, last modified on Nov 20, 2019

## Summary

- Work updates
- Updates on the status of Plenum
- Pull request review process for Indy Node

## Timezone: Europe afternoon / US morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Employer) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Matt Raffel](https://lf-hyperledger.atlassian.net/wiki/people/5d1a954543d1510d3acce0d6?ref=confluence) (Kiva) &lt;mattr@kiva.org&gt;
- [Nemanja Patrnogic](https://lf-hyperledger.atlassian.net/wiki/people/70121:03f65e06-63b9-46ac-8e98-de4f2b613a45?ref=confluence) &lt;nemanja.patrnogic@evernym.com&gt;
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (Evernym) &lt;alexander.shcherbakov@evernym.com&gt;
- [Syed Awais Ahmad](https://lf-hyperledger.atlassian.net/wiki/people/70121:c8f15963-adae-49fb-928d-3ee7a83d0463?ref=confluence) (Prove) &lt;awais.ahmad@proveglobal.com&gt;
- [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence) (Sovrin Foundation) &lt;ken@sovrin.org&gt;

## Related Calls and Announcements

- Aries Workshop/Connectathon December 3-5 in Provo, Utah
  
  - [https://www.meetup.com/Utah-Sovrin-Meetup/events/265714942/](https://www.meetup.com/Utah-Sovrin-Meetup/events/265714942/)
- [ssimeetup.org](http://ssimeetup.org) webinars
  
  - Peer DIDs Nov 21 at 1 PM MST,
  - December 17: Deep dive into the Plenum Ledger
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

- Define the pull request review process for Indy Plenum/Node
  
  - Should define the process, including how we handle exceptions (emergency fixes shouldn't be blocked, but would require notification)
  - What is important in a good review?
    
    - PR checklist items from Evernym team:
      
      - has a link to the issue in Jira
      - fix is correct according to requirements and the according to Plan of Attack (PoA) as shown in the Jira ticket and approved by an architect
      - covered by tests (implementation is TDD style: both unit and integration tests)
      - plan for documentation changes in the same issue, or links to other issues for documentation when it is a large effort (diagram creation)
      - follows good design patterns
      - follows [https://github.com/hyperledger/indy-node/blob/master/docs/source/write-code-guideline.md](https://github.com/hyperledger/indy-node/blob/master/docs/source/write-code-guideline.md)
      - multiple small pull requests are better than a single huge pull request
        
        - PoA helps decomposition of work
        - Documentation can be a separate PR for the same ticket
    - Good review feedback
      
      - Don't merge until the problem is fixed.
      - But can merge if  the suggestions are all a matter-of-taste, or smaller items that can be done in a follow-up pull request.
      - Try to provide specific suggestions on how to respond to the feedback as a list or code-sample.
  - Proposed process for cross-organization PR reviews (by Evernym team):
    
    - All Pull Requests can be reviewed by non-Evernym team members
    - Evernym team members will also do internal review in addition to external one
    - All interested parties are notified when a PR is sent
    - If a person wants to do an external review, he or she puts a comment or tag. This needs to be done in X hours.
    - Once a reviewer put a "want-to-review" tag, he or she need to finish review in Y hours
    - If no one wants to review a PR in X hours, or review is not finished in Y hours, we can do our internal review and merge the PR
    - An external review can be done against closed PRs as well, and Evernym team will process all findings ASAP
    - We may merge a PR with internal review only in case of urgency (critical fixes, release preparation etc.), and with reporting afterwards
  - Items to be defined with the Community:
    
    1. A timeframe to start
       
       1. Would like to start the process in November if possible
    2. A timeframe for external review (X):
       
       1. X=18 hours, Y=24 hours
          
          1. X being 18 hours would mean that the team doesn't usually merge pull requests in the same day they are created, but can be merged at the start of the next business day
          2. Y being 24 hours means that the review will complete the review within a day of saying that he wants to do the review. Some reviews might take longer, if the reviewer asks for additional time to complete the complicated review.
    3. What projects it should affect?
       
       1. Node is preferred for now (disrupt one project at a time)
          
          1. Most fixes at the moment are in Plenum, so can include them as well
       2. We are not proposing SDK as it will be split to Aries in any case.
    4. Who is going to commit to participate in this process?
       
       1. Ken: one review a week, at a minimum
       2. Kiva: could probably start in a month-or-so
    5. How to notify:
       
       1. GitHub list of reviewers
       2. Rocket chat #indy-maintainers can help us highlight priority reviews
  - Improvements to the proposal
  - - Alex's team labels PRs that they think would most benefit from reviews.
    - We can schedule appointments for reviewing specific PRs together.

## Future Calls

- Migration of Indy-SDK to Aries-Core
- Requirements question: IS-1099, should we allow duplicate credentials from the same issuer?
- Non-secrets in the Indy Wallet
  
  - Cam is working on pluggable crypto. The wallet shouldn't decide what encryption you should be using.
  - Use cases where we would want to move keys between wallets
    
    - Moving the link secret / credential data from one device to another (synchronized storage).
    - Debug use cases
    - Richard's hit other uses cases that were better solved with DID Doc,  pre-signing, signing API.
  - Work-around with the web-crypto API

## Action items

- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC
- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Richard and Sergey will close old pull requests with a descriptive comment.
- Mike wants to review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

[dummyfile.txt](#)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464325/19465197.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
