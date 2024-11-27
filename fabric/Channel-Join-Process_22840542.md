1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Fabric Interop Working Group](Fabric-Interop-Working-Group_22839518.html)
4. [Interop Documents](Interop-Documents_22839726.html)

# Hyperledger Fabric : Channel Join Process

Created by Brian Brian, last modified by David-Paul Dornseifer on Mar 07, 2019

For the channel join request, the focus will be on the artifacts that needs to be exchanged between orgX and orgA (as proxy for the complete business network). Only the artifacts to be exchanged is defined, the exchange process, for example via email, is outside the scope of the definition.For the channel join request, the focus will be on the artefacts that needs to be exchanged between orgX and orgA (as proxy for the complete business network). Only the artefacts to be exchanged is defined, the exchange process, for example via email, is outside the scope of the definition.

Also not defined is the interaction between any organization and vendor. It is assumed that either the organization has a direct access to the peer node and can complete all steps required, or that the organization has access to a management UI of the vendor where the relevant join steps are encapsulated.

## Join Request:

The join-request should be based on native Hyperledger Fabric definition ([protos/common.ConfigGroup](https://github.com/hyperledger/fabric/blob/release-1.4/protos/common/configtx.pb.go#L367)) since that includes all required information to represent an organization on a Hyperledger Fabric channel. Furthermore, it integrates well with the existing tooling.

The join-request can be generated with the existing Hyperledger Fabric tool set ([configtxlator](https://hyperledger-fabric.readthedocs.io/en/release-1.4/commands/configtxlator.html), [peer CLI](https://hyperledger-fabric.readthedocs.io/en/release-1.3/peer-commands.html), [configtxgen](https://hyperledger-fabric.readthedocs.io/en/release-1.4/commands/configtxgen.html)).

General Workflow:

1. VendorX/orgX creates common.ConfigGroup (e.g. using [configtxgen](https://hyperledger-fabric.readthedocs.io/en/release-1.4/commands/configtxgen.html)).
2. OrgX sends the JSON representation to orgA.
3. VendorA/OrgA generates a channel update based on the current channel configuration (e.g. using [configtxlator](https://hyperledger-fabric.readthedocs.io/en/release-1.4/commands/configtxlator.html)).
4. OrgA proposes the update to the other channel members, possibly using the “management” chaincode.
5. OrgB and orgC, if so defined or required by the business network rules, sign the update and send it to orgA (e.g. using [peer CLI](https://hyperledger-fabric.readthedocs.io/en/release-1.3/peer-commands.html)) possible with the help of a “management” chaincode. -- The “management” chaincode should support relevant rules and policies, such as which organizations are required to sign the update, which kinds of conditions should apply, such as signing algorithm, consensus algorithm, etc. It is important to understand that the “management” chaincode is a technical implementation of the rules and regulations of this very specific business network (business entity) and that it can be conceived that the “management” chaincode will be different between different business networks.
6. OrgA applies the Fabric channel update with the given signatures, signed by its own organization.

## Join Response:

The join-response should include the channelID and orderer endpoints including TLS certificates so that the joining org (orgX) can download the channel genesis block via the SDK or using the peer CLI.

The response should look like this:

```
{
	"channelID": "mybusinesschannel",
	"ordererEndpoints": ["orderer0.org1.com:7050"],
	"ordererTlsCertificates": ["YmVpc3BpZWw..."]
}
```

## Management Chaincode

The purpose of the management chaincode is to standardize the way how channel updates (new channel members, configuration parameters) are shared will all the participants and how the required signatures to authorize a channel update,  are collected.

Assumptions:

- One instance of management chaincode should be installed/instantiated on each Hyperledger Fabric channel.
- Per default it should be installed on each joined peer of the channel members.
- The recommended endorsement policy should be majority.
  
  → The chaincode endorsement policy should reflect the majority of the channel members and might be upgraded periodically.

The minimum requirement to manage channel update proposals (upload new proposal, sign proposal, list proposals) would require the following interfaces:

- proposeUpdate(proposalID string, update string)
  
  Channel members can propose a new channel update.
- - Update: the base64 encoded [protos/common.ConfigUpdate](https://github.com/hyperledger/fabric/blob/release-1.4/protos/common/configtx.pb.go#L304)
- addSignature(proposalID string, signature string)
  
  Channel members can add their signature to a proposed channel update.
- - Signature: the base64 encoded [protos/common.ConfigSignature](https://github.com/hyperledger/fabric/blob/release-1.4/protos/common/configtx.pb.go#L546)
- getProposals() (\[]Proposal)
  
  Channel members can view proposals to check the status, display them, or check if the channel policy is already met.
  
  Note: That the channel policy has to be checked manually by the user and not by the chaincode.
- - Returns: the pending(/all) proposals with their update and signatures.
- getProposal(proposalID string) (Proposal)
  
  Channel members can request the current status of the proposal.
- deleteProposal(proposalID string)
  

Using these interfaces, all members of a channel would be able to participate in the channel update process.

A rough workflow using this management chaincode could look like this:

1. OrgA receives a channel join request from orgX e.g. via email.
2. OrgA creates channel update and uses the ProposeUpdate interface of the management chaincode to store the update with a specific proposalID.
3. OrgA creates a signature on the proposed channel update and publishes it via the AddSignature interface using the proposalID.
4. \[optional] orgA informs other channel members about the new proposal.
   
   This should normally happen via a Channel Management App of the vendors.
5. OrgB and orgC add their signatures via the AddSignature interface. (This call can be triggered via the custom UI implementation of a vendor).
6. OrgA monitors the signing process and sends the channel update to the orderer when the channel update policy is fulfilled.
7. If the channel update has been accepted by the orderer, orgA compiles the channel join response message and sends it back to orgX.
8. Afterwards, OrgA can delete the proposal using the proposalID.

## Channel Join Workflow

![](attachments/22840542/22840555.jpg?width=550)

## Attachments:

![](images/icons/bullet_blue.gif) [interoperability.jpg](attachments/22840542/22840555.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
