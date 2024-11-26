1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Burrow

Created by Silas Davis, last modified by Angelo de Caro on Mar 31, 2021

Project Health

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)?

Yes

1. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)?

Added repolint.json to repo, however the repolint tool does not support node v15 via transitive dependency:

\```

error clinic@6.0.2: The engine "node" is incompatible with this module. Expected version "^13.0.0 || ^12.0.0 || ^11.0.0 || ^10.12.0". Got "15.11.0"

error Found incompatible module.  
\```

So deferring full implementation until it does. (also doesn't build with node v13 on NVM, so may need some better tooling here)

# Releases

\- [**v0.31.0**](https://github.com/hyperledger/burrow/blob/master/CHANGELOG.md#0310) - Much goodliness - complete eWASM support, Vent support for mainline Ethereum, Web3 fixes, cross-smart-contract-engine calling

# Overall Activity in the Past Quarter

After a fallow period in Q4 2020 Burrow has seen the best quarter of activity I can remember. We have made completed the [draft ewasm standard](https://github.com/ewasm/design/blob/master/eth_interface.md) supported by Sean Young's work on ([https://github.com/hyperledger-labs/solang](https://github.com/hyperledger-labs/solang)) with Burrow as a supported ledger. This means that Burrow combined with Solang offers a complete stack for compiling and running Solidity ewasm contracts. Since Fabric, Sawtooth, and Iroha already consume the Burrow EVM implementation, these could easily be extended to also include the ewasm implementation. This would make it possible to use Solang and other ewasm tooling with those ledgers.

Vent - our Ethereum-to-SQL mapping layer now supports listening to web3 JSON-RPC chains (all mainline Ethereum clients) to build tables. This opens up interesting possibilities for contract oracles, state channels, and layer-2 scaling. We have continued to keep up-to-date with the latest Tendermint.

We now also support calling between our three smart contract engines - EVM, ewasm, and Go 'natives'. Our calling and state conventions are all Ethereum, but provide a lot of flexibility compared to mainline Ethereum clients.

# Current Plans

Burrow is preparing itself to support connection to multiple other chains by supporting reading from Ethereum with Vent and we soon hope to support Cosmos via the IBC protocol which we are poised to adopt based on our use of Tendermint consensus.

I want to provide support for AssemblyScript (a subset of Typescript) contracts via ewasm that can call, and be called from Solidity.

We will be extending our NameReg service to hold Burrow-global references to external resources (like Ethereum accounts, external tokens, and Hoard and IPFS content.

# Maintainer Diversity

We have maintained our maintainer diversity:

- Greg Hill of [https://www.interlay.io/](https://www.interlay.io/)
- Sean Young of [https://github.com/hyperledger-labs/solang](https://github.com/hyperledger-labs/solang) and Linux Kernel
- Silas Davis of [https://monax.io/](https://monax.io/)
- Casey Kuhlman of [https://monax.io/](https://monax.io/)

All of whom are actively contributing.

# Contributor Diversity

We have had significant contributions from:

- [https://github.com/vgrabovski-lacero-platform](https://github.com/vgrabovski-lacero-platform) (critical EVM fixes and improvements, multiple changes)
- [https://github.com/yoongbok-lee](https://github.com/yoongbok-lee) (much expanded ewasm support, multiple change)
- [https://github.com/bzp99](https://github.com/bzp99) (OS portability imrpovements)

# Help from the TSC

One of the most battle-tested and potentially widely applicable parts of burrow is Vent - our SQL mapping layer. To my knowledge nothing else quite like it exists serving the Solidity/Ethereum community. With our recent addition of Ethereum support I believe this component of Burrow might be of significant value even to those not using Burrow today. It would be useful to have an opportunity to describe briefly how this component works, what one can do with it, and to solicit opinions on how to attract collaborators.

I think the recent developments with Vent and our ewasm abilities could position Burrow as a pragmatic state channel/oracle solution for public blockchain.

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
