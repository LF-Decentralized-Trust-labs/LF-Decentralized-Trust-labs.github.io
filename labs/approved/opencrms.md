---
layout: default
title: OpenCrMS
parent: Approved Labs
---
### Lab Name

[OpenCrMS](https://github.com/OpenCrMS)

### Short Description

OpenCrMS is an open-source Credential Management System (CrMS) designed to support the issuance, verification, and processing of verifiable credentials through secure, decentralized communication. Built around the DIDComm protocol, OpenCrMS enables peer-to-peer interactions between organizations and individuals while supporting multiple credential formats, including W3C Verifiable Credentials, Open Badges, AnonCreds, and mDocs.

OpenCrMS extends DIDComm beyond credential exchange by supporting additional protocols, including Workflow 1.0, Vaults 1.0, Signing 1.0, and WebRTC 1.0, enabling secure, interoperable interactions and credential-driven processes. The system also supports both DIDComm and OpenID for Verifiable Credential (OID4VC) exchange protocols, providing flexibility and interoperability across different digital identity ecosystems.

By combining standards-based credential management with extensible peer-to-peer communication protocols, OpenCrMS provides an open foundation for building decentralized identity and verifiable credential applications.

### Alignment with LFDT Mission

OpenCrMS aligns closely with the mission of LF Decentralized Trust (LFDT) to advance open-source technologies that enable secure, interoperable, and trustworthy decentralized systems. By providing a practical implementation of decentralized identity, verifiable credentials, and DIDComm-based communication, OpenCrMS helps translate open standards and foundational technologies into applications that organizations can deploy and use.

OpenCrMS complements existing projects within the LFDT ecosystem by providing an application-level credential management platform that integrates Self-Sovereign Identity (SSI) agents, verifiable credential standards, secure peer-to-peer communication, and cross-organizational workflow automation. Rather than introducing another credential format or identity protocol, OpenCrMS demonstrates how these technologies can work together to support real-world applications.

The project also advances LFDT's commitment to interoperability and vendor independence. OpenCrMS supports multiple credential formats, including W3C Verifiable Credentials, Open Badges, AnonCreds, and mDocs, as well as DIDComm and OpenID for Verifiable Credential (OID4VC) exchange protocols. This flexibility allows organizations to participate in decentralized trust ecosystems without being restricted to a single credential format, technology provider, or implementation.

An important aspect of OpenCrMS is its use of DIDComm as a foundation for secure, asynchronous communication between individuals, organizations, devices, and services. By implementing protocols for credential exchange, workflow automation, document signing, and other interactions, the project demonstrates how decentralized trust can extend beyond identity verification to support ongoing relationships and transactions between participants.

#### Why LF Decentralized Trust Is the Right Home

LF Decentralized Trust provides a natural home for OpenCrMS because of its established community, open governance model, and focus on technologies that support decentralized identity and trust.

As a Hyperledger Lab, OpenCrMS can benefit from collaboration with developers and organizations working on complementary technologies, including SSI agents, verifiable data registries, credential exchange protocols, and decentralized governance. This environment creates opportunities to improve interoperability, share implementation experience, and contribute practical feedback to emerging standards.

LFDT also provides a neutral environment for the project's continued development beyond its founding organizations, Ajna Inc. and VeriDID Corp. Community participation can help ensure that OpenCrMS evolves as a reusable, vendor-independent platform rather than an implementation tied to a particular commercial product.

The project is intended to encourage both nonprofit and commercial adoption. Organizations with limited budgets can deploy OpenCrMS as an open-source credential management solution, while developers and technology providers can fork and extend it to build specialized products for different industry sectors. This model supports the development of a broader decentralized trust ecosystem while encouraging contributions back to the open-source community.

By joining LFDT, OpenCrMS aims to contribute a practical, extensible implementation that connects decentralized trust infrastructure with real-world applications. In doing so, the project can help accelerate adoption, reduce barriers to entry, and demonstrate the value of open standards and decentralized technologies across industries.

### Relation to Existing LFDT Labs and Projects

OpenCrMS complements existing LF Decentralized Trust (LFDT) projects by providing an application-level platform that combines decentralized identity, verifiable credentials, secure peer-to-peer communication, and cross-organizational workflow automation.

While many decentralized trust projects focus on foundational infrastructure, such as distributed ledgers, identity agents, and credential protocols, OpenCrMS focuses on how these technologies can be integrated to support real-world business processes.

A key differentiator is OpenCrMS's use of agent-based decentralization to complement ledger-based trust systems. Through DIDComm, organizations, individuals, devices, and services can establish secure peer-to-peer connections, verify claims, and execute workflows without recording sensitive transaction details on a blockchain. Distributed ledgers can provide shared trust anchors and governance information, while the exchange of credentials, documents, and other sensitive information occurs directly between participants.

OpenCrMS extends verifiable credentials beyond issuance and verification by incorporating decentralized workflows that coordinate interactions between independent parties. These workflows provide participants with the context, authorization, and control needed to complete transactions while preserving privacy and organizational autonomy.

This architecture creates opportunities to integrate decentralized trust into emerging applications, including:

Agentic AI: Providing verifiable identity, credentials, and authorization proofs that enable AI agents to establish trust and demonstrate their authority to act on behalf of individuals or organizations.

Supply Chain and Tokenization: Supporting secure document signing, verification of organizational authority, and credential-based approval workflows associated with supply chain transactions and tokenized assets.

Cross-Organizational Processes: Enabling independent organizations to exchange verified information and coordinate business processes without relying on a centralized intermediary.

OpenCrMS is not intended to replace existing LFDT infrastructure or identity projects. Instead, it provides a reusable application framework and reference implementation that demonstrates how these technologies can work together.

Its unique contribution is the combination of verifiable credentials, persistent secure communication, and decentralized workflow orchestration within a single extensible platform. This helps bridge the gap between decentralized trust infrastructure and practical applications, reducing the complexity of building solutions that require trusted interactions across organizational boundaries.

### Does this lab produce code?

Yes

### Does this lab produce a specification?

No

### Pre-existing Repositories

https://github.com/openwallet-foundation-labs/apostille

### Initial Committers

https://github.com/dave-promulgare  Dave McKay  VeriDID
https://github.com/vinaysingh8866  Vinay Singh  Ajna Inc

### Sponsor

OpenCrMS is transitioning from the OpenWallet Foundation to LF Decentralized Trust (LFDT) as part of its continued development within the open-source decentralized identity ecosystem. Sean Bohan, who has served as the project's sponsor at the OpenWallet Foundation, has supported its development and participation in the open-source community. We appreciate his support and look forward to continuing the project's growth and collaboration within LFDT.

### Licensing

- [x] I understand that all code hosted in LFDT Labs must be made available under an Apache 2.0 license with DCO sign-off.
- [x] I understand that all specification and standards work in LFDT Labs is done under the Community Specification License 1.0 and the rest of the CSL framework.

### Governance Model or Practice

OpenCrMS will be governed by a Maintainer Council composed of a small group of active project maintainers who share responsibility for the project's technical direction, development roadmap, and code review and merge decisions. This collaborative governance model is intended to promote transparent decision-making, shared accountability, and community participation while ensuring the project's long-term sustainability.

The project's governance policies and procedures will be developed using the Cloud Native Computing Foundation (CNCF) Maintainer Council Template as a foundation. These policies will define maintainer roles and responsibilities, decision-making processes, contributor participation, and procedures for appointing new maintainers. The governance model will evolve as the community grows, supporting an open, inclusive, and vendor-neutral development environment.

### Security

OpenCrMS is committed to following the Open Source Security Foundation (OpenSSF) Best Practices to promote secure, reliable, and sustainable open-source software development. The project will work toward achieving the OpenSSF Best Practices Passing Badge by adopting transparent development processes, documented contribution guidelines, secure coding practices, and publicly accessible source code. Development will incorporate automated builds, continuous integration, code reviews, automated testing, static code analysis, dependency vulnerability scanning, and documented release management. The project will establish a responsible vulnerability disclosure process, track and remediate reported security issues, and maintain clear documentation of its security practices. Given OpenCrMS's role in managing digital identities, cryptographic keys, and verifiable credentials, particular emphasis will be placed on secure cryptographic implementations, protection of sensitive information, and adherence to established security standards. By incorporating OpenSSF best practices into its development and governance processes, OpenCrMS aims to provide a trustworthy foundation for organizations and developers building decentralized identity and credential management solutions.

### Infrastructure and Tooling

OpenCrMS currently uses GitHub as its primary development and collaboration platform, providing source code repositories, documentation, issue tracking, and continuous integration and deployment (CI/CD) through GitHub Actions. This infrastructure supports transparent development, version control, automated testing, and community contributions.

As the project grows within the LF Decentralized Trust community, we anticipate expanding our collaboration infrastructure to include a Discord channel for developer discussions and community support, a mailing list for project announcements and technical discussions, and shared meeting calendars for coordinating regular community and contributor meetings.

Where practical, OpenCrMS intends to leverage existing LFDT infrastructure and services to align with established community practices, encourage participation, and minimize administrative overhead.

### Evidence of Adoption and Use Cases

The technologies and architectural approach underlying OpenCrMS have already been applied in commercial, closed-source implementations, demonstrating their practical value across different industries. DigiCred uses a DIDComm-based Credential Management System in the U.S. education market to support the issuance, verification, and management of verifiable credentials. Similarly, Ajna Inc. uses DIDComm and decentralized workflows in Vilko, its decentralized alternative to Slack for secure team communication and collaboration.

Both implementations demonstrate how DIDComm-based peer-to-peer communication and workflow automation can support distinct applications, from educational credential management to decentralized organizational collaboration. These real-world use cases provide evidence of the viability of OpenCrMS's underlying architecture and illustrate its potential for adoption across additional industry sectors.

### Roadmap

The OpenCrMS development roadmap focuses on improving the usability, performance, and capabilities of the platform while expanding support for decentralized workflows and credential management. Over the first 12 months, the project will prioritize improvements to the existing user interface, migration to the Idiom Agent, support for multi-user and multilingual workflows, and the development of mobile and browser-based wallets.

The roadmap is organized into four phases, with incremental releases and opportunities for community contributions throughout the year.

### Trademark and Accounts Signoff

- [x] If the lab is accepted, I agree to donate all related trademarks and accounts to the LFDT.

### Additional Information

This is the migration of an Open Wallet Foundation project to an LFDT Lab.  We are looking forward to the new home and working on this under a new project name, governance, and mandate.
