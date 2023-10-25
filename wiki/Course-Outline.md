## Ultimate Go: Advanced Engineering 1.0

Learn advanced Go concepts by building a reference implementation of a blockchain in Go! The goal of this class is to share how to code complex engineering tasks required to build a blockchain technology. From the beginning, you will pair program with the instructor, walking through the design philosophies and guidelines used to engineer the code. Throughout the class, you will learn more about Go and the advanced engineering features of the language.

## Course Curriculum

### 1.0 - Introduction
Introduction to the class and all the engineering that you will learn.

- 1.1: Design Philosophy, Guidelines, What to Expect
- 1.2: Tooling to Install
- 1.3: Initial Code for the Project

### 2.0 - Practical Uses Of Blockchain Technology
An understanding of how a blockchain is a single, append-only, publicly available, transparent, and cryptographically auditable database that runs in a distributed and decentralized environment.

- 2.1: Introduction
- 2.2: Auditable/Transparent Database
- 2.3: Ownership
- 2.4: Consensus PoW
- 2.5: Consensus PoS/PoA
- 2.6: Higher Throughput

### 3.0 - Genesis
We start with the genesis package and defining the global settings for the blockchain.

- 3.1: What is Genesis
- 3.2: Configuration Options
- 3.3: Reading From Disk

### 4.0 - Digital Signature
We understand what it means to sign a piece of data digitally and write code that can support this.

- 4.1: What is a Digital Signature
- 4.2: Hashing
- 4.3: Stamping
- 4.4: Signing
- 4.5: Addressing
- 4.6: Verification

### 5.0 - Database
We understand how to structure the blockchain database, both on disk and in memory.

- 5.1: What is Inside the Blockchain Database
- 5.2: Transaction Types
- 5.3: Accounting
- 5.4: Database Management

### 6.0 - Memory Pools
We understand the importance of memory pooling and implement the mempool.

- 6.1: What is a Mempool
- 6.2: Storing Transactions
- 6.3: Transaction Selection

### 7.0 - Accepting Signed Transactions
We understand how to send and receive a signed transaction.

- 7.1: Handler function
- 7.2: Transaction Signature Verification
- 7.3: Mempool Inclusion

### 8.0 - Blocks and Cryptographic Audit Trails
We understand how to provide cryptographic audit trails into the database.

- 8.1: What is a Cryptographic Audit Trail
- 8.2: Block Types
- 8.3: Chaining
- 8.4: Merkle Tree Proofs
- 8.5: Account Database Proof

### 9.0 - Mining
We understand the concept of mining and consensus. We focus on Proof Of Work consensus but will briefly talk about Proof Of Stake as well.
 
- 9.1: What is Consensus and Mining
- 9.2: Proof Of Work Algorithm
- 9.3: Implement Mining Workflow

### 10.0 - Storage
We understand how to store mined blocks to disk and how to read these blocks on startup to recover the state of the database.

- 10.1: Storage Options
- 10.2: Writing Blocks
- 10.3: Reading and Searching Blocks

### 11.0 - Peer To Peer Networks
We understand how to implement a peer to peer network so other nodes can participate in the blockchain.

- 11.1: What is the P2P Network
- 11.2: Peer Discovery
- 11.3: Sharing Transactions
- 11.4: Sharing Blocks

### 12.0 - Proof of Authority Consensus
We introduce a new consensus model for mining blocks.
12.1: What is PoA consensus
12.2: Reviewing the basic algorithm
12.3: Adding Woker and State Support

### 13.0 - Wallets
We understand the fundamentals of wallets and build a wallet to interact with the node.

- 13.1: Chrome Plugin Basics
- 13.2: Javascript Support
- 13.3: Send Signed Transaction
