1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)

# Hyperledger Iroha : Modular cryptography providers

Created by Михаил Болдырев on Aug 26, 2020

Priority

SHOULD 

Type of change request

FEATURE

Epic link  
Status

WORK IN PROGRESS

Target release

## Background

Cryptographic operations are used in Iroha node for several purposes:

- **signing** inter-peer messages, ledger data and authentication to clients
- **verifying** other peers messages and ledger data, authentication of clients
- **hashing** stuff for identification of objects like transactions, blocks, maybe sth else

There are various implementations of these algorithms and the projects may have different requirements on them.

## Problem

Projects may need Iroha v2 to use custom cryptography providers to satisfy special security requirements. These requirements may demand specific certified algorithms or hardware secret protection.

## Solution

### overview

Decouple cryptography provider as a reusable abstraction. Implement support for widely used standard PKCS11. Implement other providers on demand as modules.

### the abstraction

It seems, that most crypto providers have several common architecture facts:

- a provider needs some initialization that has to be held in some context for future usage.
- crypto functions use keys by some handle. keys need to be created first, including public-only keys.
- crypto functions are polymorphic, e.g. same asymmetric sign/verify functions work with all supported asymmetric key types.
- there may be many available cryptographic schemes with different parameters. for example, one of them is ECDSA, which is parametrized by the curve, hashing function, hashing parameters.
- the data to sign/verify can be sent to the module (when required, in chunks), or can be hashed locally and only the hash be sent for the rest of the operation.

With that, it seems reasonable that:

- there is a stateful class for each crypto function: Signer, Verifier, Hasher.
- keys are submitted to the module once (e.g. on peer/client addition) and the identifiers are held in iroha for operation. the required crypto parameters are parsed and set up only once for each key. some of them set the key type, some are stored in Signer/Verifier/... for crypto function parameters.
- each public/private key and hash in the API has to go along with all the required identifiers of the algorithm.
- Signer and Verifier should be configurable to hash data locally (better performance in some use cases) or using the module (more control and customization when required).

### implementation

In the configuration of the node, crypto providers are described for each required operation: signing the peer messages and blocks, verifying signatures, hashing stuff. For verification, multiple providers may be configured and assigned priorities, which allows to verify signatures of various types not supported by single provider.

During startup, the configuration is parsed and the crypto providers initialized. The Signer implementation is configured with the secret data. The Verifier object is configured with all supported algorithms and the modules that provide them (for example, by querying the modules which algos they support).

During the node operation, when a new public key is added to the ledger, it is added to the Verifier instance, which initializes it as required by the backend. When a key is removed from the ledger, a call is made to Verifier to remove it. Verification of signatures produced by keys that were not previously added seems not needed, as a key should be given some trust before it can authenticate anyone.

The most desired crypto provider is, probably, PKCS11. It usually comes as a vendor-precompiled shared library implementing the standard interface. Its initialization is also to some extent standardized, so the configuration structure for such module will include the library path, slot ID, pin, and an optional signer key ID and type. The rest of initialization is usually controlled by some specific configuration file, which is searched for in hard-coded locations or by the path in some environment variable.

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
