---
layout: default
title: Interoperability Patterns for Regulated Asset Markets (IPRAM)
parent: LFDT Labs
grand_parent: Active Labs
---
# Lab Name

[Interoperability Patterns for Regulated Asset Markets (IPRAM)](https://github.com/LFDT-IPRAM)

# Short Description

The IPRAM Lab develops open implementation patterns for the interoperation of tokenised real-world regulated financial assets and the markets they participate in.

# Scope of Lab

## Problem

The tokenisation of real-world regulated financial assets has produced multiple institutional implementations of the same instrument across different execution environments. These implementations are built on each participant's own infrastructure, with few shared patterns for how they fit together. The result is a fragmented and limited ecosystem.

The cost of that fragmentation is that these tokenised assets cannot move, settle, or be used as collateral across the institutions, blockchain networks, and venues they need to reach. Each token issued under those conditions is stranded, reachable only by counterparties already inside the same institutional perimeter.

Until this gap is addressed, the tokenisation of real-world financial assets cannot compose into the market structures its economic case depends on, such as secondary liquidity, collateral mobility, and collateralised lending.

## Scope

The lab is a research and reference-development effort focused on the implementation patterns for the interoperation of tokenised financial assets. It takes up the set of unresolved questions about how those assets are structured, operated, and composed in regulated markets. The lab aims to produce open, shared patterns the industry can build on, in place of the bespoke ones currently in use. The lab's scope does not include creating new token-interface standards.

## Topics

The lab targets unresolved gaps in the interoperation of regulated digital assets through topics such as:

- **Asset Instantiation and Reconciliation**: The representation of regulated instruments and their off-chain references on-chain, and the reconciliation of that representation with the off-chain registers that hold legal authority.
- **Composition**: The composition of regulated assets into downstream liquidity, collateral, and settlement venues.
- **Identity**: The portability of identity and entitlement state with a regulated asset across infrastructures.
- **Metadata**: The persistence and interpretability of asset metadata across lifecycle events.

The specific topics the lab takes up, and the cadence at which it works into them, are scoped through the community process the lab convenes.

## Outputs

Across the topics it takes up, the lab aims to produce open, community work across three categories:

- **Research and Reports**: Problem framing, gap analyses, and findings from the lab's investigations, alongside the patterns that emerge as the work matures.
- **Technical Specifications**: Shared, open contracts, interfaces, and conformance criteria that document the interoperation patterns the lab develops, open to any participant who adopts them.
- **Reference Implementations**: Reference contracts and implementations of the lab's specifications.

# Initial Committers

- <https://github.com/richardp8io> (Conduit Digital Holdings)
- <https://github.com/gkp8io> (Cubewire)
- <https://github.com/evanp8io> (Conduit Digital Holdings / Cubewire)

# Sponsor

N/A

# Pre-existing repository

N/A
