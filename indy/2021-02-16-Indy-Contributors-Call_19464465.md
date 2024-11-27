1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-02-16 Indy Contributors Call

Created by Richard Esplin, last modified on Feb 20, 2021

## Summary

Planned:

- HIPEs for plugin helpers
- Status of indy-node CI/CD and Ubuntu upgrade
- Status of upcoming indy-sdk release and follow up issues
- Demo of freeze ledgers functionality

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- @name (Employer) &lt;email&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - Functionality to remove tokens led by [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)
    
    - Blocked by system test dependency on sovrin.deb
    - Will split Sovrin specific tests in indy-test-automation into separate repo in sovrin-foundation org
      
      - Will break the Sovrin Jenkins pipelines further. Best fix is to setup GitHub Actions pipeline for Sovrin deb.
  - GitHub actions led by [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence)
    
    - We need a GHA pipeline for Ubuntu 16.04 and Ubuntu 20.04 so that we can test in both.
    - The Ubuntu upgrade must interoperate with the then-current 16.04 release, so that we can organize the "one node at a time" Steward OS upgrades.
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) and[Ryan Marsh](https://lf-hyperledger.atlassian.net/wiki/people/557058:45ceb1ce-c3dd-4f33-9fef-f7aade227711?ref=confluence)
    
    - Making good progress, but blocked because there isn't a pipeline.
    - Draft of pipeline based on [PR1505](https://github.com/hyperledger/indy-plenum/pull/1505) : [https://github.com/udosson/indy-plenum/tree/gha-ubuntu-20.04/.github/workflows](https://github.com/udosson/indy-plenum/tree/gha-ubuntu-20.04/.github/workflows)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Documenting plan (HIPE?)
    - Merging Stable to Master ([Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence)'s next task)
    - Rename Master to Main
    - Releasing what is currently in Master
    - Evernym can help merge and test.
- Indy SDK
  
  - Next release in progress, led by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Release done?
    - Wade needs to do some work to make sure artifact publishing happens smoothly.  May be this week, but lots on Wade.
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
  - Indy Node release needs a build of Indy SDK with freeze ledgers to do system tests. Currently blocked with publishing to pypi.
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - donated to Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ([Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )

## Meeting Topics

- HIPEs for helpers to remove plugins: [PR 162](https://github.com/hyperledger/indy-hipe/pull/162)
  
  - Freeze ledgers
  - Fees in Indy
- Demo of freeze ledgers transaction [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence)(10 minutes)
- GitHub actions led by [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) - We need a GHA pipeline for Ubuntu 16.04
  
  - CI for Indy Node - merged
  - CD for Indy Node - active development - no official PR ready
  - CI/CD for Indy Plenum - draft done - a couple cleanups before merging, but still need to add the publishing part of CD
  - Completion of Sovrin release to produce final artifacts
- Ubuntu 20.04 Ryan Marsh, [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
  
  - Working on tests related to Python 3.8 upgrade – most are running, 4-5 to go, parallel looking at specific packages to be updated
- PR from Stable to Master - some conflicts, but will be done before the next meeting.

## Future Calls

Next call:

Future:

- Can we merge HIPEs for helpers to remove plugins: [PR 162](https://github.com/hyperledger/indy-hipe/pull/162) ?
- Indy Node Maintainers.md, and CODEOWNERS in Indy Node and Indy Plenum
  
  - Hyperledger standard Maintainers document?
  - Should include WadeBarnes Toktar brentzundel esplinr sergey.khoroshavin
  - Should also include udosson, m00sey, ianco, and askolesov ?
- Status of Indy-SDK release
  
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464465/19465728.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
