---
layout: default
title: Operations Smart Contract for Hyperledger Fabric
parent: Archived Labs
---
# Lab Name
[Operations Smart Contract for Hyperledger Fabric](https://github.com/hyperledger-labs/fabric-opssc)

# Short Description
Operations Smart Contract (OpsSC) is a smart contract-based system operation tool for Hyperledger Fabric-based systems,
which aims to enable efficient decentralized system operations across multiple organizations.

# Scope of Lab
The goal of OpsSC is establishing decentralized system operations across multiple organizations for Hyperledger Fabric-based systems.

In the tool, a system operational workflow is defined as a smart contract (called *OpsSC chaincode*).
Each organization's admin interacts with the OpsSC chaincodes by using *OpsSC API Server* for each organization.
In a typical use case, an admin for an organization first requests a proposal of an operation (e.g., deploying a new chaincode, adding a new organization)
and then admins for other organizations approve (vote for) the proposal.
*OpsSC Agent* for each organization executes the operation to their own nodes (e.g., peers and orderers) based on the events (including operational instructions)
issued by the OpsSC chaincode (for example, the events are issued when a majority of the votes for the proposal are collected).

This will help make end-to-end operational workflows (e.g., typical chaincode deployment and channel updates process) more efficient.

Details:
- [Presentation slide](https://github.com/satota2/fabric-opssc-materials/blob/main/materials/OpsSC_for_Hyperledger_Fabric_v2.x_pub.pdf)
- [Demo movies](https://github.com/satota2/fabric-opssc-materials#demo-movies)

# Initial Committers
- https://github.com/satota2
- https://github.com/shimos

# Sponsor
- David Enyeart (enyeart@us.ibm.com) - a TSC member, a maintainer of Hyperledger Fabric

# Pre-existing repository
- https://github.com/satota2/fabric-opssc
