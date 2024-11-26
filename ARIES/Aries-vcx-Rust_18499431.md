1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)

# Hyperledger Aries : Aries-vcx Rust

Created by Patrik Stas, last modified by James Ebert on May 29, 2024

# What is aries-vcx

Aries-vcx [https://github.com/hyperledger/aries-vcx/](https://github.com/hyperledger/aries-vcx/) is **Rust implementation of Aries protocols** and **collection of supporting projects built on top it**:

- **Aries-vcx - the first class citizen Rust crate**, library to speak **Aries protocols**, deal with **wallets**, interact with **ledger**
  
- **Mobile applications building blocks:**
  
  - **deprecated approach**: libvcx-java, libvcx-ios**:** these are C binding which enable calling aries-vcx from Objective-C and Java
  - **endorsed approach:** New approach based on UniFFI is in staged of Proof of Concept. This can generate Swift and Kotlin wrappers for aries-vcx. If you are interestd in mobile development, your contributions here would be invaluable! POC: [https://github.com/hyperledger/aries-vcx/pull/737](https://github.com/hyperledger/aries-vcx/pull/737)
- **NodeJS:** we have NodeJS bindings to build NodeJS applications on top of aries-vcx

# How to get involved

We welcome new contributors to improve aries-vcx or build on top of it!

- Talk with us on **Discord** [https://discord.com/channels/905194001349627914/955480822675308604](https://discord.com/channels/905194001349627914/955480822675308604)
- Join our **bi-weekly community calls via Zoom**: [Community calls](Community-calls_18499459.html)

# Built on top of aries-vcx

Aries-vcx is generic crate which can be used to build Rust applications and libraries. We strive to be opinion-less to enable arbitrary use-case. Aries-vcx can be used to build web, mobile, cli and potentially embedded agents.  
Example of crates built on top of aries-vcx:

- [libvcx](https://github.com/hyperledger/aries-vcx/tree/main/libvcx) - wrapper around aries-vcx to enable certain FFI approach
- [uniffi wrapper](https://github.com/hyperledger/aries-vcx/pull/737) (POC phase) - wrapper around aries-vcx to generate Kotlin and Swift mobile wrappers, using uniffi library
- [aries-vcx-agent](https://github.com/hyperledger/aries-vcx/tree/main/agents/rust/aries-vcx-agent) - simple agent implementation with in-memory storage
- [aries-vcx-backchannel](https://github.com/hyperledger/aries-agent-test-harness/tree/main/aries-backchannels/aries-vcx) - simple web agent built on top of aries-vcx-agent, used for cross testing aries-vcx with other Aries implementations in [Aries Agent Test Harness](https://wiki.hyperledger.org/to%20cross%20test%20aries-vcx%20against%20other%20aries%20implementations%C2%A0https:/github.com/hyperledger/aries-agent-test-harness)

#### Project ideas

- **Aries-vcx uniffi wrapper -** continue implementation of [uniffi\_aries\_vcx](https://github.com/hyperledger/aries-vcx/tree/main/uniffi_aries_vcx)
  
  - This can unlock building native mobile apps with aries-vcx
- **Aries mediator client -** implement rust client capable of connecting with mediation agent and use pick-up protocol [https://github.com/hyperledger/aries-rfcs/tree/main/features/0685-pickup-v2](https://github.com/hyperledger/aries-rfcs/tree/main/features/0685-pickup-v2) to receive messages
  
  - This can unlock integration of aries-vcx with different aries mediation agent implementations! This is extremely important for mobile use-cases.
- **Verifier agent** - build aries agent specialized for proof verification
  
  - In the real world, there will be presumably handful of issuers but likely many verifiers! Deploying full featured agent capable of both issuance, verification and perhaps other protocols can be complex, a narrowly focused Verifier agent could be built on `aries-vcx` . This would require minimal configuration, the agent can be largely stateless as it would only need to READ ledger, not write. Aries-vcx is perfectly positioned to be core of high-performance proof verifier.
- **Load tester** - create tool to simulate many agents simultaneously 
  
  - Creating tool which can represents many agents can be useful for load/stress testing across the aries ecosystem
- **CLI agent** - building on top of [aries-vcx-agent](https://github.com/hyperledger/aries-vcx/tree/main/agents/rust/aries-vcx-agent) and some of many console UI interface frameworks available in Rust, you could build tool to manage an Aries agent from CLI interface
  
  - First implementation POC done! [https://github.com/hyperledger/aries-vcx/pull/692](https://github.com/hyperledger/aries-vcx/pull/692)
- **Aries message mediator** - build aries mediator
  
  - there's nodejs implementation of [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) in progress, but hey, why not to build an alternative!

<!--THE END-->

- **Embedded device aries agent** - try to build aries agent for embedded uses case
  
  - this is yet rather unknown journey, who knows what it entails?

<!--THE END-->

- **DID** **parser** - a proper DID type and parser
  
  - DIDs, while similar to URLs, have slightly different composition.
  - we need to be able to compose and decompose DIDs in a consistent manner

<!--THE END-->

- **DID resolver** - a component that takes a DID and returns the data it points to
  
  - things such as `DIDDocs`  or `services`  are stored on the ledger (or some other place) and need to be retrieved by resolving their DID

<!--THE END-->

- **Protocol Registry** - a static, compile-time component that holds the protocols and versions an agent supports
  
  - the first implementation uses a lazily initialized map
  - a better approach would be to have code generation in place controlled by feature flags

**Research ideas**

- Can [https://github.com/sicpa-dlab/didcomm-rust](https://github.com/sicpa-dlab/didcomm-rust) dependency be leveraged by `aries-vcx`  ?

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
