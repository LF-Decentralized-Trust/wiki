1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Design Documents](Design-Documents_22153916.html)
4. [Modular Besu](Modular-Besu_22155011.html)

# Besu : DRAFT - Besu Software Component Map

Created by Justin Florentine, last modified on Sep 16, 2021

This document attempts to explain the current layout of the Besu project. We attempt to answer the question "why is this organized the way it is?" Software components to be considered include but are not limited to:

- Gradle projects.
- GitHub repos and sub-modules.
- Java packages

#### Design Values

There are various trade-offs we make when deciding where a software component fits in our mental model. Those trade-off choices reflect our values in organizing software, and are useful when considering where to put something and how to name it. Having a variety of values also allows us flexibility in our choices, without being constrained by a need for consistency.

- Monorepos : We value a single repo to house all submodules, since it is easy to search, and allows for greater reuse and inter-dependency. For instance, our tests may depend on a wide variety of components, depending on how high the testing scope goes. Not everything should be tested via unit tests, and for integration and system scoped testing, it is very likely to depend on many different components.
- Single Binary: This is a packaging concern that allows all the various runtime options for Besu to be met by a single executable.
- ???

#### Besu is currently divided into 49 different gradle projects.

Each of the bullet points below could likely be expanded a bit, and perhaps a README.md added next to each build.gradle file explaining it.

- ##### acceptance-tests (3 gradle subprojects)
  
  - What scope of testing does this represent?
  - Who/what is doing the accepting implied?
  - seems to provide a DSL to be used to write tests in javascript. Do these tests depend on the besu implementation specifically, or do they run over RPC and could be divorced from the besu implementation code?
- ##### metrics (2 gradle subprojects)
  
  - rocksdb is an entire gradle project for only 1 class. I am guessing this was done to isolate the metrics used to observe this db implementation.
  - core seems to be the metrics reporting scaffold, not besu specific, makes sense as its own module.
- ##### consensus(6 gradle subprojects)
  
  - consensus seems a little more important than just a feature.
  - looks like it is only the PoA stuff, why no proof-of-work?
  - each consensus mechanism
    
    - has a means of creating a block
    - has some corresponding rpc methods
    - may have some unique network messaging
    - means to validate other proposed blocks
  - the common module has a ton of bft related stuff, probably extended by ibft2 and qbft
- ##### crypto
  
  - probably makes sense to package by function instead of by feature here, to help avoid rolling your own crypto. much easier to audit and upgrade all in one place.
- ##### enclave
  
  - isolates the code needed to work with key management appliances used during PoA based private enterprise nets. It's the code for communicating with private p2p enclaves such as tessera and orion. It's mainly used for private ethereum networks.
- ##### util
- ##### config
  
  - a single package containing configuration structs, mostly for POA consensus.
- ##### plugins (1 gradle sub-project)
  
  - only contains the rocksdb submodule. this is a plugable key value store implementation.
- ##### nat
  
  - figuring out the clients IP address is non trivial in many of the environments we expect it to run.
- ##### container-tests (1 gradle sub-project)
  
  - pretty small module, looks like it is to be used by CI/CD in order to test configuration and startup of besu containers.
- ##### plugin-api
  
  - toolkit for devs who want to build plugins for besu.
- ##### besu
  
  - this can be thought of as the application module. Contains things the user interacts with, such as:
    
    - the command line interface
    - export tools, for exporting blocks to the filesystem.
    - import tools, for direct importation of blocks from the filesystem.
    - controllers - not sure what these are yet. collection of classes for wiring up plugins?
    - services - not sure what these are yet, looks like implementations of the plugin-api
- ##### privacy-contracts
  
  - this looks like some example contracts to be used on PoA networks?
- ##### testutil
  
  - same as util package, but for tests.
  - utility classes to be used when testing enterprise features like Enclave, Orion and Tessera
- ##### services (3 gradle sub-projects)
  
  - ???
- ##### ethereum  (15 gradle sub-projects)
  
  - This is where ethereum protocols are implemented.
  - All clients likely have implementations analogous to those found in this module.
    
    - are ethstats and evmtool specific to Besu, or are they implementing a spec that is common across clients?
    - what is the scope of retesteth and referencetests?
- ##### error-prone
  
  - project specific rules to be enforced by the errorprone compiler.
- ##### pki
  
  - a layer of abstraction up from cryptography. This module handles dealing with keystores and certificates, likely used by PoA networks.

Document generated by Confluence on Nov 26, 2024 13:00

[Atlassian](http://www.atlassian.com/)
