# Learning Fabric

* Build fabric for contributing: https://hyperledger-fabric.readthedocs.io/en/latest/dev-setup/devenv.html

### 1. Installation

Prereqs : https://hyperledger-fabric.readthedocs.io/en/release-2.5/prereqs.html

#### i. Install Fabric and samples : 
https://hyperledger-fabric.readthedocs.io/en/release-2.5/install.html

Get install script: curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh

./install-fabric.sh -h

Pull the Docker containers and clone the samples repo, run one of these commands for example:
./install-fabric.sh docker samples binary

Now we've completed installing Fabric samples, Docker images, and binaries to our system.

#### ii. Contract and Application APIs (will check these later)
https://hyperledger-fabric.readthedocs.io/en/release-2.5/sdk_chaincode.html

### 2. Running Fabric

#### i. Using the Fabric test network
https://hyperledger-fabric.readthedocs.io/en/release-2.5/test_network.html

* Bring up the test network
cd fabric-samples/test-network

./network.sh -h 

./network.sh up : Bring up Fabric orderer and 2 peer nodes. No channel is created

./network.sh createChannel


./network.sh deployCC -ccn basic -ccp ../asset-transfer-basic/chaincode-go -ccl go

asset transfer.go - check out

config fabric-samples/config