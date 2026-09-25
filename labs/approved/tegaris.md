---
layout: default
title: Tegaris Application Privacy
parent: Approved Labs
---
### Lab Name

Tegaris Application Privacy

### Short Description

An application-layer privacy and policy control plane for shared EVM networks. It governs participant access, contract interactions and data visibility, with approved policy changes, verifiable runtime activation and decision evidence.

### Scope of Lab

#### Mission

Enable organizations to share blockchain infrastructure while defining and enforcing each participant's authority and application-level view of the network.

Application privacy is an operating responsibility that continues as participants join, permissions change, policies are deployed, and the data used in decisions evolves. Network operators need to explain what access is permitted, which policy is actually enforced, and why a particular operation or disclosure was allowed.

The Lab will develop reusable software that connects these responsibilities: participant authority, operation-level policy, data visibility, controlled policy change, runtime enforcement and evidence. Its initial contribution will originate from Tegaris Application Layer Privacy, developed by Zeeve.

#### Proposed contribution

The planned contribution draws on the R1.0 Application Layer release scope and comprises six connected areas:

- **Participant-scoped authority.** Bind users, workloads and associated resources to the appropriate participant. Support roles, bounded delegation, revocation and an explanation of effective access. Delegated administrators operate within the authority assigned to them.

- **Governed operations and data visibility.** Apply policy to RPC methods, contract functions and arguments, state reads, transactions, receipts and events, including governed subscriptions. Distinguish permission to perform an operation from permission to see the resulting data. Support purpose-bounded disclosure through the governed interfaces.

- **Controlled policy lifecycle.** Carry policy from authoring and simulation through independent review, approval, immutable versioning, signed publication, activation and recovery. Bind approvals and deployment actions to the policy version being changed.

- **Observable runtime enforcement.** Distribute approved policy to configured runtime targets, verify activation and expose the difference between intended configuration and effective state. Support staged changes, quarantine and recovery when a target cannot establish the required state. An issued rollout command alone does not establish successful enforcement.

- **Governed decision inputs and providers.** Evaluate the provenance, freshness, completeness and chain validity of facts used in decisions. Invalidate affected inputs after a chain reorganization. Bind provider selection to approved capabilities and routes. External data or endpoint availability cannot independently widen authority.

- **Accountable operation.** Link decisions to participant context, effective policy, relevant inputs and operational evidence. Include privacy-aware investigation and export, client-signed transaction preparation, controlled delivery and reconciliation of uncertain transaction outcomes. Wallet signing keys remain with the client or its chosen custody arrangement.

The contribution includes the associated administrative interfaces, integration contracts, deployment assets, documentation and tests. Public release records will identify which capabilities are delivered and validated in each supported configuration.

#### Illustrative use case

A shared settlement network admits two institutional participants. Each participant delegates limited access to its applications. An application may be allowed to submit a particular contract operation while receiving only the transaction and event data authorized for its participant. A change to that policy is reviewed and approved, and operators can establish which runtime targets have activated it. An investigator can reconstruct the decision using the relevant policy and input versions. A revoked delegation or invalidated data source must not silently create new access.

This example describes intended behavior for implementation and conformance work; it is not a claim of production deployment.

#### Application privacy model

The Lab provides application-layer privacy by governing participant access, permitted operations and data visibility on shared EVM networks. Its controls apply to the application interfaces through which participating organizations and their applications interact with the network.

#### Origin and current stage

The project originates from Zeeve's work on Tegaris Application Layer Privacy and is in the final stages of R1.0 release preparation. Early discussions and demonstrations with prospective users have informed the requirements and approach.

We are submitting the proposal before public source-code publication. The initial source contribution will follow release preparation and agreement on the contribution boundary, licensing and repository arrangements. We will coordinate onboarding with LFDT staff if accepted. No code-publication date is committed in this proposal.

### Alignment with LFDT Mission

The work addresses a practical requirement in shared decentralized systems: participants must be able to govern application access and disclosure as their relationships and operating conditions change.

An LFDT community can bring together execution-client developers, application builders, identity specialists and network operators to review the enforcement model, develop interoperability examples and contribute reproducible tests. We seek a common implementation and public contribution process that can serve multiple operators and vendors. Early community work would focus on documented privacy boundaries, contributor onboarding and conformance scenarios for authorization, visibility, policy changes and failure behavior.

### Relation to Existing LFDT Labs and Projects

