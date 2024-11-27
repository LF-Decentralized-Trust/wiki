1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-05-10 Indy Contributors Call

Created by Stephen Curran, last modified on May 10, 2022

## Summary

- Progress on Indy / Aries Shared Components – Load Test Results
- Call for Resources: Completing the Indy Ubuntu 20.04 Upgrade
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

Sections:

- IndySDK vs. Aries Askar performance - from 0:00 to 9:10
- Ubuntu Upgrade discussion from 9:18 to the end of the recording.

Chat:

- IndySDK / Aries Askar performance comparison with ACA-Py:
  
  - 08:13:03 From Stephen Curran : [https://github.com/lissi-id/acapy-load-test-results/blob/main/AcaPy\_0-7-4/Endurance\_Test/02-0\_7\_4\_askar\_0\_2\_5-200rpm/report-test-results-0-6.pdf](https://github.com/lissi-id/acapy-load-test-results/blob/main/AcaPy_0-7-4/Endurance_Test/02-0_7_4_askar_0_2_5-200rpm/report-test-results-0-6.pdf)
- Ubuntu Upgrade:
  
  - 08:12:57 From Wade Barnes : FYI, links to the PRs for the new GHA based workflows and automated release processes for plenum and node: - [https://github.com/hyperledger/indy-plenum/pull/1590](https://github.com/hyperledger/indy-plenum/pull/1590) - [https://github.com/hyperledger/indy-node/pull/1749](https://github.com/hyperledger/indy-node/pull/1749)
  - 08:13:56 From Stephen Curran : [https://docs.google.com/presentation/d/1LPccSn6HaLRkKt6DSgcWicORpRknwUsH9knKr9LBCz4/edit#slide=id.p](https://docs.google.com/presentation/d/1LPccSn6HaLRkKt6DSgcWicORpRknwUsH9knKr9LBCz4/edit#slide=id.p)
  - 08:27:41 From Lynn Bendixsen : Has the error been seen with simply "adding" a 20.04 to an existing network with 16.04's in it? Or must one be "replaced"?
  - 08:28:35 From Christian Bormann : If i remember correctly so far, it was only seen by upgrading a node - not sure if adding a new node was tested
  - 08:28:48 From Wade Barnes : [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container) is the other option for the network for the tests.
  - 08:30:40 From Wade Barnes : Lynn, Yes adding a 20.04 node to and existing 16.04 network is known to trigger the issue.
  - 08:35:48 From Wade Barnes : About the mixed nodes issues [https://hackmd.io/GSJnYPt0Q9yFKgoNGWtcMw](https://hackmd.io/GSJnYPt0Q9yFKgoNGWtcMw)
  - 08:44:03 From Philipp Schlarb : i can look into the von side if not planned in for the sovtoken gha/gitpod changes
  - 08:46:15 From Christian Bormann : Are people planning to switch to container-based deployments for the nodes when upgrading?
  - 08:46:49 From Philipp Schlarb : as far as i know in idunion is a node running containerized
  - 08:54:27 From Wade Barnes : The GitHub issue for the mixed node network issue; [https://github.com/hyperledger/indy-node/issues/1750](https://github.com/hyperledger/indy-node/issues/1750)
  - 08:56:50 From Christian Bormann : do we also need indy-plenum packages Wade?
  - 08:57:07 From Christian Bormann : or is the current indy-node enough?

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@[e](http://esatus.com)satus.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Avast) &lt;richard.esplin@avast.com&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
- Indy SDK
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)

## Meeting Topics

- An apples to apples test of the "Shared Components" vs. the Indy-SDK shows performance is remarkably improved with the Shared Components. We'll take a look at the reports, talk about what you get when you switch, the effort and next the steps in moving this forward.
  
  - Report: [ACA-Py 0.7.4-RC with Indy-SDK](https://github.com/lissi-id/acapy-load-test-results/blob/main/AcaPy_0-7-4/Endurance_Test/04-0_7_3_indy-200rpm/report-test-results-0-END.pdf)
  - Report: [ACA-Py 0.7.4-RC with Aries Askar](https://github.com/lissi-id/acapy-load-test-results/blob/main/AcaPy_0-7-4/Endurance_Test/02-0_7_4_askar_0_2_5-200rpm/report-test-results-0-6.pdf) (and other Shared Components)
- A plan for getting the Ubuntu upgrade complete and a request for resources to help with the work.

# Upgrade Notes

- Upgrading Indy to Ubuntu 20.04 Presentation [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1LPccSn6HaLRkKt6DSgcWicORpRknwUsH9knKr9LBCz4/edit#slide=id.p)
- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - NEWIndy Shared GHA Repo
    
    - Updates being made across all repos to organize the GHAs into a single repository ([indy-shared-gha](https://github.com/hyperledger/indy-shared-gha)), and dependent updates being made to all indy repos
  - Indy-Plenum Status: 
    
    - Done, 16.04, 20.04, Jenkins and GHA
      
    - New Release Workflow PR: [https://github.com/hyperledger/indy-plenum/pull/1590](https://github.com/hyperledger/indy-plenum/pull/1590)
  - Indy-Node Status:
    
    - Done, 16.04, 20.04, Jenkins and GHA
    - One 20.04 running in the IDUnion network of 16.04 nodes
      
    - New Release Workflow PR: [https://github.com/hyperledger/indy-node/pull/1749](https://github.com/hyperledger/indy-node/pull/1749)
  - indy-test-automation Status:
    
    - Working on automated triggers across repositories but must be in the main branch – perhaps time to convert over main to 20.04, and to have a 16.04 branch.  To be discussed.
    - Working systemd image for 20.04, but the tests are not fully tested because of permissions handling decisions to be made after GHA work completed. 20.04 requires root where 16.04 doesn't and we want to confirm that to be the case.
    - There might be a solution in the indy-node-container work.  To be checked with [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence).
  - indy-node-container (moved to Hyperledger) and GitPod tools available (node and plenum)
  - Indy-SDK build progress
    
    - Unblocked – builds are going and PRs are being reviewed (and rebasing PRs).
  
  <!--THE END-->
  
  - Backlog Issue: Mixed OS versions of Indy Node have issues:
    
    - How are we going to work through this issue and upgrade the various networks?
    - Issue: - running mixed nodes 16.04 and 20.04 a consensus problem occurs "in a while" (sometimes immediately, sometimes a few days has been seen)
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464589/19466156.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
