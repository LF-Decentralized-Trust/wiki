1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)
5. [Upgrade Fabric network from 1.4.x to 2.2.x using Hyperledger Bevel](Upgrade-Fabric-network-from-1.4.x-to-2.2.x-using-Hyperledger-Bevel_21954787.html)

# Hyperledger Mentorship Program : Project Plan - Upgrade Fabric network from 1.4.x to 2.2.x using Hyperledger Bevel

Created by Jagpreet Singh Sasan, last modified by Mohit Vaish on Nov 22, 2022

## **Abstract**

[Hyperledger Bevel](https://github.com/hyperledger/bevel) is an automation framework for rapidly and consistently deploying production-ready DLT platforms.  This task aims to complete a live upgrade of a Hyperledger Fabric network from version 1.4.x to 2.2.x using Hyperledger bevel and document the steps as well as make any changes needed to automate any steps possible.

## **Mentors**

NameTime zoneDiscord IDEmail IDSownak RoyUK/BSTSownak#7728[sownak.roy@accenture.com](mailto:sownak.roy@accenture.com)Jagpreet Singh SasanISTJag#2402[jagpreet.singh.sasan@accenture.com](mailto:jagpreet.singh.sasan@accenture.com)

## **Mentee**

NameTime zoneDiscord IDEmail IDMohit VaishISTMohitv#9920[mohit\_vaish@hotmail.com](mailto:mohit_vaish@hotmail.com)

**Communication channel**:  Discord+ Github

**Project repo:** [https://github.com/hyperledger/bevel](https://github.com/hyperledger/bevel)

## **Deliverables**

- Automation of the live upgrade from version 1.4.x to 2.2.x of Hyperledger Fabric network deployed using Hyperledger Bevel
- Relevant operational guide on the live upgrade from version 1.4.x to 2.2.x of Hyperledger Fabric network deployed using Hyperledger Bevel
- Completion of relevant issues about the same on Github

## **Merged PR's**

- [**PR**](https://github.com/hyperledger/bevel/pull/2069)

## **Final Project Presentation:**

- [**Link**](https://docs.google.com/presentation/d/1f06sP8-5X2vnLp9M6anlfORMHP9FO1Fq/edit?usp=sharing&ouid=115206433217005254878&rtpof=true&sd=true)

## **Milestones**

**Eval 1:**

- Manual upgrade of the platform components (orderer, peer) of the network
- Manual upgrade of the application components (channel, chaincode) parts of the network

**Eval 2:**

- Operation Guide on how to upgrade manually

**Eval 3:**

- Helm and Ansible automation for upgrade of the components

**Eval 4:**

- Final Operation Guide and Blog on how to upgrade using Hyperledger Bevel

## **Timeline**

DatesTasks/Plan

Status

**June 1 - June 14**Mentee intro with the mentor. Introduction to the concepts of BevelDone**June 15 - June 28**Manual upgrade of non-chaincode parts of the networkDone

**June 29 - July 12**

Manual upgrade of chaincode parts of the networkDone**July 13 - July 26**Document the approach &amp; manual upgrade tasks performedDone**July 27 - Aug 9**Automate the binary upgrade process for Orderer Done**Aug 10 - Aug 23**Automate the binary upgrade process for Peers and upgrade DBDone**Aug 24 - Sept 6**Automate tasks for upgrade capabilitiesDone**Sept 7 - Sept 20**Automate tasks to update EndPoints and Endorsement PoliciesDone**Sept 21 - Oct 4**Automate tasks to update Lifecycle and ACLsDone**Oct 5 - Oct 18**Test final automationDone**Oct 19 - Nov 1**Update documentDone**Nov 2 - Nov 12**Prepare final presentation and demoDone

## **Methodology**

The planned approach can be broken into following steps:

1. Perform a manual upgrade for all required steps and verify the results. Steps performed can be found [here](https://hyperledger-fabric.readthedocs.io/en/release-2.2/upgrade.html)
2. The operator updates the JSON file 'network.yaml' for upgrade flag and upgrade version. The operator also ensures the configuration in this file reflects the current state of Hyperledger fabric deployment. Operator should also takes backup of core.yaml and orderer.yaml files, if any changes are done for existing deployment
3. Once the manual upgrade is tested. The approach is to automate the same manual steps which can be broadly divided into following:
   
   1. First upgrade orderer nodes to the upgrade version. When upgrade is finished, the script waits for operator confirmation to move to next step
   2. This step upgrade peer nodes one by one and as earlier waits for operator confirmation
   3. This step upgrade ca nodes and peer cli nodes(where available) to the upgrade version
   4. Now script will upgrade the capabilities for orderer, channel and application group for system channel and all application channels mentioned in network.yaml file
   5. Next step will update the system channel consortium and all application channel orgs for endorsement policies
   6. This step will update all the application channels 'application group' for endorsement and lifecycle policies
   7. This step will ensure that OrdererEndpoints are used in system channel and all application channels
   8. Where ACL needs to be updated, we update it in this final automated step
4. Operator should compare the new core.yaml with backup file as per step 2 and manually make the required changes
5. Operator can also deploy existing chaincode using new lifecycle of 2.2.x version.

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
