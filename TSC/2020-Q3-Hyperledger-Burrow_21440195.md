1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q3 Hyperledger Burrow

Created by Silas Davis, last modified by Troy Ronda on Oct 01, 2020

# Project

Hyperledger Burrow

Project Health

This quarter has certainly been a fallow quarter for Burrow, mostly as a consequence of Covid and in the case of Monax the need to refocus on our product built on top of Burrow. We do have more work planned and another developer coming in to work on the SQL mapping layer Vent at the end of this year to extend its functionality.

Inevitably this raises considerations that have lingered around Burrow and the level of development activity from a wider community. I think it would be premature at this stage to talk about end-of-life for Burrow as I am aware of other companies taking an interest (such as CertiK). However I think the next two quarters will be critical for Burrow and on that timescale we should revisit this question and decide whether there is a realistic prospect of Burrow leaving incubation (chiefly in having sufficient contribution-weighted contributor diversity).

I do expect Q1 2021 to be quite active in terms of work that Monax needs to do on Burrow so one way or another Burrow does need an active development home in the medium term, but I defer to the TSC to judge whether Hyperledger is that home. If we are able to garner greater community involvement then I think it could, but so far with the time and resources I have available to me for community building that has not really happened.

# Questions/Issues for the TSC

Just any reflections on the above.

# Releases

\- [\[v0.30.5\]](https://github.com/hyperledger/burrow/releases/tag/v0.30.5) Provide \`BytesToHex\` for Vent projections

# Overall Activity in the Past Quarter and Current Plans

There has been a certain amount of thinking activity away from lines of code:

- Paper design for some features to Vent that make it more capable to form projections over events - generated columns, literal columns, JSON support. You can define Solidity events (via EVM log) and form log-structured tables or realised projections (using SQL upsert idioms) to reflect your blockchain-stored evidence in a traditional SQL schema read-only, combined with other write tables, blended with views
- Idea to support event emission via AssemblyScript WASM constracts
- Using JSON Schema and tooling from the Typescript world (particularly the excellent [https://github.com/gcanti/io-ts](https://github.com/gcanti/io-ts)) to generate smart contract stub code, event schema, and database mappings

The theme of all this design work is geared towards emphasising a schema-first (OpenAPI spec/JSON schema) and code-generation heavy way of working with event streams and having Burrow specialise in storing streams of events with relatively lightweight (much more lightweight that what we have typically done in Solidity) contracts to maintain integrity of our events. Also the idea to move away from Solidity/EVM and provide a way of working with events in AssemblyScript (keeping the events isomoporphic to Solidity events).

# Maintainer Diversity

See: [https://github.com/hyperledger/burrow/blob/master/MAINTAINERS.md](https://github.com/hyperledger/burrow/blob/master/MAINTAINERS.md)

# Contributor Diversity

No new contributors

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
