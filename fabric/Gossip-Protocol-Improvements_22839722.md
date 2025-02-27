1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Design Documents](Design-Documents_22840393.html)

# Hyperledger Fabric : Gossip Protocol Improvements

Created by Swetha Repakula, last modified by Morgan Bauer on May 29, 2019

## Goals:

1. Reduce Gossip Flakes
2. time.sleep in gossip tests
3. remove data races

This is less a design document and more a "design discovery". We don't know why a lot of this is the way it is. There don't seem to be any contemporaneous records from three years ago when most of it was written.

## Gossip Flakes

The general concept of gossip is is that nodes pass data around. It is not necessarily 100% foolproof to get messages through.

Unfortunately a lot of the tests behave as if the implementation can never fail.

Why are we tracking connections at all? Should gRPC be handling that? Why do we care to try to only have one and only one connection for pkiid != pkiid?

### Connection Management

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

dup as 

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

TestBasic FAB-13539  
Assignee:

- Bi-directional connections, one side hangs up the other. Additional connection racing like the below TestAccept case, which is uni-directional.
  

Test Accept:  
Assignee: [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:503b5691-8e92-4d2d-83d3-e9e74d296436?ref=confluence)

- Same client makes two connections, does not finish servicing connection before second one comes in, causing a race
- Possible Solution:
- Separate outgoing and incoming versions of the connection -&gt; so that if we see a second incoming we don’t cancel the first incoming
- [https://jira.hyperledger.org/browse/FAB-15486](https://jira.hyperledger.org/browse/FAB-15486)

Observations on Connection (gossip/comm/conn.go).connection

- stopFlag (atomic) and stopCh manage whether the connection is being closed - &gt; We should use one or the other, not both. I think with the way most of the code is, we need the stopCh, so we should get rid of the toDie() function and select on the stopCh as appropriate
- Two peers try to make a connection to each other at the same time, will end up with both connections being closed. Solution: make a deterministic decision on which peer should drop the connection and who should keep making the connection. Logic is in getConnection. Assignee: [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:503b5691-8e92-4d2d-83d3-e9e74d296436?ref=confluence)
- Single connection, single direction
  
  - single connection is good for nodes behind a firewall
  - single direction (grpc uses either client stream or server stream) was the initial implementation. Changing that now would require a large refactor and may make the peers unable to talk to peers of older versions.

### DeMultiplexer

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

Code isn't safe to call multiple times. Rewritten in whole. Same interface.

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
