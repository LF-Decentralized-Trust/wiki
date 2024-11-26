1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-09-03 Framework Go Weekly Planning

Created by Aleksandar Likic, last modified by Troy Ronda on Sep 03, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

03 Sep 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (organization) &lt;email&gt;
- Troy Ronda (SecureKey) &lt;troy.ronda@securekey.com&gt;
- Sudesh (SecureKey)
- Filip (SecureKey)
- Firas (SecureKey)
- Talwinder (SecureKey)
- Rolson (SecureKey)
- George (SecureKey)
- Baha (SecureKey)
- Bob (SecureKey)

## Welcome / Introductions

## Announcements

- None

## Release Status

- None

## Work Updates (from the previous week)

- DIDComm inbound handlers completed (Rolson)
- Selection criteria RFC (in progress) (George)
- Controller REST API first endpoint added (Sudesh)
- Legacy DIDComm envelop (in progress) (Filip)
- Restructures aries-framework-go to create two clients and services (Firas)
- State handlers (in progress for review) (Talwinder)
- DIDComm Envelope
  
  - 50% done

## Grooming

- Splitting up crypto issues - Filip / Baha (10 mins)
  
  - DIDComm Envelope.
  - Build wrapper for Go standard packages to match up with the Python/PHP libraries.
  - [#197 Legacy Encryption](https://github.com/hyperledger/aries-framework-go/issues/197)
  - [#196 JWE Encryption](https://github.com/hyperledger/aries-framework-go/issues/196)
- [Implement RecipientKeys in CreateInvitation](https://github.com/hyperledger/aries-framework-go/issues/178) - Firas (10 mins)
  
  - Need pluggable secrets store interface &amp; wallet interface. Also need initial simple 0.1.0 implementation. (Firas: please create GitHub items and add here.)

## Design discussion

- [Implement RecipientKeys in CreateInvitation](https://github.com/hyperledger/aries-framework-go/issues/178) - Firas (10 mins)
  
  - Next steps:
    
    - Review wallet RFC &amp; Python/Rust implementations.
    - Create GitHub items.
- State handlers - Talwinder (5 min)
  
  - Topic: How the response is associated to the accepted invitations?
  - Next steps:
    
    - Design discussion on the primary key for a connection.
    - Allow transition directly from null state to requested state.
      
      - Believed to be minor tweak to the code.
      - Merge current PR (hopefully today).
    - State machine needs to execute protocol actions when performing transitions.
      
      - Groom and create GitHub issues.
    - Registration of pre/post event listeners.
      
      - Groom and create GitHub issues.
- DIDComm Inbound Handlers[\[#188\]](https://github.com/hyperledger/aries-framework-go/issues/188)/LevelDB Config[\[#148\]](https://github.com/hyperledger/aries-framework-go/issues/148) - Rolson (5 min)
  
  - Topic: Lifecycle methods for the inbound transport.
  - Next steps:
    
    - Implement.
    - framework.New &amp; framework.Close
      
      - Underlying components will have Start/Stop
      - Expect that Inbound transport is Started for framework.New
      - Expect that Framework instantiates services (not Context)
      - Framework is missing the lower-level non-exported bootstrap context. Needs refactoring.
  - Question: should context created on each call to framework.Context()? Yes
- DIDComm protocol service package contents - George / Sudesh (10 mins)
  
  - Topic: What is the API surface didcimm protocol &amp; service packages.
  - Model differences between the API of the various clients and the DIDComm protocols (based on the RFCs).
    
    - Question: Where should the respective models live?
      
      - Answer: We do not want abstractions leaking between layers. In particular, the REST API (swagger/openAPI) special models should not be part of Client nor Protocol Service.
    - ReceiveInvitation should not be a special function in the Protocol Service. The functionality should be covered by Handle.
    - AcceptInvitation is not a function of the Protocol Service but rather an Action on an Event fired by the Protocol Service.
    - CreateInvitation is not a function of the Protocol Service but rather a static utility.
    - Event messaging should use the Go idiom of channels. In Fabric SDK Go, the lower layer would create the channel and return it to the higher layer upon registration.

### Addendum (post meeting)

- Configuration for Framework
  
  - Rather than having the framework pass (and hold) a global configuration, we should directly inject appropriate configuration into each component.
    
    - The configured component instances are passed into the Framework constructor.
    - To make life easier for developers, we provide functional options in a defaults package that construct default packages with common options. We also envision the defaults package being able to read a configuration and construct from that configuration.
  - Inbound transport
    
    - Defaults to random port
    - Exposes External Endpoint and Endpoint information
      
      - Endpoint: The endpoint known by the transport
      - External Endpoint: The endpoint reported externally
    - Can be configured with a different external endpoint and configuration to set the Endpoint (e.g., host:port for HTTP transports).
  - Label should be an argument for CreateInvitation
  - DB storage path

## Milestone progress

- TBD

## Other Business

- TBD

## Future Topics

- TBD

## Action items

- TBD

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
