---
layout: default
title: Mir-BFT
parent: Archived Labs
---
# Lab Name

[Mir-BFT](https://github.com/hyperledger-labs/mirbft)

# Short Description

Mir-BFT Hyperledger lab is a repository for development of a production version of a BFT library based on the Mir-BFT protocol, described in the paper ``Mir-BFT: High-Throughput Robust BFT for Decentralized Networks'' (https://arxiv.org/pdf/1906.05552.pdf). The repository also contains the original PoC code used to obtain the research results described in the paper (under the `research' branch).

In short, Mir-BFT is a Byzantine fault-tolerant (BFT) total order broadcast protocol aimed at maximizing throughput on wide-area networks (WANs), targeting deployments in decentralized networks, such as permissioned and Proof-of-Stake permissionless blockchain systems.  Mir-BFT is the first BFT protocol that allows multiple leaders to propose transaction batches/blocks in parallel in a way which his robust to attacks, removing the single-leader throughput bottleneck of leader-based BFT protocols. Mir-BFT PoC orders more than 60000 signed Bitcoin-sized (500-byte) transactions per second on a widely distributed 100 nodes, 1 Gbps WAN setup, with typical latencies of few seconds.

# Scope of Lab

Mir-BFT library is planned to be integrated into Hyperledger Fabric as its ordering service, eventually replacing Fabric's Raft ordering service. Other distributed ledger projects under Hyperledger can also benefit from and use Mir-BFT.

# Initial Committers
- https://github.com/jyellick
- https://github.com/matejpavlovic
- https://github.com/stchrysa
- https://github.com/vukolic

# Sponsor

Angelo de Caro, Hyperledger Technical Steering Commitee member.
- https://github.com/adecaro

# Pre-existing repository
- https://github.com/IBM/mirbft (main repository)
- https://github.com/IBM/mirbft/blob/master/README.md (main README)
- https://github.com/IBM/mirbft/tree/research (`research' branch with Mir-BFT PoC code)
- https://github.com/IBM/mirbft/blob/research/README.md (PoC README)
