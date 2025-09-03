---
layout: default
title: weft
parent: Archived Labs
---
# Lab Name
[_Fabric Weft._](https://github.com/hyperledgendary/weft)

# Short Description
Simple command line utility and module, to help work Hyperledger Fabric, and other instantiations such as the IBM Blockchain Platform (IBP) and convert resources between them. This is intended to be a complement to the existing tools for each product. A lot of the code here is based on that in [hyperledger/fabric-samples](https://github.com/hyperledger/fabric-samples)

# Scope of Lab
The end goals are to obtain, irrespective of how the Fabric infrastructure is created.

- application wallets and identities for the Client SDKs to use
- the gateway connection profiles to let the Client SDKs to connect
- the MSP directory structure to permit the Fabric Peer CLIs to function
- packaged Chaincode/SmartContract


For example packaging chaincode the cli is

```
weft chaincode package

Create a chaincode package (tgz) to install on peers

Commands:
  weft chaincode package full  Include all code to run under Peer managed chaincode containers
  weft chaincode package caas  Chaincode-as-a-service Builders for user managed chaincode containers
  weft chaincode package k8s   K8S Builder for Kubernetes managed chaincode containers

Chaincode Package:
  -p, --path     Path to the root directory of the chaincode or file
  -l, --label    Label of the chaincode to use  [required]
  -q, --quiet    Quiet mode, only output the packageid to stdout  [boolean] [default: "false"]
  -a, --archive  filename of the output tgz  [string]
  ```



# Initial Committers

- https://github.com/mbwhite

# Pre-existing repository
- https://github.com/hyperledgendary/weft
