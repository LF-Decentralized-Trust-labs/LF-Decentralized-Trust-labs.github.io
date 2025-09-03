---
layout: default
title: Hyperledger Fabric SmartBFT Library
parent: Hyperledger Labs
grand_parent: Active Labs
---
# Lab Name

[SmartBFT](https://github.com/hyperledger-labs/SmartBFT)

# Short Description

Hyperledger Fabric is an enterprise-grade, permissioned distributed ledger platform that offers modularity for a broad set of industry use cases. One modular component is a pluggable ordering service that establishes consensus on the order of transactions and batches them into blocks. This proposal suggests integrating the SmartBFT consensus library into Hyperledger Labs to enhance its blockchain frameworks with a robust, scalable, and resilient consensus mechanism designed for practical BFT deployment.

This lab provides a BFT consensus library based on the [BFTSmart](https://github.com/bft-smart/library) protocol written in Go. The library is tailored to the blockchain use case yet general enough to cater to various other uses. The BFT library's design and integration into Fabric address crucial aspects left unsolved in all [prior work](https://github.com/bft-smart/library), making it unfit for production use. More details in the [maling list](https://lists.hyperledger.org/g/fabric/topic/17549966) discussion. The fundamental issue was related to the integration model tailored to the design imposed by the Kafka-based ordering service. It introduced a "thin" layer into Hyperledger Fabric ordering nodes to intercommunicate with Smart-BFT consensus, where the consensus itself was rendered as an external third-party dependency.

This lab suggests a solution that provides good abstraction layers without requiring an intimate knowledge of the Hyperledger Fabric Ordering Service architecture. It allows integration with Hyperledger Fabric, enabling ordering service with BFT-based capabilities, making it a Byzantine fault-tolerant solution.



# Scope of Lab

SmartBFT is a consensus library developed as part of the SmartBFT-Go project. It offers advancements in Byzantine Fault Tolerance with an emphasis on modularity, performance, and security. Its integration can address various challenges in distributed ledger technology, especially fault tolerance and scalability.
The scope of this lab is to provide a BFT consensus library for the Hyperledger Fabric project. The library presents a design that addresses all the BFT system's concerns.

The library suggests an easy integration with the Hyperledger Fabric, though still agnostic to the Fabric's internals implementation details, suggestion interfaces that capture the special needs of a blockchain application but are fully customizable for other use cases as well.

Finally, the library was accepted into Hyperledger Fabric with [RFC-006](https://github.com/hyperledger/fabric-rfcs/blob/main/text/006-bft-based-ordering-service.md) and is now delivered within the next version of the Hyperledger Fabric 3.0. The purpose of suggesting moving the SmartBFT library into Labs is to consolidate work and governance under Hyperledger and Linux Foundation projects.

# Initial Committers

* Yacov Manevich - https://github.com/yacovm
* Hagar Meir - https://github.com/HagarMeir
* Artem Barger - https://github.com/C0rWin
* Yoav Tock - https://github.com/tock-ibm
* Fedor Partansky - https://github.com/pfi79

# Sponsor

- https://github.com/C0rWin - Artem Barger, Hyperledger Fabric maintainer
- https://github.com/yacovm - Yacov Manevich, Hyperledger TSC, Hyperledger Fabric maintainer

# Pre-existing repository

- https://github.com/SmartBFT-Go/consensus
