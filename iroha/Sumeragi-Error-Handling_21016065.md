1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Sumeragi Error Handling

Created by Egor Ivkov on Apr 24, 2020

For error handling, you also need to add:

- CreateLeaderSuspect/SignLeaderSuspect
- CreateCommitTimout/SignCommitTimeout
- CreateVotingTimeout/SignVotingTimeout

Here is some info about each:  
LeaderSuspect

- f+1 signatures are needed to elect a new leader
- used when someone sends a tx to the leader but a new block is not created within some expected time (like the block time)

CommitTimout

- f+1 signatures are needed and if f+1 are received on this message, the f+1 signatures and the block hash are written into the successfully created block; this is done to prevent forking of stake via a committed block withholding attack
- every time a peer votes for a block, they expect a commit message within a certain amount of time and this timeout occurs if they don't get a commit message when expected; the solution is therefore to invalidate their vote and the old block and elect a new leader and proxy tail (probably randomly recording everyone so that a new leader and new proxy tail are elected is good. obviously any random reordering needs to be deterministic as every peer will need to compute the new order independently)

VotingTimeout

- this message can only be created by the proxy tail
- the proxy tail starts a timer when they receive first vote or block proposal and if the 2f+1 votes for a block are not all received before the timer goes off, the proxy tail creates this voting timeout and sends it to all the peers
- we MAY be able to get rid of this as a separate type as the commit timeout should handle this as well; let's explore this simplification

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
