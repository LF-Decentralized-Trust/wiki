1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-04-12 Indy Contributors Call

Created by Stephen Curran, last modified by Sebastian Schmittner on Apr 14, 2022

## Summary

- Before this meeting: did:indy DID Method Meeting (starts one hour earlier)
- Status of indy-node CI/CD and the Ubuntu upgrade
- Mixed version Indy networks – how to debug/fix?
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence)
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)
- [Mirko Mollik](https://lf-hyperledger.atlassian.net/wiki/people/5e411f183df51b0c93737dd4?ref=confluence)
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)
- [Sebastian Schmittner](https://lf-hyperledger.atlassian.net/wiki/people/5f3100521ac29c004582f9d5?ref=confluence) (EECC) &lt;sebastian.schmittner@eecc.de&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)
- [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
- [Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;
- [Artur Philipp](https://lf-hyperledger.atlassian.net/wiki/people/712020:80b9b689-6e02-4eee-a821-09a7a0a77e24?ref=confluence)
- [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)  (Robert Bosch GmbH) &lt;ChristianCarl.Bormann@de.bosch.com&gt;

## Related Calls and Announcements

- IIW – anyone going?  What are you planning to talk to about?
  
  - Some people on this call think that having another online version of IIW might be a good thing, regardless of COVID.

## Release Status and Work Updates

- Indy Node
- Indy SDK
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)

## Meeting Topics

- Before the meeting: ["did:indy" DID Method](https://hyperledger.github.io/indy-did-method/)
  
  - Separate meeting held one hour prior to this one.
- Meeting format changes:
  
  - did:indy DID Method Specification call to be conducted as needed within the Indy Contributors call – no longer a separate weekly call
  - Indy Contributors call moving back to starting at 8:00 Pacific (fixed) / 17:00 CET (usually) and will once again be scheduled for 1 hour
- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - NEWIndy Shared GHA Repo
    
    - Updates being made across all repos to organize the GHAs into a single repository ([indy-shared-gha](https://github.com/hyperledger/indy-shared-gha)), and dependent updates being made to all indy repos
  - Indy-Plenum Status: 
    
    - Done, 16.04, 20.04, Jenkins and GHA
  - Indy-Node Status:
    
    - Done, 16.04, 20.04, Jenkins and GHA
    - One 20.04 running in the IDUnion network of 16.04 nodes
  - indy-test-automation Status:
    
    - Working systemd image for 20.04, but the tests are not fully tested because of permissions handling decisions to be made after GHA work completed. 20.04 requires root where 16.04 doesn't and we want to confirm that to be the case.
    - There might be a solution in the indy-node-container work.  To be checked with [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence).
  - indy-node-container (moved to Hyperledger) and GitPod tools available (node and plenum)
  - Indy-SDK build progress
    
    - Unblocked – builds are going and PRs are being reviewed (and rebasing PRs).
- How are we going to work through this issue and upgrade the various networks?
  
  - Concern - running mixed nodes 16.04 and 20.04 a consensus problem occurs "in a while" (sometimes immediately, sometimes a few days has been seen)
  - Robin has the details of what tests have been run and what observations have been done. See [Hack MD](https://hackmd.io/GSJnYPt0Q9yFKgoNGWtcMw) document with some details.
  - Perhaps because of libsodium v18 and v23.
  - It might also be a ledger corruption issue, perhaps with the lead node having corruption issues and then propagating those issue.
  - Can we get the indy-node-container folks run tests with a mixed environment of nodes
  - Richard Esplin at Avast can get help answering questions about Plenum. Tag him on Discord with your question.
  - Blog post on [troubleshooting an Indy network](https://www.evernym.com/blog/troubleshooting-an-indy-network/).

## Future Calls

- GDPR and the right to be forgotten – mitigations and approaches.
- Dealing with Indy Node DoS attacks.
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

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464585/19466123.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
