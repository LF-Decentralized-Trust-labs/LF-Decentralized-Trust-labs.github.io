---
layout: default
title: VC Profile Validator
parent: Approved Labs
---
### Lab Name

[VC Profile Validator](https://github.com/vc-profile-validator)

### Short Description

A lightweight, profile-driven validation engine and CLI for checking whether Verifiable Credentials (VCs) and Verifiable Presentations (VPs) conform to declared profiles.

### Scope of Lab

VC Profile Validator provides a lightweight validation engine and CLI for checking whether a Verifiable Credential (VC) or Verifiable Presentation (VP) satisfies a declared profile.

Profiles are expressed as versioned YAML bundles. The validator evaluates credential and presentation inputs against these profiles and produces structured findings and summary results.

The project addresses a practical need for a smaller validation utility that can be used independently by implementers or integrated into broader interoperability and testing systems.

The current implementation includes:

- Profile loading and schema validation
- Rule-based VC/VP validation
- CLI and batch execution
- JSON and HTML reporting
- Docker packaging
- Test fixtures, suites, and supporting design documentation

The project is intentionally focused on profile conformance validation rather than providing a complete wallet, credential issuance platform, or interoperability testing framework.

Its modular design allows additional validation rules and profiles to be introduced without requiring changes to the core validation engine.

The project originated from practical implementation and contribution experience across the digital wallet ecosystem, where a recurring need emerged for lightweight and reusable validation tooling.

Project was independently developed by Vijay Kumar Soni and originally proposed to the OpenWallet Foundation as a Labs project via PR [74](https://github.com/openwallet-foundation/project-proposals/pull/74).  The proposal underwent community review, and a Technical Charter was subsequently finalized on July 14, 2026.

Following the transition of OWF projects to LF Decentralized Trust, this proposal seeks to continue development under LFDT Labs.

### Alignment with LFDT Mission

VC Profile Validator supports LFDT’s mission of advancing open and interoperable decentralized identity technologies.

As Verifiable Credentials become more widely adopted, developers need practical ways to validate credentials and presentations against the requirements of specific implementations and interoperability profiles.

The project addresses this need by providing a reusable validation engine that separates profile definitions from validation execution.

This allows developers to apply consistent validation rules across different implementations, test environments, and development workflows.

### Relation to Existing LFDT Labs and Projects

VC Profile Validator is intended to complement existing LFDT digital identity and interoperability projects rather than duplicate their functionality.

Projects such as OWL provide broader interoperability testing capabilities, while other identity frameworks focus on credential issuance, presentation, verification, and wallet functionality.

VC Profile Validator focuses on a narrower problem: evaluating individual credentials or presentations against reusable, versioned validation profiles.

The validator can run independently through its CLI or be incorporated into existing testing workflows.

During the original OWF proposal review, potential applications alongside OWL and other interoperability initiatives were discussed.

The project does not aim to replace existing conformance testing frameworks or claim functionality that those frameworks already provide.

Instead, it offers a small, modular validation component that developers can use without adopting an entire interoperability testing environment.

As the project develops, opportunities for integration with existing LFDT projects can be explored with their respective communities.

### Does this lab produce code?

Yes

### Does this lab produce a specification?

No

### Pre-existing Repositories

https://github.com/sonivijayk/vc-profile-validator

### Initial Committers

- [@sonivijayk](https://github.com/sonivijayk) — Vijay Kumar Soni, Independent Contributor

### Licensing

- [x] I understand that all code hosted in LFDT Labs must be made available under an Apache 2.0 license with DCO sign-off.
- [x] I understand that all specification and standards work in LFDT Labs is done under the Community Specification License 1.0 and the rest of the CSL framework.

### Governance Model or Practice

- VC Profile Validator  project was independently developed by Vijay Kumar Soni and initially proposed to the OpenWallet Foundation.

- As part of the OWF project formation process, a [Technical Charter](https://github.com/sonivijayk/vc-profile-validator/blob/master/VC-Profile-Validator-Technical-Charter-(FINAL-07.14.26).pdf) was finalized on July 14, 2026, under Linux Foundation Europe.

- The charter establishes a Technical Steering Committee (TSC) comprising project committers, responsible for technical direction, contribution management, and project governance.

- Vijay Kumar Soni is the project’s initial maintainer.

- The project will align with the LFDT Labs governance framework as part of the OWF-to-LFDT transition.

### Security

VC Profile Validator is an early-stage open-source project with automated tests and schema-based validation.

As an initial LFDT Labs work item, the project intends to assess its development and security practices against the OpenSSF Best Practices criteria and work toward the Passing badge.

CI will also be expanded to include appropriate dependency and security checks alongside the existing automated testing.

### Infrastructure and Tooling

The project currently uses GitHub for source control, issue tracking, and contributions.

The implementation is Python-based, with PyYAML and jsonschema as runtime dependencies and pytest for testing.

Docker packaging is available for containerized execution.

The project intends to use standard LFDT Labs infrastructure, including:

- GitHub repository hosting
- GitHub issues and pull requests
- CI workflows for automated functional, regression, performance, and security testing
- LFDT-provided communication tools

The project does not require any specialized infrastructure at this time.

### Evidence of Adoption and Use Cases

VC Profile Validator is an early implementation with working validation capabilities.

The existing repository demonstrates the following use cases:

- Validating Verifiable Credentials and Verifiable Presentations against declared profiles.

- Running profile-based validation during local development.

- Executing batch validation against predefined test fixtures.

- Producing JSON and HTML reports that identify validation findings.

- Running validation through Docker or automated CI workflows.

The repository includes test fixtures, suites, and supporting documentation demonstrating these capabilities.

The project was publicly proposed to the OpenWallet Foundation in April 2026 and received technical feedback from community members regarding potential applications alongside existing interoperability testing initiatives.

Original proposal:
https://github.com/openwallet-foundation/project-proposals/pull/74

The project has not yet established external production adoption.

The purpose of continuing under LFDT Labs is to develop the implementation further, encourage community contributions, and identify practical integration opportunities.

### Roadmap

The initial development priorities are:

- Improve validation coverage and work toward the OpenSSF Best Practices Passing badge.
- Review related work across LFDT and expand reusable validation profiles and test fixtures.
- Improve validation reporting and error handing.
- Incorporate contributor and community feedback and prioritize work that supports broader adoption.

### Existing Name and Logo

VC Profile Validator was independently developed by Vijay Kumar Soni in a personal capacity.

The project was made public to support its original OpenWallet Foundation proposal and community review.

The name has not been used as a commercial product or under another organization.

There are no registered trademarks or pending trademark applications associated with the project name.

The project name and any associated project assets can be transferred as part of the LFDT onboarding process.

Logo: No finalized logo has been confirmed for this submission.

### Trademark and Accounts Signoff

- [x] If the lab is accepted, I agree to donate all related trademarks and accounts to the LFDT.

### Additional Information

VC Profile Validator was originally proposed to the OpenWallet Foundation in 2026. As part of the OWF project formation process, its Technical Charter was finalized on July 14, 2026. This submission continues the project under LFDT Labs as part of the OWF-to-LFDT transition.

Original OWF proposal:
https://github.com/openwallet-foundation/project-proposals/pull/74

Technical Charter:
https://github.com/sonivijayk/vc-profile-validator/blob/master/VC-Profile-Validator-Technical-Charter-(FINAL-07.14.26).pdf
