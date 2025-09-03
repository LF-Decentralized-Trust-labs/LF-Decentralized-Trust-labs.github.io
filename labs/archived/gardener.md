---
layout: default
title: Gardener
parent: Archived Labs
---
# Lab Name
Gardener

# Short Description
An open source Blockchain Oracle implementation. https://gardeneroracle.io/

# Scope of Lab
Gardener already has some business value and you are welcome to [set it up yourself](https://gardener.readthedocs.io/en/latest/getting-started.html) or [test Gardener version deployed to Ropsten using our monitor](https://monitor.gardeneroracle.io/)

Currently, Gardener is integrated with Ethereum. Integration with Hyperledger Fabric will be added soon. It also leverages Hexagonal Architecture (ports and adapters) which means that integrating with any other blockchain is easy.

We also leverage `Intel SGX` . Currently, we [generate random values](https://gardener.readthedocs.io/en/latest/making-requests.html#random-datasource) in a secure way, leveraging Intel `SGX Remote Attestation` . In future, we are also planning to add `Intel SGX Sealing` to encrypt random data sent to blockchain. As a result, the only Third Trusted Party in entire RNG process will be `Intel`.

More complete roadmap is available [here](https://github.com/orgs/EspeoBlockchain/projects/1)

# Initial Committers
- https://github.com/kss-espeo
- https://github.com/starspire
- https://github.com/tcichowicz

# Sponsor
- Dan Middleton dan.middleton@intel.com

# Pre-existing repository
- https://github.com/EspeoBlockchain/gardener-server
- https://github.com/EspeoBlockchain/gardener-smart-contracts
- https://github.com/EspeoBlockchain/gardener-monitor
- https://github.com/EspeoBlockchain/gardener-sgx-enclave
- https://github.com/EspeoBlockchain/gardener-sgx-attestator
