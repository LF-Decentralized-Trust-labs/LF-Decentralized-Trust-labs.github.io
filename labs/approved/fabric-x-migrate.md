---
layout: default
title: Fabric-X-Migrate
parent: Approved Labs

---
# Lab Name
[Fabric-X-Migrate](https://github.com/hyperledger/fabric-x-migrate)

### Lab Name

Fabric-X-Migrate

### Short Description

A CLI tool to migrate application state from Hyperledger Fabric into Fabric-X. The proposed CLI name is `fxmigrate`.

### Scope of Lab

The goal of this lab is to bring the complete Fabric-to-Fabric-X migration tool into production-usable state and maintain it as an LFDT Labs project. It will move the existing `fabric-x-migrate-poc` (https://github.com/syndbg/fabric-x-migrate-poc) tool into an LFDT Labs repository, then develop and release it as the `fxmigrate` CLI.

`fxmigrate` will provide an end-to-end workflow for migrating Fabric application state from peer snapshots into Fabric-X. 

This work originates from the Fabric-X snapshot migration RFC ([PR #9](https://github.com/hyperledger/fabric-x-rfcs/pull/9)), which led to the migration proof of concept. The existing test harness exercises both database backends, Classic snapshot formats, a real Arma orderer, two running committers, and backup, restore, and catch-up. 

### Alignment with LFDT Mission

The lab will provide open tooling for organizations moving existing ledger state to Fabric-X. It builds on LFDT ledger projects and lets operators and contributors improve compatibility and safety practices in the open. An LFDT Lab is a suitable early-stage home while the contributor community, governance, adoption, and releases develop.

### Relation to Existing LFDT Labs and Projects

Hyperledger Fabric is the source ledger and Fabric-X is the target runtime. `fxmigrate` prepares target application state. It does not replace either ledger or change their protocols. The LFDT Labs organization also hosts a Fabric-X block explorer, which helps inspect a running network. This proposal focuses on importing state before application traffic starts.
