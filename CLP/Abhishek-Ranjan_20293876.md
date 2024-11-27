1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 1](Evaluation-1_20293737.html)

# Collaborative Learning Program : Abhishek Ranjan

Created by Abhishek Ranjan on Oct 31, 2023

   

                                       

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 1 - Report**

## Submitted By: Abhishek Ranjan

## Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Abhishek Ranjan**

**Evaluation Period**

**06-07-2023 to 11-08-2023**

**Task**

**RAFT familiarization &amp; an application implementation using it**

**Date Submitted**

**12-10-23**

**Mentor**

**Dr. Anasuya Threse Innocent**

                                   

# Tasks, Objectives, and Results

This Evaluation report consolidates the candidate’s work for Hyperledger CLP - BiniBFT project by BiniWorld Innovations Pvt Ltd during the internship (Weeks 1-6). The report has been categorized into two sections: outline the key task assigned to the candidate and day-to-day activities undertaken by the candidate.

### **Key Outline of the Task assigned to the candidate (This includes Project name, Problem statement, expected Output and other relevant details)**

# **RAFT Implementation**

It is the Raft Consensus algorithm Raft implemented in Go.

## **about Raft Protocol Description**

The Raft consensus algorithm is a distributed system protocol designed to achieve consensus among a cluster of nodes in a network. It was introduced as an alternative to the more complex Paxos algorithm, aiming to provide a clearer and more understandable approach to distributed consensus. Raft has gained popularity in the field of distributed systems due to its simplicity and reliability.

**Limitations of the Raft Consensus Algorithm:**

- Lack of Byzantine Fault Tolerance: Raft is primarily designed to handle benign failures, where nodes fail or behave unpredictably but do not actively maliciously disrupt the network. It does not provide Byzantine Fault Tolerance, making it less suitable for scenarios with potentially malicious nodes.
- Limited Use Cases: While Raft is a reliable choice for many distributed systems, it may not be the best fit for all scenarios. Complex, large-scale, and high-performance distributed systems may require more specialized consensus algorithms.
- Unavoidable Leader Election Delays: Raft relies on leader elections to ensure that the system operates correctly. During leader elections, there can be a delay in processing client requests, which may affect real-time applications that require low-latency responses.

In conclusion, the Raft consensus algorithm offers several advantages, including simplicity, clear leader election, and safety, making it an attractive choice for a wide range of distributed systems. However, it also has its disadvantages and limitations, particularly in terms of performance overhead, flexibility, and scalability. It's important to carefully consider the specific requirements of your distributed system when choosing a consensus algorithm, as no single algorithm is suitable for all use cases.

# **Implementation**

The sample uses a Go module to install the chaincode dependencies. The dependencies are listed in a go.mod file in the asset-transfer-basic/chaincode-go directory. You should take a moment to examine this file.

$ cat go.mod

module [github.com/hyperledger/fabric-samples/asset-transfer-basic/chaincode-go](http://github.com/hyperledger/fabric-samples/asset-transfer-basic/chaincode-go)

**The SmartContract type is then used to create the transaction context for the functions defined within the smart contract that read and write data to the blockchain ledger.**

func (s **\***SmartContract) CreateAsset(ctx contractapi**.**TransactionContextInterface, id string, color string, size int, owner string, appraisedValue int) error {

    exists, err :**=** s**.**AssetExists(ctx, id)

    **if** err **!=** nil {

        **return** err

    }

    **if** exists {

        **return** fmt**.**Errorf("the asset %s already exists", id)

    }

    asset :**=** Asset{

        ID:             id,

        Color:          color,

        Size:           size,

        Owner:          owner,

        AppraisedValue: appraisedValue,

    }

    assetJSON, err :**=** json**.**Marshal(asset)

    **if** err **!=** nil {

        **return** err

    }

    **return** ctx**.**GetStub()**.**PutState(id, assetJSON)

}

**The AssetTransfer class provides the transaction context for the functions defined within the smart contract that read and write data to the blockchain ledger.**

**async** CreateAsset(ctx, id, color, size, owner, appraisedValue) {

        const asset **=** {

            ID: id,

            Color: color,

            Size: size,

            Owner: owner,

            AppraisedValue: appraisedValue,

        };

        **await** ctx**.**stub**.**putState(id, Buffer**.**from(JSON**.**stringify(asset)));

    }

### The command will produce a JSON map that displays if a channel member has approved the parameters that were specified in the checkcommitreadiness command:

         {

            "Approvals": {

                    "Org1MSP": **true**,

                    "Org2MSP": **true**

            }

        }

    

## **Output:**

                                                                                            

                                                                ![](attachments/20293876/20295507.png?height=250)

                  

## Attachments:

![](images/icons/bullet_blue.gif) [Screenshot (232).png](attachments/20293876/20295506.png) (image/png)  
![](images/icons/bullet_blue.gif) [Blockchain.png](attachments/20293876/20295507.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
