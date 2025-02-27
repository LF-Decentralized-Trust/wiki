1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Archive (Dev)](22154818.html)

# Besu : Checklist for reporting privacy issues

Created by Sally MacFarlane on Jan 21, 2021

In order for us to be able to investigate your issue, we first need to be able to reproduce it. The more information you can provide, the easier this will be, enabling us to more efficiently investigate the cause of the issue. 

# Please provide the following information

- Versions of Besu, Orion and any other relevant software (as per Besu issue template)
- Instructions for how to reproduce the scenario
- - As much specific detail as possible. All required solidity contracts, deploy scripts, supporting contracts, any other prerequisites.
  - If the original contracts or deployment scripts can’t be provided, we need a minimal version of them that causes the same issue.
- Have you verified that the same scenario works in Besu without privacy ie as a public contract
- - Including instructions on how to deploy the scenario - eg Truffle deploy scripts
- Orion logs
- [Enable revert reason](https://besu.hyperledger.org/en/stable/Reference/CLI/CLI-Syntax/#revert-reason-enabled) on Besu CLI
- Ensure in the solidity code you are using strings with require/revert statements to make it possible to track where the revert is happening
- Besu log with EVM at trace level
- - Enable trace [logging](https://besu.hyperledger.org/en/stable/HowTo/Monitor/Logging/) for the EVM org.hyperledger.besu.ethereum.vm.EVM - this will log all EVM operations in the besu log which will give more info about where it is halting

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
