---
layout: default
title: Smoot
parent: Approved Labs
---
### Lab Name

Smoot

### Short Description

An open-source cross-chain interoperability framework. Smoot provides modular, extensible bridge infrastructure for transferring assets and data across heterogeneous blockchain networks.

### Scope of Lab

#### Mission

Smoot is a modular, reusable, vendor-agnostic interoperability framework for homogeneous and heterogeneous chain-to-chain interactions. It is compliant with the Enterprise Ethereum Alliance (EEA)'s DLT Interoperability Specification, reflecting a shared vision for a more open and connected decentralized future. Smoot was built by the [Wanchain](https://www.wanchain.org/) team and released to the open source community as part of [Linux Foundation Decentralized Trust (LFDT)](https://www.lfdecentralizedtrust.org).

An introduction to the framework is published on the LFDT blog: [Meet Smoot: One Framework to Connect All Chains](https://www.lfdecentralizedtrust.org/blog/meet-smoot-one-framework-to-connect-all-chains).

#### Architecture

Smoot's architecture is organized into distinct layers:

- **The Smoot Messaging Layer** – Facilitates the secure exchange of data between distinct decentralized networks while ensuring data integrity and validity at every step.
- **The Smoot Function Call Layer** – Enables the uninterrupted execution of operations across multiple distinct decentralized networks, removing barriers between chains.
- **The Smoot Application Layer** – Orchestrates complex logic and workflows across distinct decentralized networks, unlocking unified cross-chain experiences.

#### Supported standards

Smoot currently supports the following token standards and integration targets:

| Standard / Integration | Status | Notes |
|---|---|---|
| ERC20 | Supported | Fungible token transfers through the bridge framework |
| ERC721 | Supported | NFT transfer support |
| ERC3643 | Supported | Permissioned token support; implemented in a way that is compatible with ERC20-style interactions |

Additional standards and chain integrations may be added based on roadmap priorities, community demand, and partner contributions.

#### Repositories in scope

| Repository | Description |
|---|---|
| [**bridge**](https://github.com/LFDT-Smoot/bridge) | The core bridge implementation — smart contracts, relay agents, SDKs, application interfaces, deployment scripts, and tests. This is where the main development happens. |
| [**governance**](https://github.com/LFDT-Smoot/governance) | Governance documents including the [Smoot Technical Charter](https://github.com/LFDT-Smoot/governance/blob/main/Smoot%20Technical%20Charter%20Final%204-17-2025.md), configuration files, and the license. |

#### Origin and current stage

The initial code migration from Smoot's predecessor project is complete, and the team is actively developing new features and working to grow the contributor community. We are looking for collaborators from organizations interested in cross-chain interoperability — whether you want to integrate a new chain, contribute to the relay infrastructure, or build applications on top of Smoot.

### Alignment with LFDT Mission

Cross-chain messaging and function calls are infrastructure that no single ledger community can supply on its own, and a framework of this kind is only useful if it is neutral ground: participants have to be able to trust the bridge as much as they trust the chains it connects. That makes a vendor-neutral foundation the right home for the work rather than any one company's repository.

Smoot is already developed in the open, under a Technical Charter, the LFDT [Code of Conduct](https://www.lfdecentralizedtrust.org/code-of-conduct), and Apache 2.0 licensing across all repositories. Its compliance with the EEA DLT Interoperability Specification ties it to standards work in the wider Ethereum and enterprise DLT communities rather than to a single vendor's stack.

### Relation to Existing LFDT Labs and Projects

Interoperability is an area with existing work in LFDT, and Smoot is intended to sit alongside that work rather than replace it:

- **[YUI](https://lf-decentralized-trust-labs.github.io/labs/approved/yui.html)** also targets interoperability between heterogeneous ledgers, but builds on the Cosmos Inter-Blockchain Communication (IBC) protocol with extensions for Hyperledger projects. Smoot's messaging layer is not IBC-based, so the two explore different points in the design space.
- **[Harmonia](https://lf-decentralized-trust-labs.github.io/labs/approved/harmonia.html)** captures the constraints and requirements of regulated networks seeking to interoperate, and is primarily design documents, protocol definitions and sample code. Smoot is an implementation, and Harmonia's requirements work is a useful input to it.
- **[Perun](https://lf-decentralized-trust-labs.github.io/labs/approved/perun.html)** is a blockchain-agnostic state channels framework, addressing off-chain scaling rather than asset and data movement between networks.
- **Hyperledger Cacti** is LFDT's general-purpose blockchain integration framework. There is potential overlap in goals, and we would welcome a conversation with the Cacti maintainers about where the two efforts complement each other.

<!-- TODO: maintainers should confirm these characterizations and add any other projects the stewards consider adjacent. -->

### Does this lab produce code?

Yes

### Does this lab produce a specification?

No

Smoot implements the EEA DLT Interoperability Specification rather than producing a specification of its own.

### Pre-existing Repositories

- https://github.com/LFDT-Smoot/bridge
- https://github.com/LFDT-Smoot/governance

### Roadmap

Current and planned areas of development include:

- **Multi-party computation (MPC) for relayers** — Enhancing the relay layer with threshold signatures to remove single-point-of-trust assumptions.
- **Zero-knowledge proof integration** — Adding ZK-based verification for cross-chain state proofs.
- **Additional chain support** — Extending the framework to new networks including Cardano, with further integrations planned based on community demand.
- **Hybrid bridging modes** — Supporting both lock-and-mint and liquidity-pool-based transfer mechanisms.

We welcome community input on roadmap priorities. Please open an issue in the [bridge repository](https://github.com/LFDT-Smoot/bridge/issues) or raise it in our community calls.

<!-- TODO: maintainers should attach concrete milestones and target quarters to the items above. -->

### Additional Information

**Moving from project to lab.** Smoot has been running as an LFDT project with its own Technical Charter. This proposal moves the work into LFDT Labs, which is the better fit for its current stage: the code migration from its predecessor is complete but the contributor community is still being built, and Labs is where that growth is meant to happen before a project stands on its own.

**Getting started.** Review the design documents in [`bridge/design/`](https://github.com/LFDT-Smoot/bridge/tree/main/design) and the docs in [`bridge/docs/`](https://github.com/LFDT-Smoot/bridge/tree/main/docs) to understand how Smoot works, then clone the [bridge](https://github.com/LFDT-Smoot/bridge) repository and follow the setup instructions in its README.

**Contributing.** Contributions of code, documentation, testing, design feedback and use-case ideas are all welcome. Browse [open issues](https://github.com/LFDT-Smoot/bridge/issues) in the bridge repository — particularly those labeled `good first issue` or `help wanted` — introduce yourself on Discord or attend a community call, then open a pull request with a clear description of what you have done and why.
