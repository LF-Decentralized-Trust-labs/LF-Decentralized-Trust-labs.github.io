---
layout: default
title: Topologies for Hyperledger Fabric
parent: Archived Labs
---
# Lab Name
[Topologies for Hyperledger Fabric](https://github.com/hyperledger-labs/fabric-topologies)

# Short Description
Scripts and configurations to easily setup various Hyperledger Fabric topologies that exercise advanced Hyperledger Fabric capabilities. Goals:
- facilitate the learning of the product and its capabilities
- encourage the community to leverage these advanced capabilities when setting up production networks

# Scope of Lab

At [Alphaledger](https://www.alphaledger.com/) we are setting up complex multi-orgs Hyperledger Fabric networks to support the trading of municipal bonds in the US markets. Through the process we had a need to configure, implement and demonstrate in our networks some of the most advanced capabilities of the product, e.g.:

 - Channel Participation API
 - External World State Database (Couch DB Clusters)
 - Mutual TLS for all network communications
 - External Chaincode
 - LDAP-enabled Fabric CAs
 - Private Data Collections

To help with our understanding of the product we have setup individual network topologies that exercised each of these cababilities. The setup of these topologies requires very few installs on a developer's machine (Docker + Docker compose) and standing up a network is simple (just the execution of a start-up script).

Over time, we and the community can add more topologies to demonstrate the setup and configurations for other product features.

More background and information on the scope of this proposed lab is provided at the root documentation page for the the [pre-existing repository](https://github.com/alphaledger/hlfabric-topologies).

# Initial Committers
- [Alex Olaru](https://github.com/alexolaruhf)
- [Taylor Trott](https://github.com/Enchilada3687)

# Sponsor
- [David Boswell](dboswell@linuxfoundation.org) - Senior Director of Community Architecture, Linux Foundation
- [David Enyeart](enyeart@us.ibm.com) - a TSC member, a maintainer of Hyperledger Fabric

# Pre-existing repository
- https://github.com/alphaledger/hlfabric-topologies
