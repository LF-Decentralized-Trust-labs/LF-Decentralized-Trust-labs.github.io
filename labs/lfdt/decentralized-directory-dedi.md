---
layout: default
title: Decentralized Directory (DeDi)
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name
[Decentralized Directory (DeDi)](https://github.com/LF-Decentralized-Trust-labs/DeDi)

## Short Description
The Decentralized Directory (DeDi) Protocol is envisioned as a global, interoperable specification for accessing public directories. It unifies access to public information published by registrars, regardless of the underlying technology or jurisdiction, providing a standardized, open-source protocol for real-time look-up of any public directory.

## Scope of Lab

The goal of the DeDi Lab is to design, build, and validate a decentralized protocol and open-source reference implementation that enables real-time, global lookup of public registries. We're targeting both the common pain points of Gen‑1 to Gen‑3 directory systems and the fragmentation of APIs and data formats across jurisdictions. This lab will focus on robust architecture, developer tooling, and community adoption to establish trust infrastructure for digital identity, financial services, government directories, and other public‑good registries.

Our work will begin with a core protocol specification, defining URI and payload semantics (e.g., dedi://domain.com/registry-id/{record-id}), security mechanisms, and discovery patterns. This will include:

 * A modular, layered protocol stack that cleanly separates transport, registry metadata, schema validation, and cryptographic verification.

 * Security and trust models, including signed directory manifests, integrity checks, revocation notifications, and key rotation workflows.

Once the specification is established, we'll produce a reference implementation in at least one languages (e.g., JavaScript) plus integration with common registries (e.g. company registrars, CA root stores). Key milestones include:

 * A lightweight SDK for registry providers to publish, sign, and update directory manifests.

 * A client library for real-time lookup, caching, and automated revocation detection.

 * CLI tooling, a web‑based sandbox, and extensible test harnesses to simulate real-world directory use cases at scale.

To drive adoption and interoperability, the lab will also:

 * Publish test vectors, sample data, and interoperability guidelines.

 * Develop community engagement channels, including GitHub repos, discussion forums, and live webinars for implementers.

 * Collaborate with at least one public authority or trustee registry in pilot or staging mode to validate the protocol end‑to‑end.

 * Coordinate with LF Decentralized Trust projects to align with DID, Verifiable Credentials, and decentralized identity ecosystems.

## Initial Committers
- https://github.com/amarts
- https://github.com/pramodkvarma
- https://github.com/surendrasinghs

## Sponsor
- Arun S M (https://github.com/arsulegai)
- Ry Jones (https://github.com/ryjones)

## Pre-existing repository
- https://github.com/finternet-io/dedi


## Advisors from LFDT
- Julian Gordon <jgordon@linuxfoundation.org>
- Hart Montgomery <hmontgomery@linuxfoundation.org>


## Other references

- [Finternet Lab](https://finternetlab.io/)
- [GitHub](https://github.com/dedi-official) for all tools around Decentralized Directory.
