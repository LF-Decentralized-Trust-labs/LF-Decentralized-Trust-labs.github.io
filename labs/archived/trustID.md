---
layout: default
title: TrustID
parent: Archived Labs
---
# Lab Name
[TrustID](https://github.com/hyperledger-labs/trustid)

# Short Description
Decentralized Identity solution compatible with different Hyperledger platforms.

# Scope of Lab

TrustID implements identity management in an alternative way to Hyperledger Fabric (as the first step, but the idea is to be compatible with other platforms). In HF identities are centralized in the CAs, so if a CA leaves the network all the users issued by this CA will be invalid. Using trustID to manage the identities it is possible to do it in a dynamic and decentralized way. Hyperledger Fabric is the first network that we have used to implement this model of identities, but in the end, it could be compatible with other platforms. And also, users that have key pairs in other blockchains could re-use it to sign transactions in Fabric.

The solution consists of two main components:

## Trust-sdk
This sdk abstracts all the logic of Hyperledger Fabric (or logic of other platforms could be implemented, like for example ethereum’s web3 ) and also enables the creation and management of decentralized identities. With this library is possible to create, update, revoke, import, and export identities using the DID standard from the W3C. In the end, the DID standard is used to give a global ID to the identities.

## Chaincode - Smart contract
Due to the Hyperledger Fabric identity management, it is not compatible with this type of identities and signatures we have implemented chaincode that implements these functionalities. In the end, all the functionalities that we have commented in the documentation are modules of the same chaincode. In this case, when we create an identity in the sdk, this identity is also registered in the chaincode, storing the public key, so by nature, it will be decentralized. Every time somebody wants to perform a transaction, this transaction will be signed off-chain thanks to the sdk and in the chaincode the signature will be verified. If everything is okay, this chaincode will invoke the chaincode that the user wants
In the case of other platforms, the implementation of this component has to be analyzed.

# Initial Committers

- https://github.com/adlrocha - Alfonso de la Rocha
- https://github.com/mtnieto - Maria Teresa Nieto

# Sponsor

- Troy Ronda https://github.com/troyronda

# Pre-existing repository
- https://github.com/telefonicablockchain/trustid
