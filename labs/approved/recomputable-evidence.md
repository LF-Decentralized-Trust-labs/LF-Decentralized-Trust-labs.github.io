---
layout: default
title: Recomputable Evidence
parent: Approved Labs
---
# Recomputable Evidence

## Section 1 — Mission and Scope

### Lab Name
[Recomputable Evidence](https://github.com/Recomputable-Evidence)

### Short Description
A shared test bench for checking whether separate specifications for AI agent evidence still hold up when they are used together.

### Scope of Lab
**The problem.** When an AI agent takes an action — makes a payment, calls a tool, acts for someone — several groups are now writing specifications for the record it leaves behind: who authorized it, what was done, who holds the keys. Each spec can be verified on its own. Real systems combine them: one spec records the authorization, another the payment, a third the custody of the keys. Few combinations have been checked, and each check was set up by one project under its own criteria. The typical failure is quiet: one record accepts another's claim of authority as if it were its own, and the result looks valid when it isn't. There is no shared set of criteria for judging a combination that the specs' maintainers wrote together.

**What the lab does.** It keeps two things in one neutral place:
- **Test cases** that pair records from two different specs and state the expected outcome, including cases that must fail. Anyone can rerun them offline from the published bytes: no hosted service, no account.
- **Criteria** for judging a combination, written jointly by the people who maintain the specs involved, not by any single author.

**What it does not do.** It does not pick a winning spec, does not certify anyone, and does not take over any spec. Each spec keeps its own repository and maintainers.

### Alignment with LFDT Mission
LFDT builds neutral, jointly governed infrastructure. This lab applies that to testing: a place where competing specs are checked against each other under criteria none of them owns.

### Relation to Existing LFDT Labs and Projects
**Agent Authority Conformance** is the closest approved lab. It already hosts cross-stack test families, including one for action-ref and a run of a composition pack. What it does not hold yet is criteria for judging a combination, written jointly by the maintainers of the specs being combined; its vocabulary stays with its maintainer. We propose to collaborate: this lab references test families and run records hosted there by pin instead of copying them, and uses the same record rules (author-produced vs. independent runs, records never removed, a merge is not a verdict), so a record means the same thing in both places. We opened Agent-Authority-Conformance/aps-conformance-suite#121 to discuss it; nothing is agreed yet.

**Proof-of-Control** (verifiable evidence of AI agent behavior) and **Proof-of-Process** (attestation of how a digital action was produced) work nearby. We would like to explore shared test cases with both once this lab is set up.

---

## Section 2 — Lab Details

### Does this lab produce code?
Yes: test cases and a small verifier to run them.

### Does this lab produce a specification?
Not initially. The criteria ship as text alongside the test cases. The specs being tested keep their own licenses and governance; if the criteria later grow into standards work, we will raise that with the stewards as a separate step.

### Pre-existing Repository
https://github.com/giskard09/action-ref-conformance (Apache-2.0). Most of its commits have no DCO sign-off; we will squash the history into one signed-off commit when the lab repository is created.

### Initial Committers
- https://github.com/giskard09
- https://github.com/azender1 (SafeAgent — our integrator partner under a signed Revenue Share Agreement. He recuses from any decision that would directly benefit his own commercial interest.)
- https://github.com/magentixai (Martin Sansone — CEO, Magentix.AI; author of the Enhanced Fraud Data standard, Pay.UK; also steering the x402 Foundation TSC evidence-record charter, a related but separate track)
- https://github.com/kenneives (AgentGraph/AgentAvow; wrote the independence rubric)

### Licensing
☑ I understand that all code hosted in LFDT Labs must be made available under an Apache 2.0 license with DCO sign-off.
☑ I understand that all specification and standards work in LFDT Labs is done under the Community Specification License 1.0 and the rest of the CSL framework.

### Governance Model or Practice
Written down in [GOVERNANCE.md](https://github.com/giskard09/action-ref-conformance/blob/main/GOVERNANCE.md). The core rule: no criterion or test case is merged until a committer other than its author has rerun it from scratch. We already work this way: one committer wrote the first rubric, a second reran it on a fresh clone, and a third found a non-neutral detail that was fixed before merge.

### Security
No formal vulnerability process yet; we will add one before the first release.

### Infrastructure and Tooling
GitHub Actions CI on the seed repository. No mailing list or chat yet.

### Evidence of Adoption and Use Cases
- SafeAgent (azender1, a founding committer) records `action_ref` evidence in production: a live deployment, not a demo.
- The action-ref test family hosted in the Agent Authority Conformance lab was rerun by an outside runner who authored neither the vectors nor the implementation, recorded there as independent (commit a7aa94f).
- The JSON canonicalization fixtures one committer published (magentixai/axes, `portable/jcs-properties`) were checked against an independent library, `rfc8785` 0.1.4: 4 of 4 agree.

### Roadmap
Next 6 months: settle the collaboration with Agent Authority Conformance; publish the first paired test case between two separately maintained specs; add a vulnerability process.
