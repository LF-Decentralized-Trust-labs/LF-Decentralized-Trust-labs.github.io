---
layout: default
title: PDP-Connect
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name

PDP-Connect

## Executive Summary

- People's data sits locked inside platforms. They cannot move it or share it on their own terms, even though the regulation says they should be able to.
- No common technical standard exists for how that portability actually works. Every platform does it differently. Most applications do not bother.
- This Lab proposes one: the Personal Data Portability Protocol (PDPP), an open standard for how a user authorises any application to access their personal data and how that authorisation is enforced.
- AI that serves people rather than platforms needs to be grounded in real human context, with real human consent. PDPP makes that technically possible.
- This will be hosted by the Linux Foundation Decentralized Trust as we gather feedback and refine the standard's terms.
- Think open banking, but for all personal data.

# Short Description

An open standard and reference implementation for personal data portability. The Personal Data Portability Protocol (PDPP) defines how a user authorises any application to access their personal data, and how that authorisation is enforced, using standard OAuth 2.0 flows.

# Scope of Lab

## The problem

People generate data across dozens of platforms daily: health apps, social networks, financial services, productivity tools. That data belongs to them in a legal sense. In practice, they cannot access most of it, cannot move it between services, and cannot consent to its use in any technically enforceable way.

Regulation has tried to address this. GDPR Article 20 gives users the right to data portability. The EU Digital Markets Act requires large platforms to provide continuous data access. What still does not exist is a common, open standard for the consent and authorisation layer: how a user specifies exactly what they are sharing, with whom, under what terms, and how that decision is technically enforced across any platform or service.

Without that layer, portability remains fragmented. Each platform implements it differently. Applications that want to work with personal data across multiple sources must build custom integrations for every one. AI systems that could benefit from real personal context instead work with scraped public data or are locked out entirely. The gap is not in the mechanics of data transfer. It is in the authorisation infrastructure that sits upstream of any transfer and makes it trustworthy.

PDPP addresses this gap at a different layer from existing portability infrastructure. The Data Transfer Initiative (DTI) handles the mechanics of how data moves between services. Solid, developed by Sir Tim Berners-Lee, addresses where personal data lives and how it is stored. OAuth 2.0 handles whether an application is permitted to access a resource. PDPP handles what sits across all three: the consent and authorisation layer that specifies what the user has agreed to share, with whom, and under what terms, and how that agreement is enforced. It is designed to work with each of them, not replace any of them.

This is more urgent as AI becomes central to how people interact with software. AI grounded in real, consented personal context serves people better and more accurately than AI trained on public data alone. PDPP provides the technical layer through which that consent is expressed, verified, and enforced.

## What PDPP is

The Personal Data Portability Protocol (PDPP) v0.1.0 is a vendor-neutral open standard that defines the consent and authorisation layer for personal data portability. It specifies how a user grants an application access to specific personal data and how a server enforces that grant.

The protocol is built on OAuth 2.0 and RFC 9396 (Rich Authorisation Requests). Any organisation capable of serving HTTP can implement it. It has no dependency on any specific infrastructure, token, or network.

PDPP has five components:

- **Record model**: defines what personal data looks like in a portable format. A flat schema with typed fields and primary keys that any data source can produce and any application can consume.
- **Selection request**: how an application specifies exactly what data it wants and why, before the user sees a consent screen. Built on RFC 9396, integrating with existing OAuth flows.
- **Grant**: the consent artifact. An immutable record of exactly what the user approved: which data, which fields, under which stated purpose. Cryptographically bound and not modifiable after issuance.
- **Connector manifest**: how a data source declares what it can share. A machine-readable description of available data types, schemas, and the purposes for which data may be requested.
- **Resource server interface**: the HTTP API through which authorised data is served. Any server implementing this interface is PDPP-compliant.

A user sees a clear consent screen, approves a specific request, and the data flows under enforceable, auditable terms. No platform intermediary required.

PDPP operates at a different layer from DTI. DTI handles the mechanics of how data moves between services. PDPP handles the consent and authorisation that must precede any transfer: what the user has agreed to share and under what terms. The two are complementary. Appendix B of the PDPP specification sets out the technical boundary in full.

## Reference implementation

PDP-Connect demonstrates PDPP working against real data sources.

**Data Connect** is a desktop application that runs entirely on the user's machine. It authenticates with data sources using a local browser, extracts data into PDPP-compliant format, and stores it locally by default. Nothing leaves the device without the user's instruction. Apache 2.0 licensed.

**Personal Data Connectors** is a library of connectors, each implementing the PDPP connector manifest interface for a specific platform. Each connector's bundled manifest defines its runtime requirements and data model. Data Connect parses the manifest, validates its requirements, and orchestrates data collection automatically or with assistance from the user per the manifest's requirements. Current connectors: Spotify, Google, Instagram, ChatGPT, Apple Health, GitHub, LinkedIn, and Oura. Adding a connector for a new platform is designed to take approximately 10 minutes.

## Governance

All changes to the connector library and the specification go through the LFDT process: public pull requests, maintainer review, and an RFC comment period for schema changes. The initial maintainers are Anna, Tim, and Art Abal.

