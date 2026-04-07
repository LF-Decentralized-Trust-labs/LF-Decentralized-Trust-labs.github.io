---
layout: default
title: Fablo
parent: Hyperledger Labs
grand_parent: Approved Labs
---
# Lab Name
[Fablo](https://github.com/hyperledger-labs/fablo)

# Short Description
Setting up and running a custom Hyperledger Fabric network is hard. The main goal of Fablo is to make this process easy, straightforward and accessible. It transforms a single configuration file to running network.

# Scope of Lab
Fablo aims at providing single, concise and flexible configuration file that describes desired Fabric network. The file:
- COMPLETELY describes desired network topology. No later flags, commands or other adjustments are needed. We can simply transform file into running network that has everything as it was declared.
- Is as flexible as Fabric is. We can have multiple organizations, channels, chaincodes and combine them in various ways.
- Is as concise as possible.
- File has schema and syntax highlighting to speed up work.
- Validation stage detects bad design decisions and communicates with user.

Fablo supports TLS, RAFT and solo consensus protocols, multiple organizations, channels, chaincodes and private data collections. It has also integrated REST API client for basic CA and chaincode interaction.

Benefits of Fablo:
1. Single file is easy to reason about and to get familiar with network topology.
2. Offers an easy start - in a few minutes you can start initial network and implement chaincodes.
3. Having a single file for Hyperledger Fabric network configuration is great for code reviews, team sharing.
4. Fablo is a good fit for Continues Integration processes.
5. Highlighting & validation can help to detect errors at early stage. It's done before modifying the network.
6. The core of Fablo is a single configuration file that is transformed to running network. In the future we plan to handle multiple outputs (i.e. support Kubernetes Operators along with current Docker network) and inputs (right now we have JSON and YAML, we are investigating a way to create an user interface)

# Initial Committers
- [Hejwo](https://github.com/Hejwo)
- [dzikowski](https://github.com/dzikowski)

# Sponsor
No sponsors

# Pre-existing repository
- [https://github.com/softwaremill/fablo](https://github.com/softwaremill/fablo)