The proposed Lab would contribute a dedicated application-layer privacy and policy control plane to the LFDT ecosystem. [Besu](https://www.lfdecentralizedtrust.org/projects/besu) provides Ethereum execution infrastructure, while [Paladin](https://www.lfdecentralizedtrust.org/projects/paladin) provides programmable privacy for confidential transactions and smart-contract execution. The Lab would complement this work by governing participant authority, application operations and data visibility, together with controlled policy changes, runtime enforcement and decision evidence on shared EVM networks.

### Does this lab produce code?

Yes

### Does this lab produce a specification?

No

### Pre-existing Repositories

The Development repositories are private as of now. We propose agreeing the initial contribution and repository arrangements with LFDT staff during onboarding, if accepted.

### Initial Committers

- https://github.com/gnv-zeeve - Ghan Vashishtha, Zeeve
- https://github.com/supravat-zeeve - Supravat Samanta, Zeeve
- https://github.com/Nitesh-Zeeve - Nitesh Sharma, Zeeve

### Licensing

- [x] I understand that all code hosted in LFDT Labs must be made available under an Apache 2.0 license with DCO sign-off.
- [x] I understand that all specification and standards work in LFDT Labs is done under the Community Specification License 1.0 and the rest of the CSL framework.

### Governance Model or Practice

Zeeve will provide the initial contributing team. We propose public technical discussions and review, documented maintainer responsibilities, review requirements for material changes, and a contribution-based path for additional maintainers from other organizations. The Lab will operate under the applicable Labs charter. Security disclosures will use an appropriate private reporting process.

### Security

With the initial repository contribution, we will establish the following security practices:

- **Security policy and private reporting.** We will publish a SECURITY.md file with the repository. Please report vulnerabilities and other security-sensitive issues privately to Ghan Vashishtha ([ghan@zeeve.io](mailto:ghan@zeeve.io)) and Ravi Chamria ([ravi@zeeve.io](mailto:ravi@zeeve.io)). Vulnerability details should not be posted in public issues, pull requests or community channels.

- **Coordinated disclosure.** We will assess reports confidentially with the reporter and coordinate fixes or mitigations before publishing vulnerability details. Reports should include affected versions, potential impact and sanitized reproduction steps, without credentials, private keys or confidential user data.

- **Dependency management.** We will configure automated dependency vulnerability checks and review security updates as part of repository onboarding.

- **Continuous integration.** We will enforce DCO sign-off and run unit, integration and privacy regression tests, including checks for unauthorized access and cross-participant data exposure.

- **Release integrity.** Before distributing official binaries or container images, we will complete dependency license checks and provide a software bill of materials and build provenance.

### Infrastructure and Tooling

We anticipate LFDT-hosted repositories, CI, documentation hosting and community communication channels. The initial contribution will include build and test instructions, deployment examples and release documentation sufficient for external contributors to reproduce the supported scenarios. Detailed tooling and hosting needs will be finalized during onboarding.

### Evidence of Adoption and Use Cases

Initial use cases include shared financial networks, participant-scoped application access, controlled service-provider access and purpose-limited operational investigation. Some early POCs/ Pilots are being done with few banks/fintechs.

### Roadmap

The following is a proposed Lab direction derived from the Application Layer product roadmap. It distinguishes the R1.0 contribution from later candidate extensions. The 3–12 month windows below are relative to R1.0 release, not LFDT acceptance. Dates and contribution scope will be agreed as the work progresses.

| Stage | Proposed focus |
| --- | --- |
| Initial contribution, following R1.0 release preparation | Publish the agreed Application Layer components, privacy-boundary documentation, deployment examples and reproducible conformance tests. |
| Next iteration, drawing on R1.1 | Richer visual policy design, impact analysis, participant administration, effective-access investigation and transaction/evidence workflows. |
| 3–6 months after R1.0 | Candidate work on coordinated policy releases, access reviews, revocation tracking, enterprise identity integration and governed evidence export. |
| 6–9 months after R1.0 | Candidate work on external decision-source management, privacy-filtered investigation and enterprise workflow integration. |
| 9–12 months after R1.0 | Candidate work on adaptive access controls, identity federation, consortium administration and sensitive-data handling across approved application interfaces. |

Future product capabilities will be considered for the Lab individually; this proposal does not commit the complete commercial product roadmap. All code accepted into the Lab will follow its licensing requirements.

### Existing Name and Logo

Tegaris Application Privacy is the proposed Lab name and is not a commercial brand. The logo has not yet been finalized.

### Website URL

The project does not currently have a website.

### Social Media Accounts

The project does not currently have a social media presence.

### Trademark and Accounts Signoff

- [x] If the lab is accepted, I agree to donate all related trademarks and accounts to the LFDT.

### Contact name(s) and email(s)

Ghan Vashishtha — [ghan@zeeve.io](mailto:ghan@zeeve.io)
Ravi Chamria — [ravi@zeeve.io](mailto:ravi@zeeve.io)

### Contributing or sponsoring entity signatory information

**Arun S M** — [arsulegai](https://github.com/arsulegai) — arun.s.m.cse@gmail.com  
**LFDT Member/Role:** TAC Chair

### Additional Information

We are seeking proposal review ahead of the source contribution. The initial code release and repository arrangements will be coordinated separately. Confirmed sponsors may be added with their consent.

We welcome steward feedback on the proposed scope, the initial contribution milestones and opportunities to collaborate with related LFDT work.

#### Code contribution

Yes. The Lab will produce software; the source contribution will follow this proposal.

#### Specification contribution

No. The initial effort covers software and supporting documentation. Formal specification or standards development is outside the proposed activity.

#### Licensing commitments

We will contribute the Lab’s software under Apache-2.0 and comply with LFDT Labs licensing requirements. Before submitting the repository, we will ensure that the contributed code and commit history meet the applicable licensing and Developer Certificate of Origin (DCO) requirements. Our committers will include DCO sign-off on all contributions. We will follow the applicable Labs policy for documentation.

We also acknowledge that any specification or standards work undertaken by the Lab must follow the Community Specification License 1.0 and its associated framework requirements.