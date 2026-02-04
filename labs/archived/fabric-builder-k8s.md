---
layout: default
title: Hyperledger Fabric Chaincode Builder for Kubernetes
parent: Archived Labs
---
# Lab Name
[Hyperledger Fabric Chaincode Builder for Kubernetes](https://github.com/hyperledger-labs/fabric-builder-k8s)

# Short Description
External builder enabling Hyperledger Fabric peers to launch containerized chaincode using Kubernetes.

# Scope of Lab
Starting with Fabric 2.0, External Builders and Launchers enable the peer to be extended with programs that can build, launch, and discover chaincode. The aim of this lab is to develop such a builder which supports containerized chaincode using Kubernetes for deployment.

Advantages:

- prepublished chaincode images avoids compile issues at deploy time
- standard CI/CD pipelines can be used to publish containerized chaincode images
- chaincode traceability using [immutable image digests](https://docs.docker.com/engine/reference/commandline/pull/#pull-an-image-by-digest-immutable-identifier)

# Initial Committers
- [James Taylor](https://github.com/jt-nti)
- [Josh Kneubuhl](https://github.com/jkneubuh)

# Sponsor
- [Arnaud LeHors](https://github.com/lehors)  - Hyperledger TSC Member

# Pre-existing repository
- https://github.com/hyperledgendary/fabric-builder-k8s
