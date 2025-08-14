---
layout: default
title: Verazt
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name
[Verazt](https://github.com/LF-Decentralized-Trust-labs/verazt)

# Short Description

Verazt is a smart contract security toolkit that provides a set of tools performing static analysis, formal verification, and fuzz-testing to find security vulnerabilities in smart contracts.

# Scope of Lab

This lab aims to provide a comprehensive set of static analysis, formal verification, and fuzz testing tools to automatically analyze and find security vulnerabilities in smart contracts.

At the current state, we focus on analyzing Solidity smart contracts on EVM-based blockchains. We apply different techniques to analyze different code representation levels in the compilation pipeline of Solidity smart contracts. More specifically:

1. At the Solidity source code level, we implement a lightweight static analysis framework to find bugs based on checking bug patterns on the smart contracts' Abstract Syntax Tree (ASTs).

2. At the Yul intermediate code level, we implement a formal verification framework to symbolically execute smart contracts and verify if their execution states violate any pre-defined or user-defined specifications that constrain the safety, security, and correctness of smart contracts.

3. At the EVM bytecode level, we implement a fuzz testing framework to dynamically test smart contracts by generating random inputs and executing them to find potential bugs.

In the future, we will expand the scope of this lab to support other smart contract languages such as Vyper, Move, or other Rust-based smart contracts, and other blockchain platforms such as Solana, Aptos, Sui.

# Initial Committers

We are a team of researchers and engineers from the [Singapore Blockchain Innovation Programme (SBIP)](https://sbip.sg/), a research lab hosted at [School of Computing](https://www.comp.nus.edu.sg/), [National University of Singapore](https://www.nus.edu.sg/). We have been researching and working on smart contract security for several years and have developed several tools and techniques to analyze and verify smart contracts.

Our initial committers are:

- https://github.com/ooibc
- https://github.com/ooibc88
- https://github.com/xkxiao
- https://github.com/taquangtrung
- https://github.com/cassc
- https://github.com/minhhn2910
- https://github.com/thanhtoantnt

# Sponsor

N/A

# Pre-existing repository

We are maintaining several repositories implementing the tools and techniques mentioned above. We will squash them into one commit and transfer them to the new repository created by LFDT Labs organization.
