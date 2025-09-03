---
layout: default
title: solang
parent: Archived Labs
---
# Lab Name
[solang](https://github.com/hyperledger-labs/solang)

# Short Description
A Solidity to wasm compiler written in rust

# Scope of Lab
The solang compiler would be able to compile contracts written in Solidity
to WASM, rather than EVM. sawtooth-seth supports contracts in wasm already,
and burrow would like to move away from EVM to WASM.

By using standard tools like parser generators and the llvm backend, we can
write a Solidity compiler which has a small codebase, and can benefit from
the fantastic compiler optimisations in LLVM.

The license is Apache rather than the existing solidity compiler which is
GPL.

By only supporting WASM and no EVM, we can evolve the Solidity language
in new directions which suit our projects.

# Initial Committers
- https://github.com/seanyoung
- https://github.com/silasdavis

# Sponsor
- https://github.com/silasdavis - TSC Member

# Pre-existing repository
https://github.com/seanyoung/solang/
