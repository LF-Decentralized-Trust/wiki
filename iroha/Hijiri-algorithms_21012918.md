1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)

# Hyperledger Iroha : Hijiri algorithms

Created by Ivan Rybin, last modified on Mar 25, 2021

  Status

IN PROGRESS  

Stakeholders

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence)

Outcome  
Due date  
Owner

[Ivan Rybin](https://lf-hyperledger.atlassian.net/wiki/people/602171f07db80e006a08ad45?ref=confluence)

## Background

The hijiri reputation system is based on rounds. At each round, validating peers that are registered with the membership service perform the following tasks to establish trust (reliability) ratings for the peers:

- data throughput test
- version test
- computational test
- data consistency test

## Problem

Research hijiri algorithms and create literature review.

## Solution

As a solution **Incremental Eigentrust++** with custom `s` function, which will take account of several things like:

### Network locality

1\. Take P as ping time between 2 peers and MinPingTime as minimal ping time possible (something like 1ms or 0.03ms)

2\. Let `Max = -log(MinPingTime)`, as `log(MinPingTime)`is supposed to be very big negative number

3\. `log(P) / Max`should normalize P and make its value between \[-1; 1], and as P will decrease value will increase

4\. `log(P) / (2 * Max)` is supposed to be between \[-0.5; 0.5]

4\. Now `locality(P) = log(P) / (2 * log(MinPingTime)) + 0.5`, and  its value is in range \[0; 1]

### Computation power

May be calculated with something like this:

1\. sending transaction with instruction count equal to N

2\. taking time for peer to respond as T and P as ping time and PF as Ping factor (how many RTTs needed to send data to deliver response)

3\. `(T - P * PF) / N` (Should be normalized by some amount of predefined computation score maximum)

(via sending transactions with some number of instruction count and calculating aggregated time spent on them)

### Version test

Send all types of messages to peer and determine version of peer. Equation can look like this (taking V and Vp as our version and peer version):

1\. `version(V, Vp) = (V - Vp) / V`

### Data consistency

Should be checked within block synchronization.

### Success rate

It is pretty straightforward as in Eigentrust papers:

1\. `success_rate(i, j) = success(i, j) / (success(i, j) + failed(i, j))`

### S function

`s` function itself will share same properties as in **eigentrust**: it will be bound in `[0; 1]` and priorities of several parameters can be easily configured.

`s` looks like this (w\_* is just weights such that: sum(w) = 1.0):

`s(i, j) = if interacted(i, j) {`

    `w_network * network_locality(i, j) +`  
`w_comp * comp(i, j) +`  
`w_version * version(i, j) +`  
`w_data * data_consistency(i, j) +`  
`w_success * success_rate(i, j)`  
`} else {`

`p(i, j) // initial trust`

`}`

Comparison of proposal to **eigentrust** and **eigentrust++** (without incremental part). There is some pseudocode of \`s\`:

[https://pastebin.com/eUftjp6M](https://pastebin.com/eUftjp6M)

### Decisions

As a decision I propose is trying to use both ideas from Incremental **Eigentrust** and metrics related to performance from **GossipSub**.

### Alternatives

- The most widely used general solution is **Eigentrust++**\[1]. It relies upon the metrics of successful requests divided by successful and failed requests. Every peer propagates its scores to other peers and weighted transitive foreign scores are used to calculate trust to other peers.

<!--THE END-->

- In the stacking world of course stacking itself is used for reputation\[2] although it can be used in other consensus approaches\[3].

<!--THE END-->

- There is a class of blockchains which use simple local unshared trust:
  
  - This kind of solution uses **Substrate**\[4]. Every peer has a per peer trust counter which is not shared. If peer does something forbidden or not answering for a long time then its trust goes to minimum and the peer disconnects from the bad peer.
  - **GossipSub** messaging solution\[5] uses interesting formula for getting local trust. It uses several weighted parameters: time in mesh, first message deliveries, mesh message delivery rate, message delivery failures, invalid messages, application specific score, ip address collocation factor.

<!--THE END-->

- There are many variations of **Eigentrust++**:
  
  - **Incremental Eigentrust**\[6] uses snapshot comparison to reduce redundant calculations at each reputation cycle.
  - **HonestPeer**\[7] uses local trust to choose some honest peer (peer with maximum trust) and pulls data from it.
  - **AuthenticPeer++**\[8] uses **Incremental Eigentrust** relative to file storage.

### Concerns

We should think about several issues. The main priority is to improve performance of the network as we have consensus algorithm to taking care of security. Performance itself is reducible to performance of the network and performance of the reputation system. We should minimize time spent in both sending messages and computing reputation, but generally sending messages takes more time then local calculation of reputation.

### Assumptions

Assumptions is made that we need to address performance of the network and that local calculations take way less time then sending messages by network.

### Risks

## Additional Information

1. [https://nemplatform.com/wp-content/uploads/2020/05/NEM\_techRef.pdf](https://nemplatform.com/wp-content/uploads/2020/05/NEM_techRef.pdf)
2. [https://wiki.polkadot.network/docs/en/learn-consensus](https://wiki.polkadot.network/docs/en/learn-consensus)
3. [https://nymtech.net/nym-whitepaper.pdf](https://nymtech.net/nym-whitepaper.pdf)
4. [https://substrate.dev/](https://substrate.dev/)
5. [https://arxiv.org/pdf/2007.02754](https://arxiv.org/pdf/2007.02754)
6. [https://repository.upenn.edu/cgi/viewcontent.cgi?article=1430&amp;context=cis\_papers](https://repository.upenn.edu/cgi/viewcontent.cgi?article=1430&context=cis_papers)
7. [https://www.sciencedirect.com/science/article/pii/S1319157815000440](https://www.sciencedirect.com/science/article/pii/S1319157815000440)
8. [https://uksim.info/ems2017/CD/data/1410a191.pdf](https://uksim.info/ems2017/CD/data/1410a191.pdf)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
