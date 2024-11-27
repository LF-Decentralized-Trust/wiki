[invalid_url] err=parse "http://peter.somogyvari[you%20know%20what]accenture.com/": invalid URL escape "%20" url="http://peter.somogyvari[you%20know%20what]accenture.com/" 
1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Hyperleger Cactus and Hedera Hashgraph Integration

Created by Danno Ferrin, last modified by Min Yu on Dec 08, 2022

**Project Title**Hedera Hashgraph integration with Hyperledger Cactus**Status**

CANCELLED

**Difficulty**

MEDIUM  

# Description

[Hyperledger Cactus](https://www.hyperledger.org/use/cactus) is a blockchain decentralised integration tool designed to allow users to securely integrate different blockchains started by companies Fujitsu and Accenture. Cactus has pluggable architecture which makes easy to integrate various blockchain by creating [plugin](https://github.com/hyperledger-labs/blockchain-integration-framework/files/4228021/hyperledger-blockchain-integration-framework-whitepaper.pdf), currently [plugins](https://github.com/hyperledger/cactus/blob/main/whitepaper/whitepaper.md#561-ledger-connector-plugins) for Fabric, Besu, Quorum are implemented. Cactus allows to transfer not only assets but also data between multiple blockchains.

Hedera Hashgraph is a DLT built on top of an asynchronous BFT algorithm, providing smart contract, token, and consensus services to end users. The flexibility 

# Additional Information

[Hyperledger Cactus](https://www.hyperledger.org/use/cactus) ([whitepaper](https://github.com/hyperledger/cactus/blob/main/whitepaper/whitepaper.md), [whitepaper of integration](https://github.com/hyperledger-labs/blockchain-integration-framework/files/4228021/hyperledger-blockchain-integration-framework-whitepaper.pdf), [chat](https://chat.hyperledger.org/channel/cactus), [already implemented plugins](https://github.com/hyperledger/cactus/tree/main/packages))

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha))

[Hedera Hashgraph](http://hedera.com/) ([documentation](https://docs.hedera.com/guides/), [chat/discord](http://hedera.com/discord), [getting started](https://docs.hedera.com/guides/getting-started/introduction))

[Hedera SDKs](https://docs.hedera.com/guides/docs/sdks) (java, javascript, go)

# Learning Objectives

The mentee will be able to learn:

- ways of integrating different projects from architectural point of view,
- architecture of Hedera and Cactus,
- explore issues integrating a persistent networks and transient networks
- work in true spirit of open-source, communicating with both Hedera and Cactus community, joining calls and using other community tools,
- writing documentation, so anyone in the community could use the results of their work,
- following rules and standards of open-source projects created by hyperledger,

# Expected Outcome

1. Documented, ready-to-use integration of Hedera and Cactus,
2. Documented example of integration using Hedera's Testnet and Hedera's Previewnet,
3. Documented example of integration between another blockchain and Hedera using Cactus.

# Relation to Hyperledger

This project will provide integration between Hyperledger Cactus and a non-hyperledger project Hedera Hashgraph.  It is expected all necessary code would either be committed to the Hyperledger Cactus repository or a new Hyperledger Labs repository.

# Education Level

Undergraduates should have sufficient skill. It is not expected that the issues around persistent and transient blockchain integrations would require graduate level research efforts.

# Skills

- Reading english documentation,
- Programming language of one of libraries supported by Hedera Hashgrpah SDKs (e.g. Go, Java, Javascript).
- Programming language to implements Cactus plugin. It is easiest to code in NodeJS. It is also possible in other technologies (working implementations are in Rust, Kotlin) but it is necessarily to create also web-server, which can be generated with [openapi-generator](https://openapi-generator.tech/).

# Future plans

Potentially integrate other Hyperledger Projects and Labs that focus on cross-ledger utility with Hedera (Firefly, Caliper, Yui, etc)

# Preferred Hours and Length of Internship

No preference, Mentee is expected to report to mentors progress each week report progress during [bi-weekly Cactus Community meetings](https://lists.hyperledger.org/g/cactus/calendar).

# Mentor(s) Names and Contact Info

**Danno Ferrin** (Hedera Hashgraph, Hyperledger Besu Maintainer)  
email: [danno.ferrin@gmail.com](mailto:danno.ferrin@gmail.com)  
Discord: shemnon#2321

**Peter Somogyvari** (Accenture, Cactus Maintainer)  
[email: peter.somogyvari@accenture.com](http://peter.somogyvari%5Byou%20know%20what%5Daccenture.com/)  
Discord: peter\_somogyvari#3365

**Si Chen** (Open Source Strategies, Hyperledger Climate SIG)  
email: sichen@opensourcestrategies.com  
Discord: Si Chen#0557

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
