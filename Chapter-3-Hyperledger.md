# Chapter 3. Hyperledger: Distributed Ledger Frameworks and Domain Specific Blockchains

## 3.1 - Components of Hyperledger frameworks
    - Append only distributed ledger
    - Consensus algorithms for changes in the ledger
    - Privacy of the transactions through permissioned access
    - Smartcontracts to process transactions process

![Component](https://courses.edx.org/assets/courseware/v1/0747265232da64643d21679294cbbe19/asset-v1:LinuxFoundationX+LFS171x+3T2020+type@asset+block/Components_of_blockchain.jpg)

![Hyperledger DLT - Frameworks, Libraries, Tools](https://www.hyperledger.org/wp-content/uploads/2020/05/HL_Greenhouse_Current.svg)

## 3.2 - Hyperledger BESU

### What:

- Open source **ETH client**, Apache 2.0 License, written in Java.
- Can run on ETH Networks OR on private permissionned network
- Sponsor & main maintainer: PegaSys

### Consensus:

- **PoW** : through Ethash  
  - Hash function that belons to the Keccak family, it's the same family as SHA-3
  - Ethash is Asic resistant
  - Use 1gb dataset known as DAG (Directed acylic graph) and 16mb for light clients, regenerated every 30.000 blocks known as epoch.
- **PoA** (with Clique (testnets) and IBFT 2.0)

### Usage: 

-  Consortium environment due to comprehensive permissioning schemes

### Features:

- Implements EEA Specs
- EVM Machine, allows deployment and execution of smart contracts via transactions with ETH blockchain
Uses a RocksDB key-value database (high performance db) to persist chain data locally
- P2P network
- Provides user-facing APIs
- Allows you to monitor node and networks performance
- Ability to keep transactions private between involved parties
- Allow permissionning

### Appendix : 

 ![HL BESU](https://lh4.googleusercontent.com/mxQGM4M12WqO4bC3bh_NcGLkPgQx_6jNdv3NLo-UElZd3rdvCxokjxsPrk-vxo4k-kvPM8JmXwfpDPfa3TtKbEQnx8a_jTVRP3UWkCxBOwUyAqIzUWuMSCMnlrcLSSqqZ6KAzihJ)

## 3.3 - Hyperledger Burrow

### What:

- Modular blockchain framework,  Apache 2.0 License
- Permissionned Solidity smart contract interpreter
- Permissionned EVM
- Follow partly EVM specifications
- Complete single-binary blockchain distribution focussed on simplicity, speed, and developer ergonomics. 
- Supports both EVM and WASM based smart contracts
- 2012
- Sponsor & main maintainer: Intel

### Consensus:

-  BFT consensus via the Tendermint algorithm (a blockchain consensus engine (Tendermint) and a Application BlockChain Interface (ABCI) which enables the transactions to be processed in any programming language

### Usage: 

-  Optmized for sharing processes accross organizations
-  We can use  Solidity contracts within Hyperledger through the Burrow Framwork

### Features:

- API Gateway for systems integration and user interfaces
- Smart Contract Application engine facilitates integration of complex business logic (maintaining the networking stack between the nodes and ordering transactions)
- Permissioned Ethereum Virtual Machine 
- Application Binary Interface (ABI) encoding of SC, - transactions must be formulated in a binary format, which is processed by the blockchain node.
- ABCI for consensus engine

### Appendix:

![Deploy ETH contracts to HL Burrow](https://myhsts.org/img/recipes_tutorials/15/hyperledger-burrow-and-ethereum-smart-contracts.jpg)

## 3.4 - Hyperledger Fabric

### What:

- Allow confidential transations through differents channels running within the network and division of labor that characterize the diffferents nodes within the network.
- High-performance, secure, permissioned blockchain network
- Features powerful container technology to host any mainstream language for smart contracts development
- Code written in Go, chaincode written in Go, Javascript, or Java, SDKs written in Node.js, Java, Go, REST and Python.
- Sponsor & main maintainers: IBM, Digital Assets Holdings, Blockstream's libconsensus
- 2017

### Consensus:

-  Plug and play : Consensus
-  Plug and play : Memberships

### Usage: 

-  Modularity and versatility for a broad set of industry use cases.
-  Fabric offers a modular, scalable and secure platform that supports private transactions and confidential contracts.
-  Fabric helps members manage confidential obligations to each other without first passing it through a central authority.
  -  Solutions developed with Fabric to be adapted for any industry.

### Features:

- Plug-and-play components, such as consensus, privacy, and membership services.
- Enable Networks of Networks

### Model:

![Ici](https://blockgeeks.com/wp-content/uploads/2017/05/Hyperledger-Blockchain-Elli-Androulaki-fabric-model.jpg)


## 3.5 - Hyperledger Indy

### What:

- Distributed ID - Trust & Privacy (user validate)**
- Solution for Digital Crendtials
- It allows to have a route of trust to manage the keys schemas, proofs, and other information 
- Distributed ledger that provides tools, libraries,and reusable components for creating and using independent **decentralized identities**.
- Represents the idea of Self-sovereign identity (multiple logins, passwords)
- DID interoperates accross domains, applications, organizational silos.
- User control the ID not companies
- Provides strong privacy guarantees, because not stored but exchanged over P2P encrypted connections through Unique ID (masked) for each relationships avoiding leaks.
- Make sure parties knows with who they are doing business.
- Initiatied by Sovrin Foundation 2017

### Consensus:

-  RFBT
-  Cryptography : ZKP

### Usage: 

-  It allows individuals to manage and control their digital identities. Rather than having businesses store huge amounts of personal data of individuals, Hyperledger Indy allows businesses to store pointers to identity. Once the company verifies the other party's identity, it throws it away.
- Identity is a toxic asset that could present a liability to organizations
- Public Utility solution for Id related,  let users authenticate based on the attributes that they're willing to store and share themselves,
- reducing the amount of liability contained within a business
- GDPR Compliant
  
### Features:

- Provides tools, libraries, and reusable components for providing digital identities rooted on blockchains or other distributed ledgers so that they are interoperable across administrative domains, applications, and any other silo.

### Breach Level Index :

![Breach Level Index website.](https://courses.edx.org/assets/courseware/v1/a7fbe5fb8ab08e8db000c4c1374d7476/asset-v1:LinuxFoundationX+LFS171x+3T2020+type@asset+block/Screen_Shot_2019-06-12_at_1.37.09_PM.png)

### Privacy By Design :

![Privacy By Design](https://termsfeed.com/blog/wp-content/uploads/2016/11/privacy-by-design-foundation-principles-circle.jpg)

### Benefits :

![](https://blockchainsimplified.com/blog/a-kickstart-to-hyperledger-indy/hyperledger-indy-benefits.jpg)

### Architecture: 

![](https://blockchainsimplified.com/blog/a-kickstart-to-hyperledger-indy/hyperledger-indy-architecture.jpg)

### Uses cases: 

![](https://blockchainsimplified.com/blog/a-kickstart-to-hyperledger-indy/hyperledger-indy-applications.jpg)

## 3.6 - Hyperledger Iroha

### What:
 
 - Permissionned
 - **Mobile Application focus with client libraries for Android and iOS**, making it distinct from other Hyperledger frameworks.
 - Easy integration, same xp as on the web
 - 2016 contributed by : Soramitsu, Hitachi, NTT Data, and Colu

### Consensus:

- FBFT with no mining, ideal for businesses that require verifiable data consistency at low cost with YAC

### Usage: 
- simple and easy management of digital assets.
- it can be used to manage digital assets, identity and serialized data, and can be useful for applications such as interbank settlement, central bank digital currencies, payment systems, national IDs, and logistics, among others.

### Features:
- Iroha's **built-in smart contracts, called commands, allow developers to incorporate blockchain into their business processes.**
- Simple deployment and maintenance
- Variety of libraries for developers
- Role-based access control
- Modular design, driven by command-query separation principle
- Ready-to-use set of commands and queries
- Multi-signature transactions
- Uses a high-performance Byzantine fault-tolerant consensus algorithm called YAC.

### Model:

![Ici](https://miro.medium.com/max/4318/1*jZAnCuIoG32WbdZ2hSDY5w.jpeg)

## 3.7 - Hyperledger SawTooth

### What:
-   Permissionned and permissionless support
-   EVM transaction family (seth)
-   Uses single node type -> Simple deployment.  
    - **On chain governance** (**CAO** != DAO)
    -  Participants can easely add policies and agree on configuration changes using Sawtooth TX,  
    -   also **change consensus type on the fly** (kind of a DAO)
- Development kits covers lot of != languages
- We can deploy : Java, Solidity, Webassembly contracts
- **Can integrate with existing Database**, and keep value/pairs sync with the network.
- Initial contributor : Intel, 2016
- Clearly separate the core system from the application domain
- Designed for **versatility**
  
### Consensus:

- On demand (start with Raft, then harden with PBFT, or PoE)
- Can utilize various consensus algorithms based on the size of the network (PoET SGX, Raft, etc.

### Usage: 

- Healthcare
- Finances
- Supplychain

### Features:

- Uses pluggable consensus algorithms, which allows consensus to be changed by transaction on the fly 
- Smart contracts can be written in almost any language
- Parallel transaction execution for added throughput, while at the same time preventing double spending
- Ethereum contract support via Hyperledger Burrow integration
- No central authority or implementation. This increases security as there is no centralized service that could leak transaction patterns or any other confidential information
- Supports creating and broadcasting events.

### Topology:

![Hyperledger Sawtooth Topology](https://www.hyperledger.org/wp-content/uploads/2018/09/HL_Whitepaper_Metrics_Graphics-01.png)

## 3.8 - Domain Specific - Hyperledger Grid

### What:

- Domain-specific business blockchain technology Stack including component, ecosystem of technologies, frameworks, and libraries that work together
- Intends to provide 
  - Reference implementations of supply chain-centric data types, data models, and smart contract based business logic – all anchored on existing, open standards and industry best practices. 
  - Provide authentic, practical ways to combine components from the Hyperledger Stack into a single, effective business solution.
- Initiators : Cargill, Intel, Bitwise, License Apache 2.0

### Integrated standards for supplychain:

- **GS1Standards** : (structure around static and dynamic data and increase visibility, standardization, consistency, credibility, neutrality and interoperability)
  - **Global Trade Item Number (GTIN)** - it's a UID composed of Company ID + Product Id - Key for implementation 
  - **Global Location Numbers (GLN)** - UID of organisations id and location in the supply chain.
  - **GS1 barcodes** - Provide product specific info, and allow real time view of where products have been and where they are heading to.
  - **Electronic Product Code Information Services (EPCIS)**  - similar than a API.

## Appendix:

![Hyperledger Grid components](https://www.altoros.com/blog/wp-content/uploads/2019/07/Hyperledger-Grid-blockchain-framework-supply-chain-stack-architecture.png)