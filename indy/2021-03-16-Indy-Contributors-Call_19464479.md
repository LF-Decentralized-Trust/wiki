1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-03-16 Indy Contributors Call

Created by Stephen Curran, last modified on Mar 16, 2021

## Summary

Planned:

- Status of indy-node CI/CD
- Status of Ubuntu upgrade
- Status of completed indy-sdk release and follow up tasks
- Indy Contributor Campaign
- Indy DID Method Spec – actions

## Recording from the call: [20210316 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio PBC) &lt;[lynn@indicio.tech](mailto:lynn@indicio.tech)&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Evernym) &lt;richard.esplin@evernym.com&gt;
- @name (Employer) &lt;email&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - Functionality to remove tokens led by [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)
    
    - Blocked by system test dependency on sovrin.deb
    - Will split Sovrin specific tests in indy-test-automation into separate repo in sovrin-foundation org
      
      - Will break the Sovrin Jenkins pipelines further. Best fix is to setup GitHub Actions pipeline for Sovrin deb.
  - GitHub actions led by [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) and[Ryan Marsh](https://lf-hyperledger.atlassian.net/wiki/people/557058:45ceb1ce-c3dd-4f33-9fef-f7aade227711?ref=confluence)
    
    - Making good progress, but blocked because there isn't a pipeline.
    - Draft of pipeline based on [PR1505](https://github.com/hyperledger/indy-plenum/pull/1505) : [https://github.com/udosson/indy-plenum/tree/gha-ubuntu-20.04/.github/workflows](https://github.com/udosson/indy-plenum/tree/gha-ubuntu-20.04/.github/workflows)
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Documenting plan (HIPE?)
    - Merging Stable to Master ([Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) has a PR done)
    - Rename Master to Main
    - Releasing what is currently in Master
    - Evernym can help merge and test.
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
  - Indy Node release needs a build of Indy SDK with freeze ledgers to do system tests. Currently blocked with publishing to pypi.
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - donated to Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ([Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )

## Meeting Topics

- Update: GitHub actions led by [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)  - We need a GHA pipeline for Ubuntu 16.04
  
  - Indy-Node
    
    - CI for Indy Node - merged
    - CD for Indy Node - active development - no official PR ready - waiting on Plenum
    - Stable to Master merge
      
      - In process, but reintroducing things that were deleted, reverting state
  - Indy-Plenum
    
    - CI for Indy Plenum - merged
    - CD for Indy Plenum - draft done - the publishing is not added, but will be – fairly easy - Issue 1526 (Robin - DCO) - [PR1526](https://github.com/hyperledger/indy-plenum/pull/1526)
    - Stable to Master merge
      
      - In process - some issues found, but PR resolves them - waiting for review
  - Indy-SDK
    
    - CI/CD for Indy-SDK looks good – paused - ready to move forward (ABSA work).
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Working on CI/CD - Resource found for that, starting soon - Anmol Singh - contractor through Sovrin
    - Will be adding Ubuntu 20.04 support
  - indy-test-automation – had been working, but it is dependent on the Sovrin packages that are not made yet.
  - Need to research the publishing of the artifacts from GHA to the Sovrin repos – it's magic right now, needs to be brought into the open.
- Next Indy-Node release – need CD completed.  Once done, then we can plan the final steps to produce a release.
  
  - Wade to work on a checklist for what is needed, and who is doing what for the initial release.
- Ubuntu 20.04[Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) and [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
  
  - Working on tests related to Python 3.8 upgrade – most are running, 4-5 to go, parallel looking at specific packages to be updated
  - All tests resolved
  - CI-CD changes for plenum Ubuntu in progress / getting close
  - Do we still need to build the deb files of rocksdb or can we directly use [https://packages.ubuntu.com/source/focal/rocksdb](https://packages.ubuntu.com/source/focal/rocksdb) at v. 5.17.2? In Ubuntu 16.04 we use rocksdb v. 5.8.8
- Indy Contribution Campaign
  
  - Timing – HGF coming up –  timing perhaps best is after HGF
  - Video – 3 month lead time on that – Digital Identity
  - Look at second half of the year – but we need to get started
- Indy DID Method Spec organizing
  
  - Adding to the NYM transactions (write and read) a "diddocContent" item, instead of putting it into an associated ATTRIB
    
    - Per Sergey K – may want to use ATTRIB storage for the item instead of adding it to the NYM on the ledger
    - [Old Indy-SDK epic](https://jira.hyperledger.org/browse/IS-1403), [old Indy epic](https://jira.hyperledger.org/browse/INDY-51), (must login to see epics)
- Indy-SDK – done.  1.1.16 is in the wild!  Merge still needs to be done, but it's ready.  All other steps are done.
- DONE: Indy Node [Maintainers.md](http://Maintainers.md), and CODEOWNERS in Indy Node and Indy Plenum
  
  - Updated CODEOWNERS list: WadeBarnes Toktar brentzundel esplinr sergey.khoroshavin, udosson, m00sey, ianco, and askolesov
  - Hyperledger standard Maintainers document?
  - Use GitHub groups instead of CODEOWNERS? Ry set this up. We just need to approve his changes.
- repolinter - needs

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464479/19465768.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
