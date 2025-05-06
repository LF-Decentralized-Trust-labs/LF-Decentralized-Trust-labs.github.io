---
layout: default
title: One Attestation API
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name
One Attestation API

# Short Description
This lab proposes to create a single API to handle remote attestations.
Attestations are a crucial mechanism to establish trust in hardware-based trusted execution environments (TEEs).
Today, multiple attestation mechanisms are available, like SGX-EPID (which is being phased out), SGX-DCAP, TDX-DCAP and SEV-attestation.
This proposal aims to create a single abstraction for the generation and verification of hardware-based attestations.
The abstraction can benefit, and avoid redundant implementations in, multiple projects (e.g., Fabric Private Chaincode, Private Data Objects) that use TEEs to enhance software integrity and confidentiality.

# Scope of Lab
The scope of the lab is to provide tools and support for hardware/software attestations.
Contributions from the community will help support additional attestation mechanisms and TEEs.
Initially, we anticipate to integrate this tool with: Fabric Private Chaincode and Private Data Objects.

# Initial Committers
- https://github.com/bvavala

# Sponsor
- https://github.com/mbrandenburger - Marcus Brandenburger (bur@zurich.ibm.com) - LFDT TAC Member

# Pre-existing repository
Initially, this lab is meant to spin off the attestation API created in/for the Fabric Private Chaincode project.
- [https://github.com/hyperledger/fabric-private-chaincode](https://github.com/hyperledger/fabric-private-chaincode/tree/2b384e75ed1b19e8192f4c070ba9925e4a5a1ea7/common/crypto/attestation-api)

Recently, the library was extended with DCAP support and partially integrated with the Hyperledger Labs Private Data Objects project.
- [One Attestation API](https://github.com/bvavala/private-data-objects/tree/bruno.241017.move-to-attestation-api/common/crypto/attestation-api)
- [Integration in PDO](https://github.com/hyperledger-labs/private-data-objects/pull/501)
