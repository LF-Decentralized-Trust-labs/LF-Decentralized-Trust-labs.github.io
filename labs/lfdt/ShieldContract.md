# Lab Name

ShieldContract Analyzer

# Short Description

ShieldContract Analyzer is a Rust-based CLI tool in ideation phase for smart contract security analysis, with a focus on verifying compliance with token standards (e.g., ERC-20, ERC-721, ERC-1155, ERC-777) and providing quick first-check security audits. It integrates with AI providers like OpenAI, Claude, and Gemini for cross-check analysis, helping institutions entering tokenization to rapidly identify vulnerabilities and ensure standards adherence.

# Scope of Lab

This lab develops a proof-of-concept CLI tool for blockchain smart contract security, currently supporting Hyperledger Fabric chaincode and Solana programs, with modular extensions for other platforms. Key functionalities include:

- **Standards Compliance Checking**: Validates if contracts follow token standards like ERC-20 (e.g., transfer functions, balances) and stablecoin best practices, detecting deviations that could lead to security issues.
- **Security Vulnerability Detection**: Platform-specific checks, such as non-determinism in Fabric (e.g., time/rand usage), arithmetic overflows/underflows in Solana, missing signer/account validation, CPI security, and private data leaks.
- **AI Cross-Check Analysis**: Connects to multiple LLMs (OpenAI, Claude, Gemini) for consensus-based validation of findings, AI-generated code patterns, and remediation suggestions – vital for quick, reliable first checks in institutional tokenization workflows.
- **Reporting**: Outputs in JSON, Markdown, HTML, and SARIF for CI/CD integration.
- **Other Features**: Interactive mode, custom rules, Docker support, and configuration via TOML. Stubbed/planned features include full auditing.

As enterprises and business solutions are looking into developing web3 products such as institutional tokenization and stable coins, there is a pressing need for a quick CLI analyzer tool for smart contracts to see if it meets the standards and that it can fit into a CI/CD workflow. As institutions increasingly tokenize assets, this tool provides a "quick first check" for smart contracts, combining static analysis with AI to flag non-compliance and vulnerabilities early. It aligns with Hyperledger's ecosystem (e.g., Fabric integration) and could expand to support more standards/AI providers. The project is in early ideation (v0.2.0), with some features limited.

# Initial Committers

- https://github.com/KoushikGavini


# Sponsor



# Pre-existing repository

- https://github.com/KoushikGavini/ShieldContract