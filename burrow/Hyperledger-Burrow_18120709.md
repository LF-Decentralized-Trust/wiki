1. [Hyperledger Burrow (EOL)](index.html)

# ![Home Page](images/icons/contenttypes/home_page_16.png) Hyperledger Burrow (EOL) : Hyperledger Burrow

Created by Tracy Kuhrt, last modified by Ry Jones on May 12, 2022

Hyperledger Burrow was moved to [EOL status](https://github.com/hyperledger/tsc/issues/34) by the TSC on 12 May 2022.  You are welcome to use and contribute to this code, although the maintainers may or may not be responsive to any questions you have.  You would also be welcome to help reactivate this project if you are interested in continuing development of this code.

[Hyperledger Burrow Documentation](https://hyperledger.github.io/burrow)

**Project**

[![](attachments/18120709/18120780.svg?width=192)](https://lf-hyperledger.atlassian.net/wiki/display/burrow/)

**Status**

[END OF LIFE](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-incubation)

**CII Badge**

[![](https://bestpractices.coreinfrastructure.org/projects/1000/badge)](https://bestpractices.coreinfrastructure.org/projects/1000)

**Description**Permissioned Ethereum smart-contract blockchain

Burrow is a permissively licensed (Apache 2.0) EVM smart contract machine and Byzantine Fault Tolerant permissioned ledger that uses Tendermint consensus and implements some novel extensions to the EVM whilst remaining EVM-compliant. It provides EVM execution within the Ethereum account model and an internal token to meter computation in the permissioned setting with transactions finality.  Burrow is named after the trans-dimensional intergalactic tubules used by [marmots](https://www.youtube.com/watch?v=BXo1vCKTEQg) to communicate.

# Key Characteristics

Burrow has three primary aims:

- To be a good compliant and simple EVM library friendly towards integrators (see for example [https://github.com/hyperledger/sawtooth-seth](https://github.com/hyperledger/sawtooth-seth "https://github.com/hyperledger/sawtooth-seth") and [https://github.com/hyperledger/fabric-chaincode-evm](https://github.com/hyperledger/fabric-chaincode-evm))

<!--THE END-->

- To be a fast, light, lean single-process full [Tendermint](https://tendermint.com/ "https://tendermint.com/")/EVM permissioned ledger with transaction finality

<!--THE END-->

- To provide a practical base for EVM extensions in a many-chain world

Burrow is not trying to be:

- Highly pluggable (see Sawtooth or Fabric)

<!--THE END-->

- Hard to deploy

# Notable features:

- Single pure go binary including all tooling
- GRPC API interfaces (see: [https://github.com/hyperledger/burrow/tree/develop/protobuf](https://github.com/hyperledger/burrow/tree/develop/protobuf)) - use from any supported GRPC [https://grpc.io/docs/quickstart/](https://grpc.io/docs/quickstart/))
- Javascript client library: [https://github.com/hyperledger/burrow/tree/develop/js](https://github.com/hyperledger/burrow/tree/develop/js) with smart contract function mapping layer
- Go client library (via GRPC codegen): [https://github.com/hyperledger/burrow/blob/develop/rpc/rpctransact/rpctransact.pb.go](https://github.com/hyperledger/burrow/blob/develop/rpc/rpctransact/rpctransact.pb.go)
- Vent SQL mapping and projections layer ([https://github.com/hyperledger/burrow/blob/develop/vent/README.md](https://github.com/hyperledger/burrow/blob/develop/vent/README.md))
- Permissioned EVM (see: [https://github.com/hyperledger/burrow/blob/develop/permission/perm\_flag.go](https://github.com/hyperledger/burrow/blob/develop/permission/perm_flag.go))
- On-chain EVM ABIs (function and contract definitions) and contract metadata)
- Streaming execution events service ([https://github.com/hyperledger/burrow/blob/develop/protobuf/rpcevents.proto](https://github.com/hyperledger/burrow/blob/develop/protobuf/rpcevents.proto))
- Experimental WASM contract support
- Governance mechanism capable of atomically upgrading systems of contracts based on quorum voting
- Chain-global DNS-like name registry ([https://github.com/hyperledger/burrow/blob/develop/protobuf/names.proto](https://github.com/hyperledger/burrow/blob/develop/protobuf/names.proto))
- Validator bonding for proof-of-stake networks ([https://hyperledger.github.io/burrow/#/tutorials/5-bonding-validators](https://hyperledger.github.io/burrow/#/tutorials/5-bonding-validators))
- Solidity compilation, contract deployment, and testing tool \`burrow deploy\`
- Scriptable transaction tool \`burrow tx\`
- Forensics tool \`burrow examine\`
- Chain generation and genesis tool \`burrow spec\` and \`burrow configure\`
- Dump/restore functionality \`burrow dump\` and \`burrow restore\` (ship state between versions or chains) - also allows state serialisation
- Keys signing service command-line wallet and server \`burrow keys\`
- Kubernetes Helm charts: [https://hyperledger.github.io/burrow/#/tutorials/5-bonding-validators](https://hyperledger.github.io/burrow/#/tutorials/5-bonding-validators)

# [Hyperledger Burrow Documentation](https://hyperledger.github.io/burrow/)

- Godoc: [https://godoc.org/github.com/hyperledger/burrow](https://godoc.org/github.com/hyperledger/burrow)
- See also: [https://github.com/hyperledger/burrow/tree/develop/docs](https://github.com/hyperledger/burrow/tree/develop/docs) for documentation source, architecture decision records, and further historical and design documentation

# Companies building on Burrow

Please add

CompanyProjectDescription

# Project Management

Burrow is being heavily tested as the core of the [Agreements Network](https://agreements.network/ "https://agreements.network/"). It sits at the intersections of a number of emerging technologies:

\- EVM contracts and host-native code contracts - Public permissioned networks - permissioned Ethereum and public Tendermint/Cosmos - Layer 2 scaling - acting as a side-chain or state channel

We aim to provide a robust blockchain node for running multiple interconnected chains in a many-chain world. As well as blurring the public/private chain divide.

### Roadmaps

- [**Q1 2019**](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2019_q1 "projects:burrow:roadmap_2019_q1")
- [**Q4 2018**](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q4 "projects:burrow:roadmap_2018_q4") - [*post-mortem*](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q4_postmortem "projects:burrow:roadmap_2018_q4_postmortem")
- [**Q3 2018**](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q3 "projects:burrow:roadmap_2018_q3") - [*post-mortem*](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q3_postmortem "projects:burrow:roadmap_2018_q3_postmortem")
- [**Q2 2018**](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q2 "projects:burrow:roadmap_2018_q2")
- [**Q1 2018**](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q1 "projects:burrow:roadmap_2018_q1") - [*post-mortem*](https://wiki-archive.hyperledger.org/projects/burrow/roadmap_2018_q1_postmortem "projects:burrow:roadmap_2018_q1_postmortem")

# Repositories

Burrow's repository is on github here: [https://github.com/hyperledger/burrow](https://github.com/hyperledger/burrow "https://github.com/hyperledger/burrow")

The Burrow binary contains everything you need to specify, configure, run, and deploy smart contracts to a chain.

- `burrow spec` - for describing template genesis state
- `burrow configure` - for realising a specific configuration (including key generation)
- `burrow keys` - both a standalone key signing daemon and key generation tool
- `burrow deploy` - a declarative Solidity compilation, chain management, testing, and smart contract deployment tool
- `burrow dump` - a forensics, auditing, and data extraction tool
- `burrow snatives` - a tool for interacting with Burrow's 'secure natives' - host code that is callable as if it were an EVM contract
- `burrow start` - for starting a blockchain node

For deploying contracts you will need a local installation of [Solidity](https://github.com/ethereum/solidity/releases "https://github.com/ethereum/solidity/releases").

For previous versions of standalone Burrow you can find:

- **binaries**: [https://github.com/hyperledger/burrow/releases](https://github.com/hyperledger/burrow/releases "https://github.com/hyperledger/burrow/releases")
- **docker images**: [https://hub.docker.com/r/hyperledger/burrow](https://hub.docker.com/r/hyperledger/burrow "https://hub.docker.com/r/hyperledger/burrow")

### Deployment

Burrow can be deployed in any environment but we have focussed on deploying related sets of validators (or validator pools) using Kubernetes/Helm and you can find helm charts here: [https://github.com/helm/charts/tree/master/incubator/burrow](https://github.com/helm/charts/tree/master/incubator/burrow "https://github.com/helm/charts/tree/master/incubator/burrow").

### Contributing

Please fork, branch, and make pull requests to the [develop](https://github.com/hyperledger/burrow/tree/develop "https://github.com/hyperledger/burrow/tree/develop") branch.

Our build, CI, and testing process is executed via our [Makefile](https://github.com/hyperledger/burrow/blob/develop/Makefile "https://github.com/hyperledger/burrow/blob/develop/Makefile"), see the comments there for details.

# Communication

## Mailing List

- [burrow](https://lists.hyperledger.org/g/burrow)

## Chat (for questions and ephemeral discussions)

- [#burrow](https://chat.hyperledger.org/channel/burrow) - General usage questions
- [#burrow-contributors](https://chat.hyperledger.org/channel/burrow-contributors) - Contributor discussions

# Meeting

### Quarterly updates

**2019**

- [Q3 2019 Update](https://lf-hyperledger.atlassian.net/wiki/display/HYP/2019+Q3+Hyperledger+Burrow)
- [Q2 2019 Update](https://lf-hyperledger.atlassian.net/wiki/display/HYP/2019+Q2+Hyperledger+Burrow)
- [Q1 2019 Update](https://lf-hyperledger.atlassian.net/wiki/display/HYP/2019+Q1+Hyperledger+Burrow)

#### 2018

- [Q4 2018 Update](https://wiki-archive.hyperledger.org/groups/tsc/project-updates/burrow-2018-nov "groups:tsc:project-updates:burrow-2018-nov")
- [Q3 2018 Update](https://wiki-archive.hyperledger.org/groups/tsc/project-updates/burrow-2018-aug "groups:tsc:project-updates:burrow-2018-aug")
- [Q2 2018 Update](https://wiki-archive.hyperledger.org/groups/tsc/project-updates/burrow-2018-may "groups:tsc:project-updates:burrow-2018-may")
- [Q1 2018 Update](https://wiki-archive.hyperledger.org/groups/tsc/project-updates/burrow-2018-mar "groups:tsc:project-updates:burrow-2018-mar")

#### 2017

- [Q4 2017 Update](https://wiki-archive.hyperledger.org/groups/tsc/project-updates/burrow-2017-dec "groups:tsc:project-updates:burrow-2017-dec")

# History

Burrow was [approved](https://lists.hyperledger.org/g/tsc/message/737 "https://lists.hyperledger.org/g/tsc/message/737") for incubation on the 6th of April 2017 by the Hyperledger TSC.

## Recent space activity

##### Recent updates

There are no recent updates at this time.

## Space contributors

No contributors found for: authors on selected page(s)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger\_Burrow\_Logo\_Color.png](attachments/18120709/18120762.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Burrow\_Logo\_Color.svg](attachments/18120709/18120780.svg) (image/svg+xml)

Document generated by Confluence on Nov 26, 2024 12:36

[Atlassian](http://www.atlassian.com/)
