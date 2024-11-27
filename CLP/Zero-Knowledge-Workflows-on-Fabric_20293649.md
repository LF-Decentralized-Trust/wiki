1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)

# Collaborative Learning Program : Zero-Knowledge Workflows on Fabric

Created by Imre Kocsis, last modified by Min Yu on Aug 28, 2023

**Project Title**

**Zero-Knowledge Workflows on Fabric**

**Status**

CANCELLED

**Primary Focus**

CODING   

# Description

Orchestrating and tracking the steps and cross-party messages of business collaborations is a key blockchain/distributed ledger technology use case. Several tools have emerged to support blockchain-orchestrated BPM (business process management); an important subset of these takes models of the cooperation, usually captured in the Business Process and Notation (BPMN) language and generate a process manager smart contract from the model.

Most of the existing tools target Solidity, and all of them store the business process state in the clear, in the smart contract. This can be problematic even for Hyperledger Fabric – if the process state is not to be seen by the whole consortium, we must resort to the confidentiality toolbox of Fabric (multiple channels, private data collections, etc.).

We argue that this is not absolutely necessary; in a recent work (published as open source at: [https://github.com/ftsrg/zkWF](https://github.com/ftsrg/zkWF)), we created a hash-commitment scheme-based business process orchestration approach, relying on zk-SNARKs for proving the admissibility of process state commitment updates.

Our prototype implementation already supports Hyperledger Fabric to some extent (originally, we focused primarily on Solidity/EVM). Specifically, we have an implementation of the crucial element, the commitment manager and proof checker chaincode. However, proper support for Fabric needs a number of further improvements – as contributions to our open-source solution - and this is the topic of this mentorship. The specific work items we envision are the following.

- Setup and deployment support for Hyperledger Fabric
- Design and implementation of a full-fledged Fabric client (at the application/SDK level)
- Integrated handling of private message-sending (off-chain in the current scheme) through Fabric PDC
- Implementing our "fake update" mechanism, which is to protect against statistical and trace inference attacks on process state confidentiality
- If time permits, addressing (some of the) current limitations at the BPMN level

# Additional Information

The project repo: [https://github.com/ftsrg/zkWF](https://github.com/ftsrg/zkWF)

The full research report: [https://tdk.bme.hu/VIK/DownloadPaper/Kollaborativ-munkafolyamatok-titkossagmegorzo](https://tdk.bme.hu/VIK/DownloadPaper/Kollaborativ-munkafolyamatok-titkossagmegorzo)

Journal paper manuscript (submitted, under consideration): [Blockchain\_based\_confidentiality\_preserving\_orchestration\_of\_collaborative\_workflows.pdf (bme.hu)](http://mit.bme.hu/~ikocsis/Blockchain_based_confidentiality_preserving_orchestration_of_collaborative_workflows.pdf)

# Learning Objectives

- Gain familiarity with commitment-management style ZKP schemes and the ZoKrates toolkit
- Learn to implement a full-fledged Hyperledger Fabric client application
- Learn to work collaboratively and contribute to an existing code base
- Learn modelling in BPMN and handling BPMN models

# Expected Outcome

- Setup and deployment support in zkWF for Hyperledger Fabric (code, documentation)
- Full-fledged Fabric zkWF client (the key point is the SDK, the current GUI is only for demonstrational purposes)
- Fabric-specific modifications to the zkWF code base (see the description)
- "Nice to have" outcome: a design vision on integrating zkWF with Hyperledger Firefly

# Relation to Hyperledger

Hyperledger Fabric; indirectly Hyperledger Besu (*theoretically*, zkWF should work with Besu as-is); in the long run, potentially Hyperledger Firefly

# Mentee Skills

Some experience and agility in working with Linux are absolutely necessary (the whole toolchain assumes Linux); and the project is challenging to finish in a reasonable time without having some experience in Kotlin (a key language of the code base) and Hyperledger Fabric.

ZoKrates and TornadoFX experience are a plus but not necessary.

# Mentee Open Source Contribution Experience

"Show your work" - show us a code base (preferably on GitHub) you created/had a major role in creating and which you are proud of. If that's not applicable, our plan is to assign some programming tasks during the selection interview for such candidates.

# Future plans

We expect this project to gain actual momentum in the mid-term - even if not exactly in its current form (we are considering in the longer term rebasing to Firefly as well as morphing the whole approach into a Layer 2 service).

Moving the project into a Hyperledger Lab is an option we certainly don't rule out after a successful mentorship.

# Mentor(s) Names and Contact Info

Imre Kocsis, assistant professor, [kocsis.imre@vik.bme.hu](mailto:kocsis.imre@vik.bme.hu), Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group

Balázs Ádám Toldi, MSc student, [balazs.toldi@edu.bme.hu](mailto:balazs.toldi@edu.bme.hu), Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group

Document generated by Confluence on Nov 26, 2024 13:14

[Atlassian](http://www.atlassian.com/)
