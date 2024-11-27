1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [Support Clique for Besu on HL Labs BAF](Support-Clique-for-Besu-on-HL-Labs-BAF_21954777.html)

# Hyperledger Mentorship Program : Project Plan - Support Clique Consensus for Besu on HL Labs Blockchain Automation Framework

Created by Roshan Raut, last modified on Nov 15, 2021

## **Abstract**

Hyperledger Labs [Blockchain Automation Framework](https://github.com/hyperledger-labs/blockchain-automation-framework)(BAF) is a tool to deploy different DLT platforms automatically on a given Kubernetes cluster. BAF supports multi-cloud and multi-DLT deployments, and already supports HL Fabric, HL Besu, Quorum, R3 Corda. For HL Besu, currently only IBFT2 Consensus is supported by BAF. The task is to support the Clique consensus for Hyperledger Besu, so that BAF can be used to deploy and operate a HL Besu network with Clique consensus. This will also include upgrading BAF to support the latest stable Besu version.

## **Mentor and Mentee**

Mentor: Sownak Roy 

Timezone: UK/BST

Rocketchat(Hyperledger): sownak

Mentee: Roshan Raut

Timezone: IST

Rocketchat(Hyperledger): roshan13046

Mail: [roshanpk.raut@gmail.com](mailto:roshanpk.raut@gmail.com)

Communication channel:  Rocketchat + Github

**Project repo:** [https://github.com/hyperledger-labs/blockchain-automation-framework](https://github.com/hyperledger-labs/blockchain-automation-framework)

## **Deliverables**

- Helm charts required to set-up Clique consensus with Besu
- Ansible scripts to automate the generation of Helm value files.
- Documentation on how to use BAF for deploying HL Besu with Clique consensus.
- Documented, upgrade of Besu to latest stable on BAF.

## **Merged PR's:**

[**Issue 510: \[besu\] added clique consensus**](https://github.com/hyperledger-labs/blockchain-automation-framework/pull/1695)

[**Issue 1295: \[besu\] Added GCP-storageclass**](https://github.com/hyperledger-labs/blockchain-automation-framework/pull/1643)

[**Issue 510: \[besu\] Updated the documents and added doc changes for besu clique consensus**](https://github.com/hyperledger-labs/blockchain-automation-framework/pull/1704)

## **Final Project Presentation:**

[**BAF\_Besu\_Clique\_Consensus\_Project\_Presentation\_Nov\_2021**](https://docs.google.com/presentation/d/1fBORaPEFyKgJK8EpcSBOPQRBeWxa5wcB/edit#slide=id.p1)

## **Milestones**

**Eval 1:**

- Local setup of all tools, Docker, Git, Minikube, Ansible.
- Use existing BAF code to deploy Besu with IBFT consensus on local network.

**Eval 2:**

- Deploy Besu with Clique consensus on local network manually.
- Manual steps for Besu with Clique documented.

**Eval 3:**

- Helmcharts created for Besu with Clique deployment.
- Tests and Documentation created for the Helmcharts.

**Eval 4:**

- Ansible scripts to automate the deployment of Besu with Clique.
- Updated documentation.

## **Timeline**

DatesTask/PlanStatus**June 1 - June 14**Mentee intro with the mentor. Introduction to the concepts of BAF.Done**June 15 - June 28**

Setup local environment for Development

Done**June 29 - July 12**

Setup a Besu network with clique consensus manually/locally using Besu documentation.

Done

Eval Completed

**July 13 - July 26**

Setup GKE environment for Development (added because local minikube was not feasible due to memory issues)

Done**July 27 - Aug 9**

Complete local Besu network with clique consensus.

Done

**August 10 - August 23**

Set-up a small Besu network using local/GKE Kubernetes network using BAF.

Done 

Eval Completed

**August 24 - Sept 6**Document changes needed to implement Clique consensus.Done**Sept 7 - Sept 20**Make the changes in Ansible and Helm charts.Done**Sept 21 - Oct 4**

Test the scripts and make additional changes in Ansible and Helm charts.

Done

Eval Completed

**Oct 5 - Oct 18**

Buffer to complete the Besu network deployment using Clique.

Done**Oct 19 - Nov 1**

Update the documentation.

Done**Nov 2 - Nov 12**

Prepare final presentation.

Done

Eval Completed

Row 3: Eval on July 10: Provide reports for first quarter to the program organisers.

Row 6: Eval on August 20: Provide reports for first quarter to the program organisers.

Row 9: Eval on October 1: Provide reports for second quarter to the program organisers.

Row last: Final Eval on November 12: Provide reports for completion.

## **Methodology**

I am following the **“Code-Test-Document​”** methodology.

My first step while developing any software is to **design** the **process** **flow** by **understanding** the inner **Architecture of Besu and BAF**. During the initial mentorship, I along with my mentor will be doing some planning of the implementation and set important milestones for the same as represented in the **schedule** for the work(given above) for the **respective** **feature**. Once I develop each feature, I will be **Testing** the implementation code to make sure whatever I wrote is working **correctly**. At the end of the **tests**, I will be **documenting** their implementation. I am using​ **GIT​** for **version** **control** with **reviews** taking place on Github(Repo:[https://github.com/hyperledger-labs/blockchain-automation-framework](https://github.com/hyperledger-labs/blockchain-automation-framework)).

I am constantly **sharing** my progress with the **mentor** and the **community**, a **​weekly​** **update** regarding my work is shared with the mentor as a weekly meet.

## Attachments:

![](images/icons/bullet_blue.gif) [sls\_conf.png](attachments/21954772/21964839.png) (image/png)  
![](images/icons/bullet_blue.gif) [Project Plan - Support Clique Consensus for Besu on HL Labs Blockchain Automation Framework.url](attachments/21954772/21966075.url) (application/octet-stream)

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
