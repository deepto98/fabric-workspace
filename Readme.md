# Learning Fabric

* Build fabric for contributing: https://hyperledger-fabric.readthedocs.io/en/latest/dev-setup/devenv.html

### 1. Installation

Prereqs : https://hyperledger-fabric.readthedocs.io/en/release-2.5/prereqs.html

#### a.Install Fabric and samples : 
https://hyperledger-fabric.readthedocs.io/en/release-2.5/install.html

Get install script: curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh

./install-fabric.sh -h

Pull the Docker containers and clone the samples repo, run one of these commands for example:
./install-fabric.sh docker samples binary

Now we've completed installing Fabric samples, Docker images, and binaries to our system.

#### b. Contract and Application APIs (will check these later)
https://hyperledger-fabric.readthedocs.io/en/release-2.5/sdk_chaincode.html