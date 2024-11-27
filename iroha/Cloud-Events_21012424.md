1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Cloud Events

Created by Nikita Puzankov, last modified on Aug 13, 2020

Status

DECIDED

Stakeholders

[Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence) [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [Vladislav Markushin](https://lf-hyperledger.atlassian.net/wiki/people/5ecbc0c8eb77320c1f684409?ref=confluence) [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) 

Outcome

Error rendering macro 'jira' : null

Due date

07 Aug 2020

Owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence) 

## Background

Different Iroha users requested possibility to receive information about things outside of a Iroha Queries scope, like list of rejected transactions or changes in their statuses.

Because storage of this information on the Blockchain may have a big cost another approaches were considered.

## Action items

- [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence) should collect comments, make final decision and move it to [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)
- [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence) should ask mobile and frontend developers to comment this RFC

## Problem

During requirements gathering about \`Bridge\` and \`DEX\` Iroha Modules and comments on [Maintenance Endpoint](Maintenance-Endpoint_21012343.html) RFC following needs were found:

- An ability for Clients to watch for Transactions and Block changes in almost real-time manner.
- [A security mechanism](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Maintenance+Endpoint?focusedCommentId=21016385) to filter changes and do not share information that client has no permissions to obtain.

These needs were addressed as additional requirements for [Maintenance Endpoint](Maintenance-Endpoint_21012343.html) and following issues were created:

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

## Solution

As a standardized format for such an events [CloudEvents specification](https://github.com/cloudevents/spec/blob/master/spec.md) was proposed as CloudNative Computing Foundation incubating project with 1.0 version released.

Maintenance endpoint will provide API marked as "unstable" feature (for release 2.0.0) with an ability to:

- Connect [Consumer](https://github.com/cloudevents/spec/blob/master/spec.md#consumer) (Iroha Client) to the [Source](https://github.com/cloudevents/spec/blob/master/spec.md#source) (Iroha Peer) providing signed filter criteria
  
  - Criteria gives Iroha Peer information about types of Events needed
  - Signature gives Iroha Peer information about the client to check permissions

That way we will address all requirements:

- An ability to receive changes in submitted by client Transactions statuses
- An ability to receive changes in Blocks formed by Peers with information inside filtered based on Clients permissions

[![](attachments/thumbnails/21012424/21016628)](attachments/21012424/21016628.pdf) 

### Decisions

- Iroha Network library will provide protocol for a two-way interactive communications session. Iroha Client library will provide Rust API for more high level functions, like "subscribe\_to\_block\_changes" and "subscribe\_to\_transaction\_changes"
- Iroha Events will align to CloudEvents schema version 1.0
- TCP and WebSocket API will be provided by Iroha Peer
- Functionality should be optional

### Alternatives

### Concerns

- Some clients may fail to work with low-level TCP API or with rust client library

### Assumptions

- We have a two-way interactive communication session between client and peer with streams of changes from peer's side and acceptance confirmations from client's side
- Cloud Events will be marked as "unstable" for 2.0.0 version and may have breaking changes in future minor releases
- In case of network problems or client side errors changes will not be delivered
- Information about these events is not stored by Iroha Peers

### Risks

- Cloud Events will increase resources consumption and decrease performance \`\[4;7]\`
- Breaking changes in Events format will require additional updates in client libraries \`\[9;5]\`

## Additional Information

- [https://github.com/cloudevents/spec/blob/v1.0/spec.md](https://github.com/cloudevents/spec/blob/v1.0/spec.md)

## Attachments:

![](images/icons/bullet_blue.gif) [CloudEvents.pdf](attachments/21012424/21016628.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
