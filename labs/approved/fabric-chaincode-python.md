---
layout: default
title: Fabric Chaincode Python
parent: Approved Labs
---
### Lab Name

[Fabric Chaincode Python](https://github.com/hyperledger/fabric-chaincode-python)

### Short Description

Hyperledger Fabric Python chaincode shim focused on Chaincode-as-a-Service (CCAAS).

### Scope of Lab

fabric-chaincode-python provides a native Python runtime for Hyperledger Fabric chaincode with current focus on CCAAS.

MISSION
Enable Python teams to build and run Fabric chaincode without switching to Go/Java/Node.

CURRENT TECHNICAL SCOPE

[VERIFIED] Implemented now:
1. Shim runtime under `src/fabric_shim/`
- gRPC bidirectional peer-chaincode stream handling
- Chaincode and ChaincodeStub interfaces
- State operations (`get_state`, `put_state`, `delete_state`)
- Async message handling with queue/future orchestration
- CCAAS server bootstrap (`CHAINCODE_ID`, `CHAINCODE_SERVER_ADDRESS`)

2. Runnable CCAAS examples
- `examples/ccaas/asset-transfer-basic/`
- `examples/ccaas/asset-transfer-sbe/`

[VERIFIED] Current repository release/tag status:
- Maintained branches: `main`, `release-2.5`
- Latest release tag in repo: `v2.5.4`

[VERIFIED] Not complete yet:
- Full decorator-driven Contract API parity with `fabric-contract-api` patterns used by Java/Node ecosystems
- Formal security disclosure file (`SECURITY.md` not yet present)
- Full integration test matrix against full Fabric network lifecycle in CI

OUT OF SCOPE (CURRENT)
- Fabric 1.x compatibility
- Claims of production adoption by named enterprises (not publicly evidenced)

### Alignment with LFDT Mission

LFDT Mission: advance decentralized trust technologies through open collaboration.

[VERIFIED] Alignment points:
1. Ecosystem gap coverage:
- Fabric has official chaincode stacks for Go, Java, Node.
- Python is not an official equivalent project in Fabric core repos.

2. Interoperability:
- Uses Fabric protobuf/gRPC protocol model (peer-chaincode communication).
- Uses Apache-2.0 licensed ecosystem components.

3. Open governance and contribution model:
- Public GitHub repository
- Apache-2.0 license
- DCO sign-off checks in CI
- Governance document present

[INFERRED] Expected impact:
- Lowers entry barrier for Python-first teams to evaluate Fabric chaincode development.

### Relation to Existing LFDT Labs and Projects

[VERIFIED] Complementary relation:
- `fabric-chaincode-go`, `fabric-chaincode-java`, `fabric-chaincode-node` are language-specific siblings.
- `fabric-chaincode-python` targets language parity, not replacement.

### Fabric Protobuf Dependency

**[VERIFIED] Dependency relation**

* `fabric-chaincode-python` depends on the Fabric protobuf definitions and the corresponding generated Python bindings provided by the `fabric-protos` project.
* The library uses the published `fabric-protos` Python package rather than maintaining an independent copy of the generated protobuf bindings.

**[VERIFIED] Current integration**

* The `fabric-protos` repository provides Python bindings and their packaging workflow under `bindings/python`.
* `fabric-chaincode-python` consumes these bindings as its protobuf dependency, keeping the chaincode library aligned with the canonical Fabric protocol definitions.

**[PROPOSAL] Dependency and compatibility policy**

* Keep `fabric-protos` as the canonical upstream source for Python protobuf bindings.
* Define and document the compatible `fabric-protos` version range for each `fabric-chaincode-python` release.
* Avoid vendoring generated protobuf code within `fabric-chaincode-python`, reducing duplication and simplifying synchronization with future Hyperledger Fabric protocol changes.
* Add compatibility tests to detect breaking changes in the protobuf API when upgrading the `fabric-protos` dependency.

### Does this lab produce code?

Yes

### Does this lab produce a specification?

Yes (incremental). Current state is minimal and will be expanded into runtime/interface specification as part of incubation milestones.

### Pre-existing Repositories

- https://github.com/kmilodenisglez/fabric-chaincode-python

### Initial Committers

- https://github.com/kmilodenisglez

### Sponsor

https://github.com/mbwhite


# Roadmap

## 12-Month Roadmap

### Q4 2026

- [ ] Publish formal `SECURITY.md`
- [ ] Expand integration tests against Fabric test network lifecycle
- [ ] Stabilize CCAAS developer experience and examples
- [ ] Align dependency policy with upstream `fabric-protos` Python bindings

### Q1 2027

- [ ] Package/release pipeline hardening and reproducible build guidance
- [ ] Contract API design proposal and milestone definition
- [ ] Add more maintainers/contributors and governance maturity checks

### Q2 2027

- [ ] Evaluate readiness for graduation path based on adoption and maintainer health metrics

### Contact name(s) and email(s)

Camilo (Kmilo) Denis Gonzalez - kmilo.denis.glez@yandex.com - https://www.linkedin.com/in/kmilodenisglez/
