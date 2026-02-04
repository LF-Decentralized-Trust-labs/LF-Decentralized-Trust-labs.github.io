---
layout: default
title: did:webs DID Method Implementation
parent: Archived Labs
---

# did:webs DID Method Implementation

[did:webs resolver](https://github.com/hyperledger-labs/did-webs-resolver)

## Short Description

This Hyperledger Labs project is a reference implementation of the **`did:webs`
DID Method**. `did:webs` extends the web-based DID resolution concepts of the
well known `did:web` DID Method to include security and verifiability to the
DIDDoc and documents published by the DID controller. Unlike did:web, this
method’s trust is not rooted in DNS, webmasters, X509, and certificate
authorities. Instead, it uses [KERI] to provide a secure chain of cryptographic
keys events by those who control the identifier. `did:webs` is to `did:web` what
HTTPS is to HTTP.

See the [`did:webs` specification] for more details about the usage and security
properties of the DID Method.

## Scope of Lab

The lab is an open source implementation of the components of the `did:webs`
specification that can be used by Hyperledger Aries agents to create DIDs, and
publish documents for issuing Hyperledger AnonCreds verifiable credentials.

For Hyperledger Aries agents issuing AnonCreds credentials the software allows:

- Using KERI software to create a KERI Autonomic Identifier (AID), and the Key
  Event Log (KEL) that provides the history of that AID, including both key
  events (additions, rotations, etc.), and transaction events related to the use
  of the DID (signing and publishing, for example, AnonCreds schema, credential
  definitions and revocation registries.).
- Define during the creation of the AID the location on the Internet at which
  the DID will be published.
- Generate the DID for the identifier based on a combination of the URL and AID.
- Generate from the KEL a DID Document (DIDDoc) that adheres to the [DID Core
  Specification].
- Publish both the DIDDoc and KEL to the intended location of the DID.
- Update the DID DIDDoc using KERI Key and Transaction events, and when
  appropriate, publishing updates to the DIDDoc and KEL.
- Publish arbitrary files in the web path from the DID, along with a signature
  over the file contents by a key from the DID.
  - For Hyperledger Aries issuers of AnonCreds credentials, this may include
    AnonCreds schemas, Credential Definitions, Revocation Registries, [OCA for
    Aries] Bundles and more.
  - Enterprise Hyperledger Aries agents may publish files containing public
    verifiable credentials about the DID controller, such as certificates of
    Incorporation, membership in trade organizations, audit reports, and so on.

For Hyperledger Aries agents holding or verifying AnonCreds credentials, the software allows:

- Resolving the DID into a Web URL to retrieve the DIDDoc for the DID.
- Retrieving with the DIDDoc the KERI KEL/TEL file and processing the events to
  verify the provenance of the AID, and the correctness of the DIDDoc. That is,
  that the published DIDDoc is derived from the events recorded in the KERI
  KEL/TEL.
- Resolving and retrieving files in the DID web URL path. Retrieving for each
  file an associated signature across the file contents. Verifying that the
  signature is valid and, based on the KEL/TEL events, that the key used was
  published by the controller of the DID, and the event signing was a recorded.

The repository may also include open source software that publishes the
data (DIDDoc, KEL/TEL, files, and signatures) to the appropriate location on the
Internet, so that the documents can be publicly resolved.

## Initial Committers

- https://github.com/swcurran
- https://github.com/2byrds
- https://github.com/dhh1128
- https://github.com/pfeairheller
- https://github.com/peacekeeper

## Sponsor

- https://github.com/swcurran / Stephen Curran (swcurran@cloudcompass.ca) -
  Member of the Hyperledger Technical Oversight Committee (TOC).

## Pre-existing repository

To be determined if there is a pre-existing repository to be moved or this will
be a "from-scratch" implementation that uses KERI libraries as dependencies.
