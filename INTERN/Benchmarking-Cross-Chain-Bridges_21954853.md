1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Benchmarking Cross-Chain Bridges

Created by André Augusto, last modified by Min Yu on Jan 05, 2024

**Project Title**Benchmarking Cross-Chain Bridges**Status**

COMPLETED

**Primary Focus**

RESEARCH CODING  

# Description

Cross-chain bridges are a vital part of the blockchain landscape as they enable data and value to move seamlessly across different blockchains. Security is of utmost importance in this area, as these bridges can be vulnerable to malicious attacks and manipulation. In fact, until today, more than 2 billion US dollars have been hacked from these systems, a value that is representative of the work that still needs to be done in the area. In addition to securing bridges, measuring their performance and scalability is key to understanding if one is meeting the highest standards and is capable of encountering users' needs. This is mandatory to achieve mass adoption of the technology by single users and businesses.

There have been some efforts to design and implement interoperability solutions across different blockchains, some of which are within the Hyperledger ecosystem (see links in the next section). Furthermore, preliminary research has been conducted to benchmark interoperability solutions, however, we feel there is currently a lack of studies that thoroughly compare bridges – used both within and between

Hyperledger and public blockchains used in the industry. We aim to address this gap and conduct such evaluation studies, mainly through benchmarking.  
The goal of this project is to benchmark cross-chain solutions, an essential step for measuring the performance of any solution. As the adoption of cross-chain bridges grows it is increasingly important to have benchmarks to measure cross-chain solutions' performance and security.

# Additional Information

Systematically comparing the performance of bridges allows for the end-user to pick the one more suitable for their needs (knowing there might be tradeoffs, discussed in the recommended papers). We aim at studying cross-chain bridges' performance under some metrics such as latency, throughput, and total cost of transactions and how that translates into scalability. The project involves creating test environments to benchmark different interoperability solutions, including setting up multiple DLT networks, integrating solutions, and running performance tests. The results of the tests will be analyzed to evaluate solutions and identify areas for improvement. A technical report or academic paper will be written to disseminate the findings of this study to the wider community.

We provide some additional resources:

**Blockchain Interoperability:**

[Survey on Blockchain Interoperability](https://dl.acm.org/doi/10.1145/3471140)

[Metrics to evaluate Interoperability Solutions](https://dl.acm.org/doi/10.1145/3564532)

[Secure Asset Transfer Protocol (SATP) specification — a unidirectional asset transfer protocol](https://datatracker.ietf.org/doc/charter-ietf-satp/)

**Hyperledger Cacti**: [https://github.com/hyperledger/cacti](https://github.com/hyperledger/cacti)

**Hyperledger Caliper:** [https://www.hyperledger.org/use/caliper](https://www.hyperledger.org/use/caliper)

[Benchmarking Hyperledger Fabric](https://www.hyperledger.org/blog/2023/02/16/benchmarking-hyperledger-fabric-2-5-performance?utm_campaign=%2Fdev%2Fweekly%20newsletter&utm_medium=email&_hsmi=246604162&utm_content=246604130&utm_source=hs_email)

**Interoperability projects related to the Hyperledger community:**

[Central Bank Digital Currencies Bridging Solution – Between Hyperledger Fabric and Besu](https://www.techrxiv.org/articles/preprint/CBDC_bridging_between_Hyperledger_Fabric_and_permissioned_EVM-based_blockchains/21809430)

[Cross-Chain Modelling in Hyperledger Cacti](https://www.techrxiv.org/articles/preprint/Hephaestus_Modelling_Analysis_and_Performance_Evaluation_of_Cross-Chain_Transactions/20718058)

**Industry resources:**

[Cross-Chain Bridge Assessment Process](https://gov.uniswap.org/t/cross-chain-bridge-assessment-process/20148) (and the project final report)

**Existing Performance Analysis:**

[https://arxiv.org/abs/2303.10844](https://arxiv.org/abs/2303.10844)

[https://ieeexplore.ieee.org/document/9922037](https://ieeexplore.ieee.org/document/9922037)

Potential bridges to explore:

We will also explore popular industry bridges (e.g., IBC Cosmos, Polkadot Parachains, LayerZero) and Hyperledger-focused ones (e.g., [Cacti + SATP](https://github.com/hyperledger/cacti/pull/2185))

# Learning Objectives

This mentorship intends to yield a fruitful learning experience across several dimensions:

- **Open-source and teamwork**: You will learn how to contribute to an open-source project, test, and also document your work; You will be aware of the main efforts of the Hyperledger technologies, and how blockchain interoperability relates to that; you will interact with the Hyperledger community.
- **Technical**: You will refine your understanding of blockchain technology; You will strengthen your understanding of blockchain interoperability, taking a step forward to become an expert; You will refine your programming skills.
- **Scientific**: you will learn, or perfect your knowledge, on the research of a challenging topic; opens an opportunity to write a scientific paper that may have a high impact on academia.

# Expected Outcome

The expected outcome tackles the whole Hyperledger Ecosystem. In particular, the project includes Hyperledger Cactus.

- Brief **report on benchmarking testing methods**
- Brief **report on existing benchmarking results on cross-chain solutions**
- **Design a set of tests** and **choose the performance metrics** to be analyzed in bridges
- **Testing** and **documenting benchmarks** of multiple cross-chain bridges
- **Scientific paper (or technical report) on the achieved results**, that can be used to disseminate the knowledge created on this mentorship

# Relation to Hyperledger

[Hyperledger Cacti](https://lf-hyperledger.atlassian.net/wiki/display/cactus/Hyperledger+Cacti+Home) is a blockchain interoperability project. Cacti connects to several other projects: Hyperledger Fabric, Hyperledger Besu, and others. We expect using Cacti due to its relation to the cross-chain ecosystem.

We will explore the possibility of using (and extending), [Hyperledger Caliper](https://lf-hyperledger.atlassian.net/wiki/display/caliper/), a blockchain benchmarking tool.

The integration of these projects with cross-chain APIs from the industry is also a possibility, moving towards interoperability between Hyperledger projects and industry solutions.

# Mentee Skills

Masters or Ph.D. level students are preferred.

**Must**:

- Willing to contribute to a meaningful mission, in an open-source mentality
- Teamwork skills, as synergies and cooperations with other parts, are needed to successfully complete the project
- Solid understanding of blockchain technology
- Background in computer science, computer engineering, or equivalent
- Experience with NodeJS, Typescript, Git, Linux terminal commands, Docker 101

**Nice to have:** 

- Research experience (if you don’t, no worries – we can help!)
- Understanding of blockchain interoperability (please refer to the recommended papers)

# Future plans

The end of the mentorship does not need to mean an end to your collaboration. The idea is for the mentee to be connected to the Hyperledger’s ecosystem, contributing to blockchain interoperability solutions.

# Mentor(s) Names and Contact Info

André Augusto, [andre.augusto@tecnico.ulisboa.pt](mailto:andre.augusto@tecnico.ulisboa.pt), Ph.D. student at Técnico Lisboa, University of Lisbon, Portugal

Rafael Belchior, [rafael.belchior@tecnico.ulisboa.pt](mailto:rafael.belchior@tecnico.ulisboa.pt), R&amp;D at Blockdaemon, and Ph.D. student at Técnico Lisboa, University of Lisbon, Portugal

Peter Somogyvari, [peter.somogyvari@accenture.com](mailto:peter.somogyvari@accenture.com), Technology Architect, Accenture

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
