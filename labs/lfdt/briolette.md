---
layout: default
title: Briolette
[//]: parent: LFDT Labs
[//]: grand_parent: Active Labs
---
# Lab Name
Briolette

# Short Description
Briolette is an experimental system for implementing offline-enabled digital
currency with an opinionated security and privacy approach. In particular, it
relies on the cryptographic properties of direct anonymous attestation (DAA)
schemes to enable pseudonymous wallet identities, repeated offline peer-to-peer
transactions with near-finality, and system-wide double spending detection and
abuse response.

# Scope of Lab
Briolette acts as a reference implementation and experimental framework for
creating offline-enabled digital currencies that may be used like physical
cash, in-person or online.  Ideally, briolette will enable the exploration and
definition of the best practices in the digital currency, identity, and
cryptography space regardless of if it is used to inform the creation of a
layer 2 payment system or a sovereign CBDC.

Beyond efficient, offline designs, briolette's scope includes exploring means
of excluding known-double spending wallets from the system, enabling different
currency authorities to operate over the same 'network', protecting the online
services from abuse using the same primitives used for transactional safety,
and exploring system policies and mechanisms which automatically scale between
widespread connectivity outages and operational maximum 'disconnected' times
for client wallets.  Additionally, the existence of this system and its design
allows for the exploration of CBDC-specific policies, such as wallet
transaction velocity.


# Initial Committers
- https://github.com/redpig

# Sponsor
N/A

# Pre-existing repository
- https://github.com/google/briolette
