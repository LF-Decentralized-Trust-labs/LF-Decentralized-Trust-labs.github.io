---
layout: default
title: DAS Interoperability Lab
parent: LFDT Labs
grand_parent: Active Labs
---
# DAS Interoperability Lab

# Short Description
A neutral, open-source standards and pilot body dedicated to operationalizing the frameworks outlined in the whitepapers [_Building the Path Towards Digital Asset Securities Interoperability (DASI)_](https://www.dtcc.com/-/media/interoperable-digital-asset-securities-white-paper.pdf) and [_Digital Assets Securities Control Principles (DASCP)_](https://www.euroclear.com/content/dam/euroclear/news%20&%20insights/Format/Whitepapers-Reports/Euroclear_Digital_Assets_DASCP_Whitepaper.pdf). The lab aims to produce implementable digital asset securities specifications and validate them through live proofs-of-concept on real institutional infrastructure.

# Scope of Lab
The DAS Interoperability Lab has a dual mandate designed to address the fragmentation in capital markets:

* **Standards Development:** The Lab produces infrastructure-neutral digital asset securities specifications anchored to the DASI whitepaper's five capital market foundations and 29 building blocks. These standards will include conformance criteria and are designed to meet the requirements of the DASCP framework. Additionally, the lab will produce reference technical interfaces covering both on-chain and off-chain components, tied to concrete DLT stacks (e.g., EVM, Solana, DAML).
* **Pilots and Proofs-of-Concept:** The Lab runs live, chain-agnostic pilots on identified use cases to validate and refine standards before publication. Initial Phase 1 use cases would include (may be subject to change) US equity settlement finality, corporate actions on tokenized European sovereign bonds, and collateral management and digital twin substitution. The feedback loop ensures that any specification failing a pilot is revised rather than published.

### Differences with the OTAS Lab
While both the DAS Interoperability Lab and the existing Open Tokenized Asset Standards (OTAS) Lab share a protocol-agnostic approach and define smart contract interfaces for digital assets, their distinct scopes, methodologies, and technical focuses necessitate parallel tracks.
Following is an overview of the main differences between the 2 labs, based on the [OTAS description](https://lf-decentralized-trust-labs.github.io/labs/approved/otas.html). 

**I. Scope and Technical Focus**

| Dimension | DAS Interoperability Lab (Proposed) | OTAS Lab (Active) |
| :--- | :--- | :--- |
| **Core output** | Functional specifications, interface definitions, and live institutional pilots to drive market adoption. | Focused on production-grade on-chain smart contract reference implementations for academic or research purposes. |
| **Initial Tech Stack** | Hedera (Hashgraph) and HashSphere. | Ethereum (EVM) and SUI blockchain protocols. |
| **Asset focus (initially)** | Equities (settlement finality), corporate actions on bonds, and collateral management. | Sovereign bonds, tokenized deposits, and IoT-linked assets. |

**II. Methodology and Priorities**
* **DAS Interoperability Lab:** Rooted explicitly in the DASI and DASCP whitepapers published by DTCC, Clearstream, Euroclear, and BCG. It uses these frameworks to actively define, prioritize, and resolve specific digital assets requirements and interoperability frictions. 
* **OTAS Lab:** Guided by surveying existing on-chain token standards to identify interoperability gaps, focusing primarily on establishing an auditable, on-chain foundation rather than explicitly responding to the aforementioned theoretical frameworks.

# Initial Committers
https://github.com/adovale-IOB
https://github.com/kshitishb

# Sponsor
N/A

# Pre-existing repository
N/A
