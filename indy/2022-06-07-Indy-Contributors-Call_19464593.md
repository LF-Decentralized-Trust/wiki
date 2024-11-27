1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-06-07 Indy Contributors Call

Created by Stephen Curran, last modified on Jun 07, 2022

## Summary

- Completing the Indy Ubuntu 20.04 Upgrade
- Indy SDK Dependabot Notifications
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Avast) &lt;richard.esplin@avast.com&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
- Indy SDK
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Progress on completing the Ubuntu upgrade.

# Upgrade Notes

- Upgrading Indy to Ubuntu 20.04 Presentation [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1LPccSn6HaLRkKt6DSgcWicORpRknwUsH9knKr9LBCz4/edit#slide=id.p)
  
  - Summary of the work done ^^
- Update on CI/CD Update and Ubuntu Upgrade 
  
  - Indy Shared GHA Repo
    
    - Pipeline completed
  - Indy-Plenum Status: 
    
    - Pipeline completed and RC released
  - Indy-Node Status:
    
    - Pipeline completed and RC released
  - indy-test-automation Status:
    
    - To be integrated into the release workflows.
  - indy-node-container (moved to Hyperledger) and GitPod tools available (node and plenum)
  - Indy-SDK build progress
    
    - Unblocked – builds are going and PRs are being reviewed (and rebasing PRs).
  
  <!--THE END-->
  
  - Backlog Issue: Mixed OS versions of Indy Node have issues:
    
    - How are we going to work through this issue and upgrade the various networks?
    - Issue: - running mixed nodes 16.04 and 20.04 a consensus problem occurs "in a while" (sometimes immediately, sometimes a few days has been seen)
      
      - 2022.06.07
        
        - Indicio team is working on a docker environment to replicate this, they are expecting to have something running in a few days.
        - docker-compose, 4 nodes (3 16.04 and 1 20.04), running for a week, but not able to replicate the issue.
        - Lynn to share how to do this publicly so that others could contribute.
          
          - Put a folder into the indy-node-container repo about how to do it.
        - Plan is to use indy-vdr to generate DIDs and publish them to the ledger.
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464593/19466172.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
