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

**Operating constraints.** These bind the lab and its maintainers.

1. The lab certifies nothing. It issues no conformance verdicts and does not present its own outputs as verdicts.
2. Each vector records its origin and the draft revision it targets. Each published run records who executed it and against which implementation. It also records whether the run was author-produced or independently produced.
3. The absence of an independent run does not block a release. The release record discloses that absence.
4. A maintainer decision is not described as peer agreement or as consensus because it was merged.
5. A vector is marked disputed when a public issue identifies either a reproducible divergence or a conflict with the pinned draft revision. A demonstrated defect in the vector qualifies on the same terms. It stays disputed until the issue resolves on public technical evidence or on clarification of the specification, and where that clarification comes from a draft revision authored by the lab maintainer, the dispute record says so.
6. Committer access follows the contribution criteria below. There are no automatic seats, and nobody is listed as participating before they have accepted.

No reference implementation and no commercial product receives special standing. The lab repository and its releases and reports are not used to promote any implementation.

**Shared review.** When the repository has at least two committers who have accepted ongoing maintenance responsibility, removing a vector's disputed status or publishing an aggregate result summary requires review by a committer other than the author of that change. Where that review is unavailable the vector stays disputed or the summary omits it. Raw run reports and unrelated releases are not blocked.

**Committer criteria.** Access is earned by sustained contribution to the suite rather than by running it.

- A record of merged contributions to the corpus or to its runners and report tooling, sustained across at least two release cycles.
- Contributions that keep author-produced and independently produced results distinguishable under the provenance rules above.
- Explicit acceptance of ongoing maintenance responsibility, recorded in the repository before the seat is granted.

Running the corpus and publishing results is welcome from anyone and does not by itself confer committer access. A committer may be moved to emeritus status after a sustained period without activity, which returns the repository to the single-maintainer state described above.

On fit with LF Decentralized Trust: the identity and verifiable-credential work hosted here runs into the problem this corpus exists to check, which is separate implementations having to produce and accept the same signed structures before anything interoperates. Authority delegated to AI agents raises that requirement at a newer layer. Neutral hosting separates who publishes a protocol from who publishes evidence about it, and the reports distinguish author-run from independent results so that participation is visible rather than assumed.

The starting corpus is the public Apache 2.0 suite at https://github.com/aeoess/aps-conformance-suite. It covers canonical byte encoding, agent identity, scoped delegation, decision receipts, attribution, instruction provenance and negative cases, together with cross-implementation parity checks.

Additional agent-authority specifications may be proposed later, each with a defined normative target, a contributed corpus and an identified maintainer. Their results stay distinguishable from APS results.

# Initial Committers
- https://github.com/aeoess

# Sponsor
- Arun S M - https://github.com/arsulegai - chair, LF Decentralized Trust Technical Advisory Council

# Pre-existing repository
Yes: https://github.com/aeoess/aps-conformance-suite (Apache 2.0). Two things need handling on import. The existing history carries no DCO sign-offs. It also includes a third-party contribution of negative-path vectors at commit `381885a` whose attribution needs to be preserved. The import method is for steward guidance rather than something settled here.
