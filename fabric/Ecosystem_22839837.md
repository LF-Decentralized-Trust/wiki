1. [Hyperledger Fabric](index.html)
2. [Hyperledger Fabric](Hyperledger-Fabric_22839309.html)

# Hyperledger Fabric : Ecosystem

Created by Matthew White, last modified by David Enyeart on Dec 07, 2023

A curated list of active Hyperledger Fabric ecosystem projects.

## Getting Started

- [Fabric documentation](https://hyperledger-fabric.readthedocs.io/en/latest/index.html)
  
  - Official documentation including [Getting Started](https://hyperledger-fabric.readthedocs.io/en/latest/getting_started.html), [Key Concepts](https://hyperledger-fabric.readthedocs.io/en/latest/key_concepts.html), and [Tutorials](https://hyperledger-fabric.readthedocs.io/en/latest/tutorials.html)
- [fabric-samples](https://github.com/hyperledger/fabric-samples)
  
  - Official Fabric samples repository that supports the [Fabric documentation tutorials](https://hyperledger-fabric.readthedocs.io/en/latest/tutorials.html)
- [Full Stack Asset Transfer](https://github.com/hyperledger/fabric-samples/tree/main/full-stack-asset-transfer-guide)
  
  - Workshop-style exercises to take you from building a smart contract and client application in development through to a full K8s deployed solution

## Application projects (chaincode, client applications, application frameworks, interop)

![](attachments/22839837/22842994.png?height=250)

- [Application SDKs](https://hyperledger-fabric.readthedocs.io/en/latest/sdk_chaincode.html)
  
  - Build client applications written in Node, Java, or Go
- [Chaincode libraries](https://hyperledger-fabric.readthedocs.io/en/latest/sdk_chaincode.html)
  
  - Build chaincode applications written in Node, Java, or Go
- [hlf-connector](https://github.com/hyperledger-labs/hlf-connector)
  
  - Expose chaincode via REST service or Kafka messaging
- [Fabric Smart Client](https://github.com/hyperledger-labs/fabric-smart-client)
  
  - A flow-based framework for writing blockchain applications that preserves privacy between transactors
- [Fabric Token SDK](https://github.com/hyperledger-labs/fabric-token-sdk)
  
  - SDK to assist in building Token based solutions on Hyperledger Fabric (uses Fabric Smart Client)
- [Firefly](https://github.com/hyperledger/firefly)
  
  - A complete stack for enterprises to build and scale secure Web3 applications.
- [Cacti](https://github.com/hyperledger/cacti)
  
  - A multi-faceted pluggable interoperability framework to link networks built on heterogeneous distributed ledger and blockchain technologies and to run transactions spanning multiple networks.

## Docker-based deployment environments (often used for development and testing)

![](attachments/22839837/22842995.png?height=250)

- [Microfab](https://github.com/ibm-blockchain/microfab)
  
  - Single docker container with configurable organizations/peers/channels. A full fabric network startable in seconds, perfect for development
- [fabric-samples test-network](https://github.com/hyperledger/fabric-samples/tree/main/test-network)
  
  - Docker-compose network used for Fabric official [tutorials](https://hyperledger-fabric.readthedocs.io/en/latest/tutorials.html) and [samples](https://github.com/hyperledger/fabric-samples/tree/main)
- [fablo](https://github.com/hyperledger-labs/fablo)
  
  - Specify a network to spin up a docker-compose network
- [cello](https://github.com/hyperledger/cello)
  
  - Deploy to Docker including Docker Swarm support

## Kubernetes-based deployment environments (often used for production deployment)

![](attachments/22839837/22842996.png?height=250)

- [Bevel operator for Fabric](https://github.com/hyperledger/bevel-operator-fabric)
  
  - Kubernetes operator that works with Bevel deployment framework
- [Fabric Operator](https://github.com/hyperledger-labs/fabric-operator)
  
  - Kubernetes Fabric operator that powers IBM Blockchain Platform
- [Fabric Ansible Collection](https://github.com/ibm-blockchain/ansible-collection/)
  
  - Ansible roles to deploy the Fabric Operator and Operations Console (open source and the IBM support offering images)
  - Collection of Ansible modules for creation and management of Fabric Networks
- [Fabric K8s Chaincode Builder](https://github.com/hyperledger-labs/fabric-builder-k8s)
  
  - Chaincode Builder specifically targeting K8s deployments of docker based chaincode
  - [Github Action for building a K8s chaincode package](https://github.com/hyperledgendary/package-k8s-chaincode-action)

## Management and operations (agnostic to deployment environments)

- [Fabric operations console](https://github.com/hyperledger-labs/fabric-operator)
  
  - Web UI for management of Fabric Network, often used with Fabric Operator
- [Fabric Admin SDK](https://github.com/hyperledger/fabric-admin-sdk)
  
  - Build client applications to manage Fabric channels and chaincodes
- [fabric-opssc](https://github.com/hyperledger-labs/fabric-opssc)
  
  - *Operations Smart Contract (OpsSC)* is smart contract-based system operations for blockchain-based systems.
  - Enables decentralized system operations over multiple organizations.
- [Blockchain explorer](https://github.com/hyperledger-labs/blockchain-explorer)
  
  - Browse activity on the underlying blockchain network.

## Attachments:

![](images/icons/bullet_blue.gif) [image-2023-11-8\_10-51-17.png](attachments/22839837/22842992.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-11-8\_10-53-19.png](attachments/22839837/22842994.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-11-8\_10-54-24.png](attachments/22839837/22842995.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-11-8\_10-54-44.png](attachments/22839837/22842996.png) (image/png)

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
