## Description

The [blockchain](https://github.com/dmitryovchinnikov/blockchain) project is a reference implementation of a blockchain written in Go. It takes ideas from both Bitcoin and Ethereum to provide a fully functioning blockchain that can handle basic accounting transactions. This project does not implement or provide any virtual machine for smart contract support.

This project should not be considered a production useable project. With that being said, the code has been written as if this project were going to be used in production. The full set of design philosophies, guidelines, and idioms have been respected.

This class tries to teach to the core design philosophies for blockchain technology. It's important to understand that each publically available blockchain technology implements things differently for the concerns and tradeoffs that are important to them. The THE blockchain has blended these implementations together to provide a reference implementation that hopefully can be understood by a majority of people.

## Features

This project contains the following features:

* Ground up architecture and design for blockchain.
* Proof of Work and Proof of Authority consensus model.
* Account balance management.
* Mempool and transaction selection algorithms.
* Peer to peer networking over HTTP.
* Fraud detection using a mix of Bitcoin and Ethereum block design.
* Chrome based wallet with signature verification.

## Services

The following services are used within the scope of the project.

### Tooling

* **logfmt**  : Converts the structured logs into human readable logging.

### Services

* **node**    : Blockchain node that runs as a service.
* **viewer**  : Web applications that provides a visual view of different running blockchain nodes.

### Wallet

* **chrome**  : Chrome based wallet that can interact with the node.
* **cli**     : Simple CLI based tool for interacting with the node.
