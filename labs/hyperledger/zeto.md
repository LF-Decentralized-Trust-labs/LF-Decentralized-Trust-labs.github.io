---
layout: default
title: Zeto
parent: Hyperledger Labs
grand_parent: Active Labs
---

# Lab Name

[Zeto](https://github.com/hyperledger-labs/zeto)

# Short Description

Zeto is a UTXO based privacy-preserving token toolkit for EVM using Zero Knowledge Proofs.

# Scope of Lab

This project hosts the multiple patterns to implement privacy preserving tokens on EVM. The patterns all share the same basic architectural concepts:

- **Transaction model**: the UTXO model is adopted instead of the account model, for better support of parallel processing. Due to the necessity of maintaining private states offchain in order to achieve privacy, the client must continuously keep their private states in sync with the smart contract. Using an account model makes it more difficult to achieve this because incoming transfers from other parties would invalidate an account's state, making the account owner unable to spend from its account unless the private state has been sync'ed again. Solutions to this issue, often referred to as front-running, typically involve a spending window with a pending queue, which result in limited parallel processing of transactions from the same spending account. With a UTXO model, each state is independent of the others, so parallel processing is better achieved.
- **Commitments**: each UTXO is tracked by the smart contract as a hash, or commitment, of the following components: value, salt and owner public key
- **Finality**: each transaction's validity is verified by the smart contract before allowing the proposed input UTXOs to be nullified and the output UTXOs to come into existence. In other words, this is not an optimistic design and as such does not rely on a multi-day challenge period before a transaction is finalized. Every transaction is immediately finalized once it's mined into a block.

# Initial Committers

- [Andrew Richardson](https://github.com/awrichar)
- [Enrique Lacal](https://github.com/EnriqueL8)
- [Jim Zhang](https://github.com/jimthematrix)

# Sponsor

[Jim Zhang](https://github.com/jimthematrix), member of the Hyperledger Technical Oversight Committee

# Pre-existing repositories

- https://github.com/kaleido-io/zeto
