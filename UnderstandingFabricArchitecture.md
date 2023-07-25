# Architecture
Making notes from the docs - https://hyperledger-fabric.readthedocs.io/en/release-2.5
## Basics of Hyperledger Fabric
* A private and permissioned blockchain, which has a ledger, uses smart contracts, and is a system by which participants manage their transactions.
* The members of a Hyperledger Fabric network enroll through a trusted Membership Service Provider (MSP).
* Ledger data can be stored in multiple formats, consensus mechanisms can be swapped in and out, and different MSPs are supported.
* Allows us to  create channels, allowing a group of participants to create a separate ledger of transactions. If two participants form a channel, then those participants — and no others — have copies of the ledger for that channel.
* Shared Ledger : Fabric has a ledger subsystem comprising two components: the world state and the transaction log. Each participant has a copy of the ledger to every Hyperledger Fabric network they belong to.  
  * World State : The database storing the state of the ledger at a given point in time. The data store is replaceable, the default being a LevelDB key-value store database
  * Transaction Log : Records all transactions which have resulted in the current value of the world state
  * The ledger is a combination of the world state database and the transaction log history.
* Smart Contracts :  
  * Fabric smart contracts are written in chaincode, invoked by an application external to the blockchain when that application needs to interact with the ledger
  * In most cases, chaincode interacts only with the database component of the ledger, the world state (querying it, for example), and not the transaction log.
  * Currently, Chaincode can be implemented in  Go, Node.js, and Java.
  * Privacy : Fabric supports networks where privacy (using channels) is a key operational requirement as well as networks that are comparatively open.
  * Consensus : Transactions must be written to the ledger in the order in which they occur, even though they might be between different sets of participants within the network. We need:
      1. The order of transactions must be established 
      2. A method for rejecting bad transactions that have been inserted into the ledger in error 
      * There are many ways to achieve it, each with different trade-offs 
      * For example, PBFT (Practical Byzantine Fault Tolerance) can provide a mechanism for file replicas to communicate with each other to keep each copy consistent, even in the event of corruption. Alternatively, in Bitcoin, ordering happens through a process called mining where competing computers race to solve a cryptographic puzzle which defines the order that all processes subsequently build upon.
      * Fabric has been designed to allow network starters to choose a consensus mechanism



