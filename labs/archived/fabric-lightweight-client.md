---
layout: default
title: Hyperledger Fabric Lightweight Client
parent: Archived Labs
---
# Lab Name
Hyperledger Fabric Lightweight Client

# Short Description
The project aims to enable lightweight (IoT) devices to act as a Lightweight (Hyperledger Fabric)
Client and communicate through a Proxy directly with the Hyperledger Fabric network.
The device implements and runs only part of the standard Fabric SDK, namely the functions needed
to form, hash, and sign the transaction proposals and transactions. The remaining part of the SDK
(communication with the endorsing and committing peers, etc.) is performed by a proxy.


The topic was presented at the Hyperledger Global Forum in December.
https://hgf18.sched.com/event/G8s7/sdk-proxy-hyperledger-fabric-identities-for-lightweight-iot-devices-gero-dittmann-jens-jelitto-ibm-research

# Scope of Lab
The objective of the lab is to enable lightweight (IoT) devices to act as a Lightweight
(Hyperledger Fabric) Client and communicate through a Proxy directly with the Hyperledger Fabric network.
The solution allows the Lightweight Client to form and sign transactions with its preregistered
blockchain identity and to interact with the Hyperledger Fabric blockchain through a Proxy.

This approach ensures that data (e.g. sensor data, access information, door lock state) that is
captured by the Lightweight Client will be wrapped and signed by the Lightweight Client,
thereby preventing non-authorized modification of the data, even by the Proxy that serves as the
interface between the device and the Hyperledger Fabric network.
The solution aims at extending the trust that is established with blockchain ledger technology
(e.g. irrefutability, immutability) all the way to the Lightweight Client.

The Client side SDK Software (excluding any device specific crypto library) should be released as
C-code. This includes the transaction proposal and transaction forming steps of the Fabric SDK
functionality. The Open Source provisioning of the Client side SDK Software will enable providers
and users of lightweight (IoT) devices to establish device communication with Hyperledger Fabric
through the Proxy.

# Initial Committers
- https://github.com/JensJelitto
- https://github.com/GeroDittmann

# Sponsor
https://github.com/ale-linux - Alessandro Sorniotti - Research Stuff Member, Hyperledger Fabric Maintainer, IBM
https://github.com/lehors - Arnaud J Le Hors - Senior Technical Staff Member, Web and Blockchain Open Technologies, IBM


