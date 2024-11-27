1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-03-29 Indy Contributors Call

Created by Stephen Curran, last modified by Sebastian Schmittner on Apr 08, 2022

## Summary

- Before this meeting: did:indy DID Method Meeting (one hour earlier)
- Status of indy-node CI/CD and the Ubuntu upgrade
- Presentation on the [indy-node-container](https://github.com/hyperledger/indy-node-container) repo / project
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)(Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;
- [Sebastian Schmittner](https://lf-hyperledger.atlassian.net/wiki/people/5f3100521ac29c004582f9d5?ref=confluence) (EECC) &lt;sebastian.schmittner@eecc.de&gt;

## Related Calls and Announcements

- The move to Discord is done...
  
  - Invitation: [https://discord.gg/hyperledger](https://discord.gg/hyperledger)

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Phillip Schlarb has joined Wade and Robin to help here. Thanks!
    - Decluttering and outsourcing of the GHA tasks to be reusable with different Pipelines
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) 
    
    - mixed env issues are being worked on (16.04 and 18.04 nodes) if the issues persist there will be upgrade concerns.
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - old branching model was cumbersome and error prone.  New model will keep branching to a minimum. (fewer conflicts expected)
  - [indy-node-container](https://github.com/IDunion/indy-node-container/tree/main/controller) Crisitan Kubis ( [https://github.com/tsurai](https://github.com/tsurai) ), has created a Node Controller Container ([docs](https://github.com/IDunion/indy-node-container/tree/main/controller)), allows containerized indy nodes to participate in pool restart and upgrade
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
  
  - has been split to a fully api model: [https://github.com/hyperledger/indy-node-monitor/issues/36](https://github.com/hyperledger/indy-node-monitor/issues/36)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ( [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)

## Meeting Topics

- Before the meeting: ["did:indy" DID Method](https://hyperledger.github.io/indy-did-method/)
  
  - Separate meeting held prior to this one.
- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - Indy-Plenum Status: 
    
    - Done, 16.04, 20.04, Jenkins and GHA
  - Indy-Node Status:
    
    - Done, 16.04, 20.04, Jenkins and GHA
    - One 20.04 running in the IDUnion network of 16.04 nodes
    - Preparing and executing the automated release process.
  - indy-test-automation Status:
    
    - Working systemd image for 20.04, but the tests are not working – client messages not getting to the server.
    - Seems like there is a solution in the indy-node-container work.  To be checked with [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence).
  - Developer tools
    
    - indy-node-container (moved to Hyperledger) and GitPod tools available (node and plenum)
    - **NEED THIS FIXED – HELP NEEDED:** On plenum – error with building the dev containers about Indy SDK version – need to get the metadata version correct ([https://github.com/hyperledger/indy-sdk/issues/2473](https://github.com/hyperledger/indy-sdk/issues/2473))
      
      - Philipp raised a question on this, but no one had the info for an answer yet.
  - Indy-SDK build progress
    
    - Unblocked – builds are going and PRs are being reviewed (and rebasing PRs).
- NEXT MEETING: How are we going to work through this issue and upgrade the various networks?
  
  - Concern - running mixed nodes 16.04 and 20.04 a consensus problem occurs "in a while" (sometimes immediately, sometimes a few days has been seen)
  - Robin has the details of what tests have been run and what observations have been done. See [Hack MD](https://hackmd.io/GSJnYPt0Q9yFKgoNGWtcMw) document with some details.
  - Perhaps because of libsodium v18 and v23.
  - It might also be a ledger corruption issue, perhaps with the lead node having corruption issues and then propagating those issue.
  - Can we get the indy-node-container folks run tests with a mixed environment of nodes
- Presentation on the [indy-node-container](https://github.com/hyperledger/indy-node-container) repo / project by [Sebastian Schmittner](https://lf-hyperledger.atlassian.net/wiki/people/5f3100521ac29c004582f9d5?ref=confluence)

## Future Calls

- Issues that could impact indy-node on 20.04
  
  - indy-sdk: needs an upgrade to OpenSSL 1.1 to properly support Ubuntu 18.04/20.04.  For indy-node, just using indy-sdk as is.
  - Multiple libsodium versions could impact consensus – intermittent issue on a mixed network.
- **Plans for a new Indy-SDK release?**
  
  - A few people from the community have asked.
  - The most recent request has been for a release to include this feature; [https://github.com/hyperledger/indy-sdk/pull/2400](https://github.com/hyperledger/indy-sdk/pull/2400)

<!--THE END-->

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464577/19466092.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
