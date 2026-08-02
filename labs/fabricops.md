---
layout: default
title: FabricOps
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name
[FabricOps](https://github.com/dpereowei/FabricOps)

# Short Description
A Kubernetes operator and CLI for provisioning and operating Hyperledger Fabric networks from Fablo-style declarative configuration, with first-class support for Fabric CA identities, channels, Chaincode-as-a-Service, and federated organization joins.

# Scope of Lab
FabricOps aims to make Kubernetes a practical deployment target for Hyperledger Fabric networks described as network intent rather than as isolated component resources. It was started after using Fablo for Docker Compose development and needing a production-oriented path to run similar multi-organization networks on Kubernetes.

The lab will focus on:

- A `FabricNetwork` custom resource that describes a whole Fabric network, including organizations, CAs, orderers, peers, channels, chaincode, and operational settings.
- A `FabricParticipant` custom resource and join-bundle workflow for organizations that own their own Kubernetes infrastructure and need to join an existing network or channel.
- Automated Fabric CA bootstrap, admin enrollment, peer and orderer enrollment, MSP and TLS material orchestration, and certificate-aware workload configuration.
- Declarative channel bootstrapping, orderer and peer channel joins, anchor peer updates, external organization admission, and status reporting.
- Chaincode-as-a-Service lifecycle automation, including package metadata generation, install, approval, commit, upgrade, private data collection support, endorsement policies, and chaincode server workloads.
- `fabricopsctl`, a CLI for readiness, diagnostics, connection profile export, join bundle handoff, and invoke/query operations.
- Kubernetes operational concerns such as per-organization namespaces, persistent storage, resource defaults, network policies, helper Job cleanup, metrics endpoints, and Prometheus Operator integration.
- Compatibility work with Fablo so Fablo can target FabricOps when the selected engine is Kubernetes while preserving the simple Fablo configuration experience.
- A future-looking path for Fabric X support as the Hyperledger Fabric ecosystem evolves.

FabricOps is not intended to replace existing LF Decentralized Trust Labs such as fabric-operator, hlf-operator, Hyperledger Bevel, or Fablo. Those projects cover important adjacent areas, including component-level Fabric operators, broader DLT automation, and local network generation. FabricOps is intended to explore a complementary layer: translating Fablo-like full-network intent into Kubernetes reconciliation and day-two operations, with a bias toward a simple manifest, strong status feedback, and federated ownership between organizations.

The lab fits LF Decentralized Trust's mission by improving the operability and accessibility of permissioned decentralized infrastructure. Fabric networks often involve strict identity, TLS, networking, channel governance, endorsement, and chaincode lifecycle requirements. FabricOps provides a place for the community to collaborate on making those workflows reproducible, reviewable, and automatable on Kubernetes.

# Initial Committers
- https://github.com/dpereowei

# Sponsor
[Jakub Dzikowski](https://github.com/dzikowski)
[Umegbewe Nwebedu](https://github.com/umegbewe)

# Pre-existing repository
- https://github.com/dpereowei/FabricOps

The pre-existing repository is licensed under Apache License 2.0. If the Labs stewards prefer not to transfer its full history because some early and merge commits do not include DCO sign-off trailers, the code can be imported into a Labs repository as a signed-off squashed initial contribution.
