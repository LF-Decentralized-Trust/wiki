1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Quality Assurance: Tests, Strategy, Reports](22839728.html)

# Hyperledger Fabric : Testing with Fabric binaries

Created by David Enyeart, last modified by Julian Castrence on Mar 03, 2021

After cloning Fabric, you can can test fabric binaries using a sample configuration. Using the binaries and sample configuration makes it simple and quick to iteratively make code changes, rebuild fabric, and test your changes from an end-to-end consumer perspective.

**Terminal prep**

Add fabric /build/bin to your PATH so that you can easily execute the binaries.  
Set FABRIC\_CFG\_PATH to fabric /sampleconfig directory, which contains sample orderer.yaml, peer.yaml, configtx.yaml, and msp for a SampleOrg.

Make sure that the listen addresses in orderer.yaml and peer.yaml do not overlap. By default, Admin.ListenAddress of orderer.yaml and operations.ListenAddress of peer.yaml are set to port 9443. It is recommended to change the port of operations.ListenAddress to 9444.

Open three terminal windows, one each for orderer, peer, and CLI. cd to /fabric directory in each terminal.

**Build fabric**

Build fabric binaries in any terminal:  
   make orderer peer configtxgen

Build docker images in any terminal (we'll need baseos and ccenv docker images for Go chaincode, we won't be using peer or orderer docker images, therefore you only need to do this step once):

   make docker-clean docker

**orderer terminal**

Create a system channel genesis block from the configtx.yaml sample solo profile:

   configtxgen -profile SampleSingleMSPSolo -channelID test-system-channel-name -outputBlock sampleconfig/genesisblock

Start orderer, which by default will use /sampleconfig/genesisblock to bootstrap the system channel:

   orderer

**peer terminal**

Start peer (with debug logging enabled for all but the chattiest packages):

   FABRIC\_LOGGING\_SPEC=debug:cauthdsl,policies,msp,grpc,peer.gossip.mcs,gossip,leveldbhelper=info peer node start

**CLI terminal**

Create a channel genesis block from the configtx.yaml sample channel profile:

   configtxgen -channelID mychannel -outputCreateChannelTx mychannel.tx -profile SampleSingleMSPChannel

Create a channel on the orderer:

   peer channel create -c mychannel -o 127.0.0.1:7050 -f mychannel.tx

Join the peer to the channel (note, peer address in core.yaml is used)

   peer channel join -b mychannel.block

Package chaincode:

   peer lifecycle chaincode package marbles.tar.gz --path &lt;PATH\_TO\_FABRIC\_SOURCE&gt;/fabric/integration/chaincode/marbles/cmd --lang golang --label marbles\_1

Install chaincode to peer:

   peer lifecycle chaincode install marbles.tar.gz

Set CC\_PACKAGE\_ID to the value returned by install step, e.g.:

   CC\_PACKAGE\_ID=marbles\_1:f7ff247d03e736ac5bbed767fae3af132d7bbaf2138ff0b4139ab5eea2edf61e

Approve chaincode definition on channel for SampleOrg:

   peer lifecycle chaincode approveformyorg -o 127.0.0.1:7050 --channelID mychannel --name marbles --version 1 --package-id $CC\_PACKAGE\_ID --sequence 1

Commit chaincode definition to channel:

   peer lifecycle chaincode commit -o 127.0.0.1:7050 --channelID mychannel --name marbles --version 1 --sequence 1

Invoke chaincode to create a marble:

   peer chaincode invoke -o 127.0.0.1:7050 -C mychannel -n marbles -c '{"Args":\["initMarble","marble1","blue","35","tom"]}' --waitForEvent

Transfer marble:

   peer chaincode invoke -o 127.0.0.1:7050 -C mychannel -n marbles -c '{"Args":\["transferMarble","marble1","jerry"]}' --waitForEvent

Query marble:

   peer chaincode query -C mychannel -n marbles -c '{"Args":\["readMarble","marble1"]}'

**Cleanup data, chaincode containers and images**

rm -rf /var/hyperledger/production/

rm marbles.tar.gz  
rm mychannel.*  
rm sampleconfig/genesisblock

docker rm -f $(docker ps -aq)

docker rmi -f $(docker images -q --filter=reference='\*dev\*')

**The CLI commands can be scripted or copy/pasted to expedite execution:**

configtxgen -channelID mychannel -outputCreateChannelTx mychannel.tx -profile SampleSingleMSPChannel  
peer channel create -c mychannel -o 127.0.0.1:7050 -f mychannel.tx  
peer channel join -b mychannel.block  
peer lifecycle chaincode package marbles.tar.gz --path [github.com/hyperledger/fabric/integration/chaincode/marbles/cmd](http://github.com/hyperledger/fabric/integration/chaincode/marbles/cmd) --lang golang --label marbles\_1  
peer lifecycle chaincode install marbles.tar.gz  
CC\_PACKAGE\_ID=marbles\_1:274e1e4a1110e74e95973ceb7d0d5fb02347d07d7b70d43c66ea6e8b27f5fc63  
peer lifecycle chaincode approveformyorg -o 127.0.0.1:7050 --channelID mychannel --name marbles --version 1 --package-id $CC\_PACKAGE\_ID --sequence 1  
peer lifecycle chaincode commit -o 127.0.0.1:7050 --channelID mychannel --name marbles --version 1 --sequence 1  
peer chaincode invoke -o 127.0.0.1:7050 -C mychannel -n marbles -c '{"Args":\["initMarble","marble1","blue","35","tom"]}' --waitForEvent  
peer chaincode invoke -o 127.0.0.1:7050 -C mychannel -n marbles -c '{"Args":\["transferMarble","marble1","jerry"]}' --waitForEvent  
peer chaincode query -C mychannel -n marbles -c '{"Args":\["readMarble","marble1"]}'

**For legacy chaincode, replace the package/install/approve/commit chaincode with the following:**

peer chaincode install -n marbles -p [github.com/hyperledger/fabric/integration/chaincode/marbles/cmd](http://github.com/hyperledger/fabric/integration/chaincode/marbles/cmd) -v 1  
peer chaincode instantiate -C mychannel -n marbles -c '{"Args":\["init"]}' -v 1 -o 127.0.0.1:7050

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
