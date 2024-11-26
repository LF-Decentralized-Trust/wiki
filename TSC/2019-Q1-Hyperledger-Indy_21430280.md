1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q1 Hyperledger Indy

Created by Lynn Gray Bendixsen, last modified on Feb 06, 2019

Projects

##### Distributed Ledger

- [indy-node](https://github.com/hyperledger/indy-node)
- [indy-plenum](https://github.com/hyperledger/indy-plenum)

##### Client Tools

- [indy-sdk](https://github.com/hyperledger/indy-sdk)
- [indy-agent](https://github.com/hyperledger/indy-agent)

##### Shared Components

- [Indy-hipe](https://github.com/hyperledger/indy-hipe)
- [Indy-test-automation](https://github.com/hyperledger/indy-test-automation)
- [indy-crypto](https://github.com/hyperledger/indy-crypto)

Project Health

The contributors to Hyperledger Indy spent this past quarter working on these key initiatives:

1. Addressing ledger stability concerns raised during testing and during production outages of client networks.
2. Adding ledger monitoring to continue preparation for widespread usage.
3. Maturing agent standards to build ecosystem compatibility.
4. Developing reference agents so that they are usable by new participants in the ecosystem.
5. Documentation improvements to enhance ease of use and encourage new contributors.

These efforts have yielded significant results.

1. Ledger monitoring scripts have been implemented and real time notifications are in place and operational on some ledgers.
2. Work has accelerated significantly on agent standardization. Multiple implementations of agents are nearing the ability to connect to each other thanks to efforts from members of the community from many different organizations. An Agent “Connect-a-thon” is scheduled for this month (February) to demonstrate the ability to connect different agents, resolve any remaining issues, and determine next steps as a community. See [Agent Connectathon Agenda](https://docs.google.com/document/d/1dfGj5yjpSHzRF6UVPv7Ld1PTFme3fsXEwpLs0_e6NGA/edit#heading=h.ssygez1ks54i) .
3. Superb effort has been put in to consolidate the Hyperledger-Indy documentation for ease of use. See [hyperledger-indy.readthedocs.io](http://hyperledger-indy.readthedocs.io/) and [doc.sovrin.org](http://doc.sovrin.org/) .
4. Indy’s codebase has surpassed 17,000 commits from 143 unique contributors.
   

Issues

Our top issues from last quarter continue to be our central concerns, but we have made some useful progress.

### Ensure quality releases for downstream users

Improvements over last quarter have been made for this issue. Releases and deployment have been consistent and timely as improvements to the ledger have been tested and delivered.

Progress made:

- Continued improvements in the CI / CD pipeline have provided more reliable releases with consistent versions of components.

Further remediation planned:

- The Indy team will continue to focus on providing releases that can be immediately deployed downstream.
- The team is being more deliberate about preserving backwards compatibility. (More work is still needed here)

### Inconsistent documentation

Documentation quality and consolidation remains an important issue, but significant progress has been made to improve.

Progress made:

- In the past quarter we published consolidated documentation to shared sites:  [hyperledger-indy.readthedocs.io](http://hyperledger-indy.readthedocs.io/) and [doc.sovrin.org](http://doc.sovrin.org/) .

Further remediation planned:

- Publish the getting started resources somewhere that is public and likely to be found.
- Continue to consolidate redundant documentation and reworking it for different user levels.

### Incompatible agent implementations

Efforts are ongoing to increase interoperability between existing agent implementations and future implementations.

Progress made:

- Wire level message formatting has been established and merged into the Indy-SDK.
- An Agent “Connect-a-thon” will be held this month (February 19-22) demonstrating the ability of different agent implementations to connect and communicate over accepted protocols.
- Preliminary tests for connection protocol are implemented in the agent test suite and are ready for testing.
- Maintainers of libVCX have committed to implement the community approved protocols outlined in HIPEs.

Further remediation planned:

- Continue standardizing agent communication protocols, including credential exchange.
- Mature the agent test suite.

### Measuring the size and make-up of our user community

We began making progress on this issue by measuring the number of developers creating solutions by contributing to indy github projects.

Progress made:

- We are measuring GitHub contributors and can produce a week-by-week graph of contributors added over the last year.

Further remediation planned:

- Work with Hyperledger to get analytics about web sites, and Rocket Chat usage.
- Begin measuring usage of the Sovrin forums: new contributors, questions asked, and questions answered
- Measure Indy tags on Stack Overflow.

### Build Issues

Progress made:

- Significant effort has been made to move the building of client libraries and reference agents to the Sovrin Foundation and this work is nearing completion.

Further remediation planned:

- CI/CD pipelines will target prebuilt dependencies instead of building them from source.
- CI/CD pipelines will be put in place first before additional code changes are made.

# Releases

November 2018:

##### Indy SDK 1.6.8

- Fix State Proof verification for some types of GET requests to the ledger
- Additional clean-up for secrets in logs
- Update CLI help

### December 2018:

##### Indy SDK 1.7.0

- Added VCX - a library built over libindy for Verifiable Credentials eXchange. API is EXPERIMENTAL.
- - Mobile builds are not currently available - they will be added in future releases.
- Added Logging API
- - Added function indy\_get\_logger for plugins to give their logging to libindy.
  - Added function indy\_set\_logger for client apps and wrappers to receive logs from libindy
  - Integrated libindy logging into Slf4j for Java wrapper and into python logging facade.
- Updated API of Rust wrapper. Now there is not three methods for each API call, there is only one that returns Future.
- Introduced multithreading for Wallet API and CRED\_DEF generation.
- Bug fixes

##### Indy Node 1.6.79

- Fixes to improve stability.
- Output of validator-info changed and enhanced to meet growing need.
- Bug fixes

##### Indy Node 1.6.80

- Initial hotfixes for network stability issues.
- Pool restart will now work regardless of whether there is consensus on the ledger.

##### Indy Node 1.6.82

- Additional hotfixes for improved stability.

### January 2019:

No new releases

# Overall Activity in the Past Quarter

**General**

- Graduation from incubation status only requires 3 more action items:
  
  - An Indy use cases document (a community effort just started with  [this doc](https://docs.google.com/document/d/1EMiqzdd-6TB2puzamDGJSLrDTwUz_QW46xdEp2FLnbI/edit?usp=sharing)  )
  - Confirmation that indy projects implement perfect forward secrecy
  - Automated code coverage collection
    
    - This is very difficult considering our tech stack. There is active development on this front and it will hopefully be implemented soon.

**Indy Node**

- Significant focus on performance and stability. Several stability fixes have been implemented and ledgers are running better than ever.
- Continued research into a future ledger architecture.

**Indy SDK**

- Release of experimental LibVCX.
- Started work to support HIPEs defining Agent to Agent compatibility.
- The Indy team continues to work with other Hyperledger teams to transition from the indy-crypto component to Hyperledger Ursa.

##### **Indy Agent**

- Many HIPEs moved to accepted status.
- Significant iterations on and discussion surrounding several HIPEs.
- Increased collaboration with new contributors in the community.

# Current Plans

Additional organizations are making ongoing contributions. This is shown by the shared [Running Roadmap](https://wiki.hyperledger.org/projects/indy/roadmap) for Hyperledger Indy.

##### General

- Incubation status graduation.
- - Complete the three items mentioned earlier in this document and apply for graduation.
- Continue to refine documentation.
- - Consolidate documentation for onboarding contributors.
- Network stability of the first production deployment (Sovrin).
- Schema improvements!
  
  - We are currently working on enhanced schemas that will be compatible with the W3C Verifiable Credentials standards.   Our current credentials use schemas that are simple flat lists of untyped strings and this effort will allow complex data structures such as those available from [schema.org](http://schema.org/).
  - New encoding methods (to convert properties to signature values) and presentation (proof) requests will be able to preserve privacy and security through zero-knowledge proofs (ZKP) while maintaining the cryptographic assurances that the credential values have not been modified. The new encoding methods will expand the number of credential values that can be used in predicate proofs, such as "greater than", "less-than-or-equal", etc.
  - Schema re-use between Verifiable Credential issuers will promote interoperability.
- Indy Catalyst
  
  - The OrgBook implemented as part of British Columbia's Verifiable Organization Network (VON) is being contributed to Hyperledger as Indy Catalyst. It provides a template for bootstrapping credential ecosystems built on Indy.

##### Indy Node

- Consume official builds of Hyperledger Ursa (the shared crypto-lib), as they are approved.
- Further improvements to automated testing.
- Audit ledger
  
  - As we moved permission management to the config ledger, we identified the need for an audit ledger to make it easy to verify what permissions were in place with each write.
  - The audit ledger will also ensure deterministic catch-up between ledgers which resolves some BFT consensus corner cases.
- Research into Ledger 2.0
  
  - We are confident that Indy Node can scale to millions of users, but we have identified a number of problems with the existing implementation that will limit future scalability. Solutions are likely to require fundamental architectural changes.
  - Improve the stability and performance of View Change, Catch-up, and Replication.
  - Establish a cache for reads, such as observer nodes.
  - We are recruiting contributors from various organizations to assist in designing the future of the ledger and starting implementation.
- Broader OS support.

Indy SDK

- Broader OS support.
  
- The SDK is being updated to comply with HIPEs documenting interoperability standards which we call Agent to Agent compatibility.
- Consume official builds of Hyperledger Ursa (the shared crypto-lib), as they are approved.
- LibVCX, the credential exchange library, is available in Indy SDK as an experimental API. We are evolving that API to respond to community feedback.
- These efforts are likely to require backwards incompatible changes to the API, requiring an Indy SDK 2.0.

Indy Agent

- Standardizing agent-to-agent protocol through an agent test suite.
- Tests associated with each major aspect of the protocol.
- Multiple interoperable agents in the community.
  
  - Mobile agents from the Sovrin Foundation and Evernym, and web agents from BC.gov, BYU, and StreetCred.
- Addition of a reference cloud agent.

# Maintainer Diversity

Indy maintainers remain active in developing and contributing to working group calls and public discussions. The bi-weekly Indy Maintainers Circle call has consistently been the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and resolve HIPEs. The Indy Agent call continues to be the focus of much attention, and the Overlays Working Group also continues to receive a lot of interest .

# Contributor Diversity

Hyperledger Indy continues to see contributions from developers and organizations around the world. Our weekly Working Group call is normally attended by two dozen people representing nearly a dozen organizations. Please note the number of contributors and contributions listed in the Project Health section above.

# POCs, Pilots, Projects

##### Sovrin

[http://www.sovrin.org](http://www.sovrin.org/)

Sovrin is the first instantiation of the Indy codebase and is currently moving from the provisional network phase of development to production usage.

##### Verifiable Organizations Network

[https://von.pathfinder.gov.bc.ca](https://von.pathfinder.gov.bc.ca/)

The Province of British Columbia, the Government of Ontario, and Public Services and Procurement Canada are ready to launch their trusted digital network of verifiable data about organizations.

##### Brigham Young University

[https://www.byu.edu/](https://www.byu.edu/)

The University is building an agent to manage student credentials throughout their experience at the university.

##### Evernym

[https://www.evernym.com/](https://www.evernym.com/)

Evernym is creating applications that will make it easy for organizations and users to issue, hold, and verify credentials through the Sovrin network.

# Additional Information

- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

<!--THE END-->

- Join the Indy Working Group Calls: every Thursday 8am PT, 9am MT, 11am ET, 4pm BST (Join from PC, Mac, Linux, iOS or Android: [https://zoom.us/j/232861185](https://zoom.us/j/232861185) )

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
