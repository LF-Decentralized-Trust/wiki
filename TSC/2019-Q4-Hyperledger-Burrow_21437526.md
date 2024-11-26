1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q4 Hyperledger Burrow

Created by Sean Young, last modified by Angelo de Caro on Nov 13, 2019

# Project

[https://github.com/hyperledger/burrow/](https://github.com/hyperledger/burrow/)

Project Health

Our last update mentioned that there was a lack of documentation, which was inhibiting new users. This has mostly been rectified and now documentation requests are for more obscure features. 

# Questions/Issues for the TSC

Some work has gone toward promoting burrow, for example [https://www.hyperledger.org/blog/2019/10/08/burrow-the-boring-blockchain](https://www.hyperledger.org/blog/2019/10/08/burrow-the-boring-blockchain)

We are always looking for further to promote burrow. Suggestions are welcome.

# Releases

- [v0.28.0](https://github.com/hyperledger/burrow/releases/tag/v0.28.0) Burrow now remembers contact ABIs (and other metadata), bond and unbond transactions, many fixes.
- [v0.28.1](https://github.com/hyperledger/burrow/releases/tag/v0.28.1) Burrow node js module in main repo
- [v0.28.2](https://github.com/hyperledger/burrow/releases/tag/v0.28.2) burrow vent decodes evm events before applying any filters
- [v0.29.0](https://github.com/hyperledger/burrow/releases/tag/v0.29.0) web3 support, IdentifyTx, lots of new documentation. natives contracts are first class contracts.
- [v0.29.1](https://github.com/hyperledger/burrow/releases/tag/v0.29.1) bug fixes
- [v0.29.2](https://github.com/hyperledger/burrow/releases/tag/v0.29.2) bug fixes

# Overall Activity in the Past Quarter

There has been plenty of development, the vast majority from Monax employees, including:

- lots of documentation has been written and it can be read at [https://hyperledger.github.io/burrow](https://hyperledger.github.io/burrow).
- web3 support
- metadata for contract. The metadata includes  ABI, source file, contract name and compiler version. This stored on-chain. As a result  it is no longer necessary to manage ABIs in files.
- "native" contracts (written in go and compiled into the burrow binary are now first class contracts. This means that burrow supports Solidity (EVM) contracts, WASM (e.g. solang) contracts, and native golang contract which can all call each other.
- New command "burrow accounts" which lists all the contract names, ABI etc for all accounts.
- state is now serialised in protobuf, rather than go-amino
- The [node npm to interact with burrow](https://www.npmjs.com/package/@hyperledger/burrow) has been merged into main burrow repo.
- Work on identifyTx, bond, and unbond transactions.
- Many other issues have also been solved.

# Current Plans

We need to have a push on explaining Burrow and documenting. A lot has already been done towards this goal.

Now that golang native contracts (called "natives") are first class contracts it is planned that burrow functionality which unique to burrow (e.g. name reg, governance) will be implemented as natives so that the can be called from regular call transactions, or from solidity, or from our deploymen tool, burrow deploy.

Otherwise plans are unchanged since last update.

# Maintainer Diversity

No new maintainers. We have 4 from Monax, 2 non-Monax

# Contributor Diversity

No new no-Monax contributers.

# Additional Information

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:503b5691-8e92-4d2d-83d3-e9e74d296436?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
