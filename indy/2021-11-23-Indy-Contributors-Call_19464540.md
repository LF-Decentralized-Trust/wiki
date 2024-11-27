1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-11-23 Indy Contributors Call

Created by Stephen Curran, last modified by Wade Barnes on Nov 23, 2021

## Summary

- Status of indy-node CI/CD and the Ubuntu upgrade
- Containerized Indy Node + Controller Contribution from ID Union

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Wade Barnes (Neoteric Technologies Inc. ) &lt;[wade@neoterictech.ca](mailto:wade@neoterictech.ca)&gt;
- Robin Klemens  (Institute for Internet Security) &lt;[klemens@internet-sicherheit.de](mailto:klemens@internet-sicherheit.de)&gt;
- Sebastian Schmittner (EECC)&lt;[sebastian.schmittner@eecc.de](mailto:sebastian.schmittner@eecc.de) &gt;
- Philipp Schlarb
- Hakan Yildiz
- Paul Bastian
- Ayush Raj

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
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ( [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)

## Meeting Topics

- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - Indy-Plenum Status: 
    
    - Done
  - Indy-Node Status:
    
    - Done
  - indy-test-automation Status:
    
    - Progressing.  Tests are passing.
      
      - [https://github.com/hyperledger/indy-test-automation/pull/109](https://github.com/hyperledger/indy-test-automation/pull/109)
      - [https://github.com/udosson/indy-node/actions/runs/1495380875](https://github.com/udosson/indy-node/actions/runs/1495380875)
    - Missing a systemd images for Ubuntu 20.04
      
      - May need to create our own or updated the tests to not require the service arch.
      - The image is used to mimic a real network as closely as possible.
  - Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) Status:
    
    - No schedule yet.  Work needs to restarted.
- Docker Container for Indy Node Server + Controller
  
  - Crisitan Kubis ( [https://github.com/tsurai](https://github.com/tsurai) ) of the Institute for Internet Security, member of ID Union, has created a Node Controller Container in order to let containerized indy nodes participate in pool restart and upgrade
  - Modified controller files + Dockerfile: [https://github.com/IDunion/indy-node-container/tree/main/controller](https://github.com/IDunion/indy-node-container/tree/main/controller)
  - Runtime Setup: [https://github.com/IDunion/indy-node-container/blob/main/run/README.md#node-controller](https://github.com/IDunion/indy-node-container/blob/main/run/README.md#node-controller)

## Future Calls

- **Plans for a new Indy-SDK release?**
  
  - A few people from the community have asked.
  - The most recent request has been for a release to include this feature; [https://github.com/hyperledger/indy-sdk/pull/2400](https://github.com/hyperledger/indy-sdk/pull/2400)
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464540/19465909.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464540/19465907.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
