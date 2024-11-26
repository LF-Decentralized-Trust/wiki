1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Policies](Policies_22154154.html)

# Besu : Defect Prioritisation Policy

Created by Christopher Hare, last modified by Matt Nelson (Deactivated) on Jun 16, 2023

For information on the process of triaging a bug, check out [this page](Bug-Triage-Process_22154548.html)

# Definition

The process outlined in this document is only concerned with a mismatch between the behavior of a system and expectations of that system occurring, after the feature development has been completed by the responsible scrum team.

There are many definitions for bugs and defects, both in their causes and the time of their detection, unfortunately, many definitions are contradictory.

As GitHub has the ‘bug’ label, for simplicity that term will be used when referring to any problem identified after the GI (Github issue) for the feature has been updated to ‘Done’, irrespective of who discovered the issue and at what point in the software lifecycle.

# Public Networks

## Deciding Priority

When deciding how to respond to a bug, consider the two variables of probability and severity and apply them to a risk matrix to determine the priority and corresponding action. These are based on a Mainnet use-case and Proof of Stake consensus with Besu.

## Probability

How likely are actual users to encounter the issue during their use of the product?

*A feature rarely used, with a high likelihood of failure may have a lower probability than a popular feature with a low likelihood of failure (due to a high number of customers affected).*

**Frequent**

Will occur several times during common network conditions on Mainnet, across restarts, and be easily reproducible.

**Probable**

Likely to occur when engaging in a specific behavior or during common network conditions. 

**Occasional**

Likely to occur during specific network conditions or with specific CLs/environments. 

**Remote**

Unlikely but possible to occur in the lifetime of a validator.

**Improbable**

So unlikely, it can be assumed occurrence may not be experienced.

## Severity

How bad is the problem when it does get encountered?

**Catastrophic**

Data loss/corruption or slashing occurs or is very likely to occur for the user. Detrimental risk for a validator stack. Persists over a restart. 

**Critical**

Requires a restart or user interaction for a node to continue operation and for a validator to perform its duties. 

**Moderate**

Some components are not working as intended, but the validator continues its duties, i.e. RPC accuracy. 

**Marginal**

Non-critical components are functioning within limits, but with unintended behaviors or side-effects. 

**Insignificant**

No significant threat posed and can be left unmediated. 

When judging the severity of the bug as insignificant, as the bug does not need addressing it automatically gets set as P5 (very low) priority.

# Private Networks

## Deciding Priority

When deciding how to respond to a bug, consider the two variables of probability and severity, and apply them to a risk matrix to determine the priority and corresponding action.

## Probability

How often actual customers are likely to encounter the issue during their use of the product?

*A feature rarely used, with a high likelihood of failure, may have a lower overall probability than a popular feature with a low likelihood of failure (due to a high number of customers affected).*

**Frequent**

Will occur several times in the lifetime of the product.

**Probable**

Likely to occur often in the lifetime of the product.

**Occasional**

Likely to occur some time in the lifetime of the product.

**Remote**

Unlikely but possible to occur in the lifetime of the product.

**Improbable**

So unlikely, it can be assumed occurrence may not be experienced.

## Severity

How bad is the problem when it is encountered?

*An issue that causes data loss/corruption is automatically classed as Catastrophic.*

**Catastrophic**

Detrimental risk for the product as a whole.

**Critical**

Jeopardises feature(s) of the product, not ruining the product entirely.

**Moderate**

Jeopardises aspects of a feature, not ruining the feature entirely.

**Marginal**

Causes an inconvenience when using a feature of the product.

**Insignificant**

No significant threat posed and can be left unmediated. 

# Risk Matrix

**Catastrophic**

**Critical**

**Moderate**

**Marginal**

Insignificant

**Frequent**

Very High

High

High

Medium

Very Low

**Probable**

High

High

Medium

Medium

Very Low

**Occasional**

High

Medium

Medium

Low

Very Low

**Remote**

Medium

Medium

Low

Low

Very Low

**Improbable**

Medium

Low

Low

Very Low

Very Low

# Priority Levels

**Priority**

**Policy** 

(recommended actions)

P1

Very High

Added immediately to the current sprint taking priority over that work. It may very well require the effort of more than one team member, possibly including the whole team.  
Alternatively refer to [Security page](Security_22154229.html) if it is a security issue. 

P2

High

Added immediately to the current sprint and resolution starts as soon as logically possible. Ideally, should be resolved by the end of the sprint. Team decides who can best address the issue.

P3

Medium

Added as a priority for the next sprint, at the discretion of the product owner.

P4

Low

Documented. Discussed in the next sprint planning meeting at the discretion of the product owner.

*Candidate for a Good First Issue for the community.*

P5

Very Low

Documented in list of known issues. Revisited only if severity or probability increases or at the discretion of the product owner.

*Candidate for a Good First Issue for the community.*

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
