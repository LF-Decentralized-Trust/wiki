1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)

# Hyperledger Mentorship Program : HL Burrow and HL Iroha extend existing Solidity VM integration

Created by baziorek, last modified by Min Yu on Aug 25, 2021

**Project Title**Extend Solidity VM (from Hyperledger Burrow) integration in Hyperledger Iroha (1.x) and query pipeline**Status**

COMPLETED

**Difficulty**

LOW   

# Description

Hyperledger Iroha has Smart Contracts from Hyperledger Burrow. It was done in [internship project in 2019](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Integrate+Solidity+VM+%28from+Hyperledger+Burrow%29+to+Hyperledger+Iroha), then integrated into main Iroha code in [version 1.2](https://github.com/hyperledger/iroha/tree/1.2.0). Unfortunately integration does not integrate all Iroha commands and queries (currently only: [TansferAsset](https://iroha.readthedocs.io/en/master/develop/api/commands.html#transfer-asset) and [GetAccountAssets](https://iroha.readthedocs.io/en/master/develop/api/queries.html#get-account-assets) are integrated). So task is to integrate all [commands](https://iroha.readthedocs.io/en/master/develop/api/commands.html) and [queries](https://iroha.readthedocs.io/en/master/develop/api/queries.html) and also [permissions](https://iroha.readthedocs.io/en/master/develop/api/permissions.html).

# Additional Information

[Completed internship project of integration between Burrow and Iroha from 2019 year](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Integrate+Solidity+VM+%28from+Hyperledger+Burrow%29+to+Hyperledger+Iroha).  
[Documentation of current Burrow integration in Iroha](https://iroha.readthedocs.io/en/main/integrations/burrow.html).  
[Iroha code connected with smart contracts](https://github.com/hyperledger/iroha/tree/master/goSrc/src/vmCaller) (suggested files to extend: [commands.go](https://github.com/hyperledger/iroha/blob/master/goSrc/src/vmCaller/iroha/commands.go) and [native\_contract.go](https://github.com/hyperledger/iroha/blob/master/goSrc/src/vmCaller/evm/native_contract.go))

# Learning Objectives

The mentee will be able to learn:

- ways of integrating different projects from architectural point of view,
- architecture of Iroha (1.x) and optionally Burrow,
- work in true spirit of open-source, communicating with both Iroha and optionally Burrow community, joining calls and using other community tools,
- writing documentation, so anyone in the community could use the results of their work,
- following rules and standards of open-source projects created by hyperledger,
- Intern would get experience in virtual machines,

# Expected Outcome

Documented integration of all Iroha (version 1.x) commands, queries and permissions with unit tests.

# Relation to Hyperledger

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha))

[Hyperledger Burrow](https://www.hyperledger.org/use/hyperledger-burrow) ([documentation](https://hyperledger.github.io/burrow/), [chat](https://chat.hyperledger.org/channel/burrow), [wiki](https://lf-hyperledger.atlassian.net/wiki/display/burrow/))

Internship's project from 2019 year: [Integrate Solidity VM (from Hyperledger Burrow) to Hyperledger Iroha transaction and query pipeline](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Integrate+Solidity+VM+%28from+Hyperledger+Burrow%29+to+Hyperledger+Iroha)

# Education Level

Preferred undergraduate.

# Skills

- Reading english documentation,
- Skills and experience with Go programming.
- Would be nice to have Solidity and VM skills/experience.

# Future plans

Build a visual programming language over the integrated virtual machine. Opened for cooperation after successful internship.

# Preferred Hours and Length of Internship

No preference (just do Your job good before 15th August according to project plan and report to mentors every week progress and report progress during [bi-weekly Iroha Community meeting](https://lists.hyperledger.org/g/iroha/calendar)).

# Mentor Name and Contact Info

**Grzegorz Bazior** (Yonix Digital Systems, AGH University of Science and Technology)  
email: g.bazior\[you know what][yodiss.pl](http://yodiss.pl)  
gitter and Telegram and RocketChat: @baziorek

# Mentee

[Ayush Jalan](https://lf-hyperledger.atlassian.net/wiki/people/60b3c7e848549e0069ebb808?ref=confluence) IT Roorkee

# Project Results

Project Repository: [https://github.com/Ayush-Jalan/iroha](https://github.com/Ayush-Jalan/iroha)

Midterm Evaluation: [https://github.com/hyperledger/iroha/pull/1152](https://github.com/hyperledger/iroha/pull/1152)

Final Evaluation: [https://github.com/hyperledger/iroha/pull/1326](https://github.com/hyperledger/iroha/pull/1326)

Documentation: [https://github.com/hyperledger/iroha/pull/1334](https://github.com/hyperledger/iroha/pull/1334)

# Final Report

[![](attachments/thumbnails/21956755/21965567)](attachments/21956755/21965567.pdf)

# Project Presentation Session Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation - 2021.pptx.pdf](attachments/21956755/21965567.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21956755/21965581.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 14:56

[Atlassian](http://www.atlassian.com/)
