---
layout: default
title: CC-Tools
parent: Hyperledger Labs
grand_parent: Approved Labs
---
# Lab Name
CC-Tools

* [cc-tools-demo](https://github.com/hyperledger-labs/cc-tools-demo)
* [cc-tools](https://github.com/hyperledger-labs/cc-tools)
* [cc-tools docs](https://github.com/hyperledger-labs/cc-tools-doc)

# Short Description
The CC-Tools package provides a relational-like framework for programming Hyperledger Fabric chaincodes.

# Scope of Lab
The CC-Tools project aims to provide an easy to use framework to develop Hyperledger Fabric chaincodes in Golang.

CC-Tools provides a relational-like definitions of asset types, datatype validation, also allowing the creation of custom types, Fabric events management and easy transaction definition, with built-in arguments validation and callers restriction. Some pre-defined transactions includes standard method to create, delete, update and read assets.

The CC-Tools-Demo repository provides a template for CC-Tools, featuring configurations and examples of asset types, transactions and events usage. It also features scripts to easily start or upgrade a network and a rest server API written using GIN, which provides access to endpoints to communicate with the chaincode (with routes using `fabric-sdk-go` and `fabric-gateway`) and automatic subscription to CC-Tools events.

# Initial Committers
- https://github.com/bandreghetti
- https://github.com/ArthurPaivaT
- https://github.com/JoaoPedroAssis
- https://github.com/samuelvenzi
- https://github.com/goledger
- https://github.com/AlineLermen
- https://github.com/lucas-campelo
- https://github.com/andremacedopv
- https://github.com/mikaellafs
- https://github.com/jamillepp

# Sponsor
- https://github.com/denyeart - Hyperledger Fabric Maintainer and Release Manager, TOC Member

# Pre-existing repository
- https://github.com/GoLedgerDev/cc-tools
- https://github.com/GoLedgerDev/cc-tools-demo
- https://github.com/GoLedgerDev/cc-tools-doc
