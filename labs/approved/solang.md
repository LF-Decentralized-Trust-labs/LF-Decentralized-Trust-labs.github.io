---
layout: default
title: Hyperledger Solang
parent: Approved Labs
---
# Lab Name
[Hyperledger Solang](https://github.com/[hyperledger-caliper](https://github.com/hyperledger-solang))

# Sponsor(s)

- Sean Young [<sean@mess.org>](mailto:sean@mess.org)
- Lucas Steuernagel [<lucas.tnagel@gmail.com>](mailto:lucas.tnagel@gmail.com)
- Tracy A. Kuhrt [<tracy.a.kuhrt@accenture.com>](mailto:tracy.a.kuhrt@accenture.com)
- Cyrill Leutwiler [<cyrill@parity.io>](mailto:cyrill@parity.io)

# Abstract

Solang is a portable compiler for the Solidity language that targets Solana,
Substrate (Polkadot), and ewasm. It is written in Rust, and leverages the LLVM
infrastructure for the compiler backend.

# Context

The Solidity language is the [most popular programming language for smart
contracts](https://101blockchains.com/smart-contract-programming-languages/).
However, the existing Solidity compiler only targets the Ethereum
virtual machine. The Solang project aims to make Solidity available for other
blockchains, and focuses on maintaining compatibility with Solc, so that developers
can use their existing codebase for blockchains other than Ethereum with minimal
modifications.

The purpose of Solang is two-fold: first of all, developers with solidity
language knowledge can develop new smart contracts for non-ethereum blockchains
in Solidity, so they do not have to learn a new language.
Secondly, there is a large amount of existing Solidity contracts available,
which can be recompiled for a different blockchain.

Currently, Solang targets the following blockchains:

- [Solana](https://solana.com)
- [Substrate Polkadot](https://substrate.io)
- [Ethereum ewasm](https://ewasm.readthedocs.io)

At the time of writing, these chains are the 2nd, 9th, and 11th by market
capitalization according [coinmarketcap](https://coinmarketcap.com/) (the coins
are listed by market cap).

Note that public Ethereum does not currently support ewasm, however work
for ewasm support on Ethereum is underway.

Any other blockchain that wishes to have Solidity language support is welcome to a
new target to the Solang project. The cosmos blockchain
[grant foundation](https://interchain.io/) has said it would
[support a grant for adding CosmWasm support](https://github.com/hyperledger-labs/Solang/issues/582).

# Dependent Projects

None

# Motivation

The existing [Ethereum Solidity compiler](https://github.com/ethereum/solidity/)
is written in C++ and does not use modern tooling like parser generators or the
LLVM infrastructure for code optimization and generation.

A new compiler, written from scratch, like Solang, offers the following advantages:

- It can target any blockchain, not just Ethereum.
- It generates efficient code using the world-class LLVM compiler backend.
- The Solidity language can be extended to support blockchain specific features.
- The development is streamlined to only a frontend compiler, which deals with
  parsing, semantic analysis and intermediate code generation.

There is a similar Solidity compiler project, called
[SOLL](https://github.com/second-state/soll)
but development has stalled on this project. There is also the
[Ethereum Solidity compiler](https://github.com/ethereum/solidity/).

# Status

Solang can virtually parse anything Solc can and generate code for the majority of Solidity construcuts. The maintainers are focused on providing full compatibility for Solidity on both Solana and Polkadot blockchains. There is a tentative roadmap available on the repository's [README file](https://github.com/hyperledger-labs/solang#tentative-roadmap).

Improvements in performance and code generation are gradual and the project has mainly attracted Hyperledger mentees to work on such tasks.

Solang would move into incubation, if approved.

# Solution

Solang supports Solidity v0.8, the latest language version. With a few minor
exceptions, Solang supports all the language constructs that Ethereum Solidity
supports.

Solang is a compiler, and does not know anything about building transaction
or deploying contracts. The compiler merely outputs the binary contract and
the metadata; other blockchain specific tooling is required to interact
with the contract on the blockchain.

The compiler has the following stages:

## Parser

The parser using an LR(1) parser generator and a hand-written lexer. This
component has been spun out into its own rust crate
[Solang-parser](https://crates.io/crates/Solang-parser).
The parser has been tested against a huge corpus of Solidity test contracts,
including the ethereum solidity's own testsuite, which runs on Solang CI.

This crate is being
used by Foundry's [forge fmt](https://github.com/foundry-rs/foundry/tree/master/fmt) command for a rust-based Solidity Code formatter.

## SEMA

This is the semantic analysis stage. The parse tree is validated, and diagnostics
(errors and warnings) are generated for invalid syntax. The output of this
stage is a fully decorated Abstract Syntax Tree (AST) of the source code.

The sema stage is the essential piece of the Solang language server, which powers the [Visual Studio Code Solang Solidity Compiler extension](https://marketplace.visualstudio.com/items?itemName=Solang.Solang). This extension gives squiggly lines
for errors and warnings, and information for tokens (e.g. variables) when hovering over them.  This was developed under the
first [Hyperledger Mentorship](https://wiki.hyperledger.org/display/INTERN/Create+a+new+Solidity+Language+Server+%28SLS%29+using+Solang+Compiler).

## Code generation

This stage transforms the AST into a control flow graph (CFG). Solang uses its
own intermediate representation of the code in CFG form. The advantage is that we can do flow analysis passes on a higher level than LLVM
can do. For example, accessing state on a blockchain is expensive and we
remove redundant state stores or state loads from the generated contract code. Here is
an [overview of all the passes Solang has](https://Solang.readthedocs.io/en/latest/optimizer.html).

The [2nd hyperledger mentorship](https://wiki.hyperledger.org/display/INTERN/Implement+two+compiler+passes+for+the+Solang+Solidity+Compiler) implemented two additional
passes for improved code generation.

## Emit

The last stage transforms our own intermediate CFG from into LLVM IR. This stage
is fairly straightfoward.

Solang is licensed under the Apache-2.0 license.

## LLVM Backend

The LLVM backend is used for a selection of optimization passes, and generates
the correct code for the target chain to create an in-memory object file. This
is then linked using the LLVM linker into the final file.

## Testing

There is a mock implementation of the Solana, Substrate, ewasm, that serve to
implement runtime tests and assert the correctness of the compiler's output.
There are also integration tests which use the actual chain for end-to-end testing:
compile solidity, deploy it to a node of the blockchain (running in a container),
and call various contract functions.

# Effort and Resources

The aim for Solang is to be a portable compiler which supports multiple
blockchains. Therefore hosting it at Hyperledger makes sense, as this is a
neutral space where competing vendors collaborate.

Initial funding for Solang provided was through two grants from the Web3
Foundation and another grant from the Solana Foundation.

Currently there are three people working on Solang full time:

Solana Labs:
- Sean Young [<sean@mess.org>](mailto:sean@mess.org)
- Lucas Steuernagel [<lucas.tnagel@gmail.com>](mailto:lucas.tnagel@gmail.com)

Parity Tech:
- Cyrill Leutwiler [<bigcyrill@hotmail.com>](mailto:bigcyrill@hotmail.com)

It is expected that the integration with Solana will finish end by the end of 2022,
attracting more users and more relevance for the project. As the compatibility with
both Parity and Solana matures, the development focus is supposedly shifting to
performance improvements and new features to the Solidity language.

The Web3 Foundation funds gitcoin bounties for
[certain issues](https://github.com/hyperledger-labs/solang/issues?q=is%3Aissue++label%3Abounty-M%2Cbounty-S%2Cbounty-L). These are small bounties (about 400US$) for small issues.

# How To

The source code is hosted on [github](https://github.com/hyperledger-labs/Solang)
and the [documentation](https://Solang.readthedocs.io/en/latest/) is extensive.
There is documentation on how to [run Solang on the command line](https://Solang.readthedocs.io/en/latest/running.html),
and blockchain specific instructions for [Solana](https://solang.readthedocs.io/en/latest/targets/solana.html),
[Substrate](https://solang.readthedocs.io/en/latest/targets/substrate.html), and
[Burrow](https://solang.readthedocs.io/en/latest/targets/burrow.html).

# References

N/A

# How does Hyperledger Solang meet the incubation entry considerations?
### Codebase
* _Code should exist as open source software in some form. Previous accepted projects have come up through labs (e.g., Cactus, Ursa); while others previously had stand alone governance prior to joining (e.g., Besu)._

  **Solang has been in Hyperledger Labs since December, 2018. This is where the project started.**

* _DCO sign off should exists in the code repository. If not 100% ready, the code must be capable of becoming compliant upon entry (i.e., squash commit)._

  **Solang has required DCO signoffs since entry into the Labs**

### Maintainers
* _The project should have multiple maintainers. These maintainers need not be from different companies; however, having maintainers from different companies is seen as a positive sign. Proposals with only one maintainer have been rejected by prior TSCs._

  **The maintainers can be found listed in [MAINTAINERS.md](https://github.com/hyperledger-labs/solang/blob/main/MAINTAINERS.md). Multiple companies are represented in the list.**

* _The project should have demonstrable examples of POC/production uses publicly available._

  **Solang is being used for multiple Web3 engagements on Polkadot and Solana, none of them public yet. One engagement is aiming for production in the October 2022.**

* _The project should have the backing of more than one organization/individuals (i.e., the project proposers should be able to demonstrate significant, long term contribution in codebase)._

  **There have been commits from at least 23 separate individuals during its lifetime.**

### Community

* _The TSC is more likely to accept projects that have contributors familiar with open source practices. Participating in existing projects or starting in Hyperledger Labs is a great place to grow this experience._

  **As mentioned previously, Solang has been operating in an open source model since being brought into Hyperledger Labs in 2018. Solang also utilizes all of the Hyperledger community channels for answering questions and hosting meetings. We have a daily public call, use github, and discord.

  We've had conversations with Hyperledger Staff about how to leverage their support for further community building, should
  Solang be accepted into incubation.**

### Sponsors

* _Sponsors are advocates for the project. There should be more than one sponsor, and they should be from different organizations. They may or may not be committing resources to the project._

  **Multiple sponsors exist for the project as listed at the top of this document, including sponsors who are contributing and using solang.**

### Legal
* _Trademark concerns – project names should not be trademarked by a contributing company or if it is, then the trademark will need to be handed over to Hyperledger. Project names must be approved by the Hyperledger marketing committee_

  **There is no trademark that we are aware of for solang. We would the project to be called either Hyperledger Solang or we would like the Hyperledger marketing committee to propose a name for the project.**

* _Projects do not require a name prior to being submitted._

  **Hyperledger Solang for now but we are open to suggestions. The idea behind solang is many languages are called *something*-lang, golang or clang.**

* _Codebase should be Apache 2 licensable, without encumbrances_
    * _Non-Apache 2 licensed code is possible, but requires Governing board approval (Section 12 subsection d of the Hyperledger Charter)_
    * _Special examination should be given to copyleft and non-licensed code._
    * _Required patent licensing issues have prevented projects from entering Incubation._
    * _GPL licensing issues have prevented projects from entering Incubation._

  **The source code is Apache 2 licensed.**

* _If code does not already have copyright, the code should be modified to include copyright as per Copyright and License Policy prior to being brought into Hyperledger._

  **The team is working on adding the copyright information to the files.**

# Closure

The goal of Solang is to bring the Solidity language to as many blockchains as
possible. Writing a production quality compiler is a complex task, so colaboration
between blockchains will be hugely beneficial.

The success of the project can be measured by the number of projects that
use Solang as a compiler.