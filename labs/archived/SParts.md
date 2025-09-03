---
layout: default
title: SParts
parent: Archived Labs
---
# Lab Name

SParts

# Short Description

The Software Parts (SParts) lab delivers a Sawtooth-based ledger that provides both accountability and access to the open source components used in the construction of a software part. A software part is any software component (e.g., library, application, container or an entire operating system runtime) that is comprised of between 0% and 100% open source.

# Scope of Lab

The initial focus is to track the open source from which today's manufactured products and devices are constructed (think IoT). The lab allows any organization, supply chain or community to easily spin up a distributed ledger that tracks: i) the open source components used and ii) their corresponding compliance artifacts (e.g., source code, notices, SPDX data, security vulnerability data, …) for the software parts used within a supply chain. A number of important benefits are obtained by knowing which open source components are used such as: 1) ensuring manufacturers are able to identify and secure the distribution rights (licenses) for all open source components; 2) understanding the impact of open source security vulnerabilities; 3) enable identification of cryptography technologies (e.g., FIPS 140-2 certification, export licensing); and 4) enable accurate reporting on all open source parts as a requirement to obtaining functional safety certification for safety critical products (e.g., medical devices, aircraft, autonomous vehicles, elevators, …). The distributable ledger provides both accountability over and access to the compliance artifacts for any given software part.

# Initial Committers

* Mark Gisi (MarkGisi, Mark.Gisi@windriver.com)
* Sameer Ahmed (SamAhm, SameerAhmed@windriver.com)

# Sponsor

Dan Middleton (dan.middleton@intel.com)

# Pre-existing repository

There is a pre-existing public repository available at https://github.com/Wind-River/sparts. We would copy over all the code except for the /apps directory. We did not initially use the git commit sign-off option and therefore need to recommit all the code to the new repo with the sign-off option. I recommend creating a new empty repo where we can re-commit the relevant pieces using the -s option.
