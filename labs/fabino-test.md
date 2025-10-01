---
layout: default
title: Fabino-Test
parent: LFDT Labs
grand_parent: Active Labs
---

# Lab Name

Fabino Junit5 Test Extension

# Short Description

**Fabino-Test** is a lightweight Java testing library for Hyperledger Fabric that simplifies unit and integration
testing of
chaincode. It leverages **JUnit 5 extensions**, **Testcontainers**, and the **Microfab Docker image** to automatically
bootstrap a
Fabric network, install and commit chaincodes, and inject a ready-to-use **Fabric Gateway SDK** instance into test
classes.
Fabino-Test enables developers to focus on writing real test scenarios without manually managing the underlying network,
making Fabric testing fast, reproducible, and developer-friendly.

# Scope of Lab

Fabino-Test fits within the **Hyperledger Fabric developer tooling and testing** domain. Its scope includes:

- **Automated Fabric Network Bootstrapping in Java:** Start a complete Fabric network using Microfab and Testcontainers,
  fully controlled from Java, based on user-provided configuration.
- **Chaincode Lifecycle Management:** Handle packaging, installation, approval, and commit of chaincodes automatically
  within Java test environments.
- **Integration with JUnit 5 (Java):** Provide seamless extension mechanisms to manage the network lifecycle in unit and
  integration tests written in Java.
- **Dependency Injection:** Inject ready-to-use Java Fabric Gateway SDK instances (and potentially Network, Contract
  objects) into test classes.
- **Test Infrastructure Abstraction:** Enable Java developers to write reliable chaincode tests without manually
  managing peers, channels, or TLS certificates.

Fabino-Test aims to reduce the overhead of setting up Fabric test environments in Java, increase test reproducibility,
and provide a **flexible platform** for future expansion, such as supporting additional chaincode deployment models or
advanced test scenarios.

# Initial Committers

- https://github.com/aminchegeni

# Pre-existing repository

- https://github.com/aminchegeni/fabino-test
