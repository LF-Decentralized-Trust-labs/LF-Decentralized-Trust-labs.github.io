---
layout: default
title: Umbra
parent: Archived Labs
---
# Lab Name
[Umbra](https://github.com/hyperledger-labs/umbra)

# Short Description
This lab is to make running Hyperledger distributed ledgers under the
[Shadow simulator](https://github.com/shadow/shadow) possible. It began as a
research internship during the summer of 2018 and seeks to provide a tool for
doing research on consensus algorithms, smart contracts, scaling and other
blockchain related research topics.

Logo is a [tesseract](https://en.wikipedia.org/wiki/Tesseract)

# Scope of Lab
The scope is to make modifications to Shadow as well as to construct Shadow
plugins for Hyperledger distributed ledgers so that they can run under
simulation in a lab environment.

Shadow emulates the kernel interface to allow it to run unmodified binaries
to intercept threading, network, and memory system calls allowing it to
measure the behavior and performance of the binary in a repeatable way. It
is able to simulate networks of machines, each running processes that can talk
to each other through the simulated network. This makes Shadow a very useful
tool for researching distributed systems behavior and performance. This lab
is intended to be an ongoing project to provide a research tool for
understanding and improving the Hyperledger blockchain platforms as well as
for conducting future research in consensus algorithms and scalability.

I do not see this lab ever graduating into incubation as it is not intended to
be a shipping product but rather an ongoing collaboration between academic,
corporate, and hobbyist researchers improving upon existing capabilities and
also trying new things with our blockchains. I anticipate that we will maintain
the plugins for each of the Hyperledger blockchains as well as any
experiment-specific configurations and code.

# Initial Committers
- https://github.com/martmartinez91 (maintainer)
- https://github.com/dhuseby (maintainer)
- https://github.com/ahmetturkmen
- https://github.com/veyselpehlivan
- https://github.com/tapasweni-pathak

# Sponsor
- mwagner at redhat dot com - Mark Wagner

# Pre-existing repository
- https://github.com/martmartinez91/shadow-hyperledger
