1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Extend existing Iroha - Cactus integration

Created by baziorek, last modified by Min Yu on Dec 19, 2022

**Project Title**Extend HL Cactus - HL Iroha 1.* integration (Iroha plugin in Cactus) from last year with more futures and make the plugin configurable**Status**

COMPLETED

**Difficulty**

HIGH

# Description

[Hyperledger Cactus](https://www.hyperledger.org/use/cactus) is a blockchain decentralized integration tool designed to allow users to securely integrate different blockchains started by companies Fujitsu and Accenture. Cactus has pluggable architecture which makes easy to integrate various blockchain by creating [plugin](https://github.com/hyperledger-labs/blockchain-integration-framework/files/4228021/hyperledger-blockchain-integration-framework-whitepaper.pdf), currently [plugins](https://github.com/hyperledger/cactus/blob/main/whitepaper/whitepaper.md#561-ledger-connector-plugins) for Fabric, Besu, Quorum are implemented. Cactus allows to transfer not only assets but also data between multiple blockchains. On the other hand Iroha (version 1.x) is great with asset management, and has functionality to store data, which makes those two projects a perfect fit!

In previous HL Summer Mentorship Project the integration was successfully made ([link](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/HL+Iroha+and+HL+Cactus+Integration)). As a result of the project commands and queries from HL Iroha were integrated, it was Iroha 1.2, but after that year multiple features and changes was added to Iroha (e.g. Healthcheck). What is more - not all nice to have features was integrated ([list of missing features](https://github.com/hyperledger/cactus/issues?q=is%3Aissue%20is%3Aopen%20label%3Airoha)). It is also important to make the configuration flexible to make its possible to set up connection between two different blockchain networks (e.g. Iroha → Iroha).

In short, the project's goal is to:

1. Implement missing features + tests + documentation
2. Update Iroha version to newest in the integration.
3. Make the plugin configurable
4. Create tutorial demonstrating how to set up connection between multiple networks (at least Iroha - Iroha networks)

# Additional Information

[Hyperledger Cactus](https://www.hyperledger.org/use/cactus) ([whitepaper](https://github.com/hyperledger/cactus/blob/main/whitepaper/whitepaper.md), [whitepaper of integration](https://github.com/hyperledger-labs/blockchain-integration-framework/files/4228021/hyperledger-blockchain-integration-framework-whitepaper.pdf), [chat](https://chat.hyperledger.org/channel/cactus), [already implemented plugins](https://github.com/hyperledger/cactus/tree/main/packages))

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha))

Last year internship: [HL Iroha and HL Cactus Integration](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/HL+Iroha+and+HL+Cactus+Integration)

[Iroha javascript client library](https://github.com/hyperledger/iroha-javascript)

[Iroha-python client library](https://github.com/hyperledger/iroha-python)

# Learning Objectives

The mentee will be able to learn:

- ways of integrating different projects from architectural point of view,
- architecture of Iroha (1.x) and Cactus,
- work in true spirit of open-source, communicating with both Iroha and Cactus community, joining calls and using other community tools,
- writing documentation, so anyone in the community could use the results of their work,
- following rules and standards of open-source projects created by hyperledger,
- joining pair-programming sessions for HL Cactus would be helpful

# Expected Outcome

1. Documented, ready-to-use extended integration of Iroha and Cactus (Iroha version at least 1.4)
2. Documentation how to integrate multiple (two and more) iroha's networks with Cactus
3. Documented example of integration between Fabric and Iroha (Fabric plugin for Cactus is already implemented) integration,
4. Presenting changes to HL Iroha and HL Cactus communities.

# Relation to Hyperledger

This mentorship program will extend interoperability between [Hyperledger Cactus](https://www.hyperledger.org/use/cactus) and [Hyperledger Iroha](https://www.hyperledger.org/use/iroha) projects.

# Education Level

Preferred undergraduate.

# Skills

- Reading English documentation,
- NodeJS, Javascript - programming language of previous integration
- OpenApi
- Reading + modifying existing code
- Time organization

# Future plans

Open for cooperation after successful internship.

# Preferred Hours and Length of Internship

No preference, just finish in time.

# Mentor(s) Names and Contact Info

**Peter Somogyvari** (Accenture, Cactus Maintainer)  
email: peter.somogyvari@accenture.com  
Discord: peter\_somogyvari#3365

**Grzegorz Bazior** (Yonix Digital Systems, AGH University of Science and Technology, Iroha Maintainer)  
email: g.bazior\[you know what][yodiss.pl](http://yodiss.pl)  
Telegram: @baziorek  
Discord: baziorek#9186

# Mentee:

[Yashraj Desai](https://lf-hyperledger.atlassian.net/wiki/people/62cbca8e2c801edc3284953d?ref=confluence)

Email: yashrajdesai30@gmail.com

# Project results:

**Project pull requests:** 

[https://github.com/hyperledger/iroha-javascript/pull/110](https://github.com/hyperledger/iroha-javascript/pull/110)

[https://github.com/hyperledger/cactus/pull/2148](https://github.com/hyperledger/cactus/pull/2148)

[https://github.com/hyperledger/iroha-javascript/pull/125](https://github.com/hyperledger/iroha-javascript/pull/125)

[https://github.com/hyperledger/cactus/pull/2166](https://github.com/hyperledger/cactus/pull/2166)

[https://github.com/hyperledger/cactus/pull/2202](https://github.com/hyperledger/cactus/pull/2202)

# Final report:

[![](attachments/thumbnails/21954791/21967116)](attachments/21954791/21967116.pdf)

# Project Presentation Session Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [Extend existing Iroha - Cactus integration.pptx.pdf](attachments/21954791/21967116.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21954791/21967117.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
