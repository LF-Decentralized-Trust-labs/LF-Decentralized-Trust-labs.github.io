# Lab Name

[OpenReagent](https://github.com/OpenReagent)

# Short Description

OpenReagent is a toolkit and open standard for extracting vulnerability signatures from audits, enabling fast detection and structured sharing across smart contract ecosystems.

# Scope of Lab

This lab aims to build a toolkit that ingests security artifacts such as audit reports, incident analysis, and Proof-of-Concept (PoC) exploits, automatically extracts vulnerability signatures from them, and enables fast validation within the smart contract development lifecycle. Ultimately, OpenReagent seeks to evolve into an industry-grade platform for structured and secure sharing of smart contract vulnerability intelligence.

We will proceed in the following phases:

- Phase 1: This phase establishes the technical foundation for audit-driven behavioral vulnerability signatures and demonstrates their effectiveness. We design preset signature templates for selected vulnerability classes and implement PoC-execution–based signature extraction, including trace slicing of minimal vulnerability-relevant paths and IR-level canonicalization for portability. An LLM-assisted pipeline derives candidate signatures from newly published audit reports. Detection accuracy and false-positive reduction are evaluated using large-scale on-chain datasets and benchmark contracts, together with patch-based exclusion and witness-backed validation to ensure reproducible and verifiable results.
- Phase 2:  This phase transforms the extracted signatures into an enterprise-ready operational package and establishes a standardized validation framework. Verified signatures are curated into structured, deployable bundles aligned with real deployment contexts, supported by versioning and controlled release management. A standardized signature format compatible with ecosystems such as OSV/VEX is defined, with integration interfaces for CI/CD and DevSecOps pipelines. To address confidentiality requirements, we incorporate a privacy-preserving validation pipeline that enables cross-organization verification of analysis results without requiring disclosure of underlying source code, execution traces, or proprietary artifacts. The architecture separates shareable signature representations from internal analysis context and is designed to support confidential validation of both fixed-form outputs and more general, arbitrarily structured analysis signatures, while maintaining practical deployability in enterprise environments.
- Phase 3: This phase advances technical expansion and cross-organization consensus. We extend support to additional blockchains and intermediate representations to enable broader multi-chain applicability. Building upon the privacy-aware architecture introduced in Phase 2, we further expand the framework toward richer behavioral signatures and generalized confidential validation mechanisms, enabling secure verification of complex analysis artifacts without exposing sensitive internal data. This phase also promotes structured collaboration among security organizations to establish shared validation practices and governance models for secure vulnerability intelligence exchange.

We are currently in Phase 1, developing and testing PoC-execution–based behavioral signature extraction. Our focus includes trace slicing for minimal vulnerability-relevant paths, IR-level canonicalization, patch-based exclusion logic, and witness-backed validation for reproducible detection results.

# Initial Committers

- https://github.com/superkimchi
- https://github.com/jisupark

# Sponsor

N/A