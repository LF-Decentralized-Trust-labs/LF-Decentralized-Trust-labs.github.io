---
layout: default
title: YUI
parent: Hyperledger Labs
grand_parent: Active Labs
---
# Lab Name
[YUI](https://github.com/hyperledger-labs/yui-relayer)

* [yui-corda-ibc](https://github.com/hyperledger-labs/yui-corda-ibc)
* [yui-fabric-ibc](https://github.com/hyperledger-labs/yui-fabric-ibc)
* [yui-ibc-solidity](https://github.com/hyperledger-labs/yui-ibc-solidity)
* [yui-docs](https://github.com/hyperledger-labs/yui-docs)

* Note: Japanese word to represent knot, join and connect

# Short Description
YUI is a lab to achieve interoperability between multiple heterogeneous ledgers. YUI provides modules and middleware for cross-chain communication as well as modules and tools for cross-chain application development, including an explorer to track status and events for cross-chain environments.

For cross-chain communication, the design of YUI is based on Inter Blockchain Communication (IBC) protocol by Cosmos project, with extensions to support various Hyperledger projects.

Modules for cross-chain application development includes one that implements a protocol for atomic operations between ledgers, such as atomic swap of tokens.


# Scope of Lab
## Design Principles
### Cross-authentication
By relying on the on-chain verification of the other chain’s state, cross-chain communication can be achieved without any safety concern due to the behavior of off-chain actors

This allows cross-chain message relaying not only to the trusted and privileged actors, but also to any actor that satisfies the ACL of the permissioned chain.

In addition, we aim to apply the method not only to the permissioned chains, but to the public chains as well.

### Provide a unified communication method independent from a specific blockchain/DLT implementation.
This enables application developers to develop chain agnostic protocols.

### Support arbitrary data transfer and computation
Developers can design and implement the specific protocol for its cross-chain application, not limited to token transfer use case.

### Avoid adding components that introduce additional trust (apart from individual blockchains)
Introducing such components may decrease the level of security of a system as it would be bounded by the lowest component in the system.

Also, introducing new (off-chain) components with high fault tolerance will also lead to increased operational costs

### Do not introduce a new layer
Each actor (of ledgers) has only to interact with a respective ledger of its interest to complete a cross-chain operation unless the application has additional requirements.

## Use cases
Cross-chain smart contracts for arbitrary data and procedures, not limited to atomic swap of tokens.
- Cross-chain token transfer
- Cross-chain Atomic swap
  - Example includes delivery versus payment settlement
- Cross-chain atomic execution of arbitrary procedures

## Current status and future plan
We have already developed modules for Hyperledger Fabric, Hyperledger Besu, and Corda. We plan to apply these modules for practical applications as well as to expand support for other blockchains.
- At first, we are focusing on permissioned blockchain environment

Aim to enable developers in Hyperledger community to introduce interoperability in their systems and develop cross-chain applications without too many changes and increase the complexity

## Components
Client (on-chain) module and Relayer to support various ledgers in align with the design principles
- Client module should be designed to support each underlying ledger

Various software to support the development of cross-chain systems
- Modules to support the development of cross-chain contracts
  - Implementation of an atomic commit protocol for cross-chain atomic operation
  - Implementation of authentication for cross-chain contracts
- System to support the coordination of cross-chain contract and applications
  - Explorer to track the cross-chain status


# Initial Committers
- [Jun Kimura](https://github.com/bluele)
- [Ryo Sato](https://github.com/3100)
- [YOSHIDA Masanori](https://github.com/siburu)


# Pre-existing repository
- https://github.com/datachainlab/fabric-ibc
- https://github.com/datachainlab/ibc-solidity
- https://github.com/datachainlab/corda-ibc

<!--Contributors should be listed in maintainers.md -->
