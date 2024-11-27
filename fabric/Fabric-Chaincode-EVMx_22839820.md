1. [Hyperledger Fabric](index.html)
2. [Hyperledger Fabric](Hyperledger-Fabric_22839309.html)

# Hyperledger Fabric : Fabric Chaincode EVMx

Created by Bradley Shaw on May 05, 2023

DateMay 05, 2023Issues150 issues

## Summary

## Important highlights from this release

## All updates for this release

### Epic

- [FABCE-115](https://jira.hyperledger.org/browse/FABCE-115) CLOSED Update Mocks
- [FABCE-114](https://jira.hyperledger.org/browse/FABCE-114) CLOSED as a developer, I want to see debug logs when a test fails
- [FABCE-113](https://jira.hyperledger.org/browse/FABCE-113) CLOSED Use simpler network for integration tests
- [FABCE-112](https://jira.hyperledger.org/browse/FABCE-112) CLOSED Only install gotools necessary
- [FABCE-111](https://jira.hyperledger.org/browse/FABCE-111) CLOSED Check that proxy server is up before sending requests
- [FABCE-110](https://jira.hyperledger.org/browse/FABCE-110) CLOSED Maintain a Counterfeiter versioning
- [FABCE-109](https://jira.hyperledger.org/browse/FABCE-109) CLOSED Combine Web3 and Fab3 integration tests into one suite
- [FABCE-108](https://jira.hyperledger.org/browse/FABCE-108) CLOSED Improve Documentation about the EVM
- [FABCE-107](https://jira.hyperledger.org/browse/FABCE-107) CLOSED Update Contributions with new Github PR process
- [FABCE-106](https://jira.hyperledger.org/browse/FABCE-106) CLOSED Add Contribution information to README
- [FABCE-105](https://jira.hyperledger.org/browse/FABCE-105) CLOSED Fix web3 command in tutorial in fabric-chaincode-evm
- [FABCE-104](https://jira.hyperledger.org/browse/FABCE-104) CLOSED Update Docs with new Network ID
- [FABCE-103](https://jira.hyperledger.org/browse/FABCE-103) CLOSED Minor code error in EVM\_Smart\_Contracts.md
- [FABCE-102](https://jira.hyperledger.org/browse/FABCE-102) CLOSED Update Transaction Fab3 APIs with new fields
- [FABCE-100](https://jira.hyperledger.org/browse/FABCE-100) BACKLOG Improve Instructions on installing EVMCC
- [FABCE-99](https://jira.hyperledger.org/browse/FABCE-99) BACKLOG Documentation should indicate Fab3 requires a running Fabric Network
- [FABCE-98](https://jira.hyperledger.org/browse/FABCE-98) CLOSED The documentation of the chaincode-EVM should list the limitations
- [FABCE-97](https://jira.hyperledger.org/browse/FABCE-97) CLOSED Missing end bracket in Readme Instructions
- [FABCE-96](https://jira.hyperledger.org/browse/FABCE-96) CLOSED Update cli help out put for port flag
- [FABCE-95](https://jira.hyperledger.org/browse/FABCE-95) CLOSED fabric evm chaincode no longer a plugin
- [FABCE-94](https://jira.hyperledger.org/browse/FABCE-94) CLOSED Add Table of Contents to Readme
- [FABCE-93](https://jira.hyperledger.org/browse/FABCE-93) CLOSED Fix Fab3 Instructions
- [FABCE-92](https://jira.hyperledger.org/browse/FABCE-92) CLOSED Update documentation to new environment variable
- [FABCE-91](https://jira.hyperledger.org/browse/FABCE-91) CLOSED Add getLogs documentation to Fab3 Instructions
- [FABCE-90](https://jira.hyperledger.org/browse/FABCE-90) CLOSED Update Go and Fabric Version requirements
- [FABCE-89](https://jira.hyperledger.org/browse/FABCE-89) BACKLOG GetTransactionReceipt docs should explain the status field
- [FABCE-88](https://jira.hyperledger.org/browse/FABCE-88) CLOSED Improve Instructions on Building Fab3
- [FABCE-87](https://jira.hyperledger.org/browse/FABCE-87) BACKLOG Stop logging to Stderr in Fab3
- [FABCE-86](https://jira.hyperledger.org/browse/FABCE-86) CLOSED eventually in test can get stuck in failure state
- [FABCE-85](https://jira.hyperledger.org/browse/FABCE-85) CLOSED Defers should properly be executed on exit
- [FABCE-84](https://jira.hyperledger.org/browse/FABCE-84) CLOSED golint has wrong import in makefile
- [FABCE-83](https://jira.hyperledger.org/browse/FABCE-83) CLOSED Transaction Receipt Logs Data
- [FABCE-82](https://jira.hyperledger.org/browse/FABCE-82) CLOSED Add omitempty tag to ContractAddress in TxReceipt
- [FABCE-81](https://jira.hyperledger.org/browse/FABCE-81) CLOSED Fix logging in fab3 main
- [FABCE-80](https://jira.hyperledger.org/browse/FABCE-80) BACKLOG Can't interact with chaincode using Fab3
- [FABCE-79](https://jira.hyperledger.org/browse/FABCE-79) CLOSED Event marshaling anomaly during contract deployment
- [FABCE-78](https://jira.hyperledger.org/browse/FABCE-78) CLOSED getCode should not error on empty account
- [FABCE-77](https://jira.hyperledger.org/browse/FABCE-77) CLOSED Contract Address should have '0x' prefix
- [FABCE-76](https://jira.hyperledger.org/browse/FABCE-76) CLOSED GetBlockByNumber returns null GasPrice and Value
- [FABCE-75](https://jira.hyperledger.org/browse/FABCE-75) CLOSED Log Filtering/Matching should not be strict case
- [FABCE-74](https://jira.hyperledger.org/browse/FABCE-74) CLOSED makefile test invocation should always work
- [FABCE-73](https://jira.hyperledger.org/browse/FABCE-73) CLOSED Listing Ethereum accounts does not work
- [FABCE-72](https://jira.hyperledger.org/browse/FABCE-72) CLOSED Fab3 does not wait for Http Server to be created
- [FABCE-71](https://jira.hyperledger.org/browse/FABCE-71) CLOSED integration tests are polluted by existing evnironment
- [FABCE-70](https://jira.hyperledger.org/browse/FABCE-70) CLOSED Chaincode-evm's make fails if GOPATH contains more than one element
- [FABCE-69](https://jira.hyperledger.org/browse/FABCE-69) CLOSED EVM smart contracts don't have permission to call other EVM contracts
- [FABCE-68](https://jira.hyperledger.org/browse/FABCE-68) CLOSED Transaction Receipt should prefix contract addresses with '0x'
- [FABCE-67](https://jira.hyperledger.org/browse/FABCE-67) CLOSED Invalid transactions should not be shown in a block
- [FABCE-66](https://jira.hyperledger.org/browse/FABCE-66) BACKLOG getTransactionInformation fails when looking at non evm transactions
- [FABCE-65](https://jira.hyperledger.org/browse/FABCE-65) CLOSED add CODE\_OF\_CONDUCT.md
- [FABCE-64](https://jira.hyperledger.org/browse/FABCE-64) CLOSED Release fabric-chaincode-evm v0.3.0
- [FABCE-63](https://jira.hyperledger.org/browse/FABCE-63) CLOSED update baseimage version
- [FABCE-62](https://jira.hyperledger.org/browse/FABCE-62) CLOSED Allow events Solidity Contracts
- [FABCE-61](https://jira.hyperledger.org/browse/FABCE-61) CLOSED Change fab3 output file in documentation
- [FABCE-60](https://jira.hyperledger.org/browse/FABCE-60) CLOSED Consolidate Long Eventual Timeout in chaincode-evm integration tests
- [FABCE-59](https://jira.hyperledger.org/browse/FABCE-59) CLOSED Use cmd library and use flags for fab3
- [FABCE-58](https://jira.hyperledger.org/browse/FABCE-58) CLOSED Pin Fabric dependency to Fabric v1.4.0
- [FABCE-57](https://jira.hyperledger.org/browse/FABCE-57) CLOSED Cleanup Makefile and scripts
- [FABCE-56](https://jira.hyperledger.org/browse/FABCE-56) BACKLOG evaluate usage of gogo/protobuf vs golang/protobuf
- [FABCE-55](https://jira.hyperledger.org/browse/FABCE-55) CLOSED as a developer, I do not want to maintain two copies of the fab3 types
- [FABCE-53](https://jira.hyperledger.org/browse/FABCE-53) CLOSED Make release 0.1 for fabric-chaincode-evm
- [FABCE-52](https://jira.hyperledger.org/browse/FABCE-52) TO DO Change user address generation for EVM
- [FABCE-51](https://jira.hyperledger.org/browse/FABCE-51) CLOSED Implement JSON RPC APIs to support Remix
- [FABCE-50](https://jira.hyperledger.org/browse/FABCE-50) CLOSED Create a Github Pull Request Template
- [FABCE-49](https://jira.hyperledger.org/browse/FABCE-49) CLOSED fabric-chaincode-evm release v0.2.0
- [FABCE-48](https://jira.hyperledger.org/browse/FABCE-48) CLOSED refactor common pattern out of integration test
- [FABCE-47](https://jira.hyperledger.org/browse/FABCE-47) BACKLOG Switch to using \`github.com/pkg/errors\`
- [FABCE-45](https://jira.hyperledger.org/browse/FABCE-45) CLOSED Update Jenkinsfile to fetch the patchset on verify and clone the repo on merge
- [FABCE-44](https://jira.hyperledger.org/browse/FABCE-44) CLOSED Add From field
- [FABCE-43](https://jira.hyperledger.org/browse/FABCE-43) CLOSED Remove Jenkins Pipeline Files
- [FABCE-42](https://jira.hyperledger.org/browse/FABCE-42) CLOSED Allow smart contracts to create other smart contracts
- [FABCE-41](https://jira.hyperledger.org/browse/FABCE-41) CLOSED Update Dep version to 0.5.4
- [FABCE-40](https://jira.hyperledger.org/browse/FABCE-40) CLOSED Add gasPrice and value fields to fabric evm transactions
- [FABCE-39](https://jira.hyperledger.org/browse/FABCE-39) CLOSED build fabric-chaincode-evm proxy binary
- [FABCE-38](https://jira.hyperledger.org/browse/FABCE-38) CLOSED update fabric-sdk-go dependency
- [FABCE-37](https://jira.hyperledger.org/browse/FABCE-37) CLOSED ginkgo By clause should not print out during default test run
- [FABCE-36](https://jira.hyperledger.org/browse/FABCE-36) CLOSED azp verify-build step should run \`make basic-checks\` instead of \`make checks\`
- [FABCE-35](https://jira.hyperledger.org/browse/FABCE-35) CLOSED clean up linters
- [FABCE-34](https://jira.hyperledger.org/browse/FABCE-34) CLOSED Remove scripts/goListFiles.sh
- [FABCE-33](https://jira.hyperledger.org/browse/FABCE-33) CLOSED Bump burrow/evm version
- [FABCE-32](https://jira.hyperledger.org/browse/FABCE-32) CLOSED \`net\_version\` should return a quantity
- [FABCE-31](https://jira.hyperledger.org/browse/FABCE-31) CLOSED missing err checks in fab3 integration tests
- [FABCE-30](https://jira.hyperledger.org/browse/FABCE-30) CLOSED Cleanup Test Eventuallys and Extend Timeouts
- [FABCE-29](https://jira.hyperledger.org/browse/FABCE-29) CLOSED Pin evm chaincode to a Fabric release
- [FABCE-28](https://jira.hyperledger.org/browse/FABCE-28) CLOSED Improve logging in Fab3 main
- [FABCE-27](https://jira.hyperledger.org/browse/FABCE-27) BACKLOG Add transaction logs to eth\_getTransactionReceipt output
- [FABCE-26](https://jira.hyperledger.org/browse/FABCE-26) CLOSED Switch references of fabproxy to fab3
- [FABCE-25](https://jira.hyperledger.org/browse/FABCE-25) CLOSED GetBlockByNumber should return GasLimit
- [FABCE-24](https://jira.hyperledger.org/browse/FABCE-24) CLOSED make clean should call gotools-clean
- [FABCE-23](https://jira.hyperledger.org/browse/FABCE-23) CLOSED update readme
- [FABCE-22](https://jira.hyperledger.org/browse/FABCE-22) BACKLOG Add customized logger per incoming request
- [FABCE-21](https://jira.hyperledger.org/browse/FABCE-21) CLOSED Update Dep version to 0.5.0
- [FABCE-20](https://jira.hyperledger.org/browse/FABCE-20) BACKLOG Run a Jenkins job nightly for fabric-chaincode-evm
- [FABCE-19](https://jira.hyperledger.org/browse/FABCE-19) CLOSED Upgrade to Burrow 0.24.2
- [FABCE-18](https://jira.hyperledger.org/browse/FABCE-18) CLOSED \`net\_version\` should return a 53 bit or less quantity
- [FABCE-17](https://jira.hyperledger.org/browse/FABCE-17) CLOSED Add Zap logger to fabric-chaincode-evm
- [FABCE-16](https://jira.hyperledger.org/browse/FABCE-16) BACKLOG Implement BlockHash opcode
- [FABCE-15](https://jira.hyperledger.org/browse/FABCE-15) CLOSED Update fabric-chaincode-evm CI pipeline scripts using shared library
- [FABCE-14](https://jira.hyperledger.org/browse/FABCE-14) BACKLOG eth\_sendRawTransaction RPC should be supported in Fab3
- [FABCE-13](https://jira.hyperledger.org/browse/FABCE-13) BACKLOG Configure logging in Fab3 by flag
- [FABCE-12](https://jira.hyperledger.org/browse/FABCE-12) BACKLOG As a Truffle developer, i want to use Fab3 as backend
- [FABCE-11](https://jira.hyperledger.org/browse/FABCE-11) CLOSED add checks to fabric-chaincode-evm repo
- [FABCE-10](https://jira.hyperledger.org/browse/FABCE-10) CLOSED as a rando developer, I should need admin privs to deploy contract
- [FABCE-9](https://jira.hyperledger.org/browse/FABCE-9) CLOSED Proposal to Change Required Number of Reviews to Single Non Author Review
- [FABCE-8](https://jira.hyperledger.org/browse/FABCE-8) CLOSED \[Fabric-Java-SDK] Query hex option Problem
- [FABCE-7](https://jira.hyperledger.org/browse/FABCE-7) CLOSED add docker image to build
- [FABCE-6](https://jira.hyperledger.org/browse/FABCE-6) IN PROGRESS As a fabric evm chaincode user, I want to interact with my contract via Ethereum JSON RPC
- [FABCE-5](https://jira.hyperledger.org/browse/FABCE-5) CLOSED Burrow EVM support in Fabric - fab-web3 proxy
- [FABCE-4](https://jira.hyperledger.org/browse/FABCE-4) CLOSED Burrow EVM support in Fabric - phase II
- [FABCE-3](https://jira.hyperledger.org/browse/FABCE-3) IN PROGRESS Support toolings in Ethereum ecosystem
- [FABCE-2](https://jira.hyperledger.org/browse/FABCE-2) CLOSED Burrow EVM support in Fabric - phase I
- [FABCE-1](https://jira.hyperledger.org/browse/FABCE-1) CLOSED Implement EVM filtering for logs and events

### Bug

- [FABCE-149](https://jira.hyperledger.org/browse/FABCE-149) IN CR REVIEW Fab3 should default transaction receipt logs to an empty array
- [FABCE-147](https://jira.hyperledger.org/browse/FABCE-147) CLOSED Set GO111MODULE when generating Fab3 mocks

### Task

- [FABCE-150](https://jira.hyperledger.org/browse/FABCE-150) BACKLOG migrate to tools.go for tool dependency management
- [FABCE-144](https://jira.hyperledger.org/browse/FABCE-144) CLOSED Update Documentation for Found Issues
- [FABCE-54](https://jira.hyperledger.org/browse/FABCE-54) CLOSED Split EVMCC and Fab3
- [FABCE-46](https://jira.hyperledger.org/browse/FABCE-46) CLOSED Split EVMCC &amp; Fab3 dependencies

### Test Task

- [FABCE-148](https://jira.hyperledger.org/browse/FABCE-148) CLOSED Upgrade Integration to use Fabric 1.4 release branch

### Documentation

- [FABCE-146](https://jira.hyperledger.org/browse/FABCE-146) CLOSED update github PR template
- [FABCE-145](https://jira.hyperledger.org/browse/FABCE-145) CLOSED update README for 0.4.0 release
- [FABCE-101](https://jira.hyperledger.org/browse/FABCE-101) BACKLOG Indicate that \`payable\` keyword from Solidity will not work

### Sub-task

- [FABCE-143](https://jira.hyperledger.org/browse/FABCE-143) CLOSED Update the return value of net\_version
- [FABCE-142](https://jira.hyperledger.org/browse/FABCE-142) TO DO Create a unique identifier for a given EVMCC &amp; Channel
- [FABCE-141](https://jira.hyperledger.org/browse/FABCE-141) TO DO Fab3 should accept batch requests
- [FABCE-140](https://jira.hyperledger.org/browse/FABCE-140) CLOSED document eth\_getLogs
- [FABCE-139](https://jira.hyperledger.org/browse/FABCE-139) CLOSED Allow blockhash as argument to getLogs
- [FABCE-138](https://jira.hyperledger.org/browse/FABCE-138) IN CR REVIEW GetFilterLogs &amp; GetFilterChanges
- [FABCE-137](https://jira.hyperledger.org/browse/FABCE-137) CLOSED NewFilter &amp; UninstallFilter
- [FABCE-136](https://jira.hyperledger.org/browse/FABCE-136) CLOSED implement topics filter
- [FABCE-135](https://jira.hyperledger.org/browse/FABCE-135) CLOSED implement address Filter
- [FABCE-134](https://jira.hyperledger.org/browse/FABCE-134) CLOSED Add eth\_BlockNumber
- [FABCE-133](https://jira.hyperledger.org/browse/FABCE-133) CLOSED Switch net\_version to be a number
- [FABCE-132](https://jira.hyperledger.org/browse/FABCE-132) CLOSED Add eth\_getTransactionCount
- [FABCE-131](https://jira.hyperledger.org/browse/FABCE-131) CLOSED Implement minimal get logs eth\_getLogs
- [FABCE-130](https://jira.hyperledger.org/browse/FABCE-130) TO DO Implement getStorageAt
- [FABCE-129](https://jira.hyperledger.org/browse/FABCE-129) CLOSED bump baseimage to 0.4.13 to match 1.3.0 release
- [FABCE-128](https://jira.hyperledger.org/browse/FABCE-128) CLOSED Change EVMSCC to be a system chaincode plugin
- [FABCE-127](https://jira.hyperledger.org/browse/FABCE-127) CLOSED Take metadata files into consideration
- [FABCE-126](https://jira.hyperledger.org/browse/FABCE-126) CLOSED Add support in peer CLI to invoke/query evm chaincode
- [FABCE-125](https://jira.hyperledger.org/browse/FABCE-125) CLOSED create a fab-proxy to translate Ethereum JSON RPC to Fabric API
- [FABCE-124](https://jira.hyperledger.org/browse/FABCE-124) CLOSED add supports in Fabric for scc plugins
- [FABCE-123](https://jira.hyperledger.org/browse/FABCE-123) CLOSED create plugin makefile to generate .so for linux to be used with Docker
- [FABCE-122](https://jira.hyperledger.org/browse/FABCE-122) CLOSED Create a voting DApp on both Ethereum and Fabric
- [FABCE-121](https://jira.hyperledger.org/browse/FABCE-121) CLOSED Add an e2e test for evm chaincode
- [FABCE-120](https://jira.hyperledger.org/browse/FABCE-120) CLOSED handle evm contract deployment
- [FABCE-119](https://jira.hyperledger.org/browse/FABCE-119) CLOSED Implement Burrow state interfaces
- [FABCE-118](https://jira.hyperledger.org/browse/FABCE-118) CLOSED Implement EVM chaincode as a system chaincode plugin
- [FABCE-117](https://jira.hyperledger.org/browse/FABCE-117) CLOSED Add EVM implementation of core/chaincode/platforms/platform interface
- [FABCE-116](https://jira.hyperledger.org/browse/FABCE-116) CLOSED initial commit

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
