---
layout: default
title: hyperledger_fabric_flutter_labs
parent: LFDT Labs
grand-parent: Active Labs
SPDX-License-Identifier: CC-BY-4.0
---

# Lab Name

hyperledger_fabric_flutter_labs .

# Short Description

experimental playground for hyperledger fabric on flutter and dart
platforms .

# Scope of Lab

extend the original fabric-client-flutter lab filed within hyperledger
labs
.

originally filed:
[fabric-client-flutter](../archived/fabric-client-flutter.md) .

see issue #344 (
https://github.com/LF-Decentralized-Trust-labs/LF-Decentralized-Trust-labs.github.io/issues/344
) and pr #345 (
https://github.com/LF-Decentralized-Trust-labs/LF-Decentralized-Trust-labs.github.io/pull/345
) for unarchiving the originally filed lab .

homepage of lfdt labs for the originally filed lab is at
https://lf-decentralized-trust-labs.github.io/labs/archived/fabric-client-flutter.html
.

previous studies of flutter and dart platforms in a blog post on the
originally filed lab is at
https://www.lfdecentralizedtrust.org/blog/2019/12/12/2019-summer-mentee-project-update-hyperledger-fabric-sdk-for-node-js-security-extension
.

take a look at https://github.com/hyperledger/fabric-rfcs/pull/67/files
to learn more about the scope of this lab and for the request for
comments of this lab .

the extension should allow purely client side funtionality on flutter
and dart platforms through java interop package : jnigen (
https://pub.dev/packages/jnigen ) bindings of hyperledger fabric gateway
client api for java in support of hyperledger fabric version 2.4 + .

the functionalities of this lab include but not limited to client
offline signing , offline tls ca certificate loading on mobile platforms
( e.g. android ) without intermidiate parties , acme servers or csr (
certificate signing request ) , which eliminates the requirements of a
certificate registrar mentioned in [ fabn-895 ] (
https://docs.google.com/document/d/1gj5XB7yS-pfjpvZEUQh5lBGSIE6aQemu8A69tAYQtTc
) .

this lab also deduplicates or eliminates the need of a server or
[fabric-server-node](../archived/fabric-server-node.md) .

the lab introduces a playground for high-level gateway apis for
hyperledger fabric version 2.4 or later on flutter and dart platforms .
earlier versions of hyperledger fabric should reuse the old
fabric_client_flutter lab .

# Initial Committers

https://github.com/ghpZ54K8ZRwU62zGVSePPs97yAv9swuAY0mVDR4

# Sponsor

there is no offical sponsor for this lab , but previous sponosors who
sponsored / brought out the previous work were :

- https://github.com/dexhunter ( maintainer of hyperledger fabric python
sdk ) .

- https://github.com/davidkhala ( committee board member of technical
working group china ) .

# Pre-existing repository

https://github.com/ghpZ54K8ZRwU62zGVSePPs97yAv9swuAY0mVDR4/hyperledger_fabric_flutter_labs
