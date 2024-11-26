1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Iroha

Created by Sara Garifullina, last modified by Angelo de Caro on Dec 09, 2021

Project Health

Everything is on track - Iroha 1 keeps maintained. Bugs are fixe, some smaller new features and refactoring are done. Iroha 2 is in very active development with a big team. Together with the Hyperledger Team we shared a survey that should help make good design decisions on certain features. 

Community is doing good, internships are done - just some small issues need to be fixed for releases. 

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes.
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes?

# Questions/Issues for the TSC

No questions for now. 

# Releases

[https://github.com/hyperledger/iroha/releases/tag/1.3.0-rc.1](https://github.com/hyperledger/iroha/releases/tag/1.3.0-rc.1) - Pre-release, need to have some small fixes done, such as tests. Also, Iroha Libraries releases are planned soon.

# Overall Activity in the Past Quarter

Communications are on track - questions are answered; there are plans for discussing plans for Iroha with active community members. Questions are replied (thanks to our community for a lot of help there!). About the technical accomplishments, here they are: 

## v1

Worked on fixing small issues and improved stability of Iroha for releasing it:

1. Improved crash tolerance of the nodes;
2. Fixed memory issues;
3. Run sequence of high-load tests with different network configurations.

## v2

1. Core maintainers team expanded
2. All client libraries finished - now they will be periodically updated
3. Introduced p2p library to increase performance
4. Improved transaction gossiping
5. Introduced metadata to entities in WSV
6. Introduced Query Permissions

# Current Plans

## v1

1. Special Iroha mode: synchronising the nodes without taking part in consensus
2. Improve processes for Multi-signature transactions and ordering service
3. Customise cache for RocksDB

## v2

### Near Future

1. Actively preparing for the pre-release
2. Longevity stand
3. Stress testing

### General Plans

1. On chain Triggers functionality
2. Transaction fees
3. Staking for Sumeragi consensus

# Maintainer Diversity

Most of the new people joined the Iroha 2 team: 

Marin Versic (@mversic), Sato (@s8sato), Aleksander Petrosyan (@appetrosyan) - all joined Soramitsu but represent a diverse international developers from all around the world. 

# Contributor Diversity

We are happy to be working closely the last quarter with [baziorek](https://lf-hyperledger.atlassian.net/wiki/people/70121:fcfd1447-e409-47ac-bf14-f78e6031899d?ref=confluence)  and his team. Hopefully, we'll continue working on Iroha together.  

# Additional Information

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
