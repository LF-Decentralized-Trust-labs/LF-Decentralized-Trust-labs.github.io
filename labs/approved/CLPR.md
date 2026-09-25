---
layout: default
title: CLPR
parent: Approved Labs
---
### Lab Name

[CLPR](https://github.com/LFDT-CLPR)

### Short Description

CLPR ("Clipper") is an extensible **C**ross **L**edger **PR**otocol that enables reliable, asynchronous, in-order message passing between independent ledger networks without bridges, pooled liquidity, or intermediary validator networks.

### Scope of Lab

The mission of the CLPR LFDT Lab is to provide a place where people in the broader blockchain community can come together and collaborate on:

1. The CLPR specification
2. The reference implementations of the CLPR Service, Verifier Contracts, and CLPR Endpoint relays. 
3. CLPR Application development
4. Native integrations of CLPR implementations into different types of ledgers. 

The ideas behind CLPR stem from the proposals and approaches to cross-ledger communication advocated by Dr. Leemon Baird, co-founder of Hedera, and designer of the Hashgraph consensus algorithm.

CLPR initially grew out of the need and desire to facilitate fast asynchronous Byzantine Fault Tolerant (aBFT) interledger communication between Hiero based networks such as Hedera Mainnet and private HashSpheres. By introducing Verifier Contracts as the anchors of trust on communication Channels, we were able to create an extensible pattern that can support arbitrary trust paradigms and ledger data formats.

Pursuant to its agreement with the Hedera Governing Council, Hashgraph has created the initial CLPR Specification and developed an initial implementation of the CLPR specification, integrated as a native service within the Hiero consensus node. We have also implemented CLPR Service smart contracts which can be deployed to any EVM network along with prototype CLPR Endpoints which can build state-proven bundles for Besu networks. The code and documents for these elements have been open sourced. 

The Hedera Governing Council wants to donate CLPR to be incubated as an LFDT Lab project, stewarded and developed further by Hashgraph and the community of CLPR adopters. The Hedera Governing Council will donate the brand and trademark to the LFDT if the Lab proposal is accepted.

The following codebases are provided as the initial OSS for CLPR:

- https://github.com/hiero-hackers/CLPR-spec
  - This repository contains the core CLPR specification detailing the behavior of all components and the common data structures and formats.
  - This repository has a subdirectory called ADR which contains documented proposals for how the spec has evolved prior to donation to the LFDT.
  - The CLPR specification will likely go through a couple more changes to polish out some rough edges.
- https://github.com/hiero-hackers/clpr-smart-contracts
  - This repository contains both the CLPR Service smart contracts and the Verifier smart contracts written in Solidity and are deployable to Besu.
  - If this repository remains as the location where both the CLPR Service and Verifier smart contracts live for all chains, it will likely need to be reorganized by chain type.
- https://github.com/hiero-hackers/clpr-evm-endpoint
  - This repository contains a Java implementation of the CLPR Endpoint that is able to read EVM chain state and submit EVM transactions to Besu networks. It is implemented to manage the trust anchor updates for Besu QBFT consensus in remote Verifier Contracts.
  - If CLPR Endpoints are implemented natively into the validators of a chain, then the code for the CLPR Endpoint would live in that ledger's repository.
  - If a ledger is not implementing a native CLPR Service, then it doesn't matter what language the CLPR Endpoint supporting it is written in. This Java based implementation can be refactored and organized to support multiple ledger types.
- https://github.com/hiero-ledger/hiero-consensus-node/pull/27029
  - Approved by the Hedera Governing Council and pending approval by the Hiero TSC, the Hiero native implementation of the CLPR Specification is provided in the clpr-feature branch in the hiero-ledger/hiero-consensus-node repository.
  - This branch will not be merged until all requirements and standards for code hygiene, organization, testing, and documentation have been met.

### About CLPR: 

#### Terminology

- **Peer Ledger** — the other ledger that a network communicates with over CLPR.
- **State Proof** — a cryptographic proof that a specific piece of data exists in a ledger's committed state and/or history. State proofs are CLPR's sole mechanism of cross-ledger trust.
- **CLPR Endpoint** — a node responsible for periodically exchanging configuration and messages with peer Endpoints.
- **CLPR Service** — Responsible for curating CLPR state per ledger, managing communication Channel state to remote ledgers, routing messages to applications, and coordinating economic transactions between Connectors, applications, and Endpoints.
- **Channel** — an on-ledger entity representing a communication path to a specific peer CLPR Service instance, bound to one Verifier Contract for its lifetime. Multiple Channels may exist between the same two ledgers.
- **Connector** — an economic entity that authorizes messages on the source ledger and pays for their execution on the destination ledger.
- **Message** — an arbitrary byte payload plus routing metadata representing one unit of cross-ledger communication.
- **Bundle** — an ordered batch of messages transmitted together between two ledgers, accompanied by a state proof.
- **Data Message** — a message carrying application content. Every Data Message produces exactly one Response Message.
- **Response Message** — generated on the destination ledger after processing a Data Message; carries a status and reply bytes back to the source.
- **Control Message** — a protocol message that manages Channel state (e.g., configuration updates) rather than carrying application data.
- **Configuration** — a ledger's ChainID, protocol version, and throttle parameters, as published to peers.
- **Verifier Contract** — An immutable smart contract responsible for verifying state proofs from remote ledgers and decoding the bundle content from the remote ledger's data format to the local ledger's in-memory data format.
- **Trust Anchor** — the opaque, verifier-defined representation of a peer ledger's current signing authority, stored per Channel and updated only via verified proofs.


#### CLPR organizes into four layers:

- **Network layer** — Channel establishment between two ledgers (permissionless, commit-reveal registration to prevent Channel ID squatting), the protocol for syncing bundles between CLPR Endpoints of different ledgers, and the pluggable Verifier Contract interface that validates a peer ledger's state proofs and decodes the bundled data for consumption by the CLPR Service.
- **Messaging layer** — an ordered, state-proven message queue per Channel. Messages are arbitrary byte payloads batched into bundles and delivered with a cryptographic running-hash chain, so a bundle's proof extends trust across every message it carries without individually proving each one.
- **Payment & routing layer** — Connectors: economic actors that provide payment for message execution on the destination ledger and are subject to slashing for misbehavior. Connectors let applications choose their own economic backers for cross-chain delivery. The CLPR Service routes messages in bundles to the appropriate destination applications.
- **Application layer** — The CLPR Application API is a minimal interface for sending and receiving message payloads from remote applications. CLPR moves data between applications on different ledgers, and it is up to the applications to interpret and coordinate on the meaning of the messages. All interledger asset transfers and smart contract calls are application layer logic.

#### Extensibility 

When a new ledger type is added into the CLPR library of support, the following elements must be developed:

1. A CLPR Service implementation that is either native or deployed as a smart contract to the ledger. This CLPR Service implementation must conform to the CLPR Service behavior outlined in the CLPR Specification.
2. CLPR Endpoints that read the local CLPR Service ledger state and construct state-proven bundles in the data format of the source ledger. These CLPR Endpoints must implement the common bundle sync protocol to exchange bundles with the CLPR Endpoints of other ledgers. These Endpoints are also responsible for rotating the trust anchor of the ledger in remote Verifier Contracts.
3. Multiple Verifier Contract implementations, one for each target ledger type supported. The Verifier Contracts are seeded with an updateable trust anchor that stores the source ledger's signing material used in verification of state proofs coming from the source ledger. The Verifier Contracts are also responsible for translating the data format of bundles from the source ledger to the destination ledger data format expected by the receiving CLPR Service.

The alignment between the source CLPR Endpoint bundle construction and the destination Verifier Contract translating the data format from the source ledger to the destination ledger format is the magic that allows interoperable extension to new ledger types without needing to modify the implementation of the destination CLPR Service. In creating a new Channel, the address of a new ledger's Verifier Contract is provided for use along with the remote ledger's CLPR Service configuration.

#### Example of Extension Process

Steps to add a new ledger type (Solana, Polygon, ICP, etc.) to communicate with Hiero:
1. Implement CLPR Service and CLPR Endpoints for the new ledger type.
2. Implement a Hiero Verifier Contract deployable to the new ledger type.
3. Implement a Verifier Contract for the new ledger type, deployable to Hiero.
4. Deploy the respective Verifier Contracts to the opposing networks.
5. Setup a new Channel between the CLPR Services of the two networks.
6. Share the CLPR Endpoints of the opposing network with each other.
7. Setup a common Connector to bond to the Channel.
8. Deploy CLPR applications configured to use the Connector and Channel to the respective networks.

<img width="4113" height="915" alt="Image" src="https://github.com/user-attachments/assets/5c730c7f-bcce-4510-a895-119b30472a65" />

### Alignment with LFDT Mission

With the donation of CLPR to the LFDT, there becomes clear relationships between the following things: 

1. The normative CLPR Specification details the protocols, software APIs, and expected behavior of the defined CLPR components. 
2. The LFDT hosted reference implementations exemplify expected behavior and illustrate possible implementation and deployment approaches. 
3. External native or custom implementations of CLPR are maintained by other projects or organizations

The CLPR specification has no intrinsic software dependencies. It can be implemented in any programming language and be integrated with any chain.  Interoperability is determined by conformance to the APIs and protocols. A copy of the CLPR Specification has been published to the [hiero-hackers/CLPR-Spec](https://github.com/hiero-hackers/CLPR-spec) repository hosted by the LFDT. 

An initial reference implementation for Besu networks has been published to the [hiero-hackers/clpr-smart-contracts](https://github.com/hiero-hackers/clpr-smart-contracts) and [hiero-hackers/clpr-evm-endpoint](https://github.com/hiero-hackers/clpr-evm-endpoint) repositories.  The smart contract repo contains Solidity implementations of the CLPR Service and various Verifier Contracts, while the EVM endpoint repository contains a java implementation of a CLPR Endpoint able to read Besu chain state and submit bundles to the Besu network for a deployed CLPR Service smart contract.

The Hiero Improvement Proposal (HIP-1535) has been presented to the Hiero TSC. The Hedera Governing Council has approved adoption of CLPR for the Hedera network. With TSC approval, a [Hiero native implementation of the CLPR specification](https://github.com/hiero-ledger/hiero-consensus-node/pull/27029) will be merged into the Hiero consensus node. Hiero will be the first project to adopt CLPR and create a native implementation conformant to the CLPR Specification.

These donated codebases are the first instances in an extensible pattern. Under the stewardship of the LFDT, we hope to see the development of additional reference implementations for different types of ledgers and adoption by different chains to incorporate native implementations.  

Hashgraph is developing its own CLPR applications and will continue to develop CLPR Endpoint relays and smart contract based CLPR implementations deployable to different types of ledgers. We hope to do this in open collaboration with other interested parties under the governance of the LFDT.   We hope this inspires various chains to adopt CLPR and integrate their own native implementations to simplify interledger communication and trust. 

The CLPR specification and deployable reference implementations of the CLPR Service, CLPR Endpoints, and Verifier Contracts would greatly benefit from neutral, vendor-independent open-source governance within the LFDT.

Opensourcing CLPR through the LFDT is fundamentally aligned with LFDT’s mission to foster global community around blockchain and distributed trust technologies, hosting neutral infrastructure where that community can come to collaborate and work together on open solutions, drive broad adoption of these interoperable solutions, and further promote the values and success of decentralized technologies and philosophy.

### Relation to Existing LFDT Labs and Projects

As indicated in earlier sections, CLPR has been commissioned by Hedera and developed by Hashgraph as a natively integrated solution for interledger communication between disparate Hiero based networks.  The Hedera Governing Council has voted to adopt CLPR in HIP-1535.  HIP-1535 is pending approval by the TSC.  

Hashgraph has contributed significant resources to the maintenance and operations of the hiero-ledger repositories and is willing to continue that relationship of support with CLPR until responsibilities can be shared with others who join us in developing CLPR. 

As yet another interledger communication standard, how does CLPR differentiate itself from the other standards? https://xkcd.com/927/

We believe CLPR has a novel abstraction layer that allows it to be extended to arbitrary trust paradigms and ledger data formats, the details of how ledgers verify and trust each other’s state proofs is hidden from the application API, and the economic problem of paying for remote execution of messages and transactions is formally addressed.  

To be clear, CLPR may have its origins with Hiero, but it is not an EVM specific standard.  It is our goal to see CLPR used to bridge between any two ledgers or blockchains, whether they are written in Rust, WASM, Go, or any other programming language.   Hashgraph will continue to develop smart contract based implementations and deploy them to various ledgers until those ledgers choose to integrate native implementations of CLPR for themselves.  We would love to work with anyone who wants to see the same under the auspices of the LFDT. 

Within CLPR, bundle submission to the two ledgers participating in a channel of communication is permissionless.  The specification for bundles has clear semantics for how they are architected to make progress on the communication channels.  As long as a bundle makes progress, there are no further restrictions on how bundles are constructed or who constructs them.  Anyone can create their own untrusted relay mechanism between the ledgers and not have to rely on the CLPR Endpoint specification for relays. This also means the higher level CLPR APIs can be wrapped around any existing interledger transport mechanisms for delivering bundles to their destination CLPR Services.  


### Initial Committers

List of existing contributors:   (employed or contracted by Hashgraph) 

Project Administration 
- https://github.com/SimiHunjan
- https://github.com/hendrikebbers

Build/Release/Infrastructure
- https://github.com/andrewb1269
- https://github.com/nathanklick
- https://github.com/rbarker-dev
- https://github.com/jnels124

CLPR Specification
- https://github.com/edward-swirldslabs
- https://github.com/rbair23

CLPR Smart Contracts
- https://github.com/BartoszSolkaBD
- https://github.com/bootcodes
- https://github.com/jasuwienas
- https://github.com/Ferparishuertas

CLPR Endpoint
- https://github.com/mxtartaglia-sl
- https://github.com/timo0
- https://github.com/lukasz-hashgraph
- https://github.com/ashumahajan

Testing and Integration
- https://github.com/Neurone
- https://github.com/mgarbs
- https://github.com/rwalworth
- https://github.com/EMerchant90

Native Hiero Compatibility 
- https://github.com/Neeharika-Sompalli
- https://github.com/tinker-michaelj
- https://github.com/viniciusjssouza
- https://github.com/mhess-swl
- https://github.com/JivkoKelchev

Security
- https://github.com/dr20240304
- https://github.com/diogper

### Governance Model or Practice

We are willing and happy to adopt the LFDT proposed processes and best practices for governance and development for a project of this size and scope. 

Hedera and Hashgraph are initial maintainers and we hope to be joined by many more. 

### Security

Since CLPR overlaps with Hiero in terms of Hashgraph developers, it is expected that the same level of security tooling and practices will be put into place as what exists in the Hiero project. 

### Evidence of Adoption and Use Cases

Hiero is incorporating the first native implementation of the CLPR Specification.  
**PR:** https://github.com/hiero-ledger/hiero-consensus-node/pull/27029

Hashgraph is providing Solidity based smart contracts for CLPR Service and Verifier Contracts that are deployable to Besu and a Java based implementation of a CLPR Endpoint that can read Besu chain state.  These projects function as an initial reference implementation.  

Hashgraph will continue to develop smart contract based implementations of CLPR to deploy to various existing ledgers as well as distributed applications which use CLPR as a medium of communication.  

Apart from passing messages between applications on different ledgers, CLPR itself does not incorporate asset transfer standards.  Asset management and transfer is left to application business logic. CLPR is solely concerned with the reliability of passing information in an aBFT compatible way. This provides a purity of purpose and universal applicability to interledger communication problems. 


### Roadmap

It is hard to estimate the expected rate of growth for this project, but we believe the extensible architecture makes a lot of sense and will facilitate fast adoption.

The following is a rough estimate, and of course may change over time depending on how things evolve. 

**Months 1-3: Bootstrapping**

- Setup CLPR Specification governance process. 
- Setup reference implementation repositories with build, test, and development processes. 
- Iron out collaboration tooling, culture, and processes. 
- Develop educational and onboarding materials for new participants. 

**Months 4-6: Maturing**

- CLPR Application best practices
- Development of a CLPR Application Library for common boilerplate. 
- Expand the library of smart contract reference implementations of CLPR Service and Verifier Contracts.
- Expand the CLPR Endpoint implementation to interface the different ledger types that the reference implementations can be deployed to. 
- Stabilize the CLPR Specification to a publishable 1.0 version. 

**Months 7-9: Evangelizing**

- Facilitate the community development and deployment of CLPR Applications  
- Expand the library of reference implementations and deployments. 
- Outreach to various ledger maintainers towards native integration of the CLPR specification. 

**Months 10-12: Sustainment**

- Maintain a community of experts across the full CLPR stack, from CLPR Endpoint, CLPR Service, Verifier Contracts, to CLPR Application development. 
- The application ecosystem built on top of CLPR continues to mature. 


### Existing Name and Logo

CLPR is trademarked by the Hedera Hashgraph LLC, aka the Hedera Governing Council.  The logo most commonly accompanying CLPR is a spiral. 

See: https://hashgraph.com/clpr/

If accepted by the LFDT, these trademarks and logo will be donated to the LFDT.  

