---
layout: default
title: Hyperledger Fabric Token SDK
parent: Hyperledger Labs
grand_parent: Active Labs
---
# Lab Name

[Hyperledger Fabric Token SDK](https://github.com/hyperledger-labs/fabric-token-sdk)

# Short Description

[Hyperledger Fabric](https://www.hyperledger.org/use/fabric) is a permissioned, modular, and extensible open-source DLT platform. Fabric architecture follows a novel `execute-order-validate` paradigm that supports distributed execution of untrusted code in an untrusted environment. Indeed, Fabric-based distributed applications can be written in any general-purpose programming language.
Fabric does not depend on a native cryptocurrency as it happens for existing blockchain platforms that require “smart-contracts” to be written in domain-specific languages or rely on a cryptocurrency.

Blockchain technologies are accelerating the shifting towards a decentralised economy. Cryptocurrencies are reshaping the financial landscape to the extent that even central banks are now testing the technology to propose what is known as the `central bank digital currency`. But it is more than this. Real-world assets are being tokenised as fungible or non-fungible assets represented by tokens on a blockchain. Thus enabling business opportunities to extract more value.

Developing token-based applications for Hyperledger Fabric is not easy. Fabric does not provide an out-of-the-box SDK that let developers create tokens that represents any kind of asset. Developers are left on their own and this exposes them to useless duplication of code and security vulnerabilities.

What would happen if the developers could use a `Fabric Token SDK` that let:
- Create tokens that represents any kind of asset (baked by a real-world asset or virtual);
- Choose the privacy level that best fits the use-case without changing the application logic;
- Orchestrate token transaction in a peer-to-peer fashion;
- Perform atomic swaps;
- Audit transactions before they get committed;
- Interoperate with token systems in other blockchain networks;
- Add a token layer to existing Fabric distributed application?
Developing Enterprise Token-based distributed applications would become simpler and more secure.

# Scope of Lab

The scope of the lab is to deliver the `Fabric Token SDK`. A set of API and services that let developers create token-based distributed application on Hyperledger Fabric.
The `Fabric Token SDK` has the following characteristics;
- It adopts the UTXO model. In the UTXO model, a direct acyclic graph reflects the movements of the assets. Nodes are token transactions. Edges are transaction outputs. Each new token transaction consumes some the UTXOs and create new ones.
- Wallets contain a set of `secret keys` and keep track of the list of unspent outputs `owned` those keys.
- It supports different privacy levels: from a plain instantiation, where everything is in the clear on the ledger, to Zero Knowledge-based instantiations that will obfuscate the ledger while enforcing the required invariants.
- It can be easily extended to support different token exchange implementations (e.g., with different privacy levels, or cryptographic algorithms) by adopting a highly modular architecture.
- It allow the developers to write their own services on top of the Token SDK to deliver customised services for their token-based applications.

To deliver on the above promises. The `Fabric Token SDK` will offer two API levels. The first level is called `Fabric Token API`. This is agnostic to the specific token technology and is used to build token-based distributed applications or third-party libraries to enhance the Token SDK. The `Fabric Token API` converts each call to a series of calls to a second level API called `Fabric Token Driver API`. The `Fabric Token Driver API` deals with the details of the specific token implementation. This architecture allow the application developer to choose the driver implementation that better fits the requirements of the use case the developer aims to address. The actual application does not need to change.

For the driver implementation supporting privacy via Zero Knowledge, we will follow a simplified version of the blueprint described in the paper [Privacy-preserving auditable token payments in a permissioned blockchain system]('https://eprint.iacr.org/2019/1058.pdf') by Androulaki et al.

# Initial Committers

- [Elli Androulaki](https://github.com/elli-androulaki)
- [Angelo De Caro](https://github.com/adecaro)
- [Kaoutar Elkhiyaoui](https://github.com/KElkhiyaoui)
- [Mathilde Ffrench](https://github.com/mffrench)
- [Alessandro Sorniotti](https://github.com/ale-linux)

# Sponsor

- [Dave Enyeart](https://github.com/denyeart) - Hyperledger TSC member
- [Arnaud J Le Hors](https://github.com/lehors) - Hyperledger TSC chair

# Pre-existing repository

None
