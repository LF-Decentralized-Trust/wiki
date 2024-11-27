1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Maintenance Endpoint

Created by Nikita Puzankov, last modified on Aug 19, 2020

Status

DECIDED

Stakeholders

[Kamil Salakhiev](https://lf-hyperledger.atlassian.net/wiki/people/557058:07723e0b-a027-4cc4-ad6d-324e41cccb4d?ref=confluence)  [Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)   

Outcome

Error rendering macro 'jira' : null

Due date

07 Aug 2020

Owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

## Background

Iroha Users need information about "system" aspects which are not available via Iroha Queries to World State View, for example:

- Peer's Health Check (Naming of states inspired by [Prometheus](https://prometheus.io/docs/prometheus/latest/management_api/))
- Peer's Management - start, stop
- Resources Monitoring  - CPU, Memory and Disk consumption
- [Logging Configuration](Logging_21012113.html)
- Business Measurements of Iroha
  
  - Transactions per second amount
  - Blocks Storage size
  - Submitted transactions statuses changes
  - Blocks statuses changes

## Problem

For some clients and for Iroha administrators it is important to have more information than can be provided by Iroha [Data Model](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#24-data-model).

One of such a cases were described by the following requirements:

- Client should receive status changes of all transactions submitted by this client.
- Iroha Peer should guarantee that changes submitted to the client goes over synchronous protocol and messages received by client if peer and client are connected.
  
  - If peer, client or network goes down - Client should use another API to check current status of entities needed.
  - Iroha Peer will not store information about status changes and they may be lost.
  - iroha Peer will provide information available for this peer only.
- The same functionality should be provided to monitor blocks statuses.

Because transactions states changes are not stored on the Blockchain and can't be presented in World State View \`Maintenance Endpoint\` is a good place to add this functionality to.

## Solution

As a result we can create additional client-facing Iroha API which described in the table below:

APIURIProtocolCommentsConfiguration\`/config\`HTTP

REST API for managing Iroha Peer's configuration:

- log level

Monitoring\`/health\`HTTPAligned with [Prometheus](https://prometheus.io/docs/prometheus/latest/management_api/) Peer's Health Check information\`/metrics\`HTTPMetrics ready to be scraped by PrometheusEvents\`/event\`

WebSocket

Human friendly WS API for Cloud Events consumersTCP/IPLow-level API with binary messages for Cloud Events consumers

Each API responsible for subset of maintenance features. Events API available in two variants - WebSocket for mobile clients, web applications and other human oriented technologies, while TCP/IP option for those clients which resources are limited.

### Decisions

- Use HTTP for configuration and monitoring APIs (message format can be json or text based on Prometheus specification)
- Events API implemented as WebSocket and proprietary TCP/IP variants
- Additional port should be used by Maintenance Endpoint

### Alternatives

- We can stay with TCP approach but we will need to change DevOps processes and tools, Substrate Off-chain workers also will not be able to deal with TCP
- We can use HTTP for Events API but it's not effective way to handle active sessions between Iroha Peers and Substrate Off-chain workers

### Assumptions

Different [system events](Cloud-Events_21012424.html) will be aligned with [CNCF CloudEvents Specification](https://github.com/cloudevents/spec) and may be used in non-maintenance endpoints later.

### Concerns

To prevent secured information losses \`subscribers\` should receive only information they had permissions to have. The "CanAnything" permission will provide information about the entire system and most of maintenance endpoints will require accounts with it. If account has no "CanAnything" permission, it's signature should be presented in transactions to receive information about their states changes.

### Risks

- Substrate off-chain workers integration will require additional parties (no direct communication with Iroha) \`\[9;4]\`
- Support of two variants for Events API will require additional maintenance resources \`\[7;2]\`

## Additional Information

- [https://github.com/cloudevents/spec/blob/v1.0/spec.md](https://github.com/cloudevents/spec/blob/v1.0/spec.md)
- [https://prometheus.io/docs/instrumenting/exposition\_formats/](https://prometheus.io/docs/instrumenting/exposition_formats/)
- [https://substrate.dev/docs/en/knowledgebase/runtime/off-chain-workers#fetching-external-data](https://substrate.dev/docs/en/knowledgebase/runtime/off-chain-workers#fetching-external-data)

## Attachments:

![](images/icons/bullet_blue.gif) [image2020-6-25\_17-34-54.png](attachments/21012343/21016447.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
