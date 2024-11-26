1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Planning](Framework-Go-Planning_18511940.html)

# Hyperledger Aries : Framework Go v0.1.0

Created by George Aristy, last modified by Firas Qutishat on Oct 15, 2019

Objectives

- Creation and validation of [Peer DIDs](https://dhh1128.github.io/peer-did-method-spec/) (genesis version only) - contained in [\[#35\]](https://github.com/hyperledger/aries-framework-go/issues/35)
- `did-exchange` protocol - contained in [\[#42\]](https://github.com/hyperledger/aries-framework-go/issues/42)
- [Cryptographic envelopes](https://github.com/hyperledger/aries-rfcs/tree/master/features/0019-encryption-envelope) with the updates discussed in [hyperledger/aries-rfcs#133](https://github.com/hyperledger/aries-rfcs/issues/133) - contained in [\[#36\]](https://github.com/hyperledger/aries-framework-go/issues/36)
- Support for [Ed25519VerificationKey2018](https://w3c-dvcg.github.io/lds-ed25519-2018/) - contained in [\[#96\]](https://github.com/hyperledger/aries-framework-go/issues/96)
- Local storage of peer DIDs - contained in [\[#35\]](https://github.com/hyperledger/aries-framework-go/issues/35)
- Resolution of DIDs - contained in [\[#86\]](https://github.com/hyperledger/aries-framework-go/issues/86)
- Live Demo 1: simple DID exchange - contained in [\[#67\]](https://github.com/hyperledger/aries-framework-go/issues/67) [\[#68\]](https://github.com/hyperledger/aries-framework-go/issues/68) [\[#74\]](https://github.com/hyperledger/aries-framework-go/issues/74) [\[#44\]](https://github.com/hyperledger/aries-framework-go/issues/44)
- Live Demo 2: ledger-backed DID resolution using [Hyperledger Fabric and Sidetree](https://github.com/trustbloc/sidetree-fabric) via HTTPS binding - contained in [\[#124\]](https://github.com/hyperledger/aries-framework-go/issues/124)

Please also see the [0.1.0 GitHub milestone](https://github.com/hyperledger/aries-framework-go/milestone/1) description.

# Design considerations

`aries-framework-go` is a highly customizable framework that provides sensible defaults.

Details regarding the project's layout can be found here: [Framework Go Package Hierarchy.](Framework-Go-Package-Hierarchy_18511775.html)

## Creation and validation of Peer DIDs

The framework should support several DID methods of which `did:peer` is just one.

`did:peer` to be enabled for creation and resolution by default.

Validation on peer DIDs:

- [Namestring generation method](https://dhh1128.github.io/peer-did-method-spec/#namestring-generation-method)
- [Peer DID format](https://dhh1128.github.io/peer-did-method-spec/#recognizing-and-handling-peer-dids)
- When creating, a[t least one publicKey and one authorization](https://dhh1128.github.io/peer-did-method-spec/#namestring-generation-method)

Only the [genesis version](https://dhh1128.github.io/peer-did-method-spec/#dfn-genesis-version) of Peer DIDs is required for this milestone.

## Cryptographic Envelopes

Full support for cryptographic envelopes with ECDSA keys.

## Support for Ed25519VerificationKey2018

Implement the [Ed25519 Signature 2018](https://w3c-dvcg.github.io/lds-ed25519-2018/) signature suite for creating DID documents and proving ownership.

## did-exchange protocol using HTTPS as transport

The `did-exchange` protocol to be fully implemented.

The framework will support many transports of which HTTPS is one. HTTPS to be enabled by default.

## Local storage of peer DIDs

The framework will support several storage mechanisms.

No specific implementation targeted for this milestone. (note: it is assumed we will continue with the goleveldb approach for this iteration.)

Define generic storage interface that allows the Agent to protect its secrets from the storage provider.

## DID Resolution using HTTPS binding

The framework will support external DID resolution using the [HTTPS binding](https://w3c-ccg.github.io/did-resolution/#bindings-https).

We will demonstrate usage of a [Fabric enabled with the Sidetree protocol](https://github.com/trustbloc/sidetree-fabric) (exposing the HTTPS binding for DID resolution).

## Live Demo 1: simple DID exchange

The goal is to showcase the following with two non-mobile Agents both running on the same laptop:

- Creation and validation of [Peer DIDs](https://dhh1128.github.io/peer-did-method-spec/) (genesis version only)
- `did-exchange` protocol with cryptographic envelopes and using HTTPS as transport
- Local storage of peer DIDs

The presenter should be able to run the steps one by one as they showcase the demo to others.

A controller API is needed on each Agent in order to drive the demo's steps. The controller API in this framework will be closely aligned with the one in [aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python) with the goal of demonstrating interoperability.

Outline:

![](plugins/servlet/confluence/placeholder/unknown-macro)

## Live Demo 2: ledger-backed DID resolution using Hyperledger Fabric and Sidetree

The goal is to showcase usage of ledger-backed DIDs during DID exchange and also demonstrate usage of another Hyperledger DLT (Fabric). This is a variation of Live Demo.

As with Live Demo, we should be able to run step by step. In this case, we additionally want to highlight:

- Creation of the DID in fabric-sidetree.
- Demonstrate that the fabric ledger contains the DID (showing the JSON document, batch file, and block containing the hash).
- The HTTPS request &amp; response that shows we made an external call to the DID resolution endpoint of fabric-sidetree (and that it follows the HTTPS binding).
- Exchange and resolution of the Sidetree DIDs between agents.

The Fabric with Sidetree project should be pulled from [dockerhub](https://hub.docker.com/r/trustbloc/sidetree-node) and used with a docker-compose environment for easy demo setup. 

This demonstration makes progress towards one of the goals of the Hyperledger Aries project: "Cross-platform integration" (see [Aries Proposal FAQ](https://lf-hyperledger.atlassian.net/wiki/spaces/TSC/pages/21430282/Hyperledger+Aries+Proposal)), and also helps demonstrates the possibility of a cross-Hyperledger scenario.

![](plugins/servlet/confluence/placeholder/unknown-macro)

## Attachments:

![](images/icons/bullet_blue.gif) [0.1.0\_demo](attachments/18481914/18511946) (application/gliffy+json)  
![](images/icons/bullet_blue.gif) [0.1.0\_demo.png](attachments/18481914/18511947.png) (image/png)  
![](images/icons/bullet_blue.gif) [0.1.0\_demo\_ledger](attachments/18481914/18511980) (application/gliffy+json)  
![](images/icons/bullet_blue.gif) [0.1.0\_demo\_ledger.png](attachments/18481914/18511981.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
