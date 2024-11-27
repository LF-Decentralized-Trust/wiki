1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-09-14 Indy Contributors Call

Created by Stephen Curran, last modified on Sep 14, 2021

## Summary

- Status of indy-node CI/CD
- Status of Ubuntu upgrade
- Indy DID Method Repo

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) (Institute for Internet Security) &lt;klemens@[internet-sicherheit.de](http://internet-sicherheit.de)&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio, PBC) &lt;lynn@indicio.tech&gt;

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
    
    - Status: 
      
      - Adjusted pipelines to use the same flow, removed async parts
      - Updated Indy-SDK
  - Indy-Node
    
    - Status:
      
      - Updated per plenum, almost completed.
      - Both 16.04 and 20.04 are (almost) done
      - Next: PRs to be merged to update and remove pip&lt;10 dependency, tricky to merge
  - indy-test-automation
    
    - Status:
      
      - Breaking the dependencies between this and Node/Plenum
      - Uses docker-in-docker to spin off the tests, run ledgers, etc.
        
        - Wade trying to get that to run locally, and then remove the circular dependency
          
          - Move tests from Node to Sovrin – where they should be. Eliminates the circular issue.
          - Make it a dependency only in Sovrin, not in Node
          - Wade to provide details on what needs to be done, opening up getting help from Robin and team and Philipp.
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Status: &lt;To be completed&gt;
    - ETA: ??
- Indy DID Method specification repo: [indy-did-method](https://github.com/hyperledger/indy-did-method) and the published spec: [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
  
  - Huge thanks to Bosch for getting the work done!
  - Needs some cleanup – the logo link and the [Spec-Up](https://github.com/decentralized-identity/spec-up) dependabot updates.
  - And it needs to be reviewed, a backlog created and code written...
- Indy SDK
- Update: Indy to participate in the Linux Foundation Grace Hopper Day (Oct 1, 9-5am PT).
  
  - Hyperledger accepted as a group: Indy and Fabric
  - Indy needs 10-20 triaged, non-documentation, “good first issues” labeled and ready two weeks before each event.
    
    - Perhaps a number of the did:indy effort.
  - Provide 1 project representatives who are also maintainers of your project (e.g. can merge PRs), preferably women.
    
    - [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence)has volunteered to represent Indy
- Indy Contributor Campaign
  
  - Perhaps a foundation for this:
    
    - Indicio and Hyperledger talking about a joint venture for Indy certification
    - Perhaps an Indy workshop to get them through initial questions
  - Need a guide to setup dev environment, change a line of code, test locally, submit PR.
    
    - With the CI/CD to cover a lot of the details.

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464532/19465886.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
