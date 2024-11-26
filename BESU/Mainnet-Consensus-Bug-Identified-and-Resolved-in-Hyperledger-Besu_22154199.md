1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Releasing](Releasing_22154097.html)
5. [Archive](Archive_22154100.html)

# Besu : Mainnet Consensus Bug Identified and Resolved in Hyperledger Besu

Created by Tim Beiko, last modified on Dec 16, 2019

## Summary:

On December 13, 2019 a consensus issue related to the newly introduced SELFBALANCE opcode was found in Hyperledger Besu when trying to process mainnet block #9100883. The bug was quickly spotted, and an upgrade with a fix, [v1.3.7](https://github.com/hyperledger/besu/releases/tag/1.3.7), was released within hours.

**Users of Ethereum public networks (MainNet, Ropsten, and Goerli) should upgrade immediately. This upgrade is also strongly recommended for users of private networks.** 

Severity: Critical  
Occurence: Frequent (private networks) / Certain (public networks)

Affected versions: All Hyperledger Besu releases from 1.2.4 to 1.3.6, inclusively.

## Details:

The SELFBALANCE opcode was introduced as part of [EIP-1884](https://eips.ethereum.org/EIPS/eip-1884) in the recent Istanbul upgrade. It provides for cheaper access to the Ether account balance of the “current address.” Newer versions of Solidity will use this operation where appropriate only if Solidity is instructed to target the Istanbul opcodes.

On December 13, 2019, when trying to process mainnet block [#9100883](https://etherscan.io/block/9100883), Besu logged an \`InvalidBlockException\` error. Upon closer inspection, it was found that when processing transaction [0xea29026a2957e47513ae8e99c2aa513d44e17ab66a86e4a66850448cc0639dd6](https://etherscan.io/tx/0xea29026a2957e47513ae8e99c2aa513d44e17ab66a86e4a66850448cc0639dd6), which used the SELFBALANCE opcode in a contract that was called via a DELEGATECALL, instead of returning the balance of account 0xdacb1734b3259d98c8fdc755993209f9c4682cd2 (which had value), Besu returned the balance of account 0xbdbe2fb20656378753223e3f9ad08840dc579a8c (which had no value).

This led the client to execute a different block of code for zero balance conditions and produce a different result for the transaction, which resulted in a different world state and receipts hash than the block had reported. Because the receipt root hash did not match Besu rejected the block as invalid and stopped processing mainnet blocks. No additional blocks were mined on Besu after the consensus issue, so a chain split did not occur.

Upon further inspection of the EIP, it was found that the EIP did not specify a need for test cases in DELEGATECALL stacks, and no reference tests cover the operation of the SELFBALANCE in any composed context (CALL, CALLCODE, or DELEGATECALL). The [sample Geth code in the EIP](https://eips.ethereum.org/EIPS/eip-1884#implementation) also implied that the contract address was the appropriate address, but the semantics of the Contract class in go-ethereum and the address of the contract maintained in the Besu MessageFrame differ.

Luckily, because Geth, Nethermind, and Parity produced the same behavior when calling SELFBALANCE through a DELEGATECALL, all other clients stayed in consensus. 

## FAQ

### Are any funds at risk?

No.

### If I am running a node on an Ethereum public network (MainNet, Ropsten, and Goerli), am I affected?

Yes. You should upgrade your node to [v1.3.7](https://github.com/hyperledger/besu/releases/tag/1.3.7). 

### If I am running a node on a private Ethereum network (i.e. permissioned chain, consortium, etc.), am I affected?

Probably not.  In which case, you should upgrade your network to [v1.3.7 immediately to avoid any potential future disruptions.](https://github.com/hyperledger/besu/releases/tag/1.3.7)

All of the following conditions (some of which are highly unlikely for permissioned networks) must be met in order for your network to be affected::

- Your chain must track and use ether or “value.”
- - If your chain doesn’t charge for gas odds are you don’t use value.
- Your chain must have activated the Istanbul hard fork.
- Your chain must have a contract deployed that uses SELFBALANCE. This requires a special flag when invoking the Solidity contract and the code would need to have \`address\[this].balance\` as one of the expressions.
- - If your contracts never check ether balance and instead only track token balances you are not affected.
- The contract in question must be invoked via a DELEGATECALL operation.
- - Unless you are deploying “upgradable contracts” it is unlikely that this operation would occur.

### What should I do if I think my private network has been affected?

If you think your private chain has been affected, please reach out to the PegaSys team or the Besu mailing list ([besu@lists.hyperledger.org](mailto:besu@lists.hyperledger.org)) regarding next steps to upgrade your network with minimal disruption.

### I have more questions about this issue, who can I reach out to?

You can reach out to the Besu mailing list ([besu@lists.hyperledger.org](mailto:besu@lists.hyperledger.org)), the Hyperledger Besu Rocket Chat ([https://chat.hyperledger.org/channel/besu](https://chat.hyperledger.org/channel/besu) after logging in to [chat.hyperledger.org](http://chat.hyperledger.org)), or if you prefer confidentiality you can contact a [Besu maintainer](https://github.com/hyperledger/besu/blob/master/MAINTAINERS.md) directly and they can direct you from there.

## Timeline

### December 13, 2019

- **12:08PM ET:** Consensus issue discovered on Besu, at Ethereum Mainnet block #9100883.
- **3:31PM ET:** SELFBALANCE opcode &amp; transaction 0xea29026a2957e47513ae8e99c2aa513d44e17ab66a86e4a66850448cc0639dd6 identified as the cause of the consensus issue.
- **4:49PM ET:** Potential fix for the issue identified and deployed on a Besu mainnet node to test.
- **5:58PM ET:** Besu mainnet node back to the Ethereum mainnet head. Fix considered working.
- **7:35PM ET:** Besu 1.3.7 release initiated.
- **8:21PM ET:** Besu 1.3.7 release completed.

### December 14, 2019

- **7:20PM ET:** Besu 1.3.7 Announcement on Social Media

### December 16, 2019

- **2:01PM ET:** This post was published to the Hyperledger Wiki

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
