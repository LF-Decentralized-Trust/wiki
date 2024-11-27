1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Hyperledger Besu Performance with Caliper

Created by George Ţebrean on Dec 12, 2023

Suyash Nayan

Github: [github.com/7suyash7](https://github.com/7suyash7)

LinkedIn: [Suyash Nayan](https://www.linkedin.com/in/suyash-nayan-a40970198/)

PRs in Hyperledger Besu: [https://github.com/hyperledger/besu/pulls?q=is%3Apr+author%3A7suyash7+is%3Aclosed](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20author%3A7suyash7%20is%3Aclosed)

PRs in Hyperledger Caliper:

[https://github.com/hyperledger/caliper-benchmarks/pull/252](https://github.com/hyperledger/caliper-benchmarks/pull/252)

[https://github.com/hyperledger/caliper/pull/1506](https://github.com/hyperledger/caliper/pull/1506)

## Learnings and Notes

Blog Post:

[https://medium.com/web3labs/benchmarking-hyperledger-besus-qbft-network-with-hyperledger-caliper-7700a70206e3](https://medium.com/web3labs/benchmarking-hyperledger-besus-qbft-network-with-hyperledger-caliper-7700a70206e3)

### Notes

Command to run gas-free IBFT Network

//node 1  
besu --data-path=data --genesis-file=../genesis.json --rpc-http-enabled --rpc-ws-enabled=true --rpc-ws-port=8645 --rpc-http-api=ETH,NET,IBFT --host-allowlist="\*" --rpc-http-cors-origins="all" --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

// node 2  
besu --data-path=data --genesis-file=../genesis.json --bootnodes=[enode://608604d28780cbb86fa2d588efdddb906462b9432407010d7e5ed56596354c1930fdfda118aed6b85aa893d023d36bbde3d137d9b986cfa22c25f914f2d09347@127.0.0.1:30303]() --p2p-port=30304 --rpc-http-enabled --rpc-http-api=ETH,NET,IBFT --rpc-ws-enabled=true --rpc-ws-port=8646 --host-allowlist="\*" --rpc-http-cors-origins="all" --rpc-http-port=8546 --tx-pool-limit-by-account-percentage=1 ---min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

// node 3  
besu --data-path=data --genesis-file=../genesis.json --bootnodes=[enode://608604d28780cbb86fa2d588efdddb906462b9432407010d7e5ed56596354c1930fdfda118aed6b85aa893d023d36bbde3d137d9b986cfa22c25f914f2d09347@127.0.0.1:30303]() --p2p-port=30305 --rpc-http-enabled --rpc-http-api=ETH,NET,IBFT --rpc-ws-enabled=true --rpc-ws-port=8647 --host-allowlist="\*" --rpc-http-cors-origins="all" --rpc-http-port=8547 --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

//node 4  
besu --data-path=data --genesis-file=../genesis.json --bootnodes=[enode://608604d28780cbb86fa2d588efdddb906462b9432407010d7e5ed56596354c1930fdfda118aed6b85aa893d023d36bbde3d137d9b986cfa22c25f914f2d09347@127.0.0.1:30303]() --p2p-port=30306 --rpc-http-enabled --rpc-http-api=ETH,NET,IBFT --rpc-ws-enabled=true --rpc-ws-port=8648 --host-allowlist="\*" --rpc-http-cors-origins="all" --rpc-http-port=8548 --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

Make sure to replace the Enode URL.

Command to run QBFT gas-free network:

// node 1  
besu --data-path=Node-1/data --genesis-file=genesis.json --rpc-http-enabled --rpc-ws-enabled=true --rpc-ws-port=8645 --rpc-http-api=ETH,NET,QBFT --host-allowlist="\*" --rpc-http-cors-origins="all" --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

// node 2  
besu --data-path=Node-2/data --genesis-file=genesis.json --bootnodes=[enode://08782c0dfe655c4cc702d3a12d5e1fb34b4450ea5456aa39dad82d72fc7bc17184361a010dad402c00df1bf3f40686c31595df07e8dfe1e7b283ec016e6a6da2@127.0.0.1:30303]() --p2p-port=30304 --rpc-http-enabled --rpc-http-api=ETH,NET,QBFT --rpc-ws-enabled=true --rpc-ws-port=8646 --host-allowlist="\*" --rpc-http-cors-origins="all" --rpc-http-port=8546 --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

// node 3  
besu --data-path=Node-3/data --genesis-file=genesis.json --bootnodes=[enode://08782c0dfe655c4cc702d3a12d5e1fb34b4450ea5456aa39dad82d72fc7bc17184361a010dad402c00df1bf3f40686c31595df07e8dfe1e7b283ec016e6a6da2@127.0.0.1:30303]() --p2p-port=30305 --rpc-http-enabled --rpc-http-api=ETH,NET,QBFT --rpc-ws-enabled=true --rpc-ws-port=8647 --host-allowlist="\*" --rpc-http-cors-origins="all" --rpc-http-port=8547 --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

// node 4  
besu --data-path=Node-4/data --genesis-file=genesis.json --bootnodes=[enode://08782c0dfe655c4cc702d3a12d5e1fb34b4450ea5456aa39dad82d72fc7bc17184361a010dad402c00df1bf3f40686c31595df07e8dfe1e7b283ec016e6a6da2@127.0.0.1:30303]() --p2p-port=30306 --rpc-http-enabled --rpc-http-api=ETH,NET,QBFT --rpc-ws-enabled=true --rpc-ws-port=8648 --host-allowlist="\*" --rpc-http-cors-origins="all" --rpc-http-port=8548 --tx-pool-limit-by-account-percentage=1 --min-gas-price=0 --tx-pool-max-size=4096 --miner-enabled=true --miner-coinbase=0x627306090abaB3A6e1400e9345bC60c78a8BEf57

To quickly clear the network data:

rm -rf Node-1/data/DATABASE\_METADATA.json &amp;&amp; rm -rf Node-1/data/caches/ &amp;&amp; rm -rf Node-1/data/database/  
rm -rf Node-2/data/DATABASE\_METADATA.json &amp;&amp; rm -rf Node-2/data/caches/ &amp;&amp; rm -rf Node-2/data/database/  
rm -rf Node-3/data/DATABASE\_METADATA.json &amp;&amp; rm -rf Node-3/data/caches/ &amp;&amp; rm -rf Node-3/data/database/  
rm -rf Node-4/data/DATABASE\_METADATA.json &amp;&amp; rm -rf Node-4/data/caches/ &amp;&amp; rm -rf Node-4/data/database/

Command to run Caliper:

npx caliper bind --caliper-bind-sut besu:latest

npx caliper launch manager \\  
    --caliper-benchconfig benchmarks/scenario/ERC-20/config.yaml \\  
    --caliper-networkconfig networks/besu/QBFT-Network/ERC20NetworkConfig.json \\  
    --caliper-flow-skip-install \\  
    --caliper-workspace .

Setting up a Gas Free Network (Recommended Settings): 

“To avoid the limitation of gas consumption in smart contract deployment and transaction execution, we configured all Besu blockchain networks to be gas-free by setting “gasLimit” to the maximum “0x1fffffffffffff”, “contractSizeLimit” to the maximum 2147483647, and the node startup option “min-gas-price” to 0. Also, we set the difficulty to the minimum “0x1” and the transaction pool queue size to the default 4096.”

Running Async Profiler for more information about Besu:

#!/bin/bash  
\# Start the Besu node  
besu --data-path=Node-1/data --genesis-file=genesis.json --rpc-http-enabled --rpc-ws-enabled=true --rpc-ws-port=8546 --rpc-ws-host=0.0.0.0 --p2p-host=51.15.132.70 --rpc-http-host=0.0.0.0 --rpc-http-api=E&gt;

\# Get the PID of the Besu process  
BESU\_PID=$!

\# Start async-profiler  
async-profiler/profiler.sh -d 120 -f async-profiler/output.html $BESU\_PID

Setting up Prometheus and Grafana to monitor Besu:

Docs: [https://besu.hyperledger.org/23.4.0/public-networks/how-to/monitor/metrics](https://besu.hyperledger.org/23.4.0/public-networks/how-to/monitor/metrics)

Grafana: [https://grafana.com/grafana/dashboards/16455-besu-full/](https://grafana.com/grafana/dashboards/16455-besu-full/)

Node-Exporter: [https://grafana.com/grafana/dashboards/1860-node-exporter-full/](https://grafana.com/grafana/dashboards/1860-node-exporter-full/)

## Mentor(s) Names and Contact Info

**George Tebrean (Web3 Labs)**  
email: [george@web3labs.com](mailto:george@web3labs.com) / tebreangeorge@gmail.com  
Discord: gdev

**Nischal Sharma (Web3 Labs)**  
email: [nischal@w](mailto:petrosyan@soramitsu.co.jp)eb3labs.com   
Discord: nicks1106

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
