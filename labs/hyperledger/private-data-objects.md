---
layout: default
title: Private Data Objects
parent: Hyperledger Labs
grand_parent: Approved Labs
---
# Lab Name
[Private Data Objects](https://github.com/hyperledger-labs/private-data-objects)

# Short Description

The Private Data Objects lab provides technology for
confidentiality-preserving, off-chain smart contracts.

A private data object (PDO) is a stateful "smart contract" that
implements a set of access and update policies on confidential data
shared between individuals or organizations. The contract defines a set
of message handlers that act on the state of the contract; handlers can
modify state, perform some computation over the state, and/or generate
messages for other objects.

Preservation of the integrity of contract execution and the enforcement
of confidentiality guarantees come through the use of a trusted
execution environment (TEE). While the approach will work with any TEE
that guarantees integrity and confidentiality for code and data, our
current implementation uses Intel<sup>@</sup> Software Guard Extensions
(SGX).

Private data objects leverage the existence of a distributed ledger to
ensure serialization of contract commits and to enforce dependencies
between the commits. Initially, we will implement the "Commit and
Coordination Log" as a HL Sawtooth transaction family. Our future plans
include implementations for other ledger platforms.

# Scope of Lab

This project provides two substantial advances for Hyperledger
distributed ledger platforms. First, it provides a ledger-independent,
off-chain smart contract service that preserves participant, state, and
contract confidentiality. Second, the connection to existing ledgers
comes in the form of a commit and coordination log (CCL). This allows
off-chain contracts to coordinate commits without exposing details of
the contract. The CCL is similar conceptually to existing proposals for
a "Global Synchronization Log".

# Initial Committers

* andmiele1 (andrea.miele@intel.com)
* bvavala (bruno.vavala@intel.com)
* byron-marohn (byron.marohn@intel.com)
* cmickeyb (cmickeyb@gmail.com)
* EugeneYYY (yevgeniy.y.yarmosh@intel.com)
* harmonh (holly.harmon@intel.com)
* TomBarnes (thomas.j.barnes@intel.com)

# Sponsor

Dan Middleton (dan.middleton@intel.com)

# Pre-existing repository

Existing repository is internal to Intel. We plan to transfer to
Hyperledger github upon receiving required HL and Intel internal
approvals.
