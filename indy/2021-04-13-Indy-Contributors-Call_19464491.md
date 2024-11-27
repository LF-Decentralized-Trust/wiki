1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-04-13 Indy Contributors Call

Created by Stephen Curran, last modified on Apr 13, 2021

## Summary

Planned:

- Status of indy-node CI/CD
- Status of Ubuntu upgrade

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Lynn Bendixsen (Indicio, PBC) &lt;lynn@indicio.tech&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) and[Ryan Marsh](https://lf-hyperledger.atlassian.net/wiki/people/557058:45ceb1ce-c3dd-4f33-9fef-f7aade227711?ref=confluence)
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
  - Indy Node release needs a build of Indy SDK with freeze ledgers to do system tests. Currently blocked with publishing to pypi.
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - donated to Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ([Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )

## Meeting Topics

- Update: GitHub actions led by [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  
  - CD: Hyperledger Debian repo is available and being used
    
    - Package artifacts
    - Secrets managed
  - Indy-Plenum
    
    - CI for Indy Plenum - merged
      
      - Being redone because of missing tests
    - CD for Indy Plenum - ready but not merged 
      
      - CD is in master, needs to be merged into ubuntu2004 branch
      - GHA details in PR: [https://github.com/hyperledger/indy-plenum/pull/1522#issuecomment-810531932](https://github.com/hyperledger/indy-plenum/pull/1522#issuecomment-810531932)
      - In PR is ability to run the GHAs off different branches.
    - Stable to Master merge - Merged
    - Ubuntu 20.04 tests
      
      - Now mostly running – had been missing the upgrades necessary to run the tests
      - 1 test is failing, 1 split test is cancelling – details to go to Renata (Wade to provide)
        
        - Skipped tests – should verify why and make sure that is OK – Wade to review.
      - Task: Eliminate the pinned dependencies as possible – Renata's team to look at that
        
        - Requires code changes and additional tests
  - Indy-Node
    
    - Rinse and repeat the Plenum work
    - Stable to Master merge – still being reviewed (Wade); waiting on a response to a question (Renata)
  - Indy-SDK
    
    - CI/CD for Indy-SDK looks good – ready, Wade to review - waiting for Jenkins to sign off on the build (happening as we speak)
      
      - Jenkins failure is preventing merging – all tests must pass
      - Can someone look at that?  Wade reviewed and not seeing the issue.  ABSA has looked at it, but don't know the issue.
        
        - ?? To be looked at...
    - Jenkins/GHAs to run in parallel for a bit, while the GHA are finalized.
      
      - CI – deprecating that sooner than later
      - CD – need the right triggers to fire (e.g. if PR merges to master and updates the tag, publishes artifacts)
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Working on CI/CD
      
      - Dev environment is working and new docs
      - Working on the Plenum side because it was blocking him
        
        - Discovered problems with plenum upgrade – many failing tests – mostly fixed
      - Jenkins
    - Ubuntu 20.04
      
      - Upgrade from indy-crypto to ursa-crypto - done
      - Upgrade Python - done
      - Rinse and repeat from Plenum for dependencies
  - indy-test-automation – had been working, but it is dependent on the Sovrin packages that are not made yet.
  - Need to research the publishing of the artifacts from GHA to the Sovrin repos
    
    - Before – indy and sovrin artifacts were in Sovrin repos
    - To Be Done – indy artifacts will be hosted on Hyperledger Artifactory; Sovrin on Sovrin repositories
- Indy Contribution Campaign
  
  - Timing – HGF coming up –  timing perhaps best is after HGF
  - Video – 3 month lead time on that – Digital Identity
  - Look at second half of the year – but we need to get started
- Status of indy-sdk CI/CD
- Sovrin Network Upgrade process: 
  
  - **Inputs**: New CI/CD, OS Upgrade, Post Feb. 2020 functionality (e.g. Rich Schema), indy-crypto vs. ursa-crypto
  - **Today**: 16.04 with no post Feb 2020, Functionality, mix of indy-crypto/ursa-crypto
  - **Release 1**: Another 16.04 using the new CI/CD code but no code changes plus the Post-Feb. 2020 changes
    
    - Concern: Have the new GHAs been made ONLY for 20.04?  Not supposed to be, but TBD.
  - **Release 1**: Ubuntu 20.04 that runs with today's nodes.
    
    - Proposal: Call the new version 1.13.0 that is tested ONLY on Ubuntu 20.04, MUST be compatible with 1.12.4
    - One Steward at a time – 1) remove their 16.04 1.12.4 node, 2) create new 20.04 device, 3) install 20.04 node, 4) add their 1.13.0 node
    - Cannot affect consensus – we'll verify that as we go.
    - Short term request of Stewards – get ESM from Canonical
  - **Release 3**: Post Feb. 2020 changes

## Future Calls

Next call:

Future:

- Changed to indy-node as needed for [did:indy](https://lf-hyperledger.atlassian.net/wiki/display/indy/Indy+DID+Method+Specification)
- Status of Indy-SDK
  
  - Statement on the future of the Indy SDK: [PR 2329](https://github.com/hyperledger/indy-sdk/pull/2329)
  - Plans for future of Indy CLI (move to Indy VDR?)
  - Indy SDK in test for Indy Node (move to Indy VDR?)
  - Status of GitHub Actions for the Indy-SDK
- Indy bugs
  
  - Using GitHub tags "Good First Issue" and "Help Wanted"
  - [Node 1490](https://github.com/hyperledger/indy-plenum/issues/1490): problems with large catch-up
  - [Plenum 1506](https://github.com/hyperledger/indy-plenum/issues/1506): view change message consensus calculation error
- Hyperledger campaign to recruit additional developers.

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464491/19465797.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
