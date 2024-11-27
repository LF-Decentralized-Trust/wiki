1. [Hyperledger Fabric](index.html)
2. [Hyperledger Fabric](Hyperledger-Fabric_22839309.html)
3. [Contributor Meetings](Contributor-Meetings_22840714.html)

# Hyperledger Fabric : Contributor Meetings 2023

Created by David Enyeart, last modified on Dec 12, 2023

**January 11, 2023**

- Fabric v2.5 update – new ARM images and binaries
- Fabric v3 update – Smart BFT
- Admin SDK project - [https://github.com/hyperledger/fabric-admin-sdk](https://github.com/hyperledger/fabric-admin-sdk)
- Chaincode builder for kubernetes RFC
- Microfab lab - [https://github.com/hyperledger-labs/microfab](https://github.com/hyperledger-labs/microfab)

**February 8, 2023**

- Fabric v2.5 beta
- Fabric v3 update – Smart BFT
- Performance doc and blog
  
  - [https://hyperledger-fabric.readthedocs.io/en/latest/performance.html](https://hyperledger-fabric.readthedocs.io/en/latest/performance.html)
  - [https://www.hyperledger.org/blog/2023/02/16/benchmarking-hyperledger-fabric-2-5-performance](https://www.hyperledger.org/blog/2023/02/16/benchmarking-hyperledger-fabric-2-5-performance)
- Admin SDK project - [https://github.com/hyperledger/fabric-admin-sdk](https://github.com/hyperledger/fabric-admin-sdk)
- Project recommendations

**March 8, 2023**

- **Fabric recent releases**
  
  - Fabric v2.2.10 LTS – dependency updates
  - Fabric v2.4.9 – fixes including orderer cert renew without system channel

<!--THE END-->

- **Next Fabric release – v2.5.0-beta available**
  
  - Purge history of private data
  - Dependency updates
  - Next LTS release
  - ARM binaries and images (relief for M1!)
  - Remaining issue – update MSP for Go 1.19 - [https://github.com/hyperledger/fabric/pull/3774](https://github.com/hyperledger/fabric/pull/3774)

<!--THE END-->

- **Fabric v3 development - SmartBFT**
  
  - First pass of end-to-end integration merged in main branch, working on docs and sample for an early tech preview release - v3.0.0-preview?
  - Then will tackle some of the larger refactoring around “inversion of control” for orderer binaries per consensus algorithm (Raft, SmartBFT)
  - Need to address Raft CI failures in unit tests and integration tests

<!--THE END-->

- **Admin SDK for chaincode and channel management**
  
  - Developing a Go admin SDK - [https://github.com/hyperledger/fabric-admin-sdk](https://github.com/hyperledger/fabric-admin-sdk)

<!--THE END-->

- **New Hyperledger lab for Fabric Ansible Collection**
  
  - Automate the building of Hyperledger Fabric networks, uses fabric-operator lab
  - [https://github.com/hyperledger-labs/fabric-ansible-collection](https://github.com/hyperledger-labs/fabric-ansible-collection)

**April 5, 2023**

- **Fabric v2.5.0 released**
  
  - Purge history of private data
  - Dependency updates
  - ARM binaries and images (relief for M1!) - same updates in Fabric CA v1.5.6
  - Current LTS release - Users should evaluate upgrade from prior v2.2 LTS release

<!--THE END-->

- **Legacy SDK deprecation**
  
  - The legacy Fabric SDKs are deprecated.
    
    - Fabric SDK for Node v2.2, Fabric SDK for Java v2.2, Fabric SDK for Go v1.0
  - Users of the legacy SDKs are encouraged to evaluate the Fabric Gateway client API as a replacement.
    
    - Fabric Gateway client API is the recommended SDK for client applications when using Fabric v2.4 or v2.5
    - Available in Go, Node, and Java programming languages.
    - Fabric Gateway information - [https://hyperledger-fabric.readthedocs.io/en/release-2.5/whatsnew.html#fabric-gateway](https://hyperledger-fabric.readthedocs.io/en/release-2.5/whatsnew.html#fabric-gateway)
    - Fabric Gateway client API documentation - [https://hyperledger.github.io/fabric-gateway/](https://hyperledger.github.io/fabric-gateway/)
    - Fabric Gateway client API migration guide [https://hyperledger.github.io/fabric-gateway/migration](https://hyperledger.github.io/fabric-gateway/migration)

<!--THE END-->

- **Current Fabric priorities**
  
  - v2.2.11 - Update Go to v1.20; update other dependencies for prior LTS release
  - v3.0 preview for SmartBFT - Create usage documentation and sample
  - Fix Raft unit test and integration test CI flake failures
  - fabric-samples and fabric-test CI streamlining - reduce redundant tests
  - New issue template - [https://github.com/hyperledger/fabric/issues/4143](https://github.com/hyperledger/fabric/issues/4143)

<!--THE END-->

- **Admin SDK**
  
  - Call for test and feedback
  - Prepare 1st release if there is no further feedback after close [#105](https://github.com/hyperledger/fabric-admin-sdk/issues/105) and [#100](https://github.com/hyperledger/fabric-admin-sdk/issues/100)
  - Question as [#105](https://github.com/hyperledger/fabric-admin-sdk/issues/105), for external chaincode service, should we use ccaas or external as type in metadata.json?

**May 3, 2023**

- **Fabric releases**
  
  - Fabric v2.2.11 released - update to Go 1.20.3 and other dependencies to resolve vulnerabilities (*prior LTS release)*
  - Fabric v2.5.1 released - update to Go 1.20.3 (*current LTS release)*

<!--THE END-->

- **Current Fabric priorities**
  
  - v3.0 preview for SmartBFT - Create usage documentation and sample
  - Fix Raft unit test and integration test CI flake failures
  - fabric-samples test-network-k8s - Tatsuya Sato volunteered to fix issues with v2.5 and maintain going forward
  - Improve CI time
    
    - Trial of large runners in fabric and fabric-samples main branches working well - no queueing, faster execution
    - fabric-samples and fabric-test CI streamlining - reduce redundant tests

<!--THE END-->

- **Admin SDK**
  
  - Call for test and feedback
  - Prepare 1st release with [#121](https://github.com/hyperledger/fabric-admin-sdk/pull/121) leaving [#100](https://github.com/hyperledger/fabric-admin-sdk/issues/100) as open question.
  - [#122](https://github.com/hyperledger/fabric-admin-sdk/discussions/122) for 2nd version planning.

**May 31, 2023**

- **Fabric releases**
  
  - Fabric v2.5.2 coming soon - fixes and update to Go 1.20.4 (*current LTS release)*

<!--THE END-->

- **Current Fabric priorities**
  
  - v3.0 preview for SmartBFT - Create usage documentation and sample
  - Fix Raft unit test and integration test CI flake failures
  - fabric-samples test-network-k8s - DONE - Updated to v2.5, thanks to new fabric-samples maintainer Tatsuya Sato!
  - Improve CI time
    
    - Trial of large runners in fabric and fabric-samples main branches working well - no queueing, faster execution
    - fabric-samples and fabric-test CI streamlining - reduce redundant tests

<!--THE END-->

- **Admin SDK**
  
  - We have new feature request which blocks tag v0.0.0 release.
  - We are looking for use case for example, [https://github.com/hyperledger/fabric-cli](https://github.com/hyperledger/fabric-cli) or [https://github.com/hyperledger-labs/fabric-operator/tree/main](https://github.com/hyperledger-labs/fabric-operator/tree/main)
  - Waiting for [https://github.com/hyperledger/fabric-config/issues/53](https://github.com/hyperledger/fabric-config/issues/53) if there any chance for invoke fabric-config.

**June 28, 2023 - Meeting cancelled this month**

**July 19, 2023**

- **Fabric releases**
  
  - Fabric v2.2.12 - June 2 *(prior LTS release)*
    
    - Fix private data collection update during state database rebuild
  - Fabric v2.5.3 - June 14 *(current LTS release)*
    
    - Fix deadlock can occur on orderer startup while applying raft configuration changes
    - Go 1.20.5
  - Fabric v2.5.4 - Coming Soon
    
    - backport cert sanitization error checking - [https://github.com/hyperledger/fabric/pull/4307](https://github.com/hyperledger/fabric/pull/4307)
    - Go 1.20.6

<!--THE END-->

- **Recent improvements**
  
  - New Github Action - doc broken link checker - [https://github.com/hyperledger/fabric/actions/workflows/broken-link-checker.yml](https://github.com/hyperledger/fabric/actions/workflows/broken-link-checker.yml)

<!--THE END-->

- **Current Fabric priorities**
  
  - v3.0 - preview for SmartBFT - Create usage documentation and sample
  - v3.0 - ledger block cache
  - Fix Raft unit test and integration test CI flake failures
  - fabric-ca - fix CI issue
  - [Hyperledger Fabric Certified Practitioner](https://training.linuxfoundation.org/certification/hyperledger-fabric-certified-practitioner-hfcp/) - Exam is being created - any volunteers to draft questions?

<!--THE END-->

- **Chaincode builder discussion** - see [https://github.com/hyperledger/fabric/issues/3984](https://github.com/hyperledger/fabric/issues/3984).

<!--THE END-->

- **Admin SDK**
  
  - Draft release for fabric-cli investigation
  - issue found

<!--THE END-->

- **fabric 2.5 i18n zh document**

**August 16, 2023**

- **Recent Fabric releases**
  
  - Fabric v2.2.13 - August 2 *(prior LTS release)*
    
    - cert sanitization error checking
    - Go 1.20.6
  - Fabric v2.5.4 - August 2 *(current LTS release)*
    
    - Fix orderer startup issue - raft wal: max entry size limit exceeded
    - cert sanitization error checking
    - Go 1.20.6

<!--THE END-->

- **Fabric v3.0 work items**
  
  - Preview release for SmartBFT
    
    - Create usage documentation and sample
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer and the orderer
    - Improved transaction pool for SmartBFT
    - Unit test coverage for SmartBFT chain
    - Integration test coverage for SmartBFT orderer
  - Ledger block cache [PR](https://github.com/hyperledger/fabric/pull/4303) to improve performance
  - Plan for other v3.0 changes, e.g. removal of old lifecycle, removal of gossiping of blocks

<!--THE END-->

- **Admin SDK**
  
  - 1.0 released with feature which integrated with test-network with code as e2e test in golang as implementation.
  - Fabric cli integration and bug fix?
  - Open to any integration with tools as either operator or anything you want.

<!--THE END-->

- **Other**
  
  - Fix Raft unit test and integration test CI flake failures
  - [Hyperledger Fabric Certified Practitioner](https://training.linuxfoundation.org/certification/hyperledger-fabric-certified-practitioner-hfcp/) - Exam is being created - any volunteers to draft questions?

**September 13, 2023**

- **Recent Fabric releases**
  
  - Fabric v3.0.0-preview - September 1
    
    - SmartBFT technical preview
    - See mailing list [announcement](https://lists.hyperledger.org/g/fabric/message/11958) for details
  - Fabric CA v1.5.7
    
    - IdentityMixer revocation enhancements
    - Go v1.20.5

<!--THE END-->

- **Fabric v3.0 work items**
  
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer and the orderer
    - Improved transaction pool for SmartBFT
    - Unit test coverage for SmartBFT chain
    - Integration test coverage for SmartBFT orderer
  - Plan for other v3.0 changes, e.g. removal of old lifecycle, removal of gossiping of blocks
  - Fix Raft unit test and integration test CI flake failures
  - fabric-samples CI test failures

<!--THE END-->

- **Admin SDK**
  
  - update with test guidance wiki as [link](https://github.com/hyperledger/fabric-admin-sdk/wiki/How-to-test-integrate-admin-sdk-with-your-project)

<!--THE END-->

- **Other**
  
  - [RFC to extend queryapproved](https://github.com/hyperledger/fabric-rfcs/pull/45) function for all chaincodes
  - [Hyperledger Fabric Certified Practitioner](https://training.linuxfoundation.org/certification/hyperledger-fabric-certified-practitioner-hfcp/) - Exam has been beta tested, will be available soon!
  - [CC-Tools lab proposal](https://github.com/GoLedgerDev/hyperledger-labs.github.io/blob/main/labs/CC-Tools.md)
  - [Understanding Byzantine Fault Tolerance in Hyperledger Fabric](https://urldefense.proofpoint.com/v2/url?u=https-3A__www.meetup.com_hyperledger-2Dzug-2Dzurich_events_295600194_&d=DwMFaQ&c=jf_iaSHvJObTbx-siA1ZOg&r=FWiwMUSIAq7Ii1KJX8rdZWEsrplZzcrGwWreBa-fmbA&m=rEvUmojMUf0z_RH1X5iwGWe3aHBib0WUszh_Kv0bis62NqJtfnXgCkbY9VqCilDe&s=0X7lLtbmIO-EklmTAz-xNmFlZhPbfcMl4Ga6QPnrr6U&e=) - meetup - October 3
  - [Create a Currency Management Application](https://lf-hyperledger.atlassian.net/wiki/display/events/Create+a+Currency+Management+Application) - workshop October 12

**October 11, 2023**

- **Upcoming Fabric releases**
  
  - Fabric v2.2.14, v2.5.5
    
    - Go 1.21

<!--THE END-->

- **Fabric v3.0 work items**
  
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer and the orderer
    - Improved transaction pool for SmartBFT
    - Unit test coverage for SmartBFT chain
    - Integration test coverage for SmartBFT orderer
  - [Transition from](https://github.com/hyperledger/fabric/issues/4468) [github.com/pkg/errors](http://github.com/pkg/errors)
  - [Extend to lifecycle chaincode checkcommitreadiness to provide details of the discrepancies](https://github.com/hyperledger/fabric/issues/4428)
  - Plan for other v3.0 changes, e.g. removal of old lifecycle, removal of gossiping of blocks

<!--THE END-->

- **Admin SDK**

<!--THE END-->

1. - Hope to build fabric-cli base on admin sdk to reduce effort on golang package version dependency.
   - Seems new configtx structure in fabric 3.0 preview makes different with fabric 2.x ([https://github.com/hyperledger/fabric/issues/4459](https://github.com/hyperledger/fabric/issues/4459))
   - some basic function supporting([https://github.com/hyperledger/fabric-admin-sdk/pull/139](https://github.com/hyperledger/fabric-admin-sdk/pull/139))

<!--THE END-->

- **Other**
  
  - [RFC to extend queryapproved](https://github.com/hyperledger/fabric-rfcs/pull/45) function for all chaincodes
  - [Hyperledger Fabric Certified Practitioner](https://training.linuxfoundation.org/certification/hyperledger-fabric-certified-practitioner-hfcp/) - Exam is available!
  - [Create a Currency Management Application](https://lf-hyperledger.atlassian.net/wiki/display/events/Create+a+Currency+Management+Application) - privacy preserving token transfer workshop October 12

**November 8, 2023**

- **Recent Fabric releases**
  
  - Fabric v2.2.14, v2.5.5
    
    - Go 1.21
    - Additional block validations

<!--THE END-->

- **Fabric v3.0 work items**
  
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer and the orderer
    - Improved transaction pool for SmartBFT
    - Unit test coverage for SmartBFT chain
    - Integration test coverage for SmartBFT orderer
  - [Transition from](https://github.com/hyperledger/fabric/issues/4468) [github.com/pkg/errors](http://github.com/pkg/errors)
  - Plan for other v3.0 changes, e.g. removal of old lifecycle, removal of gossiping of blocks

<!--THE END-->

- **Admin SDK**

<!--THE END-->

1. - admin cli pr poc [https://github.com/hyperledger/fabric-admin-sdk/pull/146](https://github.com/hyperledger/fabric-admin-sdk/pull/146) need suggestion and feedback for current attempts, before moving next.
   - Seems new configtx structure in fabric 3.0 preview makes different with fabric 2.x ([https://github.com/hyperledger/fabric/issues/4459](https://github.com/hyperledger/fabric/issues/4459))

<!--THE END-->

- **Fabric Ecosystem update**

<!--THE END-->

- **Other**
  
  - [RFC to extend queryapproved](https://github.com/hyperledger/fabric-rfcs/pull/45) function for all chaincodes
  - [https://github.com/hyperledger/fabric-docs-i18n/pull/920](https://github.com/hyperledger/fabric-docs-i18n/pull/920) Fabric v2.5 Chinese doc translation PR

**December 6, 2023**

- **Fabric v3.0 work items**
  
  - Finalize SmartBFT for eventual production GA release
    
    - Byzantine block puller for the peer and the orderer - Yoav
    - Improved transaction pool for SmartBFT - Hagar
    - Unit test coverage for SmartBFT chain - Emil
    - Integration test coverage for SmartBFT orderer - May, Arkadi
    - Migration from Raft to SmartBFT - Yacov, May, Yoav
    - Inversion of control - one binary per consensus algorithm - Deferred from v3.0
  - [Transition from](https://github.com/hyperledger/fabric/issues/4468) [github.com/pkg/errors](http://github.com/pkg/errors)
  - Plan for other v3.0 changes, e.g. removal of old lifecycle (started), removal of gossiping of blocks (likely deferred)

<!--THE END-->

- **Other**
  
  - [RFC to extend queryapproved](https://github.com/hyperledger/fabric-rfcs/pull/45) function for all chaincodes - Approved
  - CI - Azure Pipelines migration to GitHub Actions - final repository is fabric-test, some tests will be retired
  - Hyperledger Member Summit APAC was held

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
