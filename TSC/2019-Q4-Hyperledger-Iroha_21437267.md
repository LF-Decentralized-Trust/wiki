1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q4 Hyperledger Iroha

Created by Sara Garifullina, last modified by Nathan George on Mar 31, 2020

# Project

HL Iroha

Project Health

During the last quarter we managed to release new version and a patch that made the project more stable as well as added some new features to Iroha. Internships this year were great – both HL and interns from Innopolis University – all of their projects were successful to different extent. Community is relatively active, new projects use Iroha. Overall, everything is well, with no drastic highs or lows. 

# Questions/Issues for the TSC

1\) We would really like to revive the discussion we started some time ago with [David Huseby](https://lf-hyperledger.atlassian.net/wiki/people/5c81ef6e187e8e0b95b0b1e9?ref=confluence) and [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) about what help we could gather with resources for a huge Iroha testing on 100 nodes. There was an option of creating a simulation or getting the infrastructure from CNCF, because the more interest the project gets, the more questions we receive on the performance – it is really important on this stage of project development to have good data on the performance. 

2\) Hoping that Ry was able to track down who is in charge of the HL's Transifex: [https://www.transifex.com/hyperledger/public/](https://www.transifex.com/hyperledger/public/) – we cannot continue using the service that we have now (it is impossible to decently automate it). There is also an option of using one of the open-source localisation tools if HL could provide the infrastructure – all projects could benefit from that ([Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence) has some ideas of what could be used). 

3\) Another question was the security audit. It was agreed with [David Huseby](https://lf-hyperledger.atlassian.net/wiki/people/5c81ef6e187e8e0b95b0b1e9?ref=confluence) that we will have it after we integrate Ursa into Iroha  – but there appears to be a misunderstanding about it to be a cause for the next major release. Integration of Ursa did not require that (and so the checklist that includes the audit) but at the same time, we did not have an audit for quite a while now. How can we resolve that? 

# Releases

[Hyperledger Iroha v1.1](https://github.com/hyperledger/iroha/releases/tag/1.1.0) – 24th of July

[Release 1.1.1](https://github.com/hyperledger/iroha/releases/tag/1.1.1) – 20th of September

# Overall Activity in the Past Quarter

Questions are being answered, as well as e-mails. It might be interesting to notice that we've been receiving more advanced questions recently that might mean deeper interest in the project. We also restructured documentation (also might have helped with easier questions) and added HL Google Analytics code so we could check the interest.

As for the technical updates: 

In our 1.1 we included new API features such as: RemovePeer command, GetPeers query, CompareAndSetAccountDetail command as well as the respective permissions

Added Postgres options

Integrated vcpkg for dependencies

Together with interns, integrated HL Ursa, Explorer, Burrow! 

Were accepted and integrated support for [OSS-Fuzz](https://github.com/google/oss-fuzz)

We are also trying to rework the storage (huge refactoring that is taking some time)

Work on new TUI (instead of the outdated CLI) is almost finished!

# Current Plans

As mentioned before – we are working on some major refactoring that will allow Iroha to be quicker and even more efficient. As for releases, we are planning on having one very soon – when HL Burrow integration is finalised. It will have all of the new integrations and EVM provided by Burrow. 

Also, we are working on making a pluggable BFT consensus – currently it is in research state. Also, we are hoping to fix CI issues or join HL in the universal CI for all of the projects. 

Hopefully, we'll have some news on Iroha certification, too. 

# Maintainer Diversity

[Evgeny Kovalev](https://lf-hyperledger.atlassian.net/wiki/people/712020:594f9075-4294-4635-bee5-2184c91eb7b6?ref=confluence) [https://github.com/ekovalev](https://github.com/ekovalev)

Artyom Gorbachov [https://github.com/art-gor](https://github.com/art-gor)

# Contributor Diversity

Currently, it is Soramitsu + another Japanese company currently starting to work with Iroha

+new individual contributor: [https://github.com/ericcurtin](https://github.com/ericcurtin)

# Additional Information

We went to Moscow Bootcamp and hope to see new faces among our community after it! 

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
