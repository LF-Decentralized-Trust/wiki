1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Fabric-Ethereum token bridging

Created by Imre Kocsis, last modified by André Augusto on Sep 06, 2022

**Project Title**Fabric-Ethereum token bridging**Status**

COMPLETED

**Difficulty**

HIGH  

# Description

One of the key use cases of blockchain integration is asset bridging: in essence, "locking" an asset (typically, a native coin or token) in a smart contract on its authoritative ledger and making available corresponding, newly minted (wrapped/shadow/...) assets on another. By now, bridging is supported by quite mature solutions in the cryptoworld; however, the same is not true for "consortial" distributed ledger technologies. At the same time, such functionality can be expected to become an important requirement in the not too distant future: for instance, a central bank may choose to create a high performance, Hyperledger Fabric-based Central Bank Digital Currency (CBDC) ledger with a strongly controlled set of "smart contracts", but allow controlled "bridging out" of the currency to dedicated distributed ledgers of industrial/enterprise cooperations. Last year, a CBDC prototype with such functionality was created at the Dept. of Measurement and Information Systems of the Budapest University of Technology and Economics (BME), in a research project supported by the central bank of Hungary (MNB); our initial experience with a custom Hyperledger Cactus and TokenBridge based solution showed that this is a problem worth more targeted experimentation and systematic R&amp;D.

The proposed project consists of the following major activities:

- Analysing the implementation approaches of standard "token models" (ERC20, ERC-721, ... - as far as this has been already done) in native Fabric chaincode and creating conceptual mappings between standard Ethereum token types and Fabric-native assets (including, but not limited to, the different authentication and authorization approaches).
- Creating a brief review of the bridging approaches and mature technologies widely used in the cryptoworld.
- Performing a requirement analysis for bridging assets from Fabric to Ethereum-based networks (and back), taking into account that the parties performing the bridging have to be explicitly given permission to do so by an authority and may be subject to regulatory requirements (the simplest aspect of which is enforcing, or at least proving compliance to, an "allow list" of addresses on the Ethereum side during transactions).
- Based on the available open-source components, designing and prototyping a Fabric-Ethereum bridge fulfilling the requirements.

As the proposed project bridges (excuse the pun) multiple fields, creating a centralized solution (e.g., a financial institution allowed to perform bridging) that supports only PoA Ethereum networks will be still deemed a success. Ethereum-side components of the TokenBridge project are expected to be applied in the solution, potentially along with Hyperledger Cactus.

# Additional Information

The Hyperledger Cactus white paper is a good introduction to blockchain interoperability/integration in general terms: [https://github.com/hyperledger/cactus/blob/main/whitepaper/whitepaper.md](https://github.com/hyperledger/cactus/blob/main/whitepaper/whitepaper.md)

TokenBridge is a good example of "how it's done" in the cryptoworld: [https://docs.tokenbridge.net/](https://docs.tokenbridge.net/)

Research material of the above mentioned CBDC project is only publicly available in Hungarian yet; a research report in English is available upon request, but the proposed project is not tied to the CBDC bridging use case.

In the optimal case, the successful applicant has had previous exposure to either Hyperledger Fabric or Ethereum/Solidity programming (otherwise the learning aspect of the project runs the risk of not fitting the project runtime)

# Learning Objectives

\- Introduction to open source culture and collaboration tools

\- Bridging approaches and technologies

\- Requirement-driven creation of an open-source prototype

\- Hyperledger Fabric chaincode development, Solidity development

# Expected Outcome

\- D1: report on asset representation in Hyperledger Fabric and mapping approaches to standard Ethereum tokens

\- D2: report on bridging approaches and technologies and their applicability for bridging from/to Fabric

\- D3: Requirement specification

\- D4: Design specification

\- D5: Prototype implementation and small demo of bridging at least ERC-20 or ERC-721 to Ethereum - and back

# Relation to Hyperledger

\- Hyperledger Fabric

\- Potentially Hyperledger Cactus

# Education Level

A completed BSc in computer science or computer engineering is required, or a demonstration of roughly equivalent knowledge of core competencies.

# Skills

Highly analytical thinking and the ability to read code efficiently is required. Meaningful previous exposure to either Hyperledger Fabric or Ethereum/Solidity programming is strongly preferred (otherwise the learning aspect of the project runs the risk of not fitting the project runtime). Familiarity with one of the supported native chaincode languages of Fabric is also required and Node.js specifically is expected to be beneficial. Basic knowledge of DevOps tools (git, docker, ...) will be necessary.

# Future plans

Either proposing a Hyperledger Labs project based on the results or merging the results into Hyperledger Cactus (if that is used in the final solution design).

# Preferred Hours and Length of Internship

Full time preferred as the mentors have academic obligations during the fall. 

# Mentor(s) Names and Contact Info

Imre Kocsis, kocsis.imre@vik.bme.hu, assistant professor, Budapest University of Technology and Economics (BME), Budapest, Hungary

László Gönczy, gonczy.laszlo@vik.bme.hu, assistant professor, Budapest University of Technology and Economics (BME), Budapest, Hungary

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
