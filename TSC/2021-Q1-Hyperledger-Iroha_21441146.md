1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Iroha

Created by Sara Garifullina, last modified by Gari Singh on Mar 17, 2021

# Project

Hyperledger Iroha

Project Health

Currently, there are 2 teams working on Iroha - Iroha v1 and Iroha v2. Iroha 1 team is less active and mostly works on providing and maintaining a stable 1.2 version, fixing some issues with the release while team Iroha 2 is actively working on creation of the newer version. Community is active and appropriate, we are happy to have contributors who help the new users to resolve any difficulties with using Iroha. 

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Not yet, will do
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? Not yet, will do

# Questions/Issues for the TSC

Are there any newsletters we could subscribe to to learn about important TSC solutions without following all the discussions in TSC group?

What are the due dates for renaming the master branch and adding repoliner?

# Releases

[HL Iroha v1.2](https://github.com/hyperledger/iroha/releases/tag/1.2.0)

# Overall Activity in the Past Quarter

For Iroha 1: 

We worked to release 1.2 and now to stabilise it as well as possible. 

1. With the help from Diva.exchange developers we fixed several stability issues when network is slow and some peers are disconnected
2. Improved performance by optimising some sql scripts
3. Improving Iroha to migrate between different versions with as minimum downtime as possible
4. Working on switching to KV database that expected to bring huge performance boost

For Iroha 2: 

1. Introduced Permissions model
2. Introduced Multisignature accounts and transactions
3. Developed MVP of client library in Java
4. Simplified network startup with genesis block
5. Multiple usability improvements and bug fixes

We kept our bi-weekly community calls going - some of the interesting presentations are in our wiki. 

# Current Plans

Iroha 1 plans:

1. Finish version migration feature
2. Introduce KV database
3. Replace rxcpp dependency with custom subscription engine

Overall, we plan to stay on the same path: stabilising and improving Iroha v1, maintain it and work on Iroha v2's new features. We want to keep the communication with our amazing contributors and help others use Iroha for their projects. Hopefully, we will also be able to make some interesting content about how to use Iroha. 

# Maintainer Diversity

One new Rust developer for Iroha 2 project - Ivan Rybin. 

Sonoko Mizuki is an independent contributor maintainer to Iroha 2

# Contributor Diversity

diva.exchange team is still contributing a lot into Iroha, as well as Baziorek. Also, please see maintainer diversity regarding this. 

# Additional Information

Nothing special at the moment. 

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
