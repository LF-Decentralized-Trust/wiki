1. [Technical Working Group China](index.html)
2. [Technical Working Group China](Technical-Working-Group-China_22151170.html)
3. [Events Organization](Events-Organization_22151242.html)

# Technical Working Group China : Hyperledger Online Meetups

Created by J Guo, last modified by Scott Long on Aug 16, 2020

Event List 当前排期

TopicSpeakersDate &amp; TimeDescriptionLinks (if any)Fabric 2.0 概述

郭剑南

梁志超

3月12日Fabric目前已经发布了2.0正式版，在许多方面相较于1.x进行了改进。本讲将回顾Fabric的发展历程，简要讲解整体架构、应用实践，以及社区的发展。另外，梁志超先生分享了众多基于Fabric的实际应用案例。[https://v.qq.com/x/page/t0937ourp8t.html](https://v.qq.com/x/page/t0937ourp8t.html)去中心化的合约管理Jason Yellick3月19日Fabric 2.0引入了全新的去中心化合约管理系统，相较于1.x中由单一组织定义背书策略和实例化合约，2.0中各个组织需要通过“投票”达成一致，方可启动、升级合约，以及执行相同的策略。本讲将介绍这部分功能的原理和实现，并通过例子讲解如何使用新的合约管理系统。[https://v.qq.com/x/page/s09376uefz5.html](https://v.qq.com/x/page/s09376uefz5.html)更加灵活的隐私数据编程范式乔文剑3月26日Fabric 2.0引入了一套投票系统来支撑去中心化合约管理。这套系统同时也能在用户的应用中使用。同时Fabric 2.0还增强了对隐私数据的支持，简化了隐私数据的使用。本讲将简要回顾Fabric应用开发流程和隐私数据的相关概念，着重介绍新版本功能的原理和实现，并通过实例介绍其应用。[https://v.qq.com/x/page/a09419gwu90.html](https://v.qq.com/x/page/a09419gwu90.html)使用服务的方式启动合约郭剑南4月2日在1.x版本的Fabric中，合约是由Peer以容器的方式进行启动和维护，依赖于Docker。这在一定程度上违反了安全准则，并且在管理运维中带来了麻烦。Fabric 2.0支持用户自行启动合约容器，例如将合约部署在k8s之上。本讲将介绍这部分功能的原理和实现，并且通过实例介绍其使用。[https://v.qq.com/x/page/x0944c3pswy.html](https://v.qq.com/x/page/x0944c3pswy.html)区块链赋能工业互联网安全于洪方4月9日

在工业互联网领域，网络攻击行为已经可以将破坏从虚拟世界转移到现实世界，大量关系到国计民生的关键基础设施以及工业网络面临攻击威胁。因此，增强关键基础设施及工业网络的安全防护能力至关重要。区块链技术的去中心化分布式网络、节点共识、数据防篡改可追溯等特性，可以为工业互联网设备间的通信、协作提供比传统技术更可靠的安全保障，本次分享是关于如何利用区块链技术来增强工业互联网安全方面的一些思考。

[https://v.qq.com/x/page/k0947bzxhnz.html](https://v.qq.com/x/page/k0947bzxhnz.html)Hyperledger Fabric互操作方案及蚂蚁跨链技术

董振华

邱鸿霖

4月16日

Hyperledger Fabric互操作：当前很多区块链服务要求一个联盟内的所有节点都部署在同一个云环境中。为了解决这个问题，Hyperledger Fabric社区提出了互操作方案，其主要目标是用户能够选择适合自己的环境部署Fabric节点，连接成一个业务网络。蚂蚁金服区块链团队作为该方案的主要贡献者之一，在阿里云BaaS上对互操作性做了全面支持。用户可以将阿里云BaaS上的Fabric组织和外部的Fabric组织连接成一个业务通道，共同治理业务网络，完成智能合约的执行和共识。

蚂蚁跨链技术：2019云栖大会上蚂蚁区块链发布了跨链基础产品：通用安全跨链技术产品ODATS（Open Data Access Trusted Service），打通了蚂蚁区块链、Hyperledger异构跨链蚂蚁区块。ODATS从实际业务场景出发打磨的商用跨链平台，从底层协议到高可用组件实现与业务编程界面有着诸多丰富设计。本次分享讲会分享ODATS的重点设计组成以、在标准互操作性上的思考。

[https://v.qq.com/x/page/f0954y571qp.html](https://v.qq.com/x/page/f0954y571qp.html)

Hyperledger Besu-以太坊企业区块链的技术和应用

Edmund To4月23日

Hyperledger Besu 是基于Java的以太坊客户端，是超级账本接收的第一个可以与公有链对接的项目。接受Besu代表的是企业对同时使用公有链和联盟链构造企业应用的兴趣的持续增长。本次演讲，Edmund将介绍Besu的特点如架构、以太坊虚拟机(EVM)、共识算法、存储、网络监控、隐私、批准和部署等，并介绍一些不同行业使用以太坊和Besu的应用。

[https://v.qq.com/x/page/o0957d6iyel.html](https://v.qq.com/x/page/o0957d6iyel.html)BitXHub跨链技术和场景分析

汪小益

徐才巢

4月30日

- 跨链的需求及常见方案分析
- BitXHub的架构设计
- BitXHub的跨链核心流程
- BitXHub的开源现状及未来
- 典型跨链场景分析

[https://v.qq.com/x/page/s0960r09l8v.html](https://v.qq.com/x/page/s0960r09l8v.html)

**主题一：**基于Hyperledger Fabric构建分层与跨链的高可扩展性平台

**主题二：**云链结合，区块链服务BaaS平台的实践与应用

刘长辉

吴楠

5月10日

**演讲主题一：**基于Hyperledger Fabric构建分层与跨链的高可扩展性平台

**内容摘要一：**腾讯在基于区块链支持大规模的企业应用实践中，应对当前区块链面临的扩展性问题，腾讯云区块链提出一个如何解决区块链的分层治理、多链水平扩展、跨链互操作等问题的解决方案，以支持大规模的跨区块链协作，实现统一的区块链多链平台。

**演讲主题二：**云链结合，区块链服务BaaS平台的实践与应用

**内容摘要二：**1、BaaS是区块链行业发展的重要趋势，行业标准正逐步形成；2、腾讯区块链TBaaS服务的最佳应用实践；3、基于腾讯区块链TBaaS服务的行业应用

[https://v.qq.com/x/page/o09647spntp.html](https://v.qq.com/x/page/o09647spntp.html)

**主题一：**基于Hyperledger Fabric的BaaS实现与隐私计算

**主题二：**双链融合：4D实战模型落地区块链

王云浩

郑懿

5月17日

演讲主题一：基于Hyperledger Fabric的BaaS实现与隐私计算

内容摘要一：联想区块链平台B-Connected介绍，以及如何设计和实现BaaS平台，如何在BaaS平台上实现隐私计算confidential computing，包括如何在Hyperledger Fabric上实现的完整国密改造，以及即将在今年分布式计算顶会ICDCS发表的最新论文，关于无证书机制在Hyperledger Fabric的实现。

演讲主题二：双链融合：4D实战模型落地区块链

内容摘要二：1、业务驱动：场景挖掘思维；2、以人为先：场景落地要旨；3、锁定时局：4D实践模型

[https://v.qq.com/x/page/o09680yd4d6.html](https://v.qq.com/x/page/o09680yd4d6.html)

**主题一：**基于BaaS平台的区块链应用案例分享

**主题二：**点融安全多方计算服务

刘辉

史锋锋

5月23日

演讲主题一：基于BaaS平台的区块链应用案例分享

内容摘要一：在区块链业务落地的过程中，将面临异构环境组网、网络弹性扩展、协同联盟治理、数据安全和隐私保护、访问权限控制、国密算法和通信协议的支持等诸多方面的挑战。点融区块链云服务（BaaS）为用户提供企业级的区块链基础设施服务，已帮助多家企业落地区块链业务。这次我们将结合一个案例来说明如何基于点融BaaS来建设区块链业务系统。该案例是一个基于联盟链的产品防伪溯源系统，它是一个结合物联网和区块链技术将产品生命周期的全过程信息统一接入到区块链，实现产品可验真伪、可溯源、可监管的防伪溯源综合应用平台。

演讲主题二：点融安全多方计算服务

内容摘要二：安全多方计算服务基于联盟链、智能合约、秘密共享和同态加密算法等技术，帮助多个企业在确保各自数据隐私安全的前提下，利用各方数据进行加密条件下的安全协同计算，解决企业间既想分享数据又担心数据泄露的矛盾。这次分享将介绍该服务的应用场景、基本原理，并进行现场演示。

[https://v.qq.com/x/page/c0971ch2x7w.html](https://v.qq.com/x/page/c0971ch2x7w.html)BaaS特点和应用

张小军

刘再耀

5月30日BaaS特点和应用[https://v.qq.com/x/page/w0975j5696v.html](https://v.qq.com/x/page/w0975j5696v.html)区块链政务应用蔡茂华6月6日利用区块链技术的特点与“政务共识”业务需求的高度适配性，将区块链技术的“数据可信、可靠，业务规则智能化”的优势，围绕政务数据采集、存储、交换、加工、利用全过程开展链上管理，实现政务数据跨部门、跨区域、跨层级的共同维护和利用，促进业务协同办理，深化“最多跑一次”改革，为人民群众带来更好的政务服务体验。通过区块链的加密传输机制，实现数据“可用不可见”，在确保数据隐私和安全的前提下稳步推进公共数据开放利用。[https://v.qq.com/x/page/m0979lchca5.html](https://v.qq.com/x/page/m0979lchca5.html)少代码快速构造应用印明亮6月13日介绍蚂蚁区块链的云服务集成能力，如何帮助用户省去区块链与其它产品和服务的集成开发成本，通过简单的配置即可快速实现业务数据上链，以及链上链下协同。[https://v.qq.com/x/page/e3079bwi4ar.html](https://v.qq.com/x/page/e3079bwi4ar.html)纸贵区块链产品体系和数据治理方案易晓春6月20日今天给我们带来话题分享的先生，将为我们介绍纸贵科技的产品体系和数据治理解决方案，并结合不同行业，分享区块链数据治理在各类应用场景当中的应用心得和实践案例。纸贵科技是超级账本的认证服务商，在区块链行业资历深厚，拥有强大的解决方案能力，在智慧城市、电子政务、金融、溯源、数据治理等场景有丰富的落地案例。[https://v.qq.com/x/page/k3102uh9xui.html](https://v.qq.com/x/page/k3102uh9xui.html)链上金融的探索与实践

吴桐

陈浩栋

6月27日数字经济领域知名学者吴桐先生以及百度资深研发工程师陈浩栋先生，为大家准备了一个主题为“”的主题演讲。[https://v.qq.com/x/page/b310675by0f.html](https://v.qq.com/x/page/b310675by0f.html)Hyperledger  Fabric数据安全和隐私探索和实践冯翔7月4日

主要包含四个方面：

1\. 数据安全和隐私在Hyperledger Fabric里面中的重要作用

2\. Hyperledger Fabric数据安全和隐私架构体系

3\. Hyperledger Fabric数据安全和隐私的最佳实践

4\. Hyperledger Fabric数据数据隐私隐私保护的案例

[https://v.qq.com/x/page/b31105a0704.html](https://v.qq.com/x/page/b31105a0704.html)区块链技术在产业链中的应用姜永强7月11日供应链是区块链在金融领域最适合的应用场景，智能合约、分布式账本、线上存证取证都能大大提高供应链金融的应用效率，解决其之前难以解决的痛点。在场景更加丰富的产业金融中，区块链会有更加丰富的应用模式。[https://v.qq.com/x/page/q3114e1wrtu.html](https://v.qq.com/x/page/q3114e1wrtu.html)Fabric中实现的数据防膨胀姜明润7月18日介绍了一种在Fabric中实现的数据防膨胀的方法。[https://v.qq.com/x/page/r31170h3686.html](https://v.qq.com/x/page/r31170h3686.html)区块链+安全计算解锁数据生产要素创新张佳辰7月25日

区块链作为可信数据库，保存了大量珍贵的真实数据，对机器学习非常有帮助，很多数据模型需要这样的真实数据来做训练。

区块链泛存证用例和隐私计算让数据“可用不可见”让数据真正成为生产要素，并改造金融、运营商、政务等多个产业领域。

[https://v.qq.com/x/page/b3125gbf0fc.html](https://v.qq.com/x/page/b3125gbf0fc.html)开放许可链的治理模式探讨蔡伟鑫8月8日

许可链是区块链的一个重要分类。当前许可链主要应用在一些特定的行业，而开放许可链的理念则是不限制在某一行业或者领域，而是在授权许可的前提下尽可能的为各行业、众多的企业甚至个人提供区块链的服务，因此需要探索一个合理的治理模式，明确在开放许可链的生态里各个角色具体的职责，使得开放许可链可以尽量满足各个角色的需求。

[https://v.qq.com/x/page/u31326egw3t.html](https://v.qq.com/x/page/u31326egw3t.html)Hyperledger Fabric国密化改造圆桌沙龙

刘宇翔

陈桂军

陈序

关志

马逸龙

苏云龙

8月15日

6月17日，超级账本中国技术工作组正式向社会发出倡议，邀请大家共同为最新Hyperledger Fabric版本打造一个可以共同使用的国密化版本，得到了广大Hyperledger Fabric爱好者和使用者的热烈响应。到目前为止，广大志愿者们经过了8次会议的热烈讨论，为新的国密化版本基本确定了路线图，已经进入开发阶段。

为了让更多的人了解该项目的情况，为关心国密化改造的所有朋友们答疑解惑，帮助更多的朋友参与到这个项目中来，我们特别推出这一期的节目，邀请目前部分主要的贡献者们将研发思路、开发路线、任务分配、特点难点等众多大家关心的问题，一一与大家交流。

[https://v.qq.com/x/page/e3136fovmv3.html](https://v.qq.com/x/page/e3136fovmv3.html)区块链互操作的现状与挑战魏凯8月22日

区块链经过十余年的发展，以其多方共识、分布式存储、难以篡改的特性，在缺乏信任基础的多方协作场景中得到了广泛应用。随着区块链在各行各业应用深度和广度的不断拓展，行业出现了上层应用与底层链对接切换难、不同区块链系统间互操作难、链上链下可信交互难等问题。为解决以上问题，以跨链为代表的区块链互操作技术逐渐成为行业焦点。本次分享将对区块链互操作概念进行解读，给出互操作的参考框架，分析互操作中的关键问题，并对当前互操作技术现状进行分析，探索区块链互操作演进方向。

Wish List 期待的题目

TopicDescription  
希望听到的演讲演讲内容回看链接数据分享过程中的隐私保护数据分享过程中的隐私保护

[https://v.qq.com/x/page/b31105a0704.html](https://v.qq.com/x/page/b31105a0704.html)

[https://v.qq.com/x/page/k0947bzxhnz.html](https://v.qq.com/x/page/k0947bzxhnz.html)

[https://v.qq.com/x/page/a09419gwu90.html](https://v.qq.com/x/page/a09419gwu90.html)

供应链金融场景分析供应链金融场景分析[https://v.qq.com/x/page/q3114e1wrtu.html](https://v.qq.com/x/page/q3114e1wrtu.html)Fabric国密改造Fabric国密改造[https://v.qq.com/x/page/e3136fovmv3.html](https://v.qq.com/x/page/e3136fovmv3.html)银行业应用银行业应用  
技术生态治理

技术生态治理，整个社区沟通的方式，以及技术开发的上下游，

包括Token、工具、Sample、应用等

[https://v.qq.com/x/page/k3102uh9xui.html](https://v.qq.com/x/page/k3102uh9xui.html)

[https://v.qq.com/x/page/u31326egw3t.html](https://v.qq.com/x/page/u31326egw3t.html)

[https://v.qq.com/x/page/e3136fovmv3.html](https://v.qq.com/x/page/e3136fovmv3.html)

可实践性操作解析可实践性操作解析各期都有TEE和区块链TEE和区块链，找Avalon的开发者

Document generated by Confluence on Nov 26, 2024 15:09

[Atlassian](http://www.atlassian.com/)
