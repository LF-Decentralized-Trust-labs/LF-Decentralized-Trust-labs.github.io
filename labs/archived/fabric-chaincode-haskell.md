---
layout: default
title: Hyperledger Fabric Haskell Chaincode
parent: Archived Labs
---
# Lab Name
[Hyperledger Fabric Haskell Chaincode](https://github.com/hyperledger-labs/fabric-chaincode-haskell)

# Short Description

`fabric-chaincode-haskell` is a Haskell shim for Hyperledger Fabric to allow the authoring of smart contracts in Haskell.

As chaincode often contains business and security critical code, it is important that the code is correct. Implications for contracts containing bugs and exploits can lead to attacks like the DAO and Parity attacks on the Ethereum blockchain, which can have significant economic impacts. Functionally pure and strongly typed languages like Haskell provide a much greater degree of confidence in correctness. `fabric-chaincode-haskell` allows the authorship of chaincode that gives a higher confidence of correctness.

Allowing chaincode to be authored in Haskell also opens up the world of blockchain to the large and enthusiastic community of Haskell developers.

# Scope of Lab

This lab will focus on providing support for developers to write chaincode in Haskell. This will be done through a native Haskell Shim. We aim to provide feature parity with the existing official languages for Fabric - Go, Java and JavaScript.

This lab will also experiment with formal verification of the shim as well as user-defined chaincode. This work was presented at [Hyperledger Global Forum 2020](https://sched.co/ZdFh) and a [recording of the talk is now available](https://www.youtube.com/watch?v=Y-vMHbH4vVI).

# Initial Committers

Github IDs for the initial committers.
- [nwaywood](https://github.com/nwaywood) - Nick Waywood
- [airvin](https://github.com/airvin) - Allison Irvin

# Sponsor

- Arnaud Le Hors (lehors@us.ibm.com) - Chair of Hyperledger TSC

# Pre-existing repository

- https://github.com/nwaywood/fabric-chaincode-haskell
