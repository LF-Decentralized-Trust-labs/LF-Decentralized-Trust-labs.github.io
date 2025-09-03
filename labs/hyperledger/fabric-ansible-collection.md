---
layout: default
title: Fabric Ansible Collection
parent: Hyperledger Labs
grand_parent: Active Labs
---
# Lab Name
[Fabric Ansible Collection](https://github.com/hyperledger-labs/fabric-ansible-collection)

# Short Description
An Ansible Collection create and manage Hyperledger Fabric networks

# Scope of Lab
This proposal is for the ibm-blockchain/ansible-collection repository to transfer to a hyperledger-labs. Originally targeted at the IBP platform, it is now applicable to a completely open source stack hence would be beneficial to the community.
Internally it is structured to be as agnostic as possible so could help to unify some of the variations in Fabric deployment technologies. By defining in playbooks the fabric infrastructure, it is able to abstract the practical deployment choices.

Fabric is a production deployed solution - and needs something like Ansible to help manage it.

The collection broadly splits into two parts:

- Installation of an Operator/Fabric Console
  Installs the CRDs and Operators into K8S

- Modules to manage the Fabric Nodes
  These are generic and are not specific to any form of deployment; any deployment specific is hidden behind interfaces.

Steps:
- we would need to remove the IBP specific elements: therefore would suggest a forked version of the repo be transferred to hyperledger-labs (or forked direct to hyperledger-labs if that's possible).
- document the interface to allow other operators etc - and work with those in the community to help here


Examples of the collection in use can be seen at https://github.com/hyperledgendary/fabric-cloud-infrastructure

Though it's not in a state today to move directly - I wanted to start the discussion with Hyperledger.


# Initial Committers
- https://github.com/mbwhite

# Sponsor

# Pre-existing repository
_If you currently have a Github repository that you wish to transfer to the Hyperledger Labs organization, please provide a link here. **NOTE: Please refer to the README for additional information on existing repositories.**_
