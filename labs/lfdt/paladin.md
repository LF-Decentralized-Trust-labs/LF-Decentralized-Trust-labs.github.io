---
layout: default
title: Paladin
parent: LFDT Labs
grand_parent: Active Labs
---

# Lab Name

[Paladin](https://github.com/lf-decentralized-trust-labs/paladin)

# Short Description

Paladin is a platform for building programmable privacy preserving tokens on EVM, with integrated client and wallet. Support for several privacy frameworks including ZKP tokens, issuer-backed tokens, and private smart contracts.

# Scope of Lab

This project hosts the entire code base for the Paladin implementation, which contains the following functionalities:

- Privacy preserving token smart contract samples
  - using Zero Knowledge Proofs, like [zeto](https://github.com/hyperledger-labs/zeto)
  - using the Notary certificates (included in this project)
  - using the multi-party flows with EVM private smart contracts (included in this project). This provides function similar to that provided by the [Tessera](https://github.com/consensys/tessera) project with additional interoperability and other enhancements
- Sidecar runtime next to a Besu node
- Secure channels of communication to other Paladins over which it can selectively disclose private data
- High performance transaction manager that coordinates transaction assembly, submission and confirmation across Paladin runtimes
- Enterprise grade key management integration
- Development, configuration, and deployment pipeline for privacy preserving smart contracts

Paladin supports token implementations that obey these basic principles:

- use the EVM base ledger as the source of truth for order and finality of transactions
- transactions from different tokens involved in a higher level flow like DvP or PvP are atomically interoperable via the base EVM ledger
- store states in the EVM base ledger in a securely masked format preserving:
  - Confidentiality: the data is protected via cryptography, and selectively disclosed on a need to know basis
  - Anonymity: the parties involved in a transaction, or set of transactions, cannot be determined without access to the confidential data

# Initial Committers

- https://github.com/awrichar
- https://github.com/Chengxuan
- https://github.com/dwertent
- https://github.com/EnriqueL8
- https://github.com/gabriel-indik
- https://github.com/hosie
- https://github.com/jimthematrix
- https://github.com/peterbroadhurst
- https://github.com/SamMayWork

# Sponsor

https://github.com/jimthematrix - Jim Zhang, member of the Hyperledger Technical Advisory Council

# Pre-existing repositories

- https://github.com/kaleido-io/paladin
