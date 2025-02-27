1. [Hyperledger Cello](index.html)
2. [Hyperledger Cello](Hyperledger-Cello_21659650.html)
3. [Documentation](Documentation_21660730.html)

# Hyperledger Cello : Chaincode Frontend Design

Created by Xichen Pan, last modified by feng yang on May 24, 2023

# [https://hlf.readthedocs.io/en/latest/commands/peerlifecycle.html](https://hlf.readthedocs.io/en/latest/commands/peerlifecycle.html)

# Chaincode Management Page

### Workflow

    upload chaincode→install chaincode→ approve→ commit

    1. Upload chaincode: Each organizational user uploads the packaged chaincode compressed package to their respective cello;

    2. Install chaincode: Each organizational user installs the chain code on their respective nodes;

    3. Approve: Each organization performs licensing operations on the chain code separately;

    4. Commit: When the number of licensed organizations meets the policy, one of the organizations performs the submission operation.

### APIs

1. Get chaincode information list
2. Submit chaincode

### Information List UI

NameLabelVersionPackageIdOperationCc1  
V1sha2sumInstall | Approve | Commit | Delete (if chaincode not used yet)Cc2  
V1sha2sumInstall | Approve | Commit | Delete (if chaincode not used yet)

### ![](attachments/21660911/21660952.png)

### Upload Chaincode UI

Chaincode Name:  
Description:

Version:

Choose File:  
Chaincode language:

Chaincode hash:

(maybe calculated by backend depending on performance)

![](attachments/21660911/21660953.png)

## Chaincode Installation Page

### APIs

1. Get nodes of the current organization
2. Get chaincode installation status of each node
3. Submit requests to install chaincode

### Install Chaincode UI

Choose the node to install chaincode (current org)

![](attachments/21660911/21660954.png)

## Approvement Page

### APIs

1. Get all orgs' approvement status
2. Approve current org's chaincode

### Approve Chaincode UI

Choose ChannelOrgApproved/Not ApprovedOrg1ApprovedOrg2Not ApprovedOrg3(Current Org)Not Approved (A clickable link/button)

Approving current Org's chaincode doesn't require a page. After clicking the link, it prompts a confirmation window, sends a "approve" request to backend if confirmed.

The backend checks if approvement is successful or not and returns the result to frontend (it's better to include failure info). Frontend then prompts the response.

![](attachments/21660911/21660955.png)

## Attachments:

![](images/icons/bullet_blue.gif) [image-2023-5-24\_20-2-53.png](attachments/21660911/21660951.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-5-24\_20-3-17.png](attachments/21660911/21660952.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-5-24\_20-4-29.png](attachments/21660911/21660953.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-5-24\_20-8-23.png](attachments/21660911/21660954.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-5-24\_20-16-8.png](attachments/21660911/21660955.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:04

[Atlassian](http://www.atlassian.com/)
