---
layout: default
title: Introduction
nav_order: 1
---
[//]: # (SPDX-License-Identifier: CC-BY-4.0)

# LF Decentralized Trust Labs

LF Decentralized Trust Labs provides a space (i.e., GitHub repos) where work can
easily be started without the creation of a project. Please refer to
the [LF Decentralized Trust Labs wiki page](https://wiki.hyperledger.org/display/labs)
for additional information.

## Process to propose a new lab

1. Fork the [lf-decentralized-trust-labs.github.io](https://github.com/lf-decentralized-trust-labs/lf-decentralized-trust-labs.github.io) repository.

2. Fill out the [Proposal Template](https://github.com/lf-decentralized-trust-labs/lf-decentralized-trust-labs.github.io/blob/master/proposal-template.md)
and save it into the labs subdirectory under the name of your lab,
such as mynewlab.md. It is expected that your lab repository will have
the same name so keep that in mind. Also, when picking a name for your lab, note that a lab **CANNOT** be named the same as a product, network or any other existing entity.  Open source code should have a distinct identity from any instance of that code being used as a product or service.  If you do name your lab after a product or service note that you will need to change it later.

3. In the Proposal Template, there is an entry for sponsor(s). Although not required, proposers are encouraged to seek a sponsor who can help them create ties with the rest of the LF Decentralized Trust community and ensure that the proposal is cogent and novel (in conception, proposed execution, or interested community).<br/>
To find sponsors:
   1. use your connections to existing projects and ask maintainers,
   2. find working groups or projects with affinities to the proposed lab and pitch the project (good to have the template already filled out) in associated channels and/or mailing lists. The WG chairs emails, the maintainers contacts etc can be found on the wiki or github. Make personal appeals if you can. Every repository contains a MAINTAINERS file that lists the current maintainers with their contact information and you can reach them all by posting to the [Maintainers list](https://lists.lfdecentralizedtrust.org/g/maintainers).

4. Commit your changes with proper sign-off. This means that your commit
log message must contain a line that looks like the following one,
with your actual name and email address:

        Signed-off-by: John Doe <john.doe@example.com>

   Adding the `-s` flag to your `git commit` command will add that line
automatically. You can also add it manually as part of your commit
log message or add it afterwards with `git commit --amend -s`.

5. Submit a Pull Request.

The [labs stewards](stewards) will then review your proposal. Like sponsors, stewards do not have a responsibility beyond this; ongoing work like contributing code or reviews is not tied to their role as stewards. In reviewing the proposal, the stewards make sure that the proposal is cogent and novel (in conception, proposed execution, or interested community).

## Bringing in an existing repository

By default the Lab stewards will create a new repository for you to
start from but if you have an existing github repo you would like to
bring to your proposed lab you have the option to request for that
repo to be reused instead. This is however only possible if every
commit in your existing repo is signed-off so there is no
[DCO](https://developercertificate.org/) related issues. If that is
not the case, you will need to bring your code by squashing all of
your commits into a single first commit made against your new lab
repo with your sign-off.

## License requirement

All LF Decentralized Trust software must be made available under an
[Apache 2.0 license](LICENSE).
This applies to Labs. Please, make sure to license all incoming code
and new code accordingly, and ensure that all commits are made with
proper sign-off so that no [DCO](https://developercertificate.org/)
related issue is introduced.

## Code of Conduct

All LF Decentralized Trust community members must adhere to the
[Code of Conduct](https://lf-decentralized-trust.github.io/governance/governing-documents/code-of-conduct.html#code-of-conduct).
