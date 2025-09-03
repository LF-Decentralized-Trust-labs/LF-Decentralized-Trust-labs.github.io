---
layout: default
title: Aries Agent Controller
parent: Hyperledger Labs
grand_parent: Active Labs
---
# Lab Name
[Aries Agent Controller Lab](https://github.com/hyperledger-labs/aries-agent-controller)

# Short Description
This lab focuses on running an aries agent controller. Controllers are used to facilitate interactions between different types of agents on a network.

# Scope of Lab
The scope of this lab is to provide an agent controller to help navigate interactions between different agents. The controller is implemented through aca-py as a django python application. It features docker code to help setup agents locally and various endpoints to facilitate the verifiable credential process/lifecycle. The holder agent may be run in mulit or single tenant mode as needed for different use cases. This lab assumes that an indy network is being leveraged as the underlying verifiable data registry (VDR), however hyperledger aries is chain-agnostic and can therefore be extended to work against different chains.


# Initial Committers
- [Mona Rassouli](https://github.com/monar24)
- [Nathan Randall](https://github.com/data-douser)
- [Correy Schultz](https://github.com/CorreyS)

# Sponsor
N/A

# Pre-existing repository
- https://github.com/OneOf-Inc/acapycontroller
