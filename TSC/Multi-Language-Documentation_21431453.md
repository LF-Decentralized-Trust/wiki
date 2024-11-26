1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [Project Proposals](Project-Proposals_21430788.html)
5. [2020 Finished Proposals](2020-Finished-Proposals_21430790.html)

# Technical Oversight Committee : Multi-Language Documentation

Created by Zhenhua Zhao, last modified by Nathan George on Jun 11, 2020

# Project Identifier

Support multi-language to help different language speakers learn and use hyperledger fabric at the same documentation website.

# Sponsor(s)

Rich Zhao, [zhao.zhenhua@gmail.com](mailto:zhao.zhenhua@gmail.com)

Technical Working Group China(TWGC) has been working for a long time to translate fabric documentation, so far we found it is the best way to maintain documentation.

# Abstract

Help different language speakers learn fabric in their own language. 

# Context

# Dependent Projects

# Motivation

Hyperledger Fabric documentation is written in English.  For those contributors whose native language is not English, they have difficulty contributing to or using hyperledger projects. If the documentation and log messages in software code can be translated into their own native language, it will help build a larger community of contributors and users. 

Technical Working Group China has been working for a long time to translate fabric documentation, we use a separate repo to host the documentation but if we can use the same website as the English documentation, it would be more official and convenient for users to use. 

Besides, Chinese, we do see other languages are required too.  

# Status

TWGC has translated about half of fabric v2 documentation with the current solution, it is available at [https://fabric-documentations.readthedocs.io/en/latest/](https://fabric-documentations.readthedocs.io/en/latest/)

# Solution

The solution needs：

1. documentation manage framework, sphinx which Fabric is using. Fabric English documentation uses Sphinx v1.7 to manage documentation materials, like .rst, .md files, and the structure layout and build to final output format HTML, pdf, ePUB, etc. Sphinx is a documentation framework based on python, we need to upgrade sphinx to version 2 for more compatible. It has been done through [https://gerrit.hyperledger.org/r/c/fabric/+/31667](https://gerrit.hyperledger.org/r/c/fabric/+/31667)
2. A repo to store documentation material and collaborate among contributors. Fabric English documentation uses the same repo as fabric code, it is okay for other languages to use the same existing repo, but as the documentation doesn't share the update release pace as code, it is better to use a separate repo to host ALL documentation materials.  All means do NOT separate other language documentation from English documentation, as others are translated from English. Translators/contributors need to monitor English status.
3. A translation tool. We prefer transfex.com. Because,
   
   1. it is free for open source projects. The paid account has a statistics report,  but it is fine without reports.
   2. More importantly,  it is very collaborative,  translators can working simultaneously, translating, reviewing, etc.
   3. It provides a CLI tx, like git, contributors can use tx to pull from/push to transfex
4. readthedocs account to host the documentation. Fabris is using it, just need to merge other languages into it.

For more detail refer to:  [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1lOF9kxjN4hK0b4YzlEVsHO8BcB2BjA3CMSemkfdDTdM/edit?usp=sharing)

# Efforts and Resources

Suggest using a separate repo to host all documentation material. 

# How To

# References

# Closure

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:7153872d-7890-4ca8-a633-d87fdf1e9a8d?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:62746046-52ae-43bb-827b-6dfdde9f07d7?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:24

[Atlassian](http://www.atlassian.com/)
