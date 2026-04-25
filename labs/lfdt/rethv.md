---
layout: default
title: rethv
parent: LFDT Labs
grand_parent: Approved Labs
---
# Lab Name

rethv

# Short Description

An experimental Ethereum execution client exploring a node implementation where smart contracts run in a RISC-V virtual machine instead of the EVM.

# Scope of Lab

rethv will be an experimental fork of [Reth](https://reth.rs/overview/) that replaces the [Ethereum Virtual Machine](https://ethereum.org/developers/docs/evm/) execution path with a [RISC-V](https://riscv.org/specifications/ratified/) virtual machine.

The goal of the lab is to create an open reference implementation for studying whether a RISC-V execution environment can simplify blockchain execution and improve compatibility with modern [zero-knowledge proving](https://ethereum.org/zero-knowledge-proofs/) systems.

The lab will focus on:

- Integrating a RISC-V VM into the [Reth](https://reth.rs/overview/) execution client.
- Supporting a local [Ethereum](https://ethereum.org/) devnet that can execute RISC-V smart contracts.
- Providing developer documentation and examples for building, deploying, and testing contracts in the RISC-V execution environment.
- Producing benchmarks comparing the EVM execution path with the RISC-V execution path.
- Evaluating zero-knowledge proving trade-offs, including proving time, memory usage, and cost.

The lab may reuse or study related open source work such as [R55](https://github.com/risechain/r55) and other [RISC-V/Ethereum research](https://ethereum-magicians.org/t/long-term-l1-execution-layer-proposal-replace-the-evm-with-risc-v/23617), but its focus is broader client-level integration, reproducible devnet operation, and concrete system measurements.

Relevant references:

- [Reth](https://reth.rs/overview/)
- [Long-term L1 execution layer proposal: replace the EVM with RISC-V](https://ethereum-magicians.org/t/long-term-l1-execution-layer-proposal-replace-the-evm-with-risc-v/23617)
- [R55](https://github.com/risechain/r55)

# Initial Committers

- Salaheldin Soliman - https://github.com/salaheldinsoliman

# Sponsor

- [David Boswell](https://github.com/davidwboswell) (dboswell@linuxfoundation.org; Discord: davidwboswell) - Maintainer, LF Decentralized Trust Labs
- Sean Young (sean@mess.org) - https://github.com/seanyoung

# Pre-existing repository

None
