1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-05-11 Indy Contributors Call

Created by Stephen Curran, last modified on May 11, 2021

## Summary

- Status of indy-node CI/CD
- Status of Ubuntu upgrade

## Recording from the call: [20210511 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym)  &lt;richard.esplin@evernym.com&gt;
- [Sebastian Schmittner](https://lf-hyperledger.atlassian.net/wiki/people/5f3100521ac29c004582f9d5?ref=confluence) (EECC) &lt;sebastian.schmittner@eecc.de&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) and[Ryan Marsh](https://lf-hyperledger.atlassian.net/wiki/people/557058:45ceb1ce-c3dd-4f33-9fef-f7aade227711?ref=confluence)
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
  - LibVCX tests are failing. Proposal is to deprecate LibVCX in the Indy SDK, and focus on aries-vcx.
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
  
  - Sovrin Steward Council Health Workstream has been working on it.
- Indy/Aries Shared Libraries - donated to Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
  
  - Appears that refactor has stalled? Need volunteers.
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ([Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )

## Meeting Topics

- Update:
  
  - Indy-Plenum CD is the furthest along. Thank you [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)!
    
    - PR submitted last week - for 16.04
    - Reviewed by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)today, some cleanup needed
    - No blockers
    - Next step is CD for Ubuntu 20.04
  - Indy-Node
    
    - No changes – waiting on Plenum
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Issue with libsov token builds for IOS/client side – needed for the testing, engaged Ian C/BC Gov to work this
    - Jenkins build
  - indy-test-automation – had been working, but it is dependent on the Sovrin packages that are not made yet.
    
    - Blocked on previous issue
- Indy SDK - ABSA updates merged – libvcx removed from CI / CD
- IDUnion Docker images for Indy Node ( [https://github.com/IDunion/docker-container-wg/](https://github.com/IDunion/docker-container-wg/) )
  
  - Goals: reduce dependencies, in particular from specific Ubuntu Versions
    
    - Questions around running indy node in a container in the first place (restarts/upgrades, systemd,...)
  - WIP! But we got a few (ubuntu 18, debian buster) running containers which are not ubuntu16 based.
  - Upstream Contribution
    
    - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) : Perhaps make it a part of Indy Node repo?
    - Into a separate - repo – e.g. "indy-node-container" - in case the repo is moved to Hyperledger
  - Sovrin experience goes:
    
    - Persisting the ledgers – that's easy
    - Challenge is that the network is long running and does network driven updates
      
      - Network update done, updates node themselves – new dependencies, new version of Node – but this is happening to ephemeral storage (not persisted)
        
        - Upgrade strategy for docker is that they pull a new image, not simply automate the upgrade of the running container
      - On restart, the ephemeral updates are lost, and the node is running old code again.
      - Need to persist the code changes.
    - Challenge as well is that we lose diversity if all nodes run the same docker image – how do we retain diversity?
    - Old PR about using docker: [https://github.com/hyperledger/indy-node/pull/588/](https://github.com/hyperledger/indy-node/pull/588/)

## Future Calls

Next call:

Future:

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464507/19465825.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
