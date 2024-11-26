1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Programs &amp; Grants](22155199.html)

# Besu : Besu Execution Client Incentive Program

Created by SajZ on Jan 06, 2022

- [Besu Execution Client Incentive Program](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Besu-Execution-Client-Incentive-Program)
- - [Overview](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Overview)
  - [Program Goals &amp; Eligibility](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Program-Goals-amp-Eligibility)
  - [Configuration](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Configuration)
  - [Structure](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Structure)
  - - [1. Make deposits](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#1-Make-deposits)
    - [2. Transfer control of active signing keys](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#2-Transfer-control-of-active-signing-keys)
    - [3. Client operates nodes/validators](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#3-Client-operates-nodesvalidators)
    - [4. Release sets of withdrawal credentials upon meeting milestones](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#4-Release-sets-of-withdrawal-credentials-upon-meeting-milestones)
  - [Milestones](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Milestones)
  - [Success metrics](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Success-metrics)
  - - [Metrics](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Metrics)
    - [Probation](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Probation)
    - [Slashing](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Slashing)
    - [Consensus Layer Dependencies](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Consensus-Layer-Dependencies)
  - [Terms](https://hackmd.io/bDkEQkvyQcKZA6aSaahqgA#Terms)

## **Overview**

The Ethereum Foundation is launching an Execution Layer Client Incentive Program (ELCIP). This program will provide execution-layer client teams with locked ETH in the form of live validators to be released according to certain milestones, including post-merge performance and progress towards enabling withdrawals from the beacon chain.

## **Program Goals &amp; Eligibility**

The program aims to provide long-term support and incentives for teams towards maintaining reliable clients and a healthy network overall.

For client teams to be eligible, they should already be contributing to the general development of Ethereum and intend to support the upcoming transition to proof of stake. Throughout the program, teams will need to maintain certain levels of performance to be eligible for the rewards. More on this below.

## **Configuration**

**Name**

**Value**

**Description**

NUM\_PERFORMANCE

128

Number of validators monitored for performance

NUM\_CANARIES

16

Number of canary validators

NUM\_VALIDATORS

NUM\_PERFORMANCE + NUM\_CANARIES

Number of total validators

INITIAL\_RELEASE

32

Number of validators to release at initial major milestone

TIMED\_RELEASES

\[6, 10, 14, 18, 22, 26 + NUM\_CANARIES]

Number of validators to be released each 6 months after INITIAL\_RELEASE

METRICS\_WINDOW

8192

Number of epochs over which success metrics are observed

MAX\_PROBATION\_WINDOW

32768

Maximum number of epochs that the Client can be in probation before the EF can partially or fully remove the Client from the incentivization

## **Structure**

The following are the high level steps performed by “EF” and the “Client” through the life of this plan.

1. Make deposits
2. Transfer control of active signing keys
3. Client operate nodes/validators
4. Release withdrawal credentials in waves

### **1. Make deposits**

After a client has agreed to join the program, the EF creates NUM\_VALIDATORS 32-ETH deposits.

Total ETH at stake in the client incentivization plan is equal to NUM\_VALIDATORS * 32.

In consultation with execution-layer client teams, a formal start date for this program will be determined where teams will gain control of validators, approximately between October 1st and whenever merge occurs.

### **2. Transfer control of active signing keys**

After step 1, there will be NUM\_VALIDATORS privkeys mapping to the pubkeys in the validator deposits controlled by a single mnemonic. These keys must be securely transferred to the client team.

This mnemonic is transferred to the Client via one of the following:

1. Using asymmetric encryption (e.g. PGP) via a known/validated public key of the recipient Client
2. 1. Read verbally 25% at a time over 4 encrypted calls of various platforms
3. Through an alternatively negotiated, secure means

The Client then generates NUM\_VALIDATORS keystores using the mnemonic and verifies that each privkey maps sequentially to the batch of validator pubkey deposits made in their name.

The EF retains the mnemonic in cold storage in the event that active keys must be used to exit validators from the program.

### **3. Client operates nodes/validators**

Deposits are made; keys are transferred. Now, the Client is in charge of the management of the associated validators until withdrawal credential privkeys are released. Specifically, the Client *must* use their own software as an execution-engine and is responsible for choosing and maintaining a consensus-engine throughout the incentivization period.

Performance of the Client’s validators can be assessed simply by viewing chain metrics, but additional node performance metrics might be requested.

### **4. Release sets of withdrawal credentials upon meeting milestones**

Waves of validators are to be released to the Client upon meeting pre-defined milestones via the transfer of the underlying privkeys for the validator withdrawal credentials.

When a wave of validators is released, this ends the obligation of the Client to the EF for those validators. The Client is free to choose to continue to validate, to exit, to withdrawal, etc.

These keys will be pgp encrypted and transferred in batches.

## **Milestones**

Due to the dynamic nature of the ever evolving Ethereum roadmap, simplicity is favored in the choice of milestones.

A wave of credentials are released when withdrawals from the beacon chain are enabled, with a minimum period of one year between the launch of the Execution Layer Client Incentive Program (ELCIP) and the complete release of the first wave of credentials.

If withdrawals from the beacon chain are enabled within or before the first year of the ELCIP, the first wave of credentials will be released monthly, in equal tranches, from the first month after withdrawals are enabled, to the one year mark of the program. For example, if withdrawals are enabled 6 months after the start of the program, then 1/6th of the first tranche will be released on months 6, 7, 8, 9, 10, 11 and 12. Otherwise, the first wave of credentials will be released when withdrawals are enabled. Subsequent waves are released over time if the Client continues to meet expectations. Specifically, the milestones are as follows:

1. Release INITIAL\_RELEASE validators at the time at which withdrawals from the beacon chain are enabled (WITHDRAWALS\_ENABLED\_TIME).
2. for i, num\_validators in enumerate(TIMED\_RELEASES), release num\_validators validators at time WITHDRAWALS\_ENABLED\_TIME + (i + 1) * 6\_months if client operation continues to exhibit successful metrics.

## **Success metrics**

Client/validator performance must consistently meet a set of success metrics to continue participation in this program.

The first NUM\_PERFORMANCE validators of the deposited validators are tracked by the EF to assess metrics. The last NUM\_CANARIES validators of the deposited validators are free to be used by the Client for testing, experimental releases, etc. Canary validators *are not* expected to constantly meet the success metrics but are still subject to slashing rules.

### **Metrics**

**Name**

**Value**

**Description**

MIN\_ACCEPTABLE\_BALANCE

31.75 ETH

Minimum acceptable balance of client validators

MIN\_ATTESTATION\_PERCENTAGE

95 percent

Minimum acceptable percentage of attestations created by client validators

MIN\_BLOCK\_PERCENTAGE

95 percent

Minimum acceptable percentage of blocks created by client validators

The following are the success metrics that the Client must meet:

- Client validators on average do not drop below MIN\_ACCEPTABLE\_BALANCE balance
- Client validators have at least MIN\_ATTESTATION\_PERCENTAGE percentage of expected attestations included on chain over any METRICS\_WINDOW epoch period
- Client validators have at least MIN\_BLOCK\_PERCENTAGE percentage of expected blocks included on chain over any METRICS\_WINDOW epoch period

Moreover, client teams are expected to actively participate in research and development of crucial network upgrades, including but not limited to implementation of a state management solution (e.g. state expiry). The EF is solely responsible for determining whether this metric has been met.

Above all else, the EF expects client teams to actively work toward ensuring a robust and healthy network. The EF recognizes that in some scenarios these metrics are not entirely in the control of the Client (e.g. large portion of the network offline for an extended period of time due to issues with another client). In most such cases, the METRICS\_WINDOW has been selected to be long enough to account for issues and recovery, but in such exceptional scenarios, the EF will also take into account exogenous factors outside of the Client’s control.

*Note*: In the context of this plan, validator top-ups are against the rules and should generally be avoided. If in some scenario a top-up would benefit the health of the network, the EF and client can discuss and reformulate the metrics/milestones accordingly.

### **Probation**

If the Client drops below the success metrics, the Client’s incentivization status moves into probation. During a probationary period the Client has MAX\_PROBATION\_WINDOW epochs to get metrics back to successful standards, and during a probationary period the Client cannot have any validator credentials released. The amount of time spent in probation pushes back the release of any validator credentials by at least that amount of time.

If Client metrics remain in probationary status for more than MAX\_PROBATION\_WINDOW epochs, the EF can at their discretion partially or fully remove the Client from the incentivization program and partially or fully exit the Client’s validators.

### **Slashing**

In the event that one or more of a Client’s validators is slashed, such a validator is removed from the incentive program.

If the event is relatively isolated and quickly remedied, the EF can at its sole discretion choose to place a maximum of 16 of the slashed ETH per slashed validator back into the program to be released at the final milestone.

If the slashable event is exceedingly large, negligent, or repeated, the EF can at their discretion partially or fully remove the Client from the incentivization program and partially or fully exit the Client’s validators.

*Note*: Performance and canary validators are *both* subject to the slashing rules.

### **Consensus Layer Dependencies**

While the Client is fully responsible to ensure that their operation is run in a performant and non-slashable way, we recognize that there is a limit to what execution layer teams can do to mitigate issues on the consensus layer (and vice-versa). Specifically, this means we expect the Client to adopt best practices with regards to running their validators, but will not penalize them in the case of a widespread consensus-layer issue. Best practices when running validators include:

- Ensuring that the Client can interoperate with most/all major consensus clients, at least on canary validators;
- Ensuring that the Client’s failures are decorrelated from the rest of the network, both by relying on diverse consensus layer clients and hosting setups;
- Ideally ensuring that the Client’s validators are split across &gt;1 consensus client in case of a consensus client-specific issue;
- Ensuring that the Client has the ability to switch from one consensus client to another in the case of a consensus client-specific issue.

## **Terms**

This plan is an opt-in additional incentivization plan for execution-layer clients. Participation in this plan and the amount of locked funds available in the plan will have no bearing on future client grant decisions. Clients *can* include a small stipend for node infrastructure in grant requests regardless of participation.

Prerequisites of participation in this plan are successful participation in multi-client testnets and generally demonstrating production readiness at all times.

In general and especially in the event of exceptional and unforeseen scenarios concerning the client, the client team, the Ethereum roadmap, and/or the Ethereum mainnet, the EF is solely responsible for deciding how to award withdrawal credentials and/or restructure the terms of this incentive plan at any time.

Such exceptional scenarios include, but are not limited to, the following:

- Separate client teams merging into one
- Client team splitting into two
- Client team ceasing the maintenance of a component (e.g. validator client) or the entirety of their software
- Ethereum roadmap radically changing such that the milestones no longer reflect achievable goals
- Ethereum mainnet has extended issues with stability, finality, or otherwise proper function
- Ethereum mainnet undergoes a contentious hardfork

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
