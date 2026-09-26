---
layout: default
title: Blockchain Decentralisation Index
parent: Approved Labs
---
### Lab Name

[Blockchain Decentralisation Index](https://github.com/Blockchain-Decentralisation-Index)

### Short Description

Open source tool kit for measuring the decentralisation of distributed ledgers, layer by layer — consensus, tokenomics, network, software, and beyond.

### Scope of Lab

The lab develops and maintains a suite of open source tools that collect data from live blockchain systems, parse it into a common format, and compute decentralisation metrics over it. Each tool targets a distinct layer of the stack and shares a common pipeline architecture (collect → parse → map to entities → apply metrics → publish).

The metrics themselves are drawn from several disciplines — economics (Gini, Nakamoto coefficient, HHI), information theory (entropy), and network science — and are applied uniformly across systems so that results are comparable across chains and over time rather than being one-off measurements of a single network.

Our mission is to make the decentralisation of a distributed ledger a measurable, reproducible, comparable property rather than a marketing claim — and to keep the methodology and the code that implements it in the open, where anyone can audit, criticise, and extend it.

Origin and history. The work began at the Blockchain Technology Laboratory in the School of Informatics at the University of Edinburgh, as the Edinburgh Decentralisation Index (EDI), a research project studying blockchain decentralisation from first principles. The first tool was released publicly in 2024, followed by a public dashboard and a growing set of peer-reviewed publications underpinning the methodology. 


### Alignment with LFDT Mission

LFDT exists to advance open, multi-party systems built on decentralised technology. Decentralisation is the property that the entire premise rests on — and across the ecosystem it is asserted far more often than it is measured. There is still no universally accepted methodology for quantifying how decentralised a system actually is, which means claims are easy to make. but difficult to compare and to falsify.

We believe that LFDT is the right home for this lab for two reasons:

First and foremost, neutrality. Vendor-neutral foundation governance is exactly the structure this kind of work needs, in the same way it is the structure that benchmarking and conformance efforts need generally.

Second, it is cross-cutting infrastructure for LFDT's existing portfolio. The metrics are not chain-specific. The same pipelines that measure public chains can be pointed at consortium and permissioned networks. Extending the tooling to networks built on LFDT projects is one direction that the project could take if adopted by the foundation.

### Relation to Existing LFDT Labs and Projects

No existing LFDT lab or project measures decentralisation. The closest structural analogue is Hyperledger Caliper, which benchmarks the performance of blockchain systems; this lab does for decentralisation what Caliper does for throughput and latency. The two are complements, not competitors, and address the two properties most often claimed without evidence.

Elsewhere in the ecosystem, decentralisation measurement tends to appear as one-off academic papers, single-chain dashboards maintained by that chain's own community, or closed analytics products whose methodology cannot be inspected. What distinguishes this work is the combination of: coverage of multiple layers rather than a single headline number; a common pipeline applied uniformly across heterogeneous systems; peer-reviewed and published methodology, which allows everyone to reproduce it.

### Does this lab produce code?

Yes

### Does this lab produce a specification?

No

### Pre-existing Repository

https://github.com/Blockchain-Technology-Lab/consensus-decentralization

### Initial Committers

- Christina Ovezik, University of Edinburgh, https://github.com/LadyChristina
- Zeeshan Jan, University of Edinburgh, https://github.com/ZeeshanJan
- Laura Antunes, University of Edinburgh, https://github.com/LauraAntunes1

### Sponsor

Bob Blessing-Hartley - Governing Board Member
https://github.com/bobblessinghartley 

### Governance Model or Practice

To date the work has been run as a university research project — decisions made internally by the EDI team at Edinburgh, under a published research-independence policy governing our funding relationships (https://informatics.ed.ac.uk/blockchain/edi/research_independence).

Entering the lab is the point at which we want to move to an open governance model. We would publish a GOVERNANCE.md on onboarding establishing a maintainer group (initially the committers above, with additions by maintainer consensus on demonstrated contribution) and ordinary changes by pull request with review from someone other than the author.

### Infrastructure and Tooling

To date the tooling has run on university infrastructure: self-operated full nodes for some networks (Bitcoin, Ethereum, Cardano and others) as data sources, alongside public datasets such as Google BigQuery's blockchain datasets, with dataset archival and distribution through the Edinburgh International Data Facility (EIDF). CI is GitHub Actions; the dashboard is hosted at a university server.

We envision that as part of LFDT we would move away from the university's infrastructure and replace it with an archival and distribution route that requires no university access.

### Evidence of Adoption and Use Cases

Public dashboard presenting decentralisation trends across systems and over time: https://blockchainlab.inf.ed.ac.uk/edi-dashboard/
Peer-reviewed publications underpinning the metrics and methodology: https://informatics.ed.ac.uk/blockchain/edi/publications
Archived public datasets via EIDF, enabling independent recomputation of published results.

Use cases include: regulators assessing whether a system is sufficiently decentralised to fall inside or outside a given regime; participants choosing between chains on the basis of concentration risk; researchers building on or contesting the methodology; project communities tracking whether their own decentralisation is improving or eroding over time.

### Contact name(s) and email(s)

Christina Ovezik christina.ovezik@ed.ac.uk, Mojtaba Tefagh m.tefagh@ed.ac.uk
