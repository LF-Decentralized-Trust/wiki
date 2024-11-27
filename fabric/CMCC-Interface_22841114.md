1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Fabric Interop Working Group](Fabric-Interop-Working-Group_22839518.html)
4. [Interop Documents](Interop-Documents_22839726.html)

# Hyperledger Fabric : CMCC Interface

Created by Bright Yin on Aug 08, 2019

The CMCC(Consortium Management Chaincode) will not only be used when the organization joins the channel mentioned in [Channel Join Process](https://lf-hyperledger.atlassian.net/wiki/display/fabric/Channel+Join+Process), but also can assist the organization to complete the modification of the channel configuration in the later channel management. We should clarify the definition and the behavior of the chaincode interface on the technical level, and record the consensus part reached by each participants in the Interop Working Group. Regardless of  the implementation of the CMCC or the form of deployment(user chaincode or system chaincode) in the future, if the definition and behavior of the CMCC interfaces are consistent, the interoperability between the various vendors can still be achieved on existing implementations.

We already defined the data structure of channel join request, channel join response and a general basic description of the CMCC interface in [Channel Join Process](https://lf-hyperledger.atlassian.net/wiki/display/fabric/Channel+Join+Process), we also have a basic implementation [Management Chaincode](https://lf-hyperledger.atlassian.net/wiki/display/fabric/Management+Chaincode) of CMCC interface. Here we provide a more detailed definition and clarification for the interface,  including required fields for related data structures, input parameters of the chaincode invoking interface, as well as the data format of the returned result. Besides, some extensions to the interface is also proposed.

In the management of Fabric network, there may be a variety of actions that require different organizations to sign(vote) before it can be effected. For example, in the channel join process we have already discussed, each organization needs to sign(vote) on the channel configuration changes(ConfigUpdate) that the new organization joins; in the Fabric Lifecycle 2.0, before the chaincode can be instantiated, each organization in the channel needs to vote, by default, more than half of the organization agreed on the chaincode package, then the chaincode can be instantiated and invoked. For the Peer node, we may also need some adjustments to the startup parameters; for example, the state of the system chaincodes whitelist which defined in core.yaml. So I made some minor adjustments to the existing CMCC interface: Categorize proposals into different types for future extension in different scenarios.

## 1. Data Structure

#### Proposal

Proposal is the main data structure used in CMCC interface to describe a proposal in Fabric blockchain network, which should contain at least the following fields:

- `creator`: string, contains the msp ID of the proposal creator

<!--THE END-->

- `proposal_type`: string, define the type of the proposal, see section *proposal\_type*

<!--THE END-->

- `proposal_data`: string, the content of the proposal, the type of data stored is determined by *proposal\_type*

<!--THE END-->

- `description`: string, describes the proposal

<!--THE END-->

- `signatures`: map&lt;string, string&gt;, the key of map is the msp ID of organization, the value of map is the signature data and determined by *proposal\_type*

#### proposal\_type

*proposal\_type* has the following string enumeration types, and for unlisted or unsupported types, the proposal should be ignored:

1. `ConfigUpdate`: When type is *ConfigUpdate*, Proposal's field *proposal\_data* is base64-encoded string representation of [common.ConfigUpdate](https://github.com/hyperledger/fabric/blob/release-1.4/protos/common/configtx.pb.go#L304); the value of *signatures* is base64-encoded string representation of [common.ConfigSignature](https://github.com/hyperledger/fabric/blob/release-1.4/protos/common/configtx.pb.go#L546).

\*) Other types to be added...

## 2. Chaincode Function

When the chaincode method encounters an error, it MUST use shim.ERROR to return an error message; the error message MUST start with `Code xxx:` to distinguish the type of error, 4xx for user input error, and 5xx for internal error. When the proposal ID is not found in chaincode, an error message starting with `Code 404:` SHOULD be returned.

#### 2.1. proposeConfigUpdate

IdxArgumentComment1proposalIDThe unique ID of the proposal, a string of up to 64 characters \[a-z]\[A-Z]\[-\_], cannot be the same as any existing proposal ID2configUpdateThe content of channel config update, base64-encoded string representation of common.ConfigUpdate3descriptionIt describes the proposal

*proposeConfigUpdate* proposes a channel configuration update proposal, and the organizations in the channel can sign(vote) on the proposal. The function *proposeConfigUpdate* MUST produce a Proposal of type **ConfigUpdate** and set the field *creator*. When the *proposeConfigUpdate* succeeds, the event `newProposalEvent` MUST be set and return the ID of the proposal. This method MUST check the parameter *proposalID* and SHOULD check the parameter *configUpdate* to reject malformed data.

#### 2.2. addSignature

IdxArgumentComment1proposalIDThe proposal ID that needs to add signature2signatureThe signature data that determined by **proposal\_type**

*addSignature* adds the signature of an organization to an existing proposal. When the *addSignature* succeeds, the event `newSignatureEvent` MUST be set and return the proposal ID. When the same organization invoke this method multiple times to sign the same proposal, the old signature is overwritten by the new one. This method SHOULD check the parameter **signature** and reject the malformed data.

#### 2.3. getProposals

getProposals is used to get all the proposals stored in CMCC. When the method succeeds, JSON-encoded map data is returned. The key of map is proposal ID, the value of map is *Proposal* data structure

#### 2.4. getProposal

IdxArgumentComment1proposalIDThe proposal ID

*getProposal* is used to get the current state of a proposal in CMCC. When succeeds, it returns JSON-encoded *Proposal*.

#### 2.5. deleteProposal

IdxArgumentComment1proposalIDThe proposal ID that will be deleted

*deleteProposal* is used to delete an existing proposal in CMCC. When the *deleteProposal* succeeds, the event `deleteProposalEvent` MUST be set and return the JSON-encoded *Proposal* which is deleted. A permission check MUST be performed when deleting, and only the organization who create the Proposal  can delete it.

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
