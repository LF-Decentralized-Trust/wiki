1. [Hyperledger Caliper](index.html)

# ![Home Page](images/icons/contenttypes/home_page_16.png) Hyperledger Caliper : Hyperledger Caliper

Created by Tracy Kuhrt, last modified by Ry Jones on Apr 23, 2024

**Project**

**Status**

[INCUBATION](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-incubation)

**CII Badge**

[![](https://bestpractices.coreinfrastructure.org/projects/2381/badge)](https://bestpractices.coreinfrastructure.org/projects/2381)

**Description**Blockchain benchmark framework which allows users to measure the performance of a specific blockchain implementation with a set of predefined use cases.

Caliper is a blockchain benchmark framework which allows users to measure the performance of a specific blockchain implementation with a set of predefined use cases. Caliper will produce reports containing a number of performance indicators, such as TPS (Transactions Per Second), transaction latency, resource utilisation etc. The intent is for Caliper results to be used as a reference in supporting the choice of a blockchain implementation suitable for the user-specific use-cases. Given the variety of blockchain configurations, network setup, as well as the specific use-cases in mind, it is not intended to be an authoritative performance assessment, nor to be used for simple comparative purposes (e.g. blockchain A does 5 TPS and blockchain B does 10 TPS, therefore B is better). The Caliper project references the definitions, metrics, and terminology as defined by the Performance &amp; Scalability Working Group (PSWG).

# Key Characteristics

- A unified blockchain benchmark framework. We provide a common layer to integrate with major existing blockchain framework/platforms, so that the same benchmarks can be run for different blockchain systems Some benchmark test environment will be provided to help different people run tests under the same environment, blockchain management tools like Hyperledger Cello could be integrated later to deploy and operate the environment. Also, users can use their existing environment and configure Caliper to run the test under the environment.
- A commonly accepted definition of performance indicators. You cannot compare an apple and a pear directly unless some common criteria are set. We will work closely with PSWG to provide a common definition of performance indicators that users care about, such as TPS, latency, resource utilization, etc.
- A set of commonly accepted benchmark cases. The goal of Caliper includes providing a set of easy-understandable benchmark cases so that each blockchain solution can be compared in various scenarios. This calls for much collaboration from PSWG, Requirement WG and other WG in Hyperledger community as well as blockchain practitioners to cover as many use cases that are of user’s interest as possible.

# Project Management

Issue Tracking - [https://github.com/hyperledger/caliper/issues](https://github.com/hyperledger/caliper/issues "https://github.com/hyperledger/caliper/issues")

# Repositories

Source code: [https://github.com/hyperledger/caliper](https://github.com/hyperledger/caliper "https://github.com/hyperledger/caliper")

Documentation: [https://hyperledger.github.io/caliper/](https://hyperledger.github.io/caliper/)

# Additional Materials

- [Project health charts](https://docs.google.com/spreadsheets/d/e/2PACX-1vRZCaEWwKMZZCnHf-YVNcSpU3PYd81rozu9KVrSptg7NixRdyHp64isnLIKxq8fTJG7zg26UVpIgNaq/pubhtml?gid=1454794804&single=true)
- [2019 Hong Kong Bootcamp Tutorial](https://docs.google.com/presentation/d/1MtPSBgDXf3v7DicxTNr9srB0jGmdWew2tqvItJHculo/edit#slide=id.p1) (outdated, pre-publish version)

# License Scan Results

### License Audit

[2019-03 Caliper License Audit Summary](attachments/23101536/23101538.pdf)

[2019-03 Caliper License Audit Full Report](attachments/23101536/23101539.xlsx)

### License Audit Fixes

[Hyperledger Caliper License Github Issues](https://github.com/hyperledger/caliper/issues?utf8=%E2%9C%93&q=is%3Aissue%20is%3Aopen%20labels%3Alicense)

### Crypto Audit

[Hyperledger Export Notice](https://www.linuxfoundation.org/export/)

# Communication

## Mailing List

- [caliper](https://lists.hyperledger.org/g/caliper)
- Mail alias: [caliper@lists.hyperledger.org](mailto:caliper@lists.hyperledger.org)
- Mail archive: [https://lists.hyperledger.org/g/caliper/topics](https://lists.hyperledger.org/g/caliper/topics "https://lists.hyperledger.org/g/caliper/topics")
- Mail subscription: [https://lists.hyperledger.org/g/caliper](https://lists.hyperledger.org/g/caliper "https://lists.hyperledger.org/g/caliper")

## Chat (for questions and ephemeral discussions)

Questions are welcome and best asked in Hyperledger Discord.  [Learn more about Hyperledger Discord here](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Our+chat+service), get the invite and check out one of the many Caliper project channels.  

# Meeting

There is a community call **every four weeks** on Zoom, at UTC time 3PM on Wednesday. The exact meeting details can be found in [Hyperledger meeting calendar](https://lists.hyperledger.org/calendar).

#### Minutes

- October 17, 2018 [minutes](https://docs.google.com/document/d/1bbWNJdfgbY8s1qAky2D7N0Uis3MMqxfLGrv02pWOZMU/edit "https://docs.google.com/document/d/1bbWNJdfgbY8s1qAky2D7N0Uis3MMqxfLGrv02pWOZMU/edit")
- October 24, 2018 [minutes](https://docs.google.com/document/d/1TOfod4jv65XpoK_aNzMVruz_1xs4FVg5Ebi7ySR-5yc/edit?usp=sharing)
- October 30, 2018 [minutes](https://docs.google.com/document/d/11eRl0z27IEArHjCIgYunS9suzfygRsvE3FSz2AJLsPM/edit?usp=sharing)
- November 6, 2018 [minutes](https://docs.google.com/document/d/1OdTu3q0W_vOUh3V8gdihrgVyP4PjYknEVgB_aPqwEzQ/edit?usp=sharing)
- November 14, 2018 [minutes](https://docs.google.com/document/d/1F1MPhC1QEPDdDFhA11mYuAtwg7Eu6P0BY9kIMhVyx2s/edit?usp=sharing)
- November 21, 2018 [minutes](https://docs.google.com/document/d/1NC4NmGmXRA6sPbcJYIw3o1XW50qelx4UB_5cGcCnk5A/edit?usp=sharing)
- November 27, 2018 [minutes](https://docs.google.com/document/d/1WzH0Q6tO5F4JFIDfBeYg6Zg5ECXmSQ58_x7XPrUQJwo/edit?usp=sharing)
- December 4, 2018 [minutes](https://docs.google.com/document/d/19pyqdPl0Q5HLT44_Y5kmzerIf-6ahHv6URR2Wo36qaw/edit?usp=sharing)
- December 19, 2018 [minutes](https://docs.google.com/document/d/13CmJYIPqCJvajQMMQJ4hhYHZ9frdoBJme15TMHnYb_g/edit?usp=sharing)
- January 16, 2019  [minutes](https://docs.google.com/document/d/1RjZMAO6Dz0oC1Brn5NnJPc42_CCHcs92YK-Cd8bS-pA/edit?usp=sharing)
- March 27, 2019 [minutes](https://lf-hyperledger.atlassian.net/wiki/display/caliper/2019-03-27+Minutes)
- April 3, 2019 [minutes](https://lf-hyperledger.atlassian.net/wiki/display/caliper/2019-04-03+Minutes)
- May 22, 2019 [minutes](2019-05-22-Minutes_23101530.html)

# History

- [Proposed](https://docs.google.com/document/d/1cwScsNgYUj72vP2fqZ6vihYiuQcy45Ml2C_yLRI7EoQ/edit "https://docs.google.com/document/d/1cwScsNgYUj72vP2fqZ6vihYiuQcy45Ml2C_yLRI7EoQ/edit") by Haojun ZHOU and Victor HU, Huawei
- [Approved](https://lists.hyperledger.org/g/tsc/message/1422 "https://lists.hyperledger.org/g/tsc/message/1422") by the TSC on 2018-03-15

## Recent space activity

- [![](null/aa-avatar/5e3292559029c30ca0bc9620 "5e3292559029c30ca0bc9620")](null/display/~5e3292559029c30ca0bc9620)
  
  - [d\_kelsey](null/display/~5e3292559029c30ca0bc9620)
  - [Repos](Repos_23101534.html "data-linked-resource-id=") contributed Apr 24, 2024
  - [Audits](Audits_23101536.html "data-linked-resource-id=") contributed Apr 24, 2024
- [![](null/aa-avatar/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850 "557058:078cecfc-fb17-4d9a-8759-b5b74efa6850")](null/display/~557058%3A078cecfc-fb17-4d9a-8759-b5b74efa6850)
  
  - [Ry Jones](null/display/~557058%3A078cecfc-fb17-4d9a-8759-b5b74efa6850)
  - [Hyperledger Caliper](index.html "Hyperledger Caliper") contributed Apr 23, 2024
- [![](null/aa-avatar/712020:4b6a8d7d-e65a-471e-a60d-e945d09147e2 "712020:4b6a8d7d-e65a-471e-a60d-e945d09147e2")](null/display/~712020%3A4b6a8d7d-e65a-471e-a60d-e945d09147e2)
  
  - [Attila Klenik](null/display/~712020%3A4b6a8d7d-e65a-471e-a60d-e945d09147e2)
  - [Caliper Development Plan](Caliper-Development-Plan_23101526.html "data-linked-resource-id=") contributed Nov 06, 2019
  - [Meeting Notes](Meeting-Notes_23101469.html "data-linked-resource-id=") contributed Jun 12, 2019

[Show More](/wiki/plugins/recently-updated/changes.action?theme=social&pageSize=5&startIndex=5&searchToken=1&spaceKeys=caliper&contentType=page%2C%20comment%2C%20blogpost&cursor=_f_NQ%3D%3D_sa_WzE1NjAzMzc3MzYwMDAsIlx0MjMxMDE0Njkgb1o1UF1BUD5nJ1peYFxcV21nb3RXIGNwIl0%3D) ![Please wait](images/icons/wait.gif)

## Space contributors

- [d\_kelsey](/wiki/display/~5e3292559029c30ca0bc9620) (216 days ago)
- [Ry Jones](/wiki/display/~557058%3A078cecfc-fb17-4d9a-8759-b5b74efa6850) (216 days ago)
- [Sean Bohan](/wiki/display/~634eef0301c2ff842c15f9e7) (871 days ago)
- [Attila Klenik](/wiki/display/~712020%3A4b6a8d7d-e65a-471e-a60d-e945d09147e2) (1455 days ago)
- [Nick Lincoln](/wiki/display/~557058%3Abc9b68d2-6378-4ccc-a1c0-687d78691d21) (1856 days ago)
- [...](# "6 more...")
- [David Huseby](/wiki/display/~5c81ef6e187e8e0b95b0b1e9) (2012 days ago)
- [qinghui hou](/wiki/display/~712020%3Aeea647de-9cdf-467b-86ab-6b67c5ef6b01) (2039 days ago)
- [qinghui hou](/wiki/display/~712020%3A8d3420e4-78bd-47fc-aecf-8f7170fd2496) (2063 days ago)
- [yu pan](/wiki/display/~712020%3Aca7fa922-56bd-4423-9d04-d41c5c2ad10a) (2073 days ago)
- [Tracy Kuhrt](/wiki/display/~712020%3Aeb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e) (2126 days ago)
- [Silona Bonewald](/wiki/display/~712020%3A60ad7903-c627-4d15-ac02-e45d3098bd8e) (2142 days ago)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger\_Caliper\_Logo\_Color.png](attachments/23101442/23101461.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Caliper\_Logo\_Color.svg](attachments/23101442/23101488.svg) (image/svg+xml)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Caliper.png](attachments/23101442/23101562.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Caliper.svg](attachments/23101442/23101564.svg) (image/svg+xml)

Document generated by Confluence on Nov 26, 2024 12:37

[Atlassian](http://www.atlassian.com/)
