---
layout: default
title: Perun
parent: Hyperledger Labs
grand_parent: Approved Labs
---
# Lab Name
[Perun](https://github.com/hyperledger-labs/go-perun)

* [perun-eth-backend](https://github.com/hyperledger-labs/perun-eth-backend)
* [perun-node](https://github.com/hyperledger-labs/perun-node)
* [perun-rs](https://github.com/hyperledger-labs/perun-rs)
* [perun-credential-payment](https://github.com/hyperledger-labs/perun-credential-payment)
* [perun-eth-contracts](https://github.com/hyperledger-labs/perun-eth-contracts)
* [perun-cosmwasm-contract](https://github.com/hyperledger-labs/perun-cosmwasm-contract)
* [perun-doc](https://github.com/hyperledger-labs/perun-doc)
* [perun-cosmwasm-backend](https://github.com/hyperledger-labs/perun-cosmwasm-backend)
* [perun-proposals](https://github.com/hyperledger-labs/perun-proposals)

# Short Description

Blockchain-agnostic State Channels framework.

# Scope of Lab



The Perun framework is a suite of implementations around the [Perun state
channel protocols](https://perun.network/) ([introduction
paper](https://perun.network/wp-content/uploads/Perun2.0.pdf)). The Perun protocols provide
payment and general state channel functionality to all existing blockchains
that feature smart contracts. As a blockchain scalability solution, payment
and state channels reduce transaction costs and increase the system throughput
by executing incremental transactions off-chain. The Perun protocols have been
proven cryptographically secure in the UC-framework. They are
blockchain-agnostic and only rely on a blockchain's capability to execute
smart contracts.

Currently the project consists of three main parts:

- _go-perun_ is a Go SDK that implements the core state channel protocol in a
  blockchain-agnostic fashion by following the dependency inversion principle.
  For this reason, several blockchain backends can be chosen and only
  blockchain-specific initializations need to be executed at program startup.

- _perun-eth-contracts_ contains the interconnected smart contracts for the
  Ethereum backend. They define the on-chain logic for channel deposits,
  disputes, settlements and withdrawals.

- _perun-node_ is a state channel node. It builds upon the go-perun SDK for
  establishing and operating Perun state channels, sets up a network
  for off-chain communications and provides an API interface for the user to
  interact with. To start with, Ethereum payment channels are implemented.

# Initial Committers

- <https://github.com/anagha-ks>
- <https://github.com/choeppler>
- <https://github.com/danielksan81>
- <https://github.com/ggwpez>
- <https://github.com/Gold3nboy>
- <https://github.com/manoranjith>
- <https://github.com/matthiasgeihs>
- <https://github.com/ndzik>
- <https://github.com/RmbRT>
- <https://github.com/sebastianst>
- <https://github.com/tinnendo>

# Sponsor

- <https://github.com/lehors> - Chair of the TSC

# Pre-existing repository

- <https://github.com/direct-state-transfer/go-perun>
- <https://github.com/direct-state-transfer/perun-eth-contracts>
- <https://github.com/direct-state-transfer/perun-node>
- <https://github.com/direct-state-transfer/perun-doc>
- <https://github.com/direct-state-transfer/perun-proposals>
