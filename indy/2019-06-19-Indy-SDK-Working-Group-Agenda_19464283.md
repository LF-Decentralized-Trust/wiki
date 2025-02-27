1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy SDK Working Group Agendas](Indy-SDK-Working-Group-Agendas_19464232.html)

# Hyperledger Indy : 2019-06-19 Indy SDK Working Group Agenda

Created by Richard Esplin, last modified on Jun 27, 2019

## Summary:

- Useful work updates.
- Discussion of merging this call with [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)

## Remember:

- [Linux Foundation Anti-Trust Policy](2019-06-19-Indy-SDK-Working-Group-Agenda_19464283.html)
- [Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/events/pages/21791172/Diversity+and+Code+of+Conduct)

## Attendees:

- Richard Esplin (Evernym)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass/BC Gov)
- Arjan van Eersel (Sonemas)
- Sam Curren (Sovrin Foundation)

## Release Status:

- June: Indy SDK 1.10.0
  
  - Flexible Credential Attribute Tagging (Canada.gov)
    
    - Plans for manual integration testing? Does not feel that needs additional testing, but BC.gov will put into use quickly.
    - Plans to present on the feature? Thursday WG
  - Bugfixes
- July / August:
  
  - Platform Updates (Evernym?)
  - Anoncreds 2.0 (Sovrin Foundation, BC.gov?)
    
    - [https://github.com/hyperledger/ursa-docs/tree/master/specs](https://github.com/hyperledger/ursa-docs/tree/master/specs) (build.sh will use the Latex file to build a PDF)
  - GitLab migration alongside Jenkins (Foundation)?
    
    - Linux should be ready, maybe Windows.
    - Need a plan for mobile devices.
    - Could run it right after the release.
- Other:
  
  - DID Doc / Fully Qualified DIDs / DID Resolution (Evernym?)
  - W3C Verifiable Credentials (Evernym)

# Work Updates:

- CI / CD (Mike and Steve G)
  
  - Sovrin prefers GitLab, and working on migration
  - Hyperledger is considering Circle CI
    
    - Circle CI doesn't do Windows. GitHub actions are coming.
  - Interested people should join #cicd
  - Should enable dependabot ([https://dependabot.com/](https://dependabot.com/)).
    
    - Concerns with automated pull requests until we better understand the system.
    - Sergey (as repo admin) will review on a near daily basis.
    - PRs in indy-sdk from the bot
      
      [https://github.com/hyperledger/indy-sdk/pulls?q=is%3Apr+is%3Aclosed+author%3Aapp%2Fdependabot](https://github.com/hyperledger/indy-sdk/pulls?q=is%3Apr%20is%3Aclosed%20author%3Aapp%2Fdependabot)
- SDK 2.0 architecture (Sergey)
  
  - Aries / Indy split
    
    - Evernym has started a proposal, but shouldn't prevent others from creating a proposal. Should circulate soon.
- Payment decorator (Sergey)
  
  - Aries RFC is in "Proposed" status. Will be discussed in an Aries call soon.
- Warnings from rust cargo clippy (Mike)
  
  - IS-1270 through IS-1274
  - Will look at again in July
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - Need a plan for changes to Indy Node
- Rust and Bitcode
  
  - Closed "deferred": 
    
    Error rendering macro 'jira' : null
- Non-repudiation POC (Kyle)

# Other Open PRs:

- Plans for older pull requests: either need to finish them or reject them.
  
  - PR-946
  - PR-1407

# Other Business:

- Deprecation of Indy-SDK-Language repos? (Sam)
  
  - Indy / Aries split and migration
  - indy-sdk-python: Never shipped an artifact. Code is already moved to Aries. Let's kill the repos. We are comfortable leaving a few broken URLs.
  - All other repos were initially created in Aries.
- Getting involved with Aries
  
  - Status of Aries repos (Arjan)
  - Participating in calls (timezone permitting) and RocketChat channels (#aries, #aries-sdk, etc)
  - IndyCat agent will merge into the aries-agent-python (separate from aries-sdk-python)

# Future Business:

- Merge this call with the Indy Maintainers calls, moving them to the Monday slots for alternating timezones?
  
  - Much of the business of Indy Maintainers has moved to Aries.
  - Nathan is working on a proposal for a call calendar.

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
