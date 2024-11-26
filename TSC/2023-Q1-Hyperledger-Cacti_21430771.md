1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2023 Project Updates](2023-Project-Updates_21445803.html)

# Technical Oversight Committee : 2023 Q1 Hyperledger Cacti

Created by 竹内琢磨, last modified by Bobbi Muscara on Jan 25, 2023

# Project Health

- Cactus and Weaver were merged to one project "Cacti."  The maintainers almost completed the first code merge and will release the first Cacti v2-alpha (tentative name) in Q1 2023.
- The maintainers are also discussing the new architecture of Cacti toward Cacti-V2 in order to combine the strengths of the original Cactus and Weaver to achieve a more flexible interoperability tool.
- Cacti has newly supported the interoperability with Iroha V2 and Ubiquity SDK.
- Weaver now supports organizational identity syncing and event pub/sub across Fabric networks, and atomic swaps involving ERC-standard tokens in Besu networks with Fabric and Corda networks.  These will be merged in Cacti V2-alpha release on Q1 2023.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? **Yes**
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? **Yes**
   
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo. **Yes, we use DCI-Lint as part of our CI**
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? **Yes**
   

# Questions/Issues for the TSC

- None at the moment.

# Releases

- v1.1.x: to fix the GitHub workflow errors
  
  - v1.1.3 =&gt; [https://github.com/hyperledger/cactus/tree/v1.1.3](https://github.com/hyperledger/cactus/tree/v1.1.3)
  - v1.1.2 =&gt; [https://github.com/hyperledger/cactus/tree/v1.1.2](https://github.com/hyperledger/cactus/tree/v1.1.2)
  - v1.1.1 =&gt; [https://github.com/hyperledger/cactus/tree/v1.1.1](https://github.com/hyperledger/cactus/tree/v1.1.1)

# Overall Activity in the Past Quarter

1. Major Cactus updates as merged pull-requests
   
   1. interoperability with ledgers:
      
      1. \[new\_feature] Iroha: add support for Iroha V2
         
         1. [https://github.com/hyperledger/cactus/commit/db789690b64d68b3dda70578127338bdc02e92bd](https://github.com/hyperledger/cactus/commit/db789690b64d68b3dda70578127338bdc02e92bd)
         2. [https://github.com/hyperledger/cactus/commit/6ff6aac7fff4669fca873ef40ae6b0818e70b5ec](https://github.com/hyperledger/cactus/commit/6ff6aac7fff4669fca873ef40ae6b0818e70b5ec)
      2. \[new\_feature] Ubiquity SDK: initial version
         
         1. [https://github.com/hyperledger/cactus/commit/7c597907910bd5cac919c855a3bfa9e533b6d5dd](https://github.com/hyperledger/cactus/commit/7c597907910bd5cac919c855a3bfa9e533b6d5dd)
      3. \[update] Fabric: add WatchBlocks endpoint
         
         1. [https://github.com/hyperledger/cactus/commit/0f670855b0fa0fd33f71bf5a1814fb6fcac2c7b6](https://github.com/hyperledger/cactus/commit/0f670855b0fa0fd33f71bf5a1814fb6fcac2c7b6)
      4. \[update] Fabric: add transactions signed on the client side
         
         1. [https://github.com/hyperledger/cactus/commit/0b34ca3d35a39826c05cc047e480d377c1c52bef](https://github.com/hyperledger/cactus/commit/0b34ca3d35a39826c05cc047e480d377c1c52bef)
      5. \[update] ODAP: decouple the gateway implementation from any ledger
         
         1. [https://github.com/hyperledger/cactus/commit/6975fefd4994cc9c6dd7d649dc2d6400646a59ae](https://github.com/hyperledger/cactus/commit/6975fefd4994cc9c6dd7d649dc2d6400646a59ae)
   2. support features:
      
      1. \[update] support multiple business-logic-plugins in the single server
         
         1. [https://github.com/hyperledger/cactus/commit/0f670855b0fa0fd33f71bf5a1814fb6fcac2c7b6](https://github.com/hyperledger/cactus/commit/0f670855b0fa0fd33f71bf5a1814fb6fcac2c7b6)
2. Major Weaver updates as merged pull requests (* These will be merged in Cacti V2-alpha release in Q1 2023)
   
   1. ERC-token support for Besu networks engaging in asset swaps
      
      1. [https://github.com/hyperledger-labs/weaver-dlt-interoperability/pull/299](https://github.com/hyperledger-labs/weaver-dlt-interoperability/pull/299)
   2. Identity syncing across Fabric networks using organization-specific agents running a flow
      
      1. [https://github.com/hyperledger-labs/weaver-dlt-interoperability/pull/322](https://github.com/hyperledger-labs/weaver-dlt-interoperability/pull/322)
      2. [https://github.com/hyperledger-labs/weaver-dlt-interoperability/pull/316](https://github.com/hyperledger-labs/weaver-dlt-interoperability/pull/316)
3. Created a draft architecture diagram for Cacti as a fusion of Cactus and Weaver, with the goal of providing a flexible or customizable interoperability toolkit 
   
   1. The architecture has been brushed-up among weekly maintainer calls.  This will be started to be referred on the next release (Cacti V2-beta on Q1-Q2)
   2. The architectural evolution is called out in two distinct phases:
      
      1. A common platform and toolkit with Cactus and Weaver modules and libraries coexisting and solving similar purposes
      2. An integrated platform and toolkit with similar-purpose modules and libraries from Cactus and Weaver fused into common Cacti modules and libraries

# Current Plans

1. Release plan:
   
   1. Cacti V2-alpha (Q1): The first proto version of Cacti combining the original Cactus and Weaver
   2. Cacti V2-beta (Q1-Q2): The first version of Cacti based on the new architecture (combined with the strengths of Cactus and Weaver)
2. Other features:
   
   1. Cacti Transaction GUI feature (Q1)
   2. DID registry-based identity management for cross-network data sharing
   3. Automated relay-based asset swaps using cross-network events
   4. Supporting data sharing (with proof generation and validation) in for Fabric PDCs
   5. Supporting data sharing (with proof generation and validation) in Besu networks
3. Standardization:
   
   1. Track the Secure Asset Transfer (SAT) group's efforts toward forming an official IETF Working Group
   2. If it becomes an official WG, influence and comply (i.e., in Cacti code) with protocol drafts (eventually RFCs) for interoperability standards

# Maintainer Diversity

- As is required, you can find our current maintainer list here:  [https://github.com/hyperledger/cactus/blob/main/MAINTAINERS.md](https://github.com/hyperledger/cactus/blob/main/MAINTAINERS.md).

<!--THE END-->

- Our existing maintainers are:
  
  - Jagpreet Singh Sasan (Accenture)
  - Jonathan Hamilton (Accenture)
  - Peter Somogyvari (Accenture)
  - Izuru Sato (Fujitsu)
  - Takuma Takeuchi (Fujitsu)
  - Sandeep Nishad (IBM)
  - Venkatraman Ramakrishna (IBM)

# Contributor Diversity

- [https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard](https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard)
  
  Our contributor strength has increased in this quarter compared to the previous quarter, which is great news!

# Additional Information

- N/A

# Reviewed By

- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [Marcus Brandenburger](https://lf-hyperledger.atlassian.net/wiki/people/5d6cd4bb3803ee0db6cedaaf?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Venkatraman Ramakrishna](https://lf-hyperledger.atlassian.net/wiki/people/6124c28b45f75300691e9f16?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
