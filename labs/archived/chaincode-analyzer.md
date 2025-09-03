---
layout: default
title: Chaincode Analyzer
parent: Archived Labs
---
# Lab Name
Chaincode Analyzer

# Short Description
A static tool to check and detect potentially risky codes in smart contracts (a.k.a, chaincodes).


# Scope of Lab
The aim of Chaincode Analyzer is to provide the way to check whether the smart contracts includes potentially risky codes or not.
The tool performs static analysis on chaincode source codes written in Golang and detects potentially risky parts such as generating random values, accessing outside of blockchain networks and iteration on map object.
For more details of the tool and target risks:
https://github.com/FujitsuLaboratories/ChaincodeAnalyzer

In Hyperledger Fabric, developers can use general purpose programming languages, such as JavaScript, Golang and Java, to implement their chaincodes.
Compared to using domain specific languages (DSLs) like Solidity of Ethereum, the efforts of implementing smart contracts are smaller since developers do not need to study new language for smart contracts.
On the other hand, there are some pitfalls when developers use general purpose programming languages for implementing smart contracts.
For instance, Solidity does not have a method to generate random value since it easily causes different states during nodes which execute the smart contract including random value generation.
Different to Solidity, general purpose programming languages such as Golang typically have a method to generate random value.
Therefore, we think there are needs for a tool to detect such blockchain related potential risks quickly.

# Initial Committers
- https://github.com/kzhry (Kazuhiro Yamashita)
- https://github.com/Chinlying (Ence Zhou)

# Sponsor
- https://github.com/hartm (Hart Montgomery) - Member of Hyperledger TSC

# Pre-existing repository
- There is pre-existing public repository available at (https://github.com/FujitsuLaboratories/ChaincodeAnalyzer) as explained above. We would like to copy all the code since we did not use sign-off option.
