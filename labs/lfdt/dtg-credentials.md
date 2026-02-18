---
layout: default
title: DTG Credentials
parent: LFDT Labs
grand_parent: Active Labs
---

# Lab Name

Decentralized Trust Graph (DTG) Credentials

# Short Description

Reference implementation of the LFDT ToIP Decentralized Trust Graph Working Group Credentials.

This includes:

- VMC (Verifiable Membership Credential) - proves an individual is a member of a VTC.
- VRC (Verifiable Relationship Credential) - proves a trust relationship between two nodes in a DTG.
- VIC (Verifiable Invitation Credential) - proves an invitation to join a VTC.
- VPC (Verifiable Persona Credential) - Links a persona to a relationship
- VEC (Verifiable Endorsement Credential) - Endorses skills and/or reputation
- VWC (Verifiable Witness Credential) - Witnesses a relationship or endorsement
- RCard (Relationship Card) - Human readable identity data (like a business card)

# Scope of Lab

The [Decentralized Trust Graph Working Group](https://lf-toip.atlassian.net/wiki/spaces/HOME/pages/257785857/Decentralized+Trust+Graph+Working+Group) (DTGWG) at Trust Over IP (ToIP) specifies open standard specifications for building verifiable trust communities (VTCs). VTCs are composed of cryptographically-verifiable trust relationships between the community members, including both people and AI agents. Each relationship is expressed using a verifiable credential (VC) between two or more decentralized identifiers (DIDs). Proofs of these VCs enable: a) individuals to provide privacy-preserving proof of personhood, and b) AI agents (or any digital service) to provide proof of control by an individual or an organization.

Every node in a decentralized trust graph (DTG), including people, AI agents, devices, and VTCs, are represented by a verifiable trust agent (VTA). The DTGWG also specifies protocols for standard VTA trust tasks such as generating VTC invitations, issuing/verifying/revoking DTG VCs, and reading/writing/enforcing VTC governance policies.

The scope of the DTG Credentials project includes developer SDKs and reference implementations of the components necessary to implement DTG Credentials. The initial target audience are developers working and building with DTG Credentials.

# Initial Committers

- [Glenn Gore](https://github.com/stormer78)
- [Geoff Turk](https://github.com/geoffturk)

# Sponsor

- [Drummond Reed](https://github.com/talltree) - Co-Chair of the LFDT ToIP Decentralized Trust Graph Working Group
- [Martina Kolpondinos](https://github.com/martipos) - Co-Chair of the LFDT ToIP Decentralized Trust Graph Working Group

# Pre-existing repository

None
