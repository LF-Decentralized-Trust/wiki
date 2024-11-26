1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q3 Hyperledger Indy

Created by Lynn Gray Bendixsen, last modified by Mic Bowman on Aug 08, 2019

# **Projects**

##### **Distributed Ledger**

- I[ndy-node](https://github.com/hyperledger/indy-node)
- I[ndy-plenum](https://github.com/hyperledger/indy-plenum)

##### **Client Tools**

- I[ndy-sdk](https://github.com/hyperledger/indy-sdk)
- Indy-agent (deprecated)

##### **Shared Components**

- I[ndy-hipe](https://github.com/hyperledger/indy-hipe)
- [Indy-test-automation](https://github.com/hyperledger/indy-test-automation)
- I[ndy-crypto](https://github.com/hyperledger/indy-crypto) (deprecated)

# **Project Health**

Indy is a healthy project. Indy’s codebase has 22012 commits from 170 unique contributors. This represents an increase of 6 contributors this quarter and about 2,000 additional commits. Forums and chat channels are monitored and a variety of participants are contributing helpful responses to questions. The Sovrin network saw multiple production use cases launched in the past quarter, and other Indy deployments are on track to enter production in 2019.

As part of launching project Aries, we redefined the scope and goals of the Indy project. This included transitioning most of our standards to Aries and deprecating projects like Indy Agent. We believe that Indy is in a good position to innovate even faster.

# **Issues**

We continue to track the same key issues as in previous quarters.

### **Incompatible agent implementations**

The launch of project Aries is an important step in encouraging interoperability among the various agent implementations. Aries is now responsible for defining the communication between agents, and will provide language frameworks that people can use to implement agents that comply with Aries standards.

Progress made:

- Hyperledger Aries as the new home for interoperable agent work.
- Previous work in the Indy project has led to quick releases of some Aries components:
- - Aries Cloud Agent - Python,
  - Aries Static Agent - Python,
  - Aries Framework - Go,
  - and the Aries Protocol Test Suite.

Further remediation planned:

- Continue standardizing agent communication protocols in the Hyperledger Aries Project.
- Move the relevant parts of the Indy SDK to become an Aries library that is shared by the Aries language frameworks.
- The remaining parts of the Indy SDK will evolve into a ledger resolver that matches the resolver API defined by Aries.

### **Measuring the size and make-up of our user community**

We are paying attention to key metrics, but have not yet established a formal method of tracking specific progress. This is an area where Hyperledger could assist.

Progress made:

- We see increased usage of the Stack Overflow tag #hyperledger-indy.
- More questions on Rocket Chat are being answered by people who have not contributed pull requests to the project.
- The rate of Jira issues opened by non-core contributors has increased significantly.

Future work planned:

- We expect that the Indy contributor community will shrink as much of the attention shifts to Aries.
- Work with Hyperledger to get analytics about web sites, and Rocket Chat usage.
- Begin measuring usage of the Sovrin forums: new contributors, questions asked, and questions answered

### **Build Issues**

The current Jenkins CI pipeline is difficult to maintain and extend. Hyperledger doesn’t provide build environments for many of our required environments such as Windows, OSX, and iOS, and Android. In the past quarter our build pipelines were repeatedly broken by changes to the Hyperledger devops policy regarding DCO checks, branching policy, and GitHub permissions, which resulting in wasted developer days and frustrated contributors. As a result, we are transitioning to a GitLab CI build pipeline using resources contributed by the developer community and managed by the Sovrin Foundation.

Progress made:

- The team at the Sovrin Foundation is making progress reimplementing the pipeline for Indy-SDK using Gitlab CI.

Further remediation planned:

- Other teams are committed to help move the other Indy pipelines to the GitLab infrastructure.

# **Releases**

**May 2019:**

##### **Indy SDK 1.8.3**

- Fixed behavior of auth\_rule and get\_auth\_rule request builders
- Extended windows packages to contain \*.dll.lib file.
- Fixed boolean datatype representation for FFI.

##### **Indy SDK 1.9.0**

- Added a set of functions to support work with Transaction Author Agreement concept.
- Updated Indy-CLI to use session based approach
- Updated Libindy indy\_verifier\_verify\_proof function to check restrictions on requested predicates during validation of proof.
- Updated Libindy to use [Ursa](https://github.com/hyperledger/ursa) instead of [Indy-Crypto](https://github.com/hyperledger/indy-crypto).
- Updated Indy-CLI to provide a functionality of saving transactions into CLI context and the following usage of them.
- Implemented State Proof verification for some types of GET requests to the ledger.
- Bugfixes

##### **Indy Node 1.7.1**

- Audit Ledger
- - helps keeping all other ledgers in sync
  - helps recovering of pool state by new or restarted nodes
  - can be used for external audit
- Correct support of multi-signatures
- Configurable Auth Rules in config state
- Stability fixes

##### **Indy Node 1.8.0**

- Add Transaction Author Agreement Acceptance Mechanisms and Transaction Author Agreement support
- Configurable Auth rules improvements
- Stability fixes

### **June 2019:**

##### **Indy SDK 1.8.2**

- Added auth\_rule feature
- Set default freshness threshold to 600 seconds
- Send GET requests to two Nodes
- Bugfixes

##### **Indy Node 1.8.1**

- Hotfix to repair problem that nodes were restarting every 30-50 seconds
- Other bugfixes

### **July 2019:**

##### **Indy SDK 1.10.0**

- Added indy\_build\_auth\_rules\_request function to Libindy Ledger API to change multiple ledger auth rules.
- Added correspondent ledger auth-rules command to Indy CLI.
- Bugfixes

##### **Indy SDK 1.10.1**

- Updated Indy CLI to persist command history between sessions.
- Bugfixes:
- - Corrected behavior of Indy-CLI ledger set-fees-prepare command to not add Transaction Author Agreement to request.
  - Corrected response data types in Indy-CLI ledger get-fees command.
  - Fixed State Proof verification for GET\_REVOC\_REG\_DELTA requests in case of from and to are before first entry.
  - other minor bugfixes

##### **Indy Node 1.9.0**

- Pluggable Request Handlers have been implemented

# **Overall Activity in the Past Quarter**

**General**

- With the launch of Aries, the scope of the Indy project is smaller. Aries is now responsible for defining the communication between agents, and Indy will focus on providing a stable and scalable identity ledger. This work included ratification of former Indy HIPEs as Aries RFCs and bootstrapping the Aries community.
- Indy development focused on ledger stability and features that are required to bring use cases to production such as:
- - replacing indy-crypto with Ursa in the Indy SDK,
  - deployment of an audit ledger,
  - support for multi-signature transactions,
  - a flexible system of authorization rules,
  - a new approach to ledger plugins that are easier to maintain,
  - support for transaction author agreements to protect stewards from legal liability,
  - wallet improvements that make it easier to tag and search credentials,
  - and lots of fixes.
- Rich schema improvements are maturing into a reference implementation of the [W3C standard for verifiable credentials](https://www.w3.org/TR/vc-data-model/). [HIPE 0138](https://github.com/hyperledger/indy-hipe/tree/master/text/0138-rich-schema-context) defines the context object, and community comment and feedback is underway. Work has begun on the context object, which will affect all layers of the stack: Indy node, the Indy resolver, and Aries agents. We already have code for Indy Node that can write and read contexts to and from the ledger. Initial work has started on contexts in the Indy-SDK layer as it is migrating into the Indy Resolver and Hyperledger Aries.

# **Current Plans**

##### **General**

Our previous plans have significantly evolved:

- **Indy SDK 2.0:** Our current plan is to significantly reduce the scope of the Indy SDK to focus on resolving Aries transactions on the Indy ledger. All language libraries will be moved to the Aries project, keeping in Indy only the thin language bindings required for automated testing. This should significantly reduce our maintenance burden. We then plan to refactor the Indy Resolver to address concerns with the threading model and performance.
- **Ledger 2.0 / indy-ledger-next:** Our effort to consider a different ledger implementation and architecture is on hold. We recognize that the current architecture limits scalability, but it has proven robust for the workloads we expect to see for some time. We are instead addressing the most critical stability concern with the current architecture which is the view change implementation.
- **Documentation:** The effort to refine documentation is ongoing, including an effort to publish more architecture documentation for Indy SDK as we prepare for moving code into Aries, and to consolidate documentation for onboarding contributors.
- **Other features planned:**
- - Compliance with standards such as DID Documents and W3C Verifiable Credentials.
  - Primitives necessary for Aries features such as peer DID communication.
  - Support for additional Indy SDK platforms such as Ubuntu, Fedora, and OSX.
  - And we will be adopting the new features emerging in Ursa related to Anoncreds 2.0, including new encryption curves, improved revocation, and more ZKP predicates.

# **Maintainer Diversity**

The bi-weekly Indy Maintainers call continues to be the medium by which maintainers coordinate work, discuss critical issues to the Indy codebase, and agree on HIPEs. The Semantics Working Group has been driving the work on advanced schemas. The active discussions in the Indy Agent meetings have moved to the Aries working group calls. No new Indy maintainers were added in the last quarter, but a number of Indy contributors have become official maintainers of Aries code bases.

# **Contributor Diversity**

Fewer people work on Indy now that many contributors have moved their efforts to new projects like Ursa and Aries that focus on their specific interests. Most Indy contributions are made by the Sovrin Foundation, Evernym, and the government of British Columbia. This quarter we saw an increased number of issues being opened by people trying to use the Indy code base, and we aim to nurture these users into contributors.

Coordinating the efforts across Ursa, Indy, and Aries has been a challenge. To address this need, we have increased our collaboration with the Identity Working Group by replacing the weekly Indy Working Group call with an Identity Implementers call.

# **POCs, Pilots, Projects**

There are now too many Indy projects to list here. Recent public disclosures include:

- [Anonyome Labs](https://sovrin.org/use-case-blog-anonyome-labs-integrates-ssi-into-its-sudo-platform-and-mysudo-application/)
- [The Alberta Credentials Ecosystem](https://www.evernym.com/blog/alberta-credentials-ecosystem/)
- [VIDchain](https://sovrin.org/use-case-spotlight-validated-id-and-its-ssi-solution-vidchain/)
- [Fetch.AI](https://sovrin.org/steward-spotlight-fetch-ai-unleashing-the-power-of-the-digital-economy-with-sovrin/)
- [Mattr](https://sovrin.org/use-case-spotlight-verifiable-credentials-from-mattr/)
- [The UK’s FCA Regulatory Sandbox POC](https://www.evernym.com/blog/evernym-accepted-into-fca-regulatory-sandbox/)
- [Streetcred](https://sovrin.org/use-case-stretcred/)
- [Kiva’s project in Sierra Leone](https://www.forbes.com/sites/rogerhuang/2019/01/23/kiva-partners-with-un-and-sierra-leone-to-credit-score-the-unbanked-with-blockchain/)

# **Additional Information**

- Key channels on Rocket Chat: #indy, #indy-sdk, #indy-node, #indy-maintainers
- Join the Indy Mailing List: [https://lists.hyperledger.org/g/indy](https://lists.hyperledger.org/g/indy)

# Reviewed by

- Arnaud Le Hors
- Baohua Yang
- Binh Nguyen
- Christopher Ferris
- Dan Middleton
- Hart Montgomery
- Kelly Olson
- Mark Wagner
- Mic Bowman
- Nathan George
- Silas Davis

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
