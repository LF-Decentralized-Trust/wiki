1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2024 Projects](2024-Projects_21954934.html)
5. [Cacti: Core Operators Modules for DLTs](21954936.html)

# Hyperledger Mentorship Program : Cacti Core Operators Module Project Plan

Created by Jennifer Bell, last modified by Venkatraman Ramakrishna on Jul 25, 2024

# Project Scope

The process of integrating the Cactus and Weaver modules and workflows to create a common Cacti platform conforming to the architecture illustrated in the [Cacti Roadmap](https://github.com/hyperledger/cacti/blob/main/ROADMAP.md#cacti-v2) (and below) must follow a particular sequence of steps in order to ensure backward compatibility and avoid breaking preexisting user dependencies on exported Cacti packages and images.

![](https://github.com/hyperledger/cacti/raw/main/images/cacti-architecture-v2-integration.png)

As described in the [project proposal](21954936.html), the first step we have identified in the integration process is the building of a Core Operators module (let's call it COPM) that directly acts on a network's (or system's) ledger, which can be seen at the right end of the above diagram. (*Note*: because different ledgers are built on different DLTs, Cacti will support an extensible suite of COPMs, one for each DLT.)

In this project, we need to do the following:

- Design a **generic structure** and **interface (API)** for the COPM that is portable across DLTs (while being implemented in DLT-specific ways for each ledger type.)
  
- Identify a list of Core Operator primitives to implement. Thus far, we have identified a limited set of such operators, which in some combinations can fulfil the three canonical DLT interoperability use cases: data sharing, asset exchange, and asset transfer. (*Note*: this set is meant to be extensible, to accommodate more operators if we discover functions that are not covered by the below list)
  
  - ***lockAsset***
  - ***pledgeAsset***
  - ***claimAsset***
  - ***generateProof***
  - ***verifyProof***
  - ***accessControl***
  - ***noop*** (this is a passthrough option, for Cacti modules and connectors that do not need to invoke any of the above operators)
- Implement a COPM for **Hyperledger Fabric**
  
  - On a best effort basis, implement a COPM (in part or whole) for **Corda**
  - On a best effort basis, implement a COPM (in part or whole)  for **Besu/Ethereum**
- Sketch out a template for porting to arbitrary DLTs and write **documentation** (this may end up being part of the Cacti whitepaper)
- Write **scripts to deploy** COPMs on a given network
- **Refactor existing Cacti packages** (select a few) to invoke the appropriate COPM
- Pick some **end-to-end examples** to showcase (this should cover existing Cactus examples, existing Weaver examples on data sharing, asset exchange, and asset transfer)

**Preliminary work**:

- Test and evaluate Cactus setups and examples using instructions in the [documentation](https://hyperledger.github.io/cacti/cactus/introduction/).
  
- Test and evaluate Weaver setups and samples using instructions in the [documentation](https://hyperledger.github.io/cacti/weaver/introduction/).
  
- Document bugs, required upgrades in software, instruction typos, and identify automation scripts that can help make tooling and CI more efficient.
  
- Expose Weaver modules and libraries through symlinks in the `packages`  folder to simplify the integration process.

(The intention of this project is to unify multiple interoperability frameworks by creating a reusable set of operators so that the existing frameworks can be migrated to them.)

# Key Deliverables

- Cacti Core Operators Module (COPM) design: functions (*see the list in the project scope above*) and API
  
  - API should be RESTful, built on gRPC or socket.IO, designed to be integrated with the Cacti Client API and invoked by Cacti Connectors
- Implementation of COPM:
  
  - Hyperledger Fabric: (*required*: all functions and API)
  - R3 Corda: (*best effort*: some functions and associated API)
  - Hyperledger Besu: (*best effort*: some functions and associated API)
- Selection of use cases (examples) for end-to-end testing: both Cactus (Node Server) and Weaver (Relay) modes
  
  - Weaver data sharing using test networks (minimum required)
  - Other Weaver use cases (asset exchange, asset transfer) (*best effort*)
  - Cactus examples: *TBD*
- CI-automated testing of COPM for all combinations
- Documentation:
  
  - Updates to architecture, vision, design methodology (as required)
  - Tutorials for running with Cacti samples
  - FAQs (*best effort*)
  - Suggestive instructions for adaptation to users' scenarios (*best effort*)
- Updated RFCs: COPM design and API specifications
  

# Optional Deliverables

- Unified Cacti CI GitHub workflows
- Dockerize Weaver test tooling for easy setup (equivalent of a the `fabric-tools` container offered by Fabric)
- Cactus REST APIs updated to use core operators
- Redundant code identified and removed
- Implementation of Core Operator Module in DLTs other than Fabric, Corda, and Besu

# Timeline

WeekTask/PlanStatus**June 03 - June 20**On boarding/orientation sessions. Meet with the mentors, discuss project implementation details,  
deliverables and scope. Initiate the project plan.✅**June 20 - June 27** Finalize project plan, attempt to run examples, flagging project examples that no longer work✅**June 27 - July 7**Produce COPM design (with interface). Preliminary work (*best effort*): see list in the Project Scope section  
**July 8 - July 17**Mentee vacation  
**July 17 - July 22**Implement COPM skeleton with gprc and REST API interface. Implement one core operator in Fabric, Besu and Corda .  
**July 22 - July 26**1ST QUARTER MENTEE EVALUATION  
**July 27 - August 18**Implement remaining core operators on Fabric

**August 19 - September 01**Finalize documentation  
**September 02 - September 06**

MIDTERM EVALUATIONS

**September 08 - September 22**Implement remaining core operators for Besu  
**September 23 - October 19**Implement remaining core operators for Corda  
**October 14 - October 18**3RD QUARTER MENTEE EVALUATION  
**October 19 - November 29**Optional deliverables

(Greyed out entries in the above table are placeholders, subject to review and revision.)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
