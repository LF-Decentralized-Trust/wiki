1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-06-21 Indy Contributors Call

Created by Stephen Curran, last modified on Jun 21, 2022

## Summary

- Update on the Indy Ubuntu 20.04 Upgrade
- Investigating the "Mixed Node" issue
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;

[Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio PBC) &lt;lynn@indicio.tech&gt;

[Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence)(Indicio PBC) &lt;char@indicio.tech&gt;

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
  - Indy-Plenum:
  - Indy-Node:
  - indy-test-automation:
  - indy-node-container:
    
    - Call time changed – 17:00 CET / 8:00 Pacific on Thursdays.
  - Indy-SDK build progress
  
  <!--THE END-->
  
  - Issue: Mixed OS versions of Indy Node have issues:
    
    - Issue: - running mixed nodes 16.04 and 20.04 a consensus problem occurs "in a while" (sometimes immediately, sometimes a few days has been seen)
      
      - 2022.06.21
        
        - Two efforts trying to replicate the problem [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (rust script to generate load) and Gavin Bendixsen (PR to indy\_node\_container), working on adding a node
        - At this point, the issue has not been replicated.
        - There is an indy node load generator - [https://github.com/hyperledger/indy-node/tree/master/scripts/performance](https://github.com/hyperledger/indy-node/tree/master/scripts/performance)
        - Another plan of attack: Use old artifact to try to recreate, try again with RC and see if that replicates the issue.
        - Note from Lynn: He has seen and documented consensus issues in the past – maybe this has nothing to do with 20.04.
          
          - For example: 2 nodes went down seemingly together, restarted them and issue resolved.
      - 2022.06.07
        
        - Indicio team is working on a docker environment to replicate this, they are expecting to have something running in a few days.
        - docker-compose, 4 nodes (3 16.04 and 1 20.04), running for a week, but not able to replicate the issue.
        - Lynn to share how to do this publicly so that others could contribute.
          
          - Put a folder into the indy-node-container repo about how to do it.
        - Plan is to use indy-vdr to generate DIDs and publish them to the ledger.
  - Related work - Sovrin token-plugin repo being reworked to match indy-node/plenum.
    
    - Mostly done the code.
    - Working on the pipeline
    - Linting issues documented and being cleaned
      
      - [https://github.com/sovrin-foundation/token-plugin/issues/413](https://github.com/sovrin-foundation/token-plugin/issues/413)

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464595/19466185.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
