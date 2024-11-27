1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-01-18 Indy Contributors Call

Created by Robin Klemens, last modified by Paul on Jan 19, 2022

## Summary

- Status of indy-node CI/CD and the Ubuntu upgrade
- did:indy DID Method PR review
- Getting started on the "did:indy" DID Method development work

## Recording of Call: [dummyfile.txt](#)

## Chat from Call:

- 08:28:47 From Wade Barnes : I have one Indy-SDK related topic before we end. We’ve been getting a fair number of contributors lately. The builds are failing due to Rust build dependency issues. I’m thinking I need to dig into and resolve that sooner than later. Agreed?
- 08:30:39 From Robin Klemens : @Wade. I agree since Indy-Node still relies on Indy SDK and we need a running CD pipeline there. Otherwise, the contributions won't help the community
- 08:37:36 From Dominic : The public key is generated from the private key using the Elliptic Curve Digital Signature Algorithm. You get a public address for your account by taking the last 20 bytes of the Keccak-256 hash of the public key and adding 0x to the beginning.
- 08:37:52 From Dominic : Source: [https://ethereum.org/en/developers/docs/accounts/#account-creation](https://ethereum.org/en/developers/docs/accounts/#account-creation)
- 08:38:13 From Paul Bastian : so they are using the hash of the whole public key and thats what we should do as well
- 08:38:59 From Paul Bastian : did:indy:sovrin:staging:6cgbu8ZPoWTnR5Rv5JcSMB
  
  did:indy:sovrin.staging:6cgbu8ZPoWTnR5Rv5JcSMB
- 08:39:56 From Robin Klemens : Isn't that the idea behind hashing? At any given input create a unique hash value at a specific length
- 08:42:44 From Paul Bastian : technically right Robin, but it makes sense to take the highest entropy available anyway
- 08:43:23 From Robin Klemens : which is the whole public key rather than just a fraction of it
- 08:44:28 From Paul Bastian : did:indy universal resolver driver mvp:
  
  [https://github.com/IDunion/indy-did-resolver](https://github.com/IDunion/indy-did-resolver)
- 08:45:35 From Paul Bastian : its kind of a mess, but a first working example that provides the minimal did document from a NYM
- 08:47:36 From Dominic : Awesome!

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@[cloudcompass.ca](http://cloudcompass.ca)&gt;
- [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)  (Institute for Internet Security) &lt;[klemens@internet-sicherheit.de](mailto:klemens@internet-sicherheit.de)&gt;
- [Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatusAG) &lt;p.schlarb@esatus.com&gt;
- [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence) (TU Berlin) &lt;hakan.yildiz@tu-berlin.de&gt;
- [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH)  &lt;ChristianCarl.Bormann@de.bosch.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio, PBC) &lt;lynn@indicio.tech&gt;
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)

## Related Calls and Announcements

BC Gov Indy DID Method Code With Us opportunity: [https://digital.gov.bc.ca/marketplace/opportunities/code-with-us/e3dd1605-cc1d-4c30-a9ee-245940bccd0d](https://digital.gov.bc.ca/marketplace/opportunities/code-with-us/e3dd1605-cc1d-4c30-a9ee-245940bccd0d)

- Indicio PBC will be doing Phase 1-3 (Scoping/Planning, Indy Node/Plenum Development, CI/CD)
- Dominic Wörner will be doing Phase 4 (Indy VDR changes)

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - [indy-node-container](https://github.com/IDunion/indy-node-container/tree/main/controller) Crisitan Kubis ( [https://github.com/tsurai](https://github.com/tsurai) ), has created a Node Controller Container ([docs](https://github.com/IDunion/indy-node-container/tree/main/controller)), allows containerized indy nodes to participate in pool restart and upgrade
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ( [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)

## Meeting Topics

- Developer Experience:
  
  - Recent merges...  [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - Indy-Plenum Status: 
    
    - Done, 16.04, 20.04, Jenkins and GHA
  - Indy-Node Status:
    
    - Done, 16.04, 20.04, Jenkins and GHA
    - One 20.04 running in the IDUnion network of 16.04 nodes
    - Merged PRs:
      
      - Automated indy-test-automation (w00t!!) - [https://github.com/hyperledger/indy-node/pull/1725](https://github.com/hyperledger/indy-node/pull/1725)
        
        - 16.04, prepared for 20.04 – need the systemd image to support 20.04
      - Documentation for creating new network: [https://github.com/hyperledger/indy-node/pull/1689](https://github.com/hyperledger/indy-node/pull/1689)
    - Ready to do a first release - working towards that.
      
      - Artifacts being produced and consumed from Artifactory
      - Move all within Hyperledger GitHub
      - Ready to produce a release
  - indy-test-automation Status:
    
    - Merged (no circular dependencies!!!!!) - 16.04
    - Still to be done: 20.04 – systemd image needs to be replaced – may have to be created.
    - Workflow to trigger - needs a secret setup / [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) - Done - can't be run for a PR, just for an RC or manually triggered
  - Currently releasing development artifacts – left to do is a tag-based official release process - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) with help from [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
  - \** Sovrin Release - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) Status:
    
    - Working ready to start in the three repos in Sovrin
- Scoping/Planning the ["did:indy" DID Method](https://hyperledger.github.io/indy-did-method/)
  
  - Pull Requests:
    
    - Privacy Considerations - [#29](https://github.com/hyperledger/indy-did-method/pull/29) - Merged
    - Security Considerations - [#28 - Merged](https://github.com/hyperledger/indy-did-method/pull/28)
    - New method for self-certifying NYMs - [#26](https://github.com/hyperledger/indy-did-method/pull/26)
      
      - Change to use SHA-256, but use the full public key as input
    - Proposal - change the separator for the sub-network from ":" to "." - [#25](https://github.com/hyperledger/indy-did-method/pull/25)  - Merged
    - Fix Typos - [#24](https://github.com/hyperledger/indy-did-method/pull/24)
    - Add the new Indy DID method to the W3C registry: [https://github.com/w3c/did-spec-registries](https://github.com/w3c/did-spec-registries) - [#393](https://github.com/w3c/did-spec-registries/pull/393)
      
      - Updated to reflect merges and now approved.
  - Next Steps:
    
    - Itemizing the work – particularly in Indy Node/Plenum
      
      - Indy HIPE?
    - Code evaluation to feedback into the specification – are there easier ways to accomplish some of the goals?
  - Issue: If Indy SDK is not updated, how do we run the Indy Node/Plenum tests?  TBD

## Future Calls

- Ideas for "Good First Task" for the Indicio class coming up in two weeks
- Issues that could impact indy-node on 20.04
  
  - indy-sdk: needs an upgrade to OpenSSL 1.1 to properly support Ubuntu 18.04/20.04.  For indy-node, just using indy-sdk as is.
  - Multiple libsodium versions could impact consensus – intermittent issue on a mixed network.
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

![](images/icons/bullet_blue.gif) [20220118 Indy Contributors Call Text.txt](attachments/19464548/19465958.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464548/19465957.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464548/19465942.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
