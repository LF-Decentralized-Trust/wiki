1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Design](Framework-Go-Design_18512160.html)

# Hyperledger Aries : Issue-credential flow

Created by derektrider, last modified by Talwinder Kaur on Nov 19, 2019

This page documents the Issue-credential technical flow (as described in the spec [here](https://github.com/hyperledger/aries-rfcs/tree/master/features/0036-issue-credential)) between two Aries agents: Agent A (the Issuer) and Agent B (the Holder).

There are three alternate flows. We will be focusing on the "holder begins with a proposal" flow. The other two flows are essentially just subsets of this flow.

1. We're taking the "happy path" - no errors.
2. An ack for the receipt of the credential was not requested.

Before implementing the full flow, we could instead start with a simpler version first, and then expand upon it later. Here's what a simplified version might look like. It eliminates the propose-offer cycle and instead merges the proposal message into the request message, effectively turning the exchange into a two-step process:

![](attachments/18483298/18512687.png?width=800)

# High Level Design - Methods, Inputs/Actions - Simplified Flow

### SendCredentialRequest

Sends a *request-credential* message to another agent.

**Input:**

1. Connection ID: Used to identify the agent to send this proposal to.
2. Desired credential data (optional)
3. Requested formats for credential.
4. Comment (optional)
5. Schema ID - a filter to request credentials based on a particular schema (optional).
6. Credential definition ID - a filter to request a credential based on a particular credential definition (optional).

**Actions:**

1. Send *request-credential* message to other agent, along with a unique *Credential\_exchange\_id*.
2. Create a *credential\_exchange\_record* with the unique *Credential\_exchange\_id*.
3. Update state to *credential-requested* for given *credential\_exchange\_record*.

### HandleCredentialRequest

Receives a *request-credential* message from another agent.

**Input:**

1. A c*redential\_exchange\_id*.
2. A *request-credential* message.

**Actions:**

1. Validate incoming message.
2. Update state to *credential\_requested* for given *credential\_exchange\_record*.
3. Notify business logic via client.

### SendIssueCredential

Sends an *issue-credential* message to another agent.

**Input:**

1. A c*redential\_exchange\_id*.
2. The issued credentials.
3. Comment (optional)

**Actions:**

1. Send *issue-credential* message to other agent.
2. Update state to *credential-issued* for given *credential\_exchange\_record.*

### HandleIssueCredential

Receives an *issue-credential* message from another agent.

**Input:**

1. A credential\_exchange\_id.
2. An issue-credential message.

**Actions:**

1. Validate incoming message.
2. Store the credential.
3. Update state to *credential\_received* for given *credential\_exchange\_record*.
4. Notify business logic via client.

Below shows the full flow.

![](attachments/18483298/18512675.png?width=800)

# High Level Design - Methods, Inputs/Actions - Full Flow

### SendProposal

Sends a *propose-credential* message to another agent.

**Input:**

1. Connection ID: Used to identify the agent to send this proposal to.
2. Desired credential data (optional)
3. Comment (optional)
4. Schema ID - a filter to request credentials based on a particular schema (optional)
5. Credential definition ID - a filter to request a credential based on a particular credential definition (optional)

**Actions:**

1. Send proposal message to other agent, along with a unique *Credential\_exchange\_id*.
2. Create a *credential\_exchange\_record* with the unique *Credential\_exchange\_id*.
3. Update state to *proposal\_sent* for given *credential\_exchange\_record*.

### HandleProposal

Receives a *propose-credential* message from another agent.

**Input:** A propose-credential message and a *credential\_exchange\_id*.

**Actions:**

1. Validate incoming message.
2. Create a *credential\_exchange\_record* with the provided unique *credential\_exchange\_id*.
3. Update state to *proposal\_received* for given *credential\_exchange\_record.*
4. Notify business logic.

### SendOffer

Sends *offer-credential* message to another agent.

**Input:**

1. A *credential\_exchange\_id*.
2. Connection ID: Used to identify the agent to send this offer to.
3. Credential preview: Represents the credential data that the issuer wants to issue.
4. "Offers" attachment: An array of attachments that further define the credential being offered. Could be used to clarify the format of the credentials.
5. Comment (optional)

**Actions:**

1. Validate incoming message.
2. Send *offer-credential* message to other agent.
3. Update state to *offer\_sent* for given *credential\_exchange\_record*.

### HandleOffer

Receives an *offer-credential* message from another agent.

**Input:** An *offer-credential* message and a c*redential\_exchange\_id*.

**Actions:**

1. Update state to *offer\_sent* for given *credential\_exchange\_record*.
2. Notify business logic via client.

### SendCredentialRequest

Sends a *request-credential* message to another agent.

**Input:**

1. A *credential\_exchange\_id*.
2. Requested formats for credential.

**Actions:**

1. Send *request-credential* message to other agent.
2. Update state to *credential-requested* for given *credential\_exchange\_record.*

### HandleCredentialRequest

Receives a *request-credential* message from another agent.

**Input:**

1. A c*redential\_exchange\_id*.
2. A *request-credential* message.

**Actions:**

1. Validate incoming message.
2. Update state to *credential\_requested* for given *credential\_exchange\_record*.
3. Notify business logic via client.

### SendIssueCredential

Sends an *issue-credential* message to another agent.

**Input:**

1. A c*redential\_exchange\_id*.
2. The issued credentials.
3. Comment (optional)

**Actions:**

1. Send *issue-credential* message to other agent.
2. Update state to *credential-issued* for given *credential\_exchange\_record.*

### HandleIssueCredential

Receives an *issue-credential* message from another agent.

**Input:**

1. A credential\_exchange\_id.
2. An issue-credential message.

**Actions:**

1. Validate incoming message.
2. Store the credential.
3. Update state to *credential\_received* for given *credential\_exchange\_record*.
4. Notify business logic via client.

# Additional details

## Layer responsibilities

Business logic: Initiates the protocol and ultimately determines whether to accept/refuse going to the next step.

Client: The first step in sending a message to another agent happens here. The business logic/controller does not call the underlying service directly. Note that there can be different clients depending on the need (e.g. Go client, REST client, etc)

Service: Last step in the chain for sending messages and also the first step in the chain for receiving messages. Responsible for tracking state and saving messages to the local store.

## Other Details

The issuer and holder are assumed to have already established a connection previously via DID Exchange.

# Unknowns - Clarification Needed!

The [spec](https://github.com/hyperledger/aries-rfcs/tree/master/features/0036-issue-credential) generally seems to be assuming that Indy is being used. There are some parts of the spec that, in the absence of Indy, are unclear:

The propose-credential message has schema\_id and cred\_def\_id fields. In the ACA-Py demo they are used to identify the credential format, which is stored in the ledger. What should we do here?

The offer-credential message has an "offers~attach" field. It says that it's supposed to be an "array of attachments that further define the credential being offered". The specific example it provides describing what this looks like is for Indy. What do we do?

The request-credential message has a "requests~attach" field. Similar to the "offers~attach" field from offer-credential, it is supposed to define the requested formats for the credential. In the absence of Indy, what does this look like?

One of the supported flows is to send a *request-credential* message without going through the propose-offer cycle. How does this work?

## **Design Questions TBD :**

1. How to register schema on the ledger?
2. Go through VC and refactor if required ?
3. At what point we need to store the schema to the ledger and retrieve from ledger ?
4. If schema ID is related to verifiable credential ?

## Attachments:

![](images/icons/bullet_blue.gif) [Issue-credential\_flow\_holderRequest.png](attachments/18483298/18512620.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2019-11-17 at 11.08.03 AM.png](attachments/18483298/18512677.png) (image/png)  
![](images/icons/bullet_blue.gif) [Issue-credential\_simplified.png](attachments/18483298/18512687.png) (image/png)  
![](images/icons/bullet_blue.gif) [Issue-credential\_flow\_proposalFullFlow.png](attachments/18483298/18512675.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
