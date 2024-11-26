1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q2 Hyperledger Burrow

Created by Silas Davis, last modified by David Enyeart on Jul 29, 2021

Project Health

Burrow is doing better than ever before. We've added some significant features and [random people from the internet are fixing our off-by-ones](https://github.com/hyperledger/burrow/pull/1488). We also have a new team, Damascus Mile, with funding from the UK Cabinet Office who are building out a logistics platform on top of Burrow.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)?
   
   yes
   
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)?
   
   yes

# Questions/Issues for the TSC

No issues, but would like to call out Typescript code generation (AKA solts) along with the improved Javascript/Typescript client gives a *vastly*  improved application-building experience (here is an [example of the generated code](https://github.com/hyperledger/burrow/blob/1f0dcffb3c70beb7ede57a09f26dd39c79a8c6f3/js/src/solts/sol/Eventer.abi.ts)). [@hyperledger/burrow](https://www.npmjs.com/package/@hyperledger/burrow) now exposes a \`build\` function that takes a Solidity source tree and generates strongly typed bindings for Burrow that embed the contract bytecode, ABI, metadata, and allows you to deploy the contract, stream events, and call functions all via a strongly typed interfaces. Kudos to [Gregory Hill](https://lf-hyperledger.atlassian.net/wiki/people/712020:f4f398ef-d40e-4c66-90c9-47062a10976a?ref=confluence) for building the original solts.

Um, as ever, this is [not very well documented](https://github.com/hyperledger/burrow/blob/main/js/src/solts/build.ts#L24-L31) ¯\\\_(ツ)\_/¯.

# Releases

- 0.31.1 - Web3 and Vent fixes
- 0.31.2 - Dump/restore fixes
- 0.31.3 - Dump/restore improvements
- 0.32.0 - Burrow.js rewrite in Typescript, better ABI library, core state cache concurrency fix
- 0.32.1 - Improved errors and Javascript type coercion
- 0.33.0 - Introduced Solidity-to-Typescript client-side code generation, fixed client-side events, fixed finite stream bounds
- 0.33.1 - Inline JS source maps and fixed BytesNN typing
- 0.34.0 - Simplified JS codegen Provider interface (supporting other implementations), codegen fixes

See [https://github.com/hyperledger/burrow/blob/main/CHANGELOG.md](https://github.com/hyperledger/burrow/blob/main/CHANGELOG.md) for more details.

# Overall Activity in the Past Quarter

Chat remains relatively quiet generating a handful of messages per month. Github has seen some small but deep patches which seems to indicate there is some 'serious' usage going on. Damascus Mile has chosen to use Burrow as an ideal 'root stock' for their logistics project - hopefully evidence of Burrow's effort to be extensible and modular. Development activity has picked up quite a bit over previous two quarters.

# Current Plans

Two major roadmap items are in play:

1. State-splitting - providing a better way to divide account state while preserving commitments/proofs. Also the possibility of projecting out some state in an 'export' while preserving proofs. The relevance being around state channels/optimistic roll-ups where we would like to be able to provide a more granular subset of state than our current single global state root allows.
2. Providing more practical support for WASM contracts (including AssemblyScript being given our Typescript leanings) by providing client library support and doing more testing.

# Maintainer Diversity

We have added Ommi Shimizu from Monax.

**Active Maintainers**

NameGitHubemailGreg Hill[@gregdhill](https://github.com/gregdhill)[gregorydhill@outlook.com](mailto:gregorydhill@outlook.com)Sean Young[@seanyoung](https://github.com/seanyoung)[sean@mess.org](mailto:sean@mess.org)Casey Kuhlman[@compleatang](https://github.com/compleatang)[casey.kuhlman@monax.io](mailto:casey.kuhlman@monax.io)Silas Davis[@silasdavis](https://github.com/silasdavis)[silas.davis@monax.io](mailto:silas.davis@monax.io)Ommi Shimizu[@ommish](https://github.com/ommish)[ommi.shimizu@monax.io](mailto:ommi.shimizu@monax.io)

# Contributor Diversity

We have had around five new individual contributors this quarter and interest in using us from Damascus Mile.

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
