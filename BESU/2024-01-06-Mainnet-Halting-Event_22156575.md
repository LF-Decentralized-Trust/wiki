1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Incident Reports](Incident-Reports_22154962.html)

# Besu : 2024-01-06 Mainnet Halting Event

Created by Matt Nelson (Deactivated), last modified by Sally MacFarlane on Jun 12, 2024

# Executive Summary:

On January 6th, 2024 at block 18947893, an estimated 70% of Besu nodes on Mainnet experienced a halt. This included those running recent software releases, up to and including 23.10.3. Affected clients ceased processing blocks and updating the Ethereum state, until workarounds were communicated out to users, and a hotfix was published.

What follows is a more detailed outline of the event, how it was mitigated, and the reasoning processes involved.

# Preamble:

In late November, during development of new features, the Besu team identified a problem with the [Bonsai state storage format.](https://consensys.io/blog/bonsai-tries-guide)  Specifically, how Bonsai encoded the state changes in “trie logs.”  Trielogs are essentially a delta of the ethereum state from block to block - they record the changed state values prior to block execution (preimage) and the new values that result from block execution.  The defect related to how Besu logged [metamorphic contract deployment](https://mixbytes.io/blog/metamorphic-smart-contracts-is-evm-code-truly-immutable).  In some specific cases Besu could write an incorrect preimage in the trielog for storage that was self-destructed.  This defect, in some form, had been present in the Bonsai code for quite some time. We had been working on a couple fixes which addressed the root of the problem.   

On Dec 19th we discovered several of our canary Besu nodes on the Sepolia network had halted.  Most of the Sepolia canary nodes had stopped at the same block.  Looking more closely, we discovered that on Dec 18th, a freshly funded [address](https://sepolia.etherscan.io/address/0x0c27f8c61db4e6c37214d64fc867eb9775963f7d) was experimenting with SELFDESTRUCT/CREATE2 patterns.  This was essentially the same case that we had discovered internally and were testing a fix for.

This address tested a few iterations of this pattern, but the first iteration that caused an issue for Besu was a [transaction](https://sepolia.etherscan.io/tx/0xe5e29a1a1a679bc1a538788031e230a82027b4d6b502290937a4b3aa1c6b4ce9#internal) in block 4913001. This version created, self-destructed and re-created the contract via create2 in a single transaction, ensuring that all of the transactions land in the same block.  Besu executed this block fine, but most recent versions of Besu created an invalid trielog with a bad preimage.  When Besu subsequently moved the worldstate head to this block via the [engine api](https://github.com/ethereum/execution-apis/blob/main/src/engine/common.md), it would halt while trying to apply the invalid trielog.  A similar pattern occurred on [4913006](https://sepolia.etherscan.io/tx/0xc055db058785e7c040caad7a8c57753b3ef9eff06c9c5266863164e22c6e4c37#internal).  The last iteration was 4913057, where the contract was finally self-destructed and not recreated.  

We run and monitor many canary instances of Besu on different networks, but we only had a few different versions of Besu running on Sepolia. Most of them halted on the first block.  Some halted on the final block.  Some development versions did not halt at all.  In short, they didn’t all present with the same error or halt on the same block.  When we looked at the pattern of activity for this address, we had a suspicion that this was intentional or malicious activity, so we decided to expedite the work already in progress to fix this issue so we could get it out in the last release of the year, 23.10.3.

Leading up to 23.10.3, we took great care to exercise the fix.  We completed a full sync on all test nets and found Besu had no problem with the blocks that halted it previously.  An additional Sepolia node was running a special version of Besu that would explicitly roll the state back and forth on each block to exercise the trielogs and ensure they were created and could be applied correctly.  When that testing completed we were confident we had fixed the issue.  Dec 30 we announced the release 23.10.3 on the hyperledger discord and strongly recommended users upgrade to that version.  Unfortunately the github release was left in draft, so some users that monitor github releases did not see the new release.  What we didn’t realize was that full sync testing operates directly on the main mutable world state, and does not exercise some aspects of block execution that are used in the engine api.  So the bad trielog bug was still lurking even in the latest version.

# The Main Event:

Christmas and New Years were quiet for Besu nodes.  There wasn’t anything in particular that stood out as a problem, until the morning of Jan 6. A Besu engineer was the first to note that something was amiss when nearly all of our Mainnet nodes halted at block [18947983](https://etherscan.io/block/18947893.).  A freshly funded account had deployed a [contract](https://etherscan.io/address/0xb05e7ed9ff00afe304370a7d1c1a4f7fbaae852b#internaltx) and sent transactions resulting in a bad trie log that halted most versions of Besu on Mainnet.

Checking discord, we found many users alerting us to the same problem, looking for an explanation and support getting back online.  We quickly got our own nodes back online and used that to come up with [multiple options](https://github.com/hyperledger/besu/releases/tag/23.10.3-hotfix) to get Besu validators back online as quickly as possible and to share the same operations with Besu node runners. The community support from Besu users was really outstanding - sophisticated users and devs from other projects were helping troubleshoot and to get other users back online (shoutout to the Nethermind team for help in tracing the problematic block).   

We were still trying to figure out what happened and why users on the latest version of Besu, 23.10.3, were affected.  We were reasonably certain that the metamorphic contract was the culprit, but we had to do some quick analysis, debugging, and reproduce the original case that caused the halt.  Some hours in, we discovered the condition that led to the fix not working when the block was executed via the engine API.  But reproducing the error condition was time consuming and difficult.  After consulting with our Teku counterparts about the best way to get a consensus layer client at a specific epoch, we decided it would be best to generate a beacon chain initial state from an archive consensus layer node just prior to the problem block.  We put out a call on discord for someone with a Mainnet archive consensus layer that could help us generate that state, and Jim McDonald from Attestant was able to help us.  

Now we had a candidate fix and a way to reproduce the issue, all that was left was to test the fix, package it and get it out the door as a hotfix.  We decided to add an additional condition to the hotfix that would force a backward sync if the worldstate was unavailable or corrupt when the engine api was executing newPayload or forkchoiceUpdated calls.  In most cases, this would allow Besu to just auto-heal, and users could simply install the hotfix as a resolution. 

With the ability to recreate the state before the problem, we instrumented Besu and observed the state and generated trielogs as it executed the problem block.  The first time without a fix to prove we had reproduced the problem, and subsequently with the fix to ensure Besu produced the correct trielogs and state.  After we were certain the fix for the root cause was good, we also started the hotfix on halted nodes to observe whether Besu would auto heal correctly.  In most cases Besu would auto-heal correctly, but there were still some outliers.  For example on some EL/CL pairs the consensus layer went off on a fork because Besu was reporting an invalid block.  Those cases were not able to auto-heal and still required some manual intervention.

The fix was good and the auto-heal was good enough, so we decided to release the hotfix asap since there was nothing preventing some new similar block from halting all of the newly recovered Besu nodes.

After publishing the hotfix, we announced on discord and communicated to users through various channels that it was important to upgrade even if they had already recovered their node(s).  We continued to run support through discord for a day or two to help as many users as possible, and things eventually relaxed a bit and gave us time to reflect.

# Circumstances:

The timing is suspicious.  The contract deployed on Mainnet did not look like the experiment that was done on Sepolia.  If the Mainnet contract was indeed intentionally malicious, it was well camouflaged to look innocuous, if peculiar.  The contract deployment followed a similar pattern of being funded just before the incident, with no transaction history before or since, and all the contracts involved were self-destructed afterwards.  

If this was an intentional attack, the attacker is certainly clever, but without clear motivation.  Perhaps there was some sunk cost after watching our attempts to patch this issue. They may have wanted to trigger this bug while they still could before a release.  As a reminder, halting bugs of this severity are eligible for the [EF Bug Bounty program](https://ethereum.org/en/bug-bounty/). The deployer could have earned thousands in USD as a bounty for this finding. More importantly their discovery could be celebrated publicly and earn the goodwill of client teams and the ethereum ecosystem.  The rewards of cooperation are better in this case, certainly. 

# Conclusion:

This experience has highlighted the need for client diversity on Ethereum. Thankfully, Besu being impacted as a client under the 33% threshold caused no finality issues for the network nor did besu users have a significant correlated inactivity leak on Mainnet. Our learnings from this experience underscore the importance of maintaining canaries alongside an archive CL node. Given the complexity of managing state for Bonsai, we understand that it is crucial to implement specific test cases to prevent accidental future regressions. Moving forward, we plan to create more Besu-specific tests for Bonsai and to introduce new [Hive engine API tests](https://github.com/ethereumjs/ethereumjs-monorepo/issues/2838) for this particular case. In a more light-hearted vein, we intend to celebrate the deprecation of the self-destruct opcode with a bottle of champagne at DenCun!

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
