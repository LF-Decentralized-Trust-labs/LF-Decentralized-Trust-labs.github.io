---
layout: default
title: Hyperledger Fabric Smart Client
parent: Hyperledger Labs
grand_parent: Active Labs
---
# Lab Name

[Hyperledger Fabric Smart Client](https://github.com/hyperledger-labs/fabric-smart-client)

# Short Description

[Hyperledger Fabric]('https://www.hyperledger.org/use/fabric') is a permissioned, modular, and extensible open-source DLT platform. Fabric architecture follows a novel `execute-order-validate` paradigm that supports distributed execution of untrusted code in an untrusted environment. Indeed, Fabric-based distributed applications can be written in any general-purpose programming language.

Developing applications for Hyperledger Fabric is often hard, sometimes painful. Fabric is a very powerful ecosystem whose building blocks must be carefully orchestrated to achieve the desired results. Currently, the Fabric Client SDKs are too limited. They do not offer any advanced capabilities to let the developers focus on the `application business processes`, and harness the full potential of Fabric.

What would happen if the developers could use a `Smart(er) Fabric Client` that offers:
- A high level API that hides the complexity of Fabric;
- A Peer-to-Peer infrastructure that let business parties talk to each as required by the business processes;
- An advanced transaction orchestration mechanism;
- A simplified model to interact with chaincodes;
- A local storage place where to store the states the application cares about;
- A State-based programming model that let you forget about RW sets and focus on business objects and their interactions?
Developing Fabric-based distributed applications would become simpler and joyful.
If you are a domain expert, the Fabric Smart Client hides the complexity of Fabric and allows you to focus on the business interactions.
If you are a skilled software engineer, you will be able to leverage the full power of Fabric.

# Scope of Lab

The scope of this lab is to deliver the `Fabric Smart Client` (FSC, for short), the `Next-Generation Fabric Client SDK`. FSC simplifies the development of Fabric-based distributed applications by putting at the centre the `business processes`, and by `hiding the unnecessary burden` of dealing with Fabric.

A `business process` is a collection of `related, structured activities` carried by `business parties` in which a specific sequence of steps serves a particular `business goal`. In other words, a business process is an `interactive protocol` among `business parties` each of which has its own `business view` (or simply `view`) of the process. A `view` is then the sequence of steps that a business party must execute to serve a particular `business goal`.
FSC aims to offer a comfortable environment to build such interactive protocols backed by the Hyperledger Fabric blockchain.

FSC will consist of multiple SDKs each of which provides a set of API and services that can be either used directly by FSC developers, to build their applications, or by other SDKs. A network node that runs the FSC stack is called `FSC node`. FSC nodes form an `FSC network` that will live on a side of one or more Fabric networks.

These are the first two SDKs that will form the FSC backbone:
- The `View SDK` is the core of FSC. It offers API and services to allow FSC nodes:
-- To connect to each other in a peer to peer fashion.
-- To manage and execute the business views the nodes are equipped with.
- The `Fabric SDK` is built on top of the `View SDK` and offers API and services to allow FSC nodes to communicate with Fabric. The Fabric SDK is not just the usual Fabric Client SDK, it is more. Indeed, we can identify the following components that make the Fabric SDK different from the current Fabric Client SDK:
-- `Chaincode API`: These are APIs that allow the developer to invoke any chaincode and assemble Fabric Transaction as she would do with the Fabric Client SDK.
-- `Identity Management`: The Fabric SDK allows a FSC node to play the role of an `Endorser`, not just that of a `Fabric Client`.
-- `State-Based Programming Model API` (`SPM`, for short): Instead of dealing directly with a Read-Write Set (RWS, for short), the SPM API allows the developer to think directly in terms of business objects. The SPM API takes care of translating these business objects to a well formed RWS. Therefore, FSC nodes can collaboratively assemble a Fabric Transaction and its RWS, and then other FSC nodes, playing the role of endorsers, endorse the assembled transaction. This gives much more flexibility than the default chaincode-centric protocol to assemble transactions, that Fabric offers.
-- `Vault`: The Fabric SDK equips a FSC node with a local storage system that contains only the transactions the node is interested in or helped to assemble. A FSC node does not need to store the entire ledger but only what is relevant. This storage space allows the FSC nodes to keep temporary version of the transactions they are assembling before they get submitted for ordering.

# Initial Committers

- [Angelo De Caro](`https://github.com/adecaro`)
- [Kaoutar Elkhiyaoui](`https://github.com/KElkhiyaoui`)
- [Alessandro Sorniotti](`https://github.com/ale-linux`)
- [Mathilde Ffrench](`https://github.com/mffrench`)

# Sponsor

- [Dave Enyeart](https://github.com/denyeart) - Hyperledger TSC member
- [Arnaud J Le Hors](https://github.com/lehors) - Hyperledger TSC chair

# Pre-existing repository

None
