---
layout: default
title: Proof-of-Process
parent: LFDT Labs
grand_parent: Approved Labs
---
# Lab Name
Proof-of-Process

# Short Description
A protocol and reference implementation for Proof-of-Process (PoP) attestation — cryptographic verification that digital actions originated from human cognitive processes rather than synthetic generation, built on the IETF RATS framework.

# Scope of Lab
Proof-of-Process provides a decentralized, privacy-preserving mechanism for attesting that digital actions were performed through genuine human cognitive effort. It achieves this through behavioral entropy analysis and hardware-backed evidence collection, without relying on centralized biometric databases or surveillance infrastructure.

The lab encompasses four areas: the core PoP attestation protocol, aligned with the IETF RATS architecture (RFC 9334) and its Attester, Verifier, and Relying Party roles; reference implementations for behavioral evidence capture in text composition environments, including keystroke dynamics, pause patterns, and editing trajectories; Verifier components that evaluate attestation evidence against human-process baselines; and integration patterns for C2PA content credentials and decentralized identity systems compatible with CAWG and DIF specifications.

This work addresses a critical gap in decentralized trust infrastructure. Existing identity and attestation frameworks can verify who performed an action but cannot verify whether a human cognitive process was involved in performing it. As AI-driven automation becomes capable of impersonating human activity across text, code, and media, Proof-of-Process provides Sybil resistance and human-presence verification. The project complements existing LFDT efforts in decentralized identity and verifiable credentials — such as Identus and the broader DIF ecosystem — by adding an "evidence of effort" layer beneath the identity layer.


# Initial Committers
- https://github.com/dcondrey

# Sponsor
Seeking sponsor. Hart Montgomery (CTO, LFDT) has reviewed the initial proposal, directed the project to formal GitHub submission, and indicated interest in the underlying research.

# Pre-existing repository
The lab will use a new repository. Related prior work is available at https://github.com/WritersLogic/witnessd, which serves as the basis for the reference implementation to be contributed.