Governance documents (GOVERNANCE.md, CONTRIBUTORS.md, and schema RFC templates) will live in the LFDT-hosted repository.

Vana Foundation will lead the initial setup and implementation of the Lab. As the standard matures and the community grows, governance will expand to include external contributors and maintainers. PDPP is designed to be infrastructure-neutral and compatible with multiple networks, including the Vana network, as one implementation among many.

### Relationship to Solid

Solid, the decentralised data protocol developed by Sir Tim Berners-Lee and standardised through the W3C, returns personal data to users: stored in user-owned pods, portable, and accessible on the user's terms. PDPP extends this work into the consent and authorisation layer. Where Solid defines where data lives and how it is stored, PDPP defines how a user grants an application access to specific records under a stated purpose, with that grant cryptographically enforced.

The two protocols address different parts of the same problem. PDPP is built on the same standards-based, open principles as Solid, and on the same conviction that people should control their own data. We are in conversation with contributors to the Solid ecosystem and welcome their participation in the PDP-Connect Working Group.

### Relationship to the Data Transfer Initiative

The Data Transfer Initiative (DTI), whose members include Apple, Google, and Meta, has built practical infrastructure for data portability at scale: a Data Trust Registry that enables platforms to verify trusted data recipients and unlock access to their portability APIs.

PDPP extends this work into the consent and authorisation layer. Where DTI focuses on the mechanics of how data moves between services, PDPP focuses on the agreement that must precede any transfer: what the user has consented to share, with whom, and under what terms, and how that agreement is technically enforced. The two protocols operate at different layers and are designed to work together.

We are in conversation with the Data Transfer Initiative and welcome their participation in the PDP-Connect Working Group.

### Relationship to OAuth 2.0

PDPP is built on OAuth 2.0 and does not replace it. OAuth 2.0 handles authorisation between an application and a resource server: whether an app is permitted to access a resource. PDPP uses this as its authorisation transport and proposes to extend it with a structured purpose declaration in the request, and a persistent consent artifact that records what the user approved, for what purpose, and when.

Standard OAuth 2.0 tokens are typically ephemeral. PDPP proposes a grant that is auditable and durable. The design intent is for it to be storage-agnostic, with no mandate on where it lives.

We are seeking community input on both the purpose declaration model and the persistence design through the PDP-Connect Working Group.

## Fit with LFDT's mission

LFDT exists to host open-source infrastructure for decentralised trust: identity, data governance, verifiable credentials, and the standards that connect them. PDPP sits squarely in this space.

The LFDT ecosystem already addresses how people prove who they are and how trust is established between parties. Trust Over IP defines the architecture for internet-scale digital trust. AnonCreds provides privacy-preserving verifiable credentials. LFDT projects provide the underlying ledger and smart contract infrastructure. What is missing is the layer that governs personal data itself: how a user specifies what they are sharing, with whom, and under what terms, and how that decision is enforced.

Identity and data feed each other. A person's activity and data across platforms is part of their digital identity. It is how trust relationships are built, how context is verified, and how AI systems understand who they are serving. Without consent-governed data portability, that context stays locked inside platforms and unavailable to the trust infrastructure LFDT is building. PDPP is the layer that makes personal data portable and consent-governed, so that it can flow into identity systems, AI applications, and trust graphs on the user's terms.

PDPP belongs in LFDT because a neutral open standard for this layer needs to be governed by its community, not by any single company. Hosted under the Linux Foundation, it becomes citable by regulators, implementable by any organisation, and governed through an open process.

## What is out of scope

- Any chain-specific infrastructure
- Commercial products built on top of the protocol

# Initial Committers

- [https://github.com/annakaz](https://github.com/annakaz) — Anna, Technical Lead
- [https://github.com/tnunamak](https://github.com/tnunamak) — Tim, Spec Architect
- [https://github.com/artvana](https://github.com/artvana) — Art Abal, Project Director

# Sponsors

- Sheila Warren — formerly CEO, Project Liberty
- Tricia Wang — CEO, Advanced AI Society
- Michael Casey — Advanced AI Society
- Justin Slaughter — Paradigm VC
- Lisa Dusseault* — CTO, Data Transfer Initiative
- Gavin Starks — founding CEO, Open Data Institute; co-chair, UK Open Banking Standard
- Drummond Reed* — co-author, Self-Sovereign Identity; Trust Over IP
- Prof. James Mickens — Harvard University, Computer Science
- Brandon Miller — Berkman Klein Center, Harvard
- Meg Marco — Berkman Klein Center, Harvard
- Ramesh Raskar — MIT Media Lab

\* = TBC

# Pre-existing repository

The following repositories are being audited and prepared for contribution to the LFDT Labs organisation:

- [https://github.com/vana-com/pdpp](https://github.com/vana-com/pdpp) (currently private)
- [https://github.com/vana-com/data-connect](https://github.com/vana-com/data-connect)
- [https://github.com/vana-com/data-connectors](https://github.com/vana-com/data-connectors)

Because these repositories' histories do not carry DCO sign-offs, we plan to copy the code into the new lab repositories as squashed, signed-off initial commits after the project has been approved, instead of transferring the repositories themselves.
