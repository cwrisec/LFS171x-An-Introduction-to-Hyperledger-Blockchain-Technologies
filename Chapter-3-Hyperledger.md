# Chapter 3. Hyperledger: Distributed Ledger Frameworks and Domain Specific Blockchains

## 3.1 - Components of Hyperledger frameworks
    - Append only distributed ledger
    - Consensus algorithms for changes in the ledger
    - Privacy of the transactions through permissioned access
    - Smartcontracts to process transactions process

![Component](https://courses.edx.org/assets/courseware/v1/0747265232da64643d21679294cbbe19/asset-v1:LinuxFoundationX+LFS171x+3T2020+type@asset+block/Components_of_blockchain.jpg)

## 3.2 - Hyperledger BESU

What:

    - Open source **ETH client**, Apache 2.0 License, written in Java.
    - Can run on ETH Networks OR on private permissionned network
    - Sponsor & main maintainer: PegaSys

Consensus:

    - **PoW** : through Ethash  
      - Hash function that belons to the Keccak family, it's the same family as SHA-3
      - Ethash is Asic resistant
      - Use 1gb dataset known as DAG (Directed acylic graph) and 16mb for light clients, regenerated every 30.000 blocks known as epoch.
      - 
    - **PoA** (with Clique (testnets) and IBFT 2.0)

Usage: 

    -  Consortium environment due to comprehensive permissioning schemes

Features:

    - Implements EEA Specs.
    - **EVM Machine, allows deployment and execution of smart contracts via transactions with ETH blockchain.**
    - Uses a RocksDB key-value database (high performance db) to persist chain data locally
    - P2P network
    - Provides user-facing APIs
    - Allows you to monitor node and networks performance
    - **Ability to keep transactions private between involved parties**
    - Allow permissionning

Appendix : 

 ![HL BESU](https://lh4.googleusercontent.com/mxQGM4M12WqO4bC3bh_NcGLkPgQx_6jNdv3NLo-UElZd3rdvCxokjxsPrk-vxo4k-kvPM8JmXwfpDPfa3TtKbEQnx8a_jTVRP3UWkCxBOwUyAqIzUWuMSCMnlrcLSSqqZ6KAzihJ)

## 3.3 - Hyperledger Burrow

What:

    - Modular blockchain framework,  Apache 2.0 License
    - Permissionned Solidity smart contract interpreter
    - Permissionned EVM
    - Follow partly EVM specifications
    - Complete single-binary blockchain distribution focussed on simplicity, speed, and developer ergonomics. 
    - Supports both EVM and WASM based smart contracts
    - 2012
    - Sponsor & main maintainer: Intel


Consensus:

    -  BFT consensus via the Tendermint algorithm (a blockchain consensus engine (Tendermint) and a Application BlockChain Interface (ABCI) which enables the transactions to be processed in any programming language

Usage: 

    -  Optmized for sharing processes accross organizations
    -  We can use  Solidity contracts within Hyperledger through the Burrow Framwork

Features:

    - **API Gateway** for systems integration and user interfaces
    - **Smart Contract Application** engine facilitates integration of complex business logic (maintaining the networking stack between the nodes and ordering transactions)
    - **Permissioned Ethereum Virtual Machine **
    - **Application Binary Interface (ABI) encoding of SC,** - ransactions must be formulated in a binary format, which is processed by the blockchain node.
    - **ABCI for consensus engine

Appendix:

![Deploy ETH contracts to HL Burrow](https://myhsts.org/img/recipes_tutorials/15/hyperledger-burrow-and-ethereum-smart-contracts.jpg)

## 3.4 - Hyperledger Fabric

What:

    - High-performance, secure, permissioned blockchain network
    - Features powerful container technology to host any mainstream language for smart contracts development
    - Code written in Go, chaincode written in Go, Javascript, or Java, SDKs written in Node.js, Java, Go, REST and Python.
    - Sponsor & main maintainers: IBM, Digital Assets Holdings, Blockstream's libconsensus
    - 2017
    - Allow confidential transations through differents channels running within the network and division of labor that characterize the diffferents nodes within the network.


Consensus:

    -  Plug and play : Consensus
    -  Plug and play : Memberships


Usage: 

    -  Modularity and versatility for a broad set of industry use cases.
    -  Fabric offers a modular, scalable and secure platform that supports private transactions and confidential contracts.
    -  Fabric helps members manage confidential obligations to each other without first passing it through a central authority.
    -  Solutions developed with Fabric to be adapted for any industry,
    -  
Features:

    - **plug-and-play components**, such as consensus, privacy, and membership services.
    - Enable **Networks of Networks**

Model:

![Ici](https://blockgeeks.com/wp-content/uploads/2017/05/Hyperledger-Blockchain-Elli-Androulaki-fabric-model.jpg)


## 3.4 - Hyperledger Fabric

What:

    - High-performance, secure, permissioned blockchain network
    - Features powerful container technology to host any mainstream language for smart contracts development
    - Code written in Go, chaincode written in Go, Javascript, or Java, SDKs written in Node.js, Java, Go, REST and Python.
    - Sponsor & main maintainers: IBM, Digital Assets Holdings, Blockstream's libconsensus
    - 2017
    - Allow confidential transations through differents channels running within the network and division of labor that characterize the diffferents nodes within the network.


Consensus:

    -  Plug and play : Consensus
    -  Plug and play : Memberships


Usage: 

    -  Modularity and versatility for a broad set of industry use cases.
    -  Fabric offers a modular, scalable and secure platform that supports private transactions and confidential contracts.
    -  Fabric helps members manage confidential obligations to each other without first passing it through a central authority.
    -  Solutions developed with Fabric to be adapted for any industry,
    -  
Features:

    - **plug-and-play components**, such as consensus, privacy, and membership services.
    - Enable **Networks of Networks**

Model:

![Ici](https://blockgeeks.com/wp-content/uploads/2017/05/Hyperledger-Blockchain-Elli-Androulaki-fabric-model.jpg)