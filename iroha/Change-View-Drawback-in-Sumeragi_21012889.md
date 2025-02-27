1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Change View Drawback in Sumeragi

Created by Egor Ivkov, last modified on Feb 16, 2021

  Status

DECIDED

Stakeholders[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence)Outcome

Error rendering macro 'jira' : null

Due date

18 Feb 2021 

Owner[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)

## Background

[Whitepaper Sumeragi Description](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#28-consensus)

Network Topology roles order initially is based on the last committed block hash.

Change View - The process of shifting network topology roles by one

F - Number of faulty peers the network can tolerate

2F+1 Peers signatures needed to commit a block

3F+1 Minimum peers in a network given F potential faults

## Problem

This problem can happen with different number of peers and faults, but for simplicity let's take F = 2 and the minimum total number of peers N = 3F+1 = 7.

Assume that the transaction was submitted and the block should be created and committed. It is not important for this case who the leader and proxy tails is.

Assume that 2 peers are offline and therefore there are not enough signatures to commit the block, but there are enough signatures to change view.

The diagrams below demonstrate how the events will unfold.

Observing peer

Validator peer

X - Faulty peer

0 View changes (5 signatures needed for commit, 3 received)

X  
X

1 View change (5 signatures needed for commit, 3 received)

X  
X

2 View changes (5 signatures needed for commit, 3 received)

X  
X

3 View changes (5 signatures needed for commit, 4 received)

X  
X

4 View changes (5 signatures needed for commit, 4 received)

X  
X

5 View changes (5 signatures needed for commit, 4 received)

X  
X

6 View changes (5 signatures needed for commit, 4 received)

X  
X

This shows that it will not be possible to commit block and the view will be changing until the network is stopped or more peers join.

The problem is with that the faulty peers are distributed across the topology, if they were close together, the change views would help.

## Solution

It is suggested to try at first shifting peers by 1 as was done previously up to N times. Then if the problems persist change view by shuffling peers (as in after the blocks are committed) instead of shifting by one. And to make the process deterministic take the tuple (block\_height, n\_change\_views) as a seed for this shuffling.

### Decisions

### Alternatives

Shuffle peers at every change view - can be costly and not optimal in cases with faulty leader.

### Concerns

As with any random process shuffling does not guarantee that particular network topology will be reached, and the network theoretically still can be stuck for forever, though with a very low probability.

### Assumptions

### Risks

## Additional Information

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
