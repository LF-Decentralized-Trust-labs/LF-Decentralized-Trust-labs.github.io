---
layout: default
title: Agent Authority Conformance
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name
Agent Authority Conformance

# Short Description
Conformance vectors, verifier adapters and reproducible run reports for agent identity, delegated authority, signed decision receipts, attribution and provenance. The initial corpus targets the Agent Passport System.

# Scope of Lab
This lab hosts conformance material for agent authority and the evidence produced under it: versioned test vectors, verifier adapters, negative and adversarial cases with declared expected outcomes, and reproducible reports from runs against the corpus. Each corpus release identifies the protocol revision it targets. Lab code, vectors, schemas and documentation are Apache 2.0, and imported material retains its required notices and attribution.

The lab does not govern or amend the Agent Passport System specification, and nothing merged here transfers its stewardship. APS remains specified outside the lab in IETF Internet-Draft draft-pidlisnyi-aps, and the reference SDKs remain in their existing repositories. The lab may define the non-normative schemas, runner interfaces and report formats it needs to execute and report the tests.

The lab does not certify or endorse products. Reports distinguish runs performed by the protocol author from runs performed by independent parties, and no reference implementation or commercial product receives special standing.

On fit with LF Decentralized Trust: the identity and verifiable-credential work hosted here runs into the problem this corpus exists to check, which is separate implementations having to produce and accept the same signed structures before anything interoperates. Authority delegated to AI agents raises that requirement at a newer layer. Neutral hosting separates who publishes a protocol from who publishes evidence about it, and the reports distinguish author-run from independent results so that participation is visible rather than assumed.

The starting corpus is the public Apache 2.0 suite at https://github.com/aeoess/aps-conformance-suite. It covers canonical byte encoding, agent identity, scoped delegation, decision receipts, attribution, instruction provenance and negative cases, together with cross-implementation parity checks.

Additional agent-authority specifications may be proposed later, each with a defined normative target, a contributed corpus and an identified maintainer. Their results stay distinguishable from APS results.

# Initial Committers
- https://github.com/aeoess

# Sponsor
- Arun S M - https://github.com/arsulegai - chair, LF Decentralized Trust Technical Advisory Council

# Pre-existing repository
Yes: https://github.com/aeoess/aps-conformance-suite (Apache 2.0). Its existing history does not meet the DCO sign-off requirement, so it would not be transferred. Subject to steward guidance and a provenance review, eligible material would be imported into a new lab repository as a single signed-off initial commit, with required notices and third-party attribution preserved.
