---
layout: default
title: hyperledger_fabric_flutter_labs
parent: LFDT Labs
grand-parent: Active Labs
SPDX-License-Identifier: CC-BY-4.0
---

# Lab Name

Hyperledger Fabric Flutter Labs .

# Short Description

Experimental playground for Hyperledger Fabric on Flutter and Dart
platforms .

# Scope of Lab

Extend original fabric_client_flutter lab filed within Hyperledger Labs
.

Filed: ../hyperledger/fabric_client_flutter.md .

Hyperledger Labs homepage:
https://lf-decentralized-trust-labs.github.io/labs/hyperledger/fabric_client_flutter.html
.

The extension should allow purely client side funtionality on Flutter
and Dart platforms through Java interop package : jnigen (
https://pub.dev/packages/jnigen ) bindings of Hyperledger Fabric Gateway
Client API for Java in support of Hyperledger Fabric v2.4 + .

The functionalities include but not limited to client offline signing ,
offline TLS CA certificate loading on mobile platforms ( e.g. Android )
without intermidiate parties, ACME servers or CSR ( Certificate Signing
Request ) , which eliminates the requirements of [ FABN-895 ] (
https://docs.google.com/document/d/1gj5XB7yS-pfjpvZEUQh5lBGSIE6aQemu8A69tAYQtTc
) .

This lab also deduplicates or eliminates the need of a server or
fabric-server-node ( ../archived/fabric-server-node.md ) .

The lab introduces a playground for high-level gateway APIs for
Hyperledger Fabric version 2.4 or later on Flutter and Dart platforms .
Earlier versions of Hyperledger Fabric should reuse the old
fabric_client_flutter lab .

# Initial Committers

https://github.com/ghpZ54K8ZRwU62zGVSePPs97yAv9swuAY0mVDR4

# Sponsor

There is no offical sponsor for this lab , but previous sponosors who
sponsored / brought out the previous work were :

- https://github.com/dexhunter ( maintainer of Hyperledger Fabric Python
SDK ) .

- https://github.com/davidkhala ( committee board member of Technical
Working Group China ) .

# Pre-existing repository

https://github.com/ghpZ54K8ZRwU62zGVSePPs97yAv9swuAY0mVDR4/hyperledger_fabric_flutter_labs

