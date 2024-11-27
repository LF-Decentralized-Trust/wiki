1. [Hyperledger Fabric](index.html)
2. [Hyperledger Fabric](Hyperledger-Fabric_22839309.html)
3. [Contributor Meetings](Contributor-Meetings_22840714.html)

# Hyperledger Fabric : Contributor Meetings 2024

Created by David Enyeart, last modified on Nov 23, 2024

**January 17, 2024 ([recording](https://www.youtube.com/watch?v=PuQOD8MC4T0))**

- **Fabric v3.0 work items**
  
  - [RFC to extend queryapproved](https://github.com/hyperledger/fabric-rfcs/pull/45) function for all chaincodes - Completed (thank you Tatsuya Sato)
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer (merged) and the orderer (in progress) - Yoav
    - Improved transaction pool for SmartBFT - Hagar
    - Unit test coverage for SmartBFT chain - Emil
    - Integration test coverage for SmartBFT orderer - May, Arkadi
    - Migration from Raft to SmartBFT - Yacov, May, Yoav
    - Inversion of control - one binary per consensus algorithm - Deferred from v3.0
  - Removal of old lifecycle - Artem
  - [Transition from](https://github.com/hyperledger/fabric/issues/4468) [github.com/pkg/errors](http://github.com/pkg/errors)
  - [Protocol buffer APIv2](https://github.com/hyperledger/fabric/issues/3650)
  - Removal of gossiping of blocks (likely deferred)

<!--THE END-->

- **CI - Azure Pipelines migration to GitHub Actions**
  
  - Complete for most fabric repositories
  - Subset of fabric-test tests moved to GitHub actions (HSM test)
  - Retire SDK and Chaincode interop tests in fabric-test in favor of scheduled testing in SDK and Chaincode repositories (test against Fabric v2.5 and v3.0?)
  - Switch fabric development docker images from jfrog artifactory to github package registry

<!--THE END-->

- **Admin sdk**
  
  - 3.0 bft preview supported
  - Create feature branch for CLI use of admin SDK - Dave

**February 21, 2024 ([recording](https://youtu.be/kFnC0c3SP2U))**

- **Recent Fabric releases**
  
  - Fabric v2.2.15, v2.5.6, CA v1.5.9
    
    - Dependency updates
    - Remove dependency between Fabric CA and Fabric (common code pushed down to fabric-lib-go)

<!--THE END-->

- **Fabric v3.0 work items**
  
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer (merged) and the orderer (in progress) - Yoav
    - Improved transaction pool for SmartBFT - defer based on performance trial
    - Unit test coverage for SmartBFT chain - in progress - Emil
    - Integration test coverage for SmartBFT orderer - in progress - May, Arkadi
    - Migration from Raft to SmartBFT - done

**March 20, 2024 ([recording](https://youtu.be/yK_VG0yijc8))**

**- Fabric v3.0.0-beta ([announcement](https://lists.hyperledger.org/g/fabric/message/12191)) - March 14**

**- Logo update ([charts](https://www.canva.com/design/DAF95dr6sQk/rLWvQbEMDhasZvdeQ1cKJQ/view))**

**- Remaining items for production v3.0 release**

- Already removed features
  
  - system channel
  - solo ordering
  - kafka ordering
- Need to finish
  
  - Finish SmartBFT tests, SmartBFT library moved to hyperledger-labs already
  - Finish v1 chaincode lifecycle removal - keep external APIs but just return an error message - Artem finishing it out
- Deprecated features in v2 that could potentially be removed in v3
  
  - Specifying orderer endpoints at the global level in channel configuration (instead, utilize v2 'OrdererEndpoints' in org config) - let's remove it, Yacov will find someone
  - configtxgen flag `--outputAnchorPeersUpdate`  flag (instead, utilize channel config updates) - let's remove it, Tatsuya will take it
  - fabric-tools image (instead, utilize client connection to network), note fabric-tools still used by fabric-samples as a convenience for jq commands - Sam will assess
  - Block dissemination via gossip (instead, configure all peers as org leaders to receive blocks from ordering service). Minimally, let's set blockGossipEnabled default to false.
- [#3663](https://github.com/hyperledger/fabric/issues/3663) Fabric v3 epic misc items 
  
  - [#3306](https://github.com/hyperledger/fabric/issues/3306) new channel config for CouchDB max\_document\_size, use during validation to prevent transactions too large to persist, along with application capability - Dave will assess
  - [#3650](https://github.com/hyperledger/fabric/issues/3650) fabric-protos Go bindings based on protocol buffer APIv2 (v1 protobuf is deprecated) - potential deferral
  - [#3704](https://github.com/hyperledger/fabric/issues/3704) older v3 ideas from Jira - e.g. Remove support for remaining Go plugins (endorsement and validation plugins) - potential deferral
  - [#3343](https://github.com/hyperledger/fabric/pull/3343) ed25519 support
- Identity Mixer replacement proposal from Ale
  
  - Update Idemix to use the aries-provided, standard-draft-compatible implementation as opposed to the legacy implementation used in Fabric v2. Fabric v2 would still uses the legacy implementation of idemix, which is still available. For v3 switch fabric to use the new implementation. The change will not be backward-compatible so existing networks that use the legacy fabric implementation will need to remain on Fabric v2.
  - The new idemix implementation would no longer be supported by fabric-ca. Idemixgen would be the default issuance tool. Users could build customised issuing services using idemixgen as a library.

**April 17, 2024 ([recording](https://www.youtube.com/watch?v=NCt03lCL_gs))**

- **Recent Fabric releases**
  
  - Fabric v2.5.7, CA v1.5.10
    
    - Dependency updates
    - Note that v2.2 is no longer being maintained, users are encouraged to upgrade to v2.5 LTS release

<!--THE END-->

- **Fabric v3**
  
  - See prior meeting for notes on remaining items.
  - Progress has been made on removing [`--outputAnchorPeersUpdate` flag](https://github.com/hyperledger/fabric/pull/4809), removing [global orderer endpoints](https://github.com/hyperledger/fabric/pull/4800), and removing [fabric-tools image](https://github.com/hyperledger/fabric/pull/4775).
  - Still need to complete:
    
    - SmartBFT final tests
    - v1 lifecycle removal
    - channel config for CouchDB max\_document\_size
    - Identity Mixer update - current thinking is to defer any changes from v3.

<!--THE END-->

- **Chaincode builders/launchers and k8s builder** - James Taylor
  
  - [https://github.com/hyperledger-labs/fabric-builder-k8s/issues/111](https://github.com/hyperledger-labs/fabric-builder-k8s/issues/111)

<!--THE END-->

- **fabric-admin-sdk**  - Sam  Yuan
  
  - [https://github.com/hyperledger/fabric-admin-sdk/discussions/187](https://github.com/hyperledger/fabric-admin-sdk/discussions/187#discussioncomment-9137289)

**May 15, 2024 ([recording](https://youtu.be/Cm7MMWc3q8I))**

**- Remaining items for production v3.0 release**

- Previously deprecated features that have already been removed in v3 main branch
  
  - system channel
  - solo ordering (instead, utilize single node Raft)
  - kafka ordering (instead, utilize Raft)
  - configtxgen flag `--outputAnchorPeersUpdate`  flag (instead, utilize channel config updates)
  - fabric-tools image (instead, utilize client connections into Fabric networks)

<!--THE END-->

- Need to finish
  
  - Finish SmartBFT
    
    - Finish tests
    - Fix frequent test failures in SmartBFT unit tests and integration test
    - Allow the peer delivery client to select between Deliverer or BFTDeliverer - PR [#4856](https://github.com/hyperledger/fabric/pull/4856)
  - Finish v1 chaincode lifecycle removal - keep external APIs but just return an error message - Tatsuya can help Artem
  - Remove ability to specify orderer endpoints in channel configuration at global level 'Orderer.Addresses' as deprecated in v2 (instead, utilize v2 'OrdererEndpoints' in org config) - PR [#4800](https://github.com/hyperledger/fabric/pull/4800)
  - Change peer property blockGossipEnabled default to false - Block dissemination via gossip already deprecated in v2 (recommendation is to configure all peers as org leaders to receive blocks from ordering service).

<!--THE END-->

- [#3663](https://github.com/hyperledger/fabric/issues/3663) Fabric v3 epic misc items 
  
  - [#3306](https://github.com/hyperledger/fabric/issues/3306#issuecomment-2112287799) new channel config MaxWriteSize, prevents large writes that potentially exceeds CouchDB max\_document\_size
  - [#3343](https://github.com/hyperledger/fabric/pull/3343) ed25519 support
  - [#3650](https://github.com/hyperledger/fabric/issues/3650) fabric-protos Go bindings based on protocol buffer APIv2 (v1 protobuf is deprecated) - potential deferral
  - [#3704](https://github.com/hyperledger/fabric/issues/3704) older v3 ideas from Jira - e.g. Remove support for remaining Go plugins (endorsement and validation plugins) - potential deferral

**June 19, 2024 ([recording](https://youtu.be/lq-jw0u6-Nk))**

**- Recent Fabric releases**

- Fabric v2.5.9, CA v1.5.12 - June 18
  
  - Dependency updates

**- Remaining items for production v3.0 release**

- Previously deprecated features that have already been removed in v3 main branch
  
  - system channel
  - solo ordering (instead, utilize single node Raft)
  - kafka ordering (instead, utilize Raft)
  - Remove ability to specify orderer endpoints in channel configuration at global level 'Orderer.Addresses' as deprecated in v2 (instead, utilize v2 'OrdererEndpoints' in org config, enforced when channel capability at V3\_0 )
  - configtxgen flag `--outputAnchorPeersUpdate`  flag (instead, utilize channel config updates)
  - fabric-tools image (instead, utilize client connections into Fabric networks)

<!--THE END-->

- Need to finish
  
  - Finish SmartBFT
    
    - Finish tests
    - Fix frequent test failures in SmartBFT unit tests and integration test
  - Finish v1 chaincode lifecycle removal - keep external APIs but just return an error message - Tatsuya can help Artem
    
    - Legacy lifecycle has been removed from integration test and peer cli, meaning no one could use it.
    - Updated tests and removed logic that relied on legacy LCC.
    - What is still to be done?
      
      - Need to remove the initialization of the LSCC code as a chaincode (in progress)
      - Need to ensure peers won't crash in case we get connected to the legacy system, meaning the system is probably being upgraded. We need to ensure newly joined peers won't crash on instantiate transactions; the validation part should still be aware of these updates.
      - The last thing is mostly cosmetics to refactor the code to move or fuse legacy validation logic with new \_lifecycle.
      - Ensure all documentation is updated
  - Change peer property blockGossipEnabled default to false - Block dissemination via gossip already deprecated in v2 (recommendation is to configure all peers as org leaders to receive blocks from ordering service) - [https://github.com/hyperledger/fabric/pull/4911](https://github.com/hyperledger/fabric/pull/4911)

<!--THE END-->

- [#3663](https://github.com/hyperledger/fabric/issues/3663) Fabric v3 epic misc items 
  
  - [#3306](https://github.com/hyperledger/fabric/issues/3306#issuecomment-2112287799) new channel config MaxWriteSize, prevents large writes that potentially exceeds CouchDB max\_document\_size - defer
  - [#3343](https://github.com/hyperledger/fabric/pull/3343) ed25519 support

**July 17, 2024 ([recording](https://youtu.be/fytjclm2Rks))**

- Release update
  
  - Remaining v3 release work item - finish v1 chaincode lifecycle removal (see June update above for details)

<!--THE END-->

- Creating a project charter for Fabric - Sean Bohan (Linux Foundation)
  
  - [Draft project charter text](https://docs.google.com/open?id=1Gd4g_Y-TZVHVnpkQtLeIIdCBatIBGv1oIqyXYaXcpyw)
  - The goal of having project charters is to follow open source best practices and to make the governance of Hyperledger projects more clear, transparent, and easily discoverable
  - Please review by July 31 and make any edits if needed on the doc in suggestion mode so we can see what changes you are proposing
  - If you have any questions about this, let us know and we can help

<!--THE END-->

- v2 Go chaincode API (using v2 protocol buffers) - Mark Lewis

![](plugins/servlet/confluence/placeholder/unknown-attachment)

**August 21, 2024 ([recording](https://youtu.be/guZJxlvuc_k))**

- v3 release preparation
- - remove v1 capabilities? No...see [https://github.com/hyperledger/fabric/pull/4954](https://github.com/hyperledger/fabric/pull/4954)
  - blog post
  - documentation
- Fabric project charter

**September 18, 2024 ([recording](https://youtu.be/wAIf2Jmc8fg))**

- v3.0.0 release
  
  - release candidate - [https://github.com/hyperledger/fabric/releases/tag/v3.0.0-rc1](https://github.com/hyperledger/fabric/releases/tag/v3.0.0-rc1)
  - upgrade documentation - [https://hyperledger-fabric.readthedocs.io/en/latest/upgrade.html](https://hyperledger-fabric.readthedocs.io/en/latest/upgrade.html)
  - blog post - [https://www.lfdecentralizedtrust.org/blog/hyperledger-fabric-v3-delivering-smart-byzantine-fault-tolerant-consensus](https://www.lfdecentralizedtrust.org/blog/hyperledger-fabric-v3-delivering-smart-byzantine-fault-tolerant-consensus)
  - recent updates
    
    - ubuntu 20.04 → 22.04
    - utilize fabric-protos-go-apiv2 protocol buffer bindings (using new protocol buffers API, wire compatible with v2.5.x nodes)
    - continue to utilize existing node chaincode and java chaincode images with fabric v3.0 (fabric-nodeenv:2.5 and fabric-javaenv:2.5)

**November 20, 2024 ([recording](https://youtu.be/7eDfzRd3AXs))**

- Fabric v3.0.0 released September 20th - Feedback welcome on SmartBFT ordering feature
- Fabric v2.5.10 released September 20th - Current LTS release
- Call for contributors and maintainers
- [Push all Fabric images to Github Container Registry](https://github.com/hyperledger/fabric/issues/4998)
- RFC - [Improve chaincode performance by batching writes](https://github.com/hyperledger/fabric-rfcs/pull/58)

Document generated by Confluence on Nov 26, 2024 16:21

[Atlassian](http://www.atlassian.com/)
