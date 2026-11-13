---
layout: default
title: Circulattice
parent: Approved Labs
---
### Lab Name

[Circulattice](https://github.com/Circulattice)

### Short Description

An open-source toolkit for constrained multilateral obligation netting, independent result verification, and liquidity-aware settlement research across conventional and tokenized financial infrastructure.

### Scope of Lab

Circulattice proposes an open, ledger-neutral research and engineering toolkit for computing and testing feasible offsets among financial payment obligations. Given a network of obligations and explicit participant, agreement, currency, and operational constraints, its goal is to compute feasible netting solutions, independently check their compliance with those constraints, and study their effect on funding needs, settlement timing, and reliability.

The work originates from research undertaken by AksumLabs OÜ, an Estonian private limited company focused on advanced software and financial infrastructure engineering. The existing private development system includes a working constrained-netting solver, a separate feasibility verification path, experiments in liquidity-aware scheduling and rolling operation, and modelled failure/recovery behavior. Internal test and benchmark artifacts exist, but the public project does not yet have independently reproducible published results, institutional adoption, or a production release. Some research components remain outside a clean, unified release.

The proposed initial contribution is deliberately narrower than the private research system: a self-contained, properly licensed reference netting engine, a separate checker for declared feasibility invariants, synthetic obligation datasets, reproducible baseline comparisons, and clear documentation of mathematical assumptions and failure cases. Follow-on research may cover liquidity constraints, queueing and deadline tradeoffs, incremental/rolling scenarios, and reference interfaces to simulated RTGS and permissioned-DLT environments.

Open problems are part of the proposed work. The current internal implementation has not demonstrated a consistent advantage over a strengthened conventional comparison baseline, some development workloads exceeded their performance budget, and operational and specification questions remain unresolved. The Lab seeks to make such tradeoffs visible and testable rather than claiming they have been solved.

The project would neither move real funds nor issue digital currency. It would not provide production-grade settlement assurances, legal finality determinations, regulatory certification, or an institution-approved payment system.

### Alignment with LFDT Mission

Trustworthy digital financial infrastructure benefits from interoperable components whose constraints, decisions, and limitations can be independently inspected. Circulattice seeks to make settlement-obligation optimization auditable and reusable rather than embedded in a particular ledger, financial institution, or proprietary workflow.

The Lab would complement the LFDT ecosystem's work on distributed ledgers, tokenization, interoperability, and financial applications by addressing the computational layer before settlement: determining which obligations may be offset under stated constraints and how the resulting decisions can be verified. LFDT Labs is an appropriate venue to test this work in public, invite independent engineering contributions, develop transparent governance, and discover practical integration points without presenting a research prototype as a mature project.

### Relation to Existing LFDT Labs and Projects

- CBWeb3: explores tokenized central-bank money, cross-border payment-versus-payment, and interoperable settlement workflows. Circulattice would focus on constrained pre-settlement obligation optimization and verification, not currency issuance or an alternative CBDC network. Possible integration would be explored only after interfaces and safety assumptions are agreed.
- Hyperledger Cacti: develops cross-ledger interoperability and transaction coordination. Circulattice is not a replacement for connectors or an interoperability protocol; it could later expose results through adapter interfaces for settlement simulators.
- VeltoraCore: concerns on-chain market/liquidity optimization. Circulattice's target domain is institutional payment obligations subject to participant and settlement constraints, not automated-market-maker execution.

Traditional multilateral netting, liquidity-saving mechanisms, and maximum-circulation methods have substantial prior art. The proposed novel contribution, if validated, would be in the open research methodology, verification architecture, constraints, and interoperable implementation rather than the invention of netting mathematics

### Does this lab produce code?

Yes

### Does this lab produce a specification?

No

### Initial Committers

https://github.com/amanhij — Aman.H

### Licensing

- [x] I understand that all code hosted in LFDT Labs must be made available under an Apache 2.0 license with DCO sign-off.
- [x] I understand that all specification and standards work in LFDT Labs is done under the Community Specification License 1.0 and the rest of the CSL framework.

### Governance Model or Practice

The proposed Lab would begin with an identifiable initial maintainer, public GitHub issues, transparent design discussions, and reviewed pull requests. Changes affecting financial semantics, supported invariants, or benchmark methodology would require an issue or proposal explaining assumptions, alternatives, and tests. Maintainers would publish contribution guidance, a code of conduct, security reporting instructions, and a documented path for adding independent maintainers as the community grows.

### Security

This is research-stage software, not an externally audited financial system. Existing internal verification and tests do not constitute a security certification. The initial public release will require a defined threat model, input validation and bounds checking, dependency/license review, secret scanning, a responsible vulnerability disclosure channel, CI checks, and documented limitations. Deterministic arithmetic, independent feasibility checks, and adversarial synthetic cases are priorities. An OpenSSF Best Practices badge and third-party audit are not currently claimed.

### Infrastructure and Tooling

The private research environment has reported test, benchmark, and package-build workflows, which will be revalidated before public claims. Proposed public infrastructure is an LFDT-hosted GitHub repository, issue and review workflows, Apache-2.0 licensing with DCO, automated tests, reproducible example datasets, a documented command-line demonstration, benchmark scripts, and versioned releases. Initial scenarios can run locally against synthetic data; no live financial-network connection or dedicated infrastructure is necessary for the first phase.

### Evidence of Adoption and Use Cases

No external institutional adoption, live-bank deployment, paid production use, or public independent assessment is claimed. The work has been used internally for engineering research and synthetic scenarios; the current evidence remains private and requires revision-specific validation before public publication.

Research use cases include multilateral offsetting of institutional payment obligations; analysis of liquidity-versus-deadline tradeoffs; comparison of conventional and constrained netting strategies; studies of queueing and rolling settlement; and simulation of obligations involving tokenized deposits, wholesale central-bank money, or permissioned financial ledgers.

### Roadmap

Months 1–3 : Open baseline: settle the public contribution boundary and licensing; define input constraints and arithmetic assumptions; publish a small reference solver, independent feasibility checker, synthetic examples, and initial governance/security documents, subject to rights clearance.

Months 4–6 : Reproducible comparisons: publish fixed datasets and comparator definitions; run transparent baseline tests; report where optimization matches, improves on, or underperforms alternatives; specify performance and verification budgets.

Months 7–9 : Operational research: investigate settlement queue and deadline interactions, rolling/incremental netting, participant behavior, and bounded fault/recovery scenarios. Define what a verifier can and cannot establish.

Months 10–12 : Community and interoperability: invite external review and contributions; explore one thin adapter to a simulated RTGS or permissioned-DLT environment if justified; refine documentation and governance; decide whether expanded LFDT project status is warranted.

### Existing Name and Logo

“Circulattice” is a proposed new Lab identity. There is no known existing Lab-specific logo, account, or registered trademark being offered with this proposal. The underlying research originated at AksumLabs OÜ, whose corporate name, logo, website, unrelated accounts, confidential materials, and private codebase are separate and are not being proposed as Lab assets. The suggested name remains subject to trademark and LFDT naming review.

### Trademark and Accounts Signoff

- [x] If the lab is accepted, I agree to donate all related trademarks and accounts to the LFDT.
