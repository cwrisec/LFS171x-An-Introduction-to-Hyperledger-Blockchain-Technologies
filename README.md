# Chapter 1. See written notes in sub-folder.
# Chapter 2. See written notes in sub-folder.

## Benefits of blockchain 

Blockchains are a new infrastructure for securely validating and automating transactions across complex networks, with the potential to dramatically reduce the backend costs of modern financial systems and expedite the delivery of e-government services. 

They have four main benefits:

- **Automation**: Blockchain-based smart contracts automate business logic across multiple parties, reducing settlement time and costs.
- **Security**: Blockchains use advanced cryptography to guarantee tamper-proof data coordination and storage across large networks of counterparties.
- **Reliability**: A blockchain’s decentralized architecture prevents single points of failure and ensures the network is highly available.
- **Transparency**: A blockchain’s digital, immutable ledger provides auditability and accountability around business transactions and the origin of data.

![Bridging the Governance Gap: Interoperability for blockchain and legacy systems](https://assets.weforum.org/editor/responsive_large_webp_IoDx8JwqCUWC5PsUh8CajPme9yQkXWq-y5zwE8_ICdw.webp)

(WEF, Sergey Nazarov - 2020 - https://www.weforum.org/agenda/2020/12/the-missing-link-between-blockchain-and-existing-systems/)

(77 DLT Uses cases - Chainlink - 2020 - https://blog.chain.link/44-ways-to-enhance-your-smart-contract-with-chainlink/ )

# Chapter 3. Hyperledger: **Distributed Ledger Frameworks and Domain Specific Blockchains**

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

- Enterprisegrade, permissioned, open source, vendor neutral, modular, plug-and-play
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

- Distributed ID - Trust & Privacy (user validate)
- **Business blockchain framework for supporting independent identity on distributed ledgers**
- Solution for Digital Crendtials
- It allows to have a route of trust to manage the keys schemas, proofs, and other information 
- **Distributed ledger that provides tools, libraries,and reusable components for creating and using independent decentralized identities**.
- Represents the idea of Self-sovereign identity (multiple logins, passwords)
- **DID interoperates accross domains, applications, organizational silos.**
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
  - Focus on IoT implementations. 
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

- On demand (start with Raft, then harden with PBFT, or PoEt)
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

# Chapter 4. Hyperledger: **Tools**

We will look at the Hyperledger tools, which are auxiliary softwares used for things like deploying and maintaining blockchains, examining the data on the ledgers, as well as tools to design, prototype, and extend blockchain networks. 

## 4.1 Hyperledger Avalon

### What:
- Implementation of the Offchain Trusted Compute Specification pushed by EEA
- Enable the secure movement of blockchain processing off the main chain to dedicated computing resources.
- Link with : SGX, Trustet enclaves encryption
- 2019 Sponsors: Intel, iExec Blockchain Tech, Alibaba Cloud, Baidu, BGI, Chainlink, Consensys, EEA, Espeo, IBM, Kaleido, Microsoft, Banco Santander, Wipro, Oracle, and Monax

### Allow :
- Enables developers to accelerate throughput and improve data privacy
- The initial implementation of Hyperledger Avalon uses Intel Software Guard Extensions (SGX)
- Uses the Off-Chain Trusted Compute Specification as a starting point to apply a consistent and compatible approach to all supported blockchains. 

## 4.2 Hyperledger Cactus

-  Blockchain Integration Framework
-  Aims to provide decentralized, secure and adaptable integration between blockchain networks
- 2020 Sponsors: Fujitsu, Accenture
- Plug-in based collaborative development
- 
### Summary:

![Hyperledger Cactus - what's it ?](https://101blockchains.com/wp-content/uploads/2020/05/Hyperledger-cactus.png)

## 4.3 Hyperledger Caliper

### What?
- **Benchmark tool** that measures the performance of various blockchain systems by using a set of predefined cases.
- Normalized rules
- Reporting (ressources utilization, tx, latency, TPS)
- Sponsor : 2018 Huawei, Hyperchain, Oracle, Bitwise, Soramitsu, IBM and the Budapest University of Technology and Economics

### Characteristics
- Unified blockchain benchmark framework
- Commonly accepted definition of performance indicators
- Commonly accepted benchmark cases. 

### Supports

- Hyperledger Besu, Hyperledger Burrow, Ethereum, Hyperledger Fabric, FISCO BCOS, Hyperledger Iroha and Hyperledger Sawtooth.

![](https://hyperledger.github.io/caliper/assets/img/report.png)

## 4.4 Hyperledger Cello

### What?

- Cello aims to bring the on-demand 'as-a-service' deployment model to the blockchain ecosystem
- Blockchain orchestrator : K8S, Docker....
- Operators can create and manage such blockchains through a dashboard
- Sponsors: IBM, with sponsors from Soramitsu, Huawei, and Intel

### Features:

- **Deploy, manage and operate blockchains efficiently and automatically**
- Support customized blockchain requests (support for Hyperledger Fabric)
- Support various infrastructures (baremetal, VM platforms, container cloud)
- Support advanced operational analytics for system status and ledger behavior

 ![](https://hyperledger.github.io/cello/images/scenario.png)

## 4.5 Hyperledger **Explorer**

### What?

- Open source tool for **visualizing blockchain operations**
- Sponsors : DTCC, Intel, and IBM in 2016.
- Hyperledger Explorer supports Hyperledger Fabric and Hyperledger Iroha.

### Features: 

- Blocks
- Transactions and associated data
- Network information (name, status, list of nodes)
- Smart contracts (chain codes and transaction families)
- Other relevant information stored in the ledge

![](https://miro.medium.com/max/3638/1*9wQ_cMzUYlu0-tIW7ZLvtA.png)

# Chapter 5. Hyperledger: **Libraries**

In this chapter we will take a look at the Hyperledger libraries for **enterprise-grade blockchain deployments.**

## 5.1 Hyperledger Aries

### What:

- provides a **shared**, **reusable**, and **interoperable tool kit** designed for initiatives and **solutions focused on creating, transmitting and storing** **verifiable digital credentials**
- Aims to change the client layed in HL Indy to be interoperable with others ID projects
- Link with the DLT Framework : Hypeledger Indy
- Link with library : HL Ursa (for cryptography) 
- Initiators (2019) : Sovrin Foundation, the Government of British Columbia, and other Indy community developers
- Privacy containers for personnals folders files

![](https://www.evernym.com/wp-content/uploads/2019/05/hyperledger-aries-indy-architecture.jpg) 

## 5.2 Hyperledger Quilt

### What:

- Provide **Interoperability** between ledgers - **Inter Ledger Protocol (ILP)**
- **Java implementation of the Interledger protocol (ILP) which is a payement protocol**
- Provide libraries and reference implementations of the core interledger components.
- With ILP, money can be packetized, routed, and delivered over communication networks with automatic routing and a series of secure, multi-hop payments.
- **connecting bank accounts to digital wallets and everything in between**
- 2017 Initiated by NTT Data and Ripple 

### Goals of Quilt 

Long term, Quilt can become a ledger interoperability solution that enables more than just payment transactions, but a means to exchange any sort of asset across the many different blockchain networks that will exist.

### Features

- Provides a set of rules for enabling ledger **interoperability with basic escrow semantics**
- Furnishes a standard for ledger-independent address and data packet formats that enable connectors to route payments
- Supplies a framework for designing higher-level use case specific protocols.

## 5.3 Hyperledger Transact

### What

- Transaction execution platforfm component / library
- Initiators: Bitwise, Cargill, Intel, IBM and Hacera in 2019 

### Features:

- Serial and parallel transaction scheduling
- Pluggable state backend
- Transaction receipts
- Events that can be generated by smart contracts
- Support for Sabre and Seth, etc.

## 5.4 Hyperledger Ursa

### What:

- Shared cryptographic library
- Initators : Fujitsu, The Linux Foundation, Sovrin Foundation, Intel, DFINITY, State Street, IBM, Sai Infratel, and Bitwise (2019)

# Chapter 6. : The Promise of Business Blockchain Technologies

  ## Finance's usage of DLT

  - **transferring assets and recording trade agreements** (stock sales, bonds, options, and cash transactions)

  Blockchain technologies are very good at **recording state transitions**

  ## Legal industry's usage of DLT

  -  record property rights and the transfer of those rights

  ## Insurance industry's usage of DLT

  - pooling funds from unaffiliated individuals

## Health industry's usage of DLT

- record and share data, such as patient health records, or pharmacy information.

## Material and product supplychain's usage of DLT

- improved resource, sourcing, and allocation.

## DLT Advantages for businesses

- **Smart contracts eliminate the middleman and add accountability** (used in various industry sectors, such as real estate, healthcare, government, music, etc.)
- **Internet of Things (IoT)-based blockchain applications**:
  -  add a higher level of security
  -  add transparency 
  (in industries like supply chain, healthcare, banking and financial services, automotive, cybersecurity, etc.). Hyperledger Fabric is at the forefront of this revolution. 
- **Identity security is a key area where enterprise blockchain technologies can make a difference**, bringing, for example
    - a much-needed reduction in identity fraud and theft claims
    - cutting the red tape of government and local administration bureaucracy
    - and more.
  
  Hyperledger Indy, Hyperledger Fabric, etc. are just a couple of technology examples successfully used in production in this area.

- **Blockchain adds data transparency and automation**
  - supply management and logistics
  - by building trust and enabling leaner, more cost-effective processes.


 ## Production usescases

- **Supply Chain** - IBM Food Trust, powered by Hyperledger Fabric,
- **Airline Industry**  - NIIT Technologies developed a new blockchain application, Chain-m, using Hyperledger Fabric.
- **Enterprise Operations Management** - JD.com, the largest retailer in China, has developed its own enterprise blockchain platform aimed at streamlining numerous operational procedures, such as tracking and tracing the movement of goods, charity donations, authenticity certification, property assessment, transaction settlements, digital copyrights, etc.Hyperledger Fabric.
- **Insurance Compliance Data** - The American Association of Insurance Services has developed openIDL (open Insurance Data Link), a system built on IBM Blockchain, thus powered by Hyperledger Fabric, which is designed to automate insurance regulatory reporting.
- **Decentralized Identities and Trusted Credentials** - In an attempt to streamline their business-oriented services, the government of British Columbia started working on a project based on Hyperledger Indy. OrgBook BC is an online directory that can be used to quickly verify if an organization is legally registered to do business in British Columbia as a corporation. This is just the first step of a larger blockchain-based initiative aimed at streamlining government services.

## Supplychain Management

**Defintion** : The oversight of funds, raw materials, components, and finished products, as they move from suppliers, to manufacturers, to wholesalers, to retailers, to consumers, within one or several companies

- Important part of enterprise resource planning (ERP)
- Supplychain + Trade Finance

**Why is blockchain useful in supplychain ?**
- Audit trail
- Eliminate the need for a trusted third party to certify raw materials, components, or finished products, as they travel through a supply chain
- Improves resource allocation.
- Although a record of the transaction is public and tied to the movement of physical items across the network, specifics such as the quantity of goods, or the identity of the parties transacting, can be done pseudo-anonymously in a blockchain. Such a granular view of movement through supply chains improves resource allocation.
  
**Challenges** :  
- Stocking the right amount of inventory over time is also known as **supply demand synchronization** 
- DLT can provide for **just-in-time lean manufacturing** and distribution
- Overstocking inventory is costly
- Inter companies settlements is difficult because no integration with the differents ERP systems - 
- Data doesn't flow well through the handshakes or interface points between systems. 
-  Transfert of ownership & Changes of status of products through their synchronization between parties
-  **Visibility is limited at the hand-off points of funds, raw materials, components, or finished products and it's intented**

**Idea developped : Integrate trade finance**
-  WTO : "up to 80 percent of global trade is supported by some sort of financing or credit insurance" (2016)
- The trade finance industry can also leverage information visible in a supply chain blockchain. trade finance manages capital required for international trade.
- An exporter needs to mitigate the risk of non-payment, while an importer wants to mitigate the supply risk. The function of trade finance is to act as a third party to remove the payment risk and the supply risk, whilst providing the exporter with accelerated receivables, and the importer with extended credit. Institutions that provide capital during these trades can leverage the information visible in a supply chain blockchain to better evaluate companies for lending.

 
![Supply chain tuna](https://courses.edx.org/assets/courseware/v1/f8b777bb4b2add9a426b97b8f2556aad/asset-v1:LinuxFoundationX+LFS171x+3T2020+type@asset+block/Supply_Chain_of_Tuna.png)

Other examples: Ibm Food with WallMart, CoffeeChain...

## Property Rights

**Definition**:

-  Division of law whereby the rights and responsibilities associated with owning an asset are established
- Rights : 
  - use
  - profit
  - exclude others
  - transfer for any assets (partly or completely)
- Reponsabilities:
  - Tax
  - Maintenance and repair costs, 
  - Payment for injuries caused by unsafe or defective conditions of the asset.

**Link with NFT and tokenization.**
**Intellectual property includes copyright, trademark, and patents alsoon chain**

  ![Property rights on the blockchain - toknization of house](https://courses.edx.org/assets/courseware/v1/7606d1ed26d6415a1dda083274cffdb4/asset-v1:LinuxFoundationX+LFS171x+3T2020+type@asset+block/PROPERTY_RIGHTS.jpg)
*Property Titles on a Blockchain via a Smart Contract*

**Why DLT in IP?**:

- minimize disputes around property rights
- record ownership rights and responsibilities.
- governments have put land registry records on blockchain
- it can provide an immutable, secure, timestamped record for the creation of intellectual propert
- A blockchain may record a hash of a document.
  - As an example, photographers could place a hash of their unique digital photographs on the blockchain. 
    - The hash of a digital photograph will be constant so long as the photograph file has not been altered
    - Blockchain can control and track the distribution of the photograph
    - Detect the introduction of counterfeit images
    - Blockchain can be used to resolve disputes as to who first introduced the image
    - -> By placing a hash of intellectual property documents on the blockchain, a party can publicly demonstrate data ownership, 
    - -> Prove the existence of certain documents at a given moment in time, without revealing the actual data. 
    - -> In addition to the hash, you may also choose to store the location of the file in the blockchain, which could be used for retrieval.

**Audience**: 

Strong brand value in particular, Such as the fashion industry and luxury good providers, are interested in more efficient ways to protect their intellectual property