1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-05-25 Indy Contributors Call

Created by Stephen Curran, last modified on May 25, 2021

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
- [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) (Linux Foundation) &lt;ry@linux.com&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio, PBC) &lt;lynn@indicio.tech.

## Related Calls and Announcements

- [Monthly DevRel call 02 JUN](https://lists.hyperledger.org/g/tsc/viewevent?repeatid=26090&eventid=1151793&calstart=2021-06-02): please attend!

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
    
    - PR submitted for the publishing side – CD
    - Works, but the organization is not quite right – changes requested.
    - Supports only 16.04 publishing.
    - Hoping to get Devin Smith to help out on the indy-plenum stuff
  - Indy-Node
    
    - Waiting on indy-plenum
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Waiting on indy-node
    - CI is working, CD
    - Working through some build dependency issues - recursive – 1.16 to client side libsovtoken release – testing
      
      - Mac issues – being investigated
      - Windows issues – being investigated
  - indy-test-automation
    
    - Had been working, but it is dependent on the Sovrin packages that are not made yet.
- Indy SDK
  
  - ABSA updates merged
    
    - GHA changes – libvcx removed from CI / CD
  - Animo/Timo – some updates to the Node-JS wrapper – dependency and build issues
- IDUnion Docker images for Indy Node ( [https://github.com/IDunion/docker-container-wg/](https://github.com/IDunion/docker-container-wg/) )
- Aries VCX work ongoing
  
  - Adding it to Aries Agent Test Harness

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464511/19465835.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
