1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-10-21 Indy Contributors Call

Created by Richard Esplin, last modified on Oct 26, 2019

## Summary

- The future of consensus in Indy Node (moving from RBFT to Aardvark?)
- Indy / Aries split
- Pull request review process for Indy Node

## Timezone: US morning and Europe afternoon

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Alexander Shcherbakov (Evernym) &lt;alexander.shcherbakov@evernym.com&gt;
- Nemanja Patrnogic (Evernym) &lt;nemanja.patrnogic@evernym.com&gt;

## Related Calls and Announcements

- Previous Indy Contributors call
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.

## Release Status

- Indy Node
  
  - October: 1.11.0
    
    - PBFT view change
  - November: 1.11.1
    
    - Bug fixes
- Indy SDK
  
  - October: 1.12.1
    
    - Bug fixes
  - November
    
    - ?
  - Future
    
    - GitLab migration alongside Jenkins (Foundation)?
    - Aries / Indy split: next step is aries-core-wallet
    - Anoncreds 2.0 (Sovrin Foundation, BC.gov?)
- Indy Catalyst
  
  - Production deployment testing: volume loads.
  - Won't go live in production at BC.gov until October.
  - Not yet migrated to Hyperledger. Needs more documentation.

## Work Updates

- Documentation improvements: Michael B and Stephen C
  
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Michael is working on Indy Agent walkthrough using C#
  - Finishing work on ReadTheDocs (2 more weeks?)
  - Cloud Compass is building the Linux Foundation EdX courses for Indy and Aries
- SDK 2.0 architecture / Indy-Aries split (Sergey)
  
  - Evernym: A PR with an example how the wallet can be separated; this is internal work
  - Kiva is working on a Futures implementation of threading (instead of call-backs)
- CI / CD: GitLab migration (Mike and Steve G)
- Advanced Schemas and W3C creds (Ken)
- Warnings from rust cargo clippy (Mike and Axel)
  
  - Epic: IS-1410
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)
- Replacing Indy-Crypto with Ursa in Indy Node (Mike and Cam)

## Main Business

- The future of consensus in Indy Node: proposal for moving from RBFT to Aardvark
  
  - Error rendering macro 'jira' : null
  - **Kiwa is OK**
  - **No other comments or concerns**
- Update on Indy / Aries split
  
  - Watch last Aries call recording
  - Error rendering macro 'jira' : null
    
    \- create repos for Aries
  - Error rendering macro 'jira' : null
    
    \- move Indy wallet into Aries
- Define the pull request review process for Indy Plenum/Node
  
  - Should define the process, including how we handle exceptions (emergency fixes shouldn't be blocked, but would require notification)
  - What is important in a good review?
    
    - Items from Evernym team:
      
      - covered by tests
      - has a link to the issue in Jira
      - fixed according to PoA
      - follows [https://github.com/hyperledger/indy-node/blob/master/docs/source/write-code-guideline.md](https://github.com/hyperledger/indy-node/blob/master/docs/source/write-code-guideline.md)
  - Proposed Process (by Evernym team):
    
    - All Pull Requests can be reviewed by non-Evernym team members
    - Evernym team members will also do internal review in addition to external one
    - All interested parties are notified when a PR is sent
    - If a person wants to do an external review, he or she puts a comment or tag. This needs to be done in X hours.
    - Once a reviewer put a "want-to-review" tag, he or she need to finish review in Y hours
    - If no one wants to review a PR in X hours, or review is not finished in Y hours, we can do our internal review and merge the PR
    - An external review can be done against closed PRs as well, and Evernym team will process all findings ASAP
    - We may merge a PR with internal review only in case of urgency (critical fixes, release preparation etc.)
  - Items to be defined with the Community:
    
    1. A timeframe for external review (X):
       
       - X=12 hours, Y=2 days?
    2. What projects it should affect?
       
       - Plenum and Node?
       
       - Only Node?
       
       - We are not proposing SDK as it will be split to Aries in any case
    3. Who is going to commit to participate in this process?
- **No volunteers on this call**

## Future Calls

- Requirements question: IS-1099, should we allow duplicate credentials from the same issuer?
- Non-secrets in the Indy Wallet
  
  - Cam is working on pluggable crypto. They wallet shouldn't decide what encryption you should be using.
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

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
