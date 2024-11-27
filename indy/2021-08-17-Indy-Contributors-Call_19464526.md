1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-08-17 Indy Contributors Call

Created by Stephen Curran, last modified by Ry Jones on Aug 17, 2021

## Summary

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
- Ry Jones (Linux Foundation) [rjones@linuxfoundation.org](mailto:rjones@linuxfoundation.org)
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Evernym) [richard.esplin@evernym.com](mailto:richard.esplin@evernym.com)
- [Sebastian Schmittner](https://lf-hyperledger.atlassian.net/wiki/people/5f3100521ac29c004582f9d5?ref=confluence) (EECC) [sebastian.schmittner@eecc.de](mailto:sebastian.schmittner@eecc.de)

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
  - LibVCX tests are failing. Proposal is to deprecate LibVCX in the Indy SDK, and focus on aries-vcx.
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
  
  - Appears that refactor has stalled? Need volunteers.
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ([Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )

## Meeting Topics

- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - GitHub Issues
    
    - Indy-Plenum - issues – "[2004](https://github.com/hyperledger/indy-plenum/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22Ubuntu%2020.04%22)" tag, including some help wanted
  - Indy-Plenum
    
    - Basically done CI/CD, 16.04 and 20.04
      
      - Still need to adjust the 20.04 publishing structure because of package collisions. - Robin
    - To be done post-publishing: [https://github.com/hyperledger/indy-plenum/issues/1554](https://github.com/hyperledger/indy-plenum/issues/1554)
      
      - Things in Jenkins and not in GHA
    - [Security issue](https://github.com/hyperledger/indy-plenum/security/dependabot/setup.py/Pygments/open) around Pygments – but it is only used in the docs, not in the code.
  - Indy-Node
    
    - Work is happening here now
    - A loop in the test automation – need Sovrin packages to test node, but need node to release Sovrin packages.
      
      - Devin started on this, but it's not working yet.  Wade is focusing on that next.
  - indy-test-automation
    
    - Enable node testing without Sovrin dependencies.
    - Work will continue as/when needed.
    - TBD from Devin Smith – where was this left off.
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Work will resume following the work on Plenum and Node.
    - Once it's complete, Evernym can test the release candidate.
- Indy Plenum issuer reported: [IC Queue getting quite large](https://github.com/hyperledger/indy-plenum/issues/1542)
  
  - Evernym has provided feedback and Dom is looking into things further on his end.
- Indy SDK
  
  - Async libindy [https://github.com/hyperledger/indy-sdk/pull/2319](https://github.com/hyperledger/indy-sdk/pull/2319) - what's the plan?
  - IndySDK LibVCX - should be removed from IndySDK?
    
    - Consensus - Yes
    - PR for removal: [https://github.com/hyperledger/indy-sdk/pull/2416](https://github.com/hyperledger/indy-sdk/pull/2416)
  - Should Indy CLI be part of indy-node or put into it's own repository.
    
    - Could it pulled out and put on indy-vdr?
    - Possibly post as a help wanted – pulling out of indy-sdk and into indy-cli
- Plan for migrating Ubuntu 20.04 from a branch in Indy-Node and Indy-Plenum into Main.
  
  - This release is the last release that will support Ubuntu 16.04.
  - Need pipelines that support Ubuntu 20.04 LTS and Ubuntu 22.04 LTS.
  - After this release we can start decommissioning Jenkins.
- Issue with Indy Sandbox BCovrin Test
  
  - Had been running for years, used by developers
  - Yesterday - crashed
  - On restart, it went into a startup crash loop – recovering and then aborted.
    
    - All nodes had the same issue.
  - Could read the config and pool ledger, but could not read the domain ledger.
  - Forced to reset the ledger to make it available again.
  - Backup taken and needs to be investigated.  How did we lose the ledger across all nodes?
- Invitation for Indy to participate in the Linux Foundation Grace Hopper Day (Oct 1, 9-5am PT).
  
  - A project with 30-100 triaged, non-documentation, “good first issues” labeled and ready two weeks before each event.
  - Provide 2 project representatives who are also maintainers of your project (e.g. can merge PRs), preferably women.
    
    - [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence)has volunteered to represent Indy
  - Should hear back next week on whether Indy is selected.
- Important bug in Indy SDK impacts Android wallets: [https://github.com/hyperledger/indy-sdk/issues/2382](https://github.com/hyperledger/indy-sdk/issues/2382)
- Process for supporting IDunion Network
  
  - Contact Main Incubator to become an endorser.

## Future Calls

- Indy Contributor Campaign
  
  - Focus: Indy Generation Next
    
    - Audience: Organizations building Indy Instances, applications built on Indy
      
      - Not going for casual, independent developers, more on organizations that can assign developers to work on the project for a set chunk of time (e.g one month)
    - Key Features:
      
      - Indy network of networks support
      - Indy support for W3C DID Standard 1.0
    - Tasks:
      
      - Update NYM to support new "diddoc\_content" data element
      - Indy-sdk, indy-vdr support for new "diddoc\_content" data element
      - Indy DID Resolver support for new "diddoc\_content"
      - indy-sdk, indy-vdr support for multiple ledgers
      - Support for new ledger object identifiers
      - Handling cred\_defs that references schema on other ledgers
      - Possible: support for NYM "keri\_keystate" data element, indy-sdk/indy-vdr support and DID resolver support
      - Other?
    - Foundational Work:
      
      - did:indy spec. as a spec.
      - Tasks in GitHub Issues - tagged for campaign
      - Getting started with developing indy-plenum and indy-node
        
        - Tutorial: Sample feature to add to indy-node
          
          - Example: [rich schema feature flag](https://github.com/hyperledger/indy-node/pull/1633)
    - Campaign work
      
      - Landing page
      - Video: Intro to Indy Generation Next
      - Meetup channels

<!--THE END-->

- Changes to indy-node needed for [did:indy](https://lf-hyperledger.atlassian.net/wiki/display/indy/Indy+DID+Method+Specification)
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464526/19465872.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
