1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries DIDCommV2 Working Group](Aries-DIDCommV2-Working-Group_18499949.html)

# Hyperledger Aries : Aries DIDCommV2 Working Group 2023-04-24 meeting

Created by Ry Jones, last modified by Lance Byrd on Apr 24, 2023

## Zoom: [https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09](https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09)

## Summary:

- IIW April 2023 connect-a-thon debrief

## Date

24 Apr 2023 (6AM Los Angeles, 9AM New York, 2PM London, 3PM CET, 17H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries WG
  
  - Presented a comparison of did:keri (lite) and did:peer (algo2... algo1 is used in AFJ)
  - Need to do pros/cons spreadsheet comparing the priorities/reqs/community needs
- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
    
    - Encryption envelope (Askar impl) not fully-developed yet. We could use different libraries (SICPA Rust). SICPA DIDComm impl is what will be used... resolves did peers natively. The keys will have to be transported out of Askar, but that is acceptable for now. SICPA is the most widely used.
      
      - SICPA for DIDComm and did:peer [https://github.com/sicpa-dlab/didcomm-python](https://github.com/sicpa-dlab/didcomm-python)
      - No near-term Askar support for the DIDComm v2 encryption envelope and core protocols.
    - Protocols related to credential exchange and connection establishment. Distinguish between DIDComm v1 and v2. DID Exchange will be adapted.  The main focus is on Out-of-Band protocol.
    - Very important to extend the AATH.
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1096#issuecomment-1343833016](https://github.com/hyperledger/aries-framework-javascript/pull/1096#issuecomment-1343833016)
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1211](https://github.com/hyperledger/aries-framework-javascript/pull/1211)
    - Issue related to multi-base from SICPA for DID peer
  - Picos as Aries agents (DIDComm v1: [https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico) ; DIDComm v2 work in progress)
    
    - students have returned and they are using SICPA for envelope encryption, pack/unpack and hopeful sending messages
    - DIF Picos working group, useful for IoT devices.
    - Rich API and Internet connected to be a capable L2 agent.
    - Using Trinsic as VC as a service.
  - Swift Framework
  - Veramo Framework
    
    - WACI support [https://github.com/uport-project/veramo/issues/1106](https://github.com/uport-project/veramo/issues/1106)
    - DID Peer support [https://github.com/uport-project/veramo/issues/1105](https://github.com/uport-project/veramo/issues/1105)
      
      - Using Brian's (AviaryTech) DID Peer impl, adapting it as a plugin
        
        - PR submitted and in review [https://github.com/roots-id/didpeer-plugin](https://github.com/roots-id/didpeer-plugin)
    - Merged Mediation, agent can mediate. A Veramo mediator will be published soon.
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - working on Pickup support
  - DIDComm v2 support would probably originate from this meeting/community
- AviaryTech DIDComm TS impl
  
  - [https://github.com/aviarytech/didcomm](https://github.com/aviarytech/didcomm)
  - [https://github.com/aviarytech/did-peer](https://github.com/aviarytech/did-peer)
  - Focused on OIDC lately
- KERI Working Group
  
  - Alternative to peer DID.  More refinements to the proposal. Then present it to the Aries groups.  Similar to Algo2 of the peer DID.
    
    - KERI parameter on the DID in order to get the document. Public encryption key and serviceEndpoint.
    - Query param w/ base 64 path that you can decode
      
      - encryption keys, service endpoint, etc.
      - Compared to did:peer, the keri long form is longer
        
        - inception event only
        - But follow-on messages only need to use the short-form of KERI DID
      - So, this is not a Persistent did
    - [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) Will add a README and sample output.
- ToIP Trust Spanning Protocol
  
  - Good back and forth between Sam, Daniel, and others [https://github.com/trustoverip/trust-spanning-protocol/discussions/17](https://github.com/trustoverip/trust-spanning-protocol/discussions/17)
  - Daniel present his proposal this week, at the Wednesday TSPTF
  - Sam joins the task force and has a video of Sam's that diagrams his TSP vision [https://zoom.us/rec/play/1EcHtXeGPPynwwBvU3X4uAAw0xhFPC3CwwAIXwQ-P\_E6tPlzvBskHuzTYftS1ZrmjPw5EiBZWYwiTgdI.tx021j9JATi2l5Xq?continueMode=true&amp;\_x\_zm\_rtaid=noVlj\_2fRpuccKG26Jmytw.1675686252575.5cf45b925f44c52d0118a3fdef8541ea&amp;\_x\_zm\_rhtaid=714](https://zoom.us/rec/play/1EcHtXeGPPynwwBvU3X4uAAw0xhFPC3CwwAIXwQ-P_E6tPlzvBskHuzTYftS1ZrmjPw5EiBZWYwiTgdI.tx021j9JATi2l5Xq?continueMode=true&_x_zm_rtaid=noVlj_2fRpuccKG26Jmytw.1675686252575.5cf45b925f44c52d0118a3fdef8541ea&_x_zm_rhtaid=714)

## Discussion Topics

April 2023 IIW was awesome! Pics added, more lessons learned to come.

- [https://hackmd.io/j6U6JpQ2SRexSUKL7i2XRg](https://hackmd.io/j6U6JpQ2SRexSUKL7i2XRg)

From our last meeting:

Nessus Demo

- Amazing progress by [Thomas Diesler](https://lf-hyperledger.atlassian.net/wiki/people/557058:ef106bd5-665a-489d-a319-dfb455bd44c1?ref=confluence) on his client showing an airport scenario with multi-tenant, multi-credential presentation for [travel with a minor](https://www.w3.org/TR/vc-use-cases/#international-travel-with-minor-and-upgrade)
- [2023 04 03 Aries DIDComm V2 User Group Meeting.txt](https://lf-hyperledger.atlassian.net/wiki/download/attachments/18504069/2023%2004%2003%20Aries%20DIDComm%20V2%20User%20Group%20Meeting.txt?version=1&modificationDate=1681131758937&api=v2)

<!--THE END-->

- OOB with a 'public' did document that anyone can use. Chicken and the egg for Root-of-trust.
  
  - Start with a trust ping.
  - Request a credential? For extra validation.
- SICPA did peer Java PRs have brought it to usable place
- Demo in two weeks
  
  - OPA verification policies
  - W3C JSON-LD and JWT
    
    - We will check with [Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence) to see if we can accept an issued credential from [Thomas Diesler](https://lf-hyperledger.atlassian.net/wiki/people/557058:ef106bd5-665a-489d-a319-dfb455bd44c1?ref=confluence)
  - Technology Compatibility Kit (TCK) in java provides compliance for J2EE, similar concept to AIP
    
    - This is a large market for licensing in the java world
    - DIDComm could have a similar
  - Reference implementation
    
    - First or most complete Agent that passes the TCK
  - Can DIF own the TCK?
    
    - Create a test harness similar to what Fabio Pinheiro is asking for in DIDComm v2
- IBM w/ DIF?

### April 2023 IIW DIDComm v2 interop

- How can we get the word out?j
  
  - [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) posted on Discord [https://discord.com/channels/905194001349627914/1032736844053483621/1082338707597697055](https://discord.com/channels/905194001349627914/1032736844053483621/1082338707597697055)
- Receive a credential over OIDC (OIDC4VC) and present proof with DIDComm
  
  - Who in the OIDC to connect with? Also, connect with Sam. Ask Drummond.
  - [Walt.id](http://Walt.id) supports OIDC
- Which agents might participate:
  
  - AFJ
    
    - [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence)
    - Animo
  - Veramo
    
    - Nick
    - Cody
  - BlockTrust
    
    - [Björn Sandmann](https://lf-hyperledger.atlassian.net/wiki/people/712020:d396d505-6647-4f81-ae30-67348ec7161d?ref=confluence)
  - AviaryTech
    
    - [Brian Richter](https://lf-hyperledger.atlassian.net/wiki/people/5df66bd01833f80cb2ece346?ref=confluence)
  - Indicio
    
    - [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence)
  - PicoAgents
    
    - [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence)
  - RootsID
    
    - RootsWallet
  - Atala Prism
    
    - [Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence) [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence)
    - Anyone from Atala team attending?
  - Nessus
    
    - [Thomas Diesler](https://lf-hyperledger.atlassian.net/wiki/people/557058:ef106bd5-665a-489d-a319-dfb455bd44c1?ref=confluence) might be a recording
- What protocols do we want to highlight/use
  
  - Basic Message
  - Trust Ping
  - Mediation
  - Issue Credential
    
    - This is more complex, which format, etc.
  - Verification
  - Schema Validation
- Pre-record video showing the interop between them
  
  - For the session it needs to be very scripted so that everyone is successful
    
    - Group chat? New protocol, maybe in Fall IIW?
- Veramo agent as a test harness for DIDComm?
- BlockTrust is implementing mediator, etc and will be at IIW
  
  - No usable .NET lib, had to write it from scratch
    
    - Crypto is especially challenging
  - Reference implementations help a lot
    
    - SICPA libs continue to gain adoption and are nice for reference

Interop Profile

- AIP3 hackmd table created to compare did peer/keri/key/ etc. pros/cons/needs
  
  - [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ?both](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ?both)
- Initial contact through OOB
  
  - DID Doc should contain the endpoint which should establish the connection

DWN &amp; KERI &amp; DIDComm comparison

- [https://hackmd.io/S7RczUDxQgyHxWKBmBVW\_A](https://hackmd.io/S7RczUDxQgyHxWKBmBVW_A)

DIDComm short DIDs

- Agents can cache DIDs to know if they have resolved the long-form, etc. This cache needs to be well protected or the conversation is lost.
- DIDComm provides a way to rotate Ephemeral DIDs, specifying a new DID (even from a different DID method).

<!--THE END-->

- Ecosystem of DIDCommV2 Services or local agents
  
  - One other DCV2 agent required to work on true interop
  - Plus one agent agnostic Technology Compatibility Kit (TCK)
  - Nessus-tech domain service
  
- Nessus
  
  - [Nessus DIDComm 23.2.0 First Release](https://github.com/tdiesler/nessus-didcomm/releases)
    
    - Wallet abstraction for AcaPy + Nessus native
    - Camel Http Endpoint for Nessus agent
    - Support for RFC0434 Out-of-Band Invitation V1 &amp; V2
    - Support for RFC0023 Did Exchange V1
    - Support for RFC0048 Trust Ping V1 &amp; V2
    - Support for RFC0095 Basic Message V1 &amp; V2
    - CLI to work with supported protocols and model
    - Uses SICPA and [Walt.id](http://Walt.id)
      
      - [Recently accepted PR with SICPA](https://github.com/sicpa-dlab/didcomm-jvm/pull/66)
    - Will eventually be wrapped in a Camel component, enabling Camel endpoints to support DIDCommV2
      
      - open the doors for adoption from the Camel enterprises
- DIDComm v1 vs v2
  
  - [https://didcomm.org/book/v2/whatsnew](https://didcomm.org/book/v2/whatsnew)
    
    - simple explanation of the benefits of upgrading
  - DIDComm v1 is tightly coupled to the Aries RFCs (encryption envelope) and v2 introduces some simplicity in terms of connections
  
  AIP3
  
  - [HackMD from the last Aires WG meeting, regarding AIP 3.0](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
  - Should we specify how the did methods (like did peer) are used?
    
    - We are focused on DIDComm v2 communication but does the rest of the AIP community know that?
    - WACI issuance
      
      - Do you need to be able to resolve indy, cheqd, etc. in order to issue credential
  - Discussed sub-roles [https://raw.githubusercontent.com/hyperledger/aries-rfcs/main/features/0453-issue-credential-v2/credential-issuance.png](https://raw.githubusercontent.com/hyperledger/aries-rfcs/main/features/0453-issue-credential-v2/credential-issuance.png)
  
  Aries Agent Test Harness
  
  - What did methods are supported? And how do you configure to use did indy, orb, etc.
  - What is the priority of tests to create that will eventually be AIP3 tagged tests?
  - How is mediation tested?
    
    - With the mediation role (what is the name like bob, alice, faber, etc) and show you support the mediation features.
  - Current DIDComm-V2 specific tests:
    
    **DIDComm-V2 tests**
    
    ```
    aries-agent-test-harness % ./manage tests --tags @DIDComm-V2 
Selecting: ['@DIDComm-V2']

Feature: WACI Issuance
 @T001-IssueCredentialV3 @DIDComm-V2 - WACI issuance flow

Feature: DIDComm V2 Establishing Connections
 @T001-OobV2 @DIDComm-V2 - Establish a connection between two agents using DIDComm V2

Feature: Aries agent present proof v3
 @T001-PresentProofV3 @DIDComm-V2 - Present Proof of specific types and proof is acknowledged with a Citizenship credential type with a DID Exchange Connection
    ```
  - New tag in AATH that are not credential related, maybe:
    
    - DIDCommV2\_Peer
    - DIDCommV2\_Simple
    - Didcommv2\_base
    - Didcommv2\_layer2
  - See [https://github.com/tdiesler/aries-agent-test-harness/tree/camel/aries-backchannels/camel#aip-10-status](https://github.com/tdiesler/aries-agent-test-harness/tree/camel/aries-backchannels/camel#aip-10-status)
  
  Grand Unified Theory (GUT) Alliance
  
  - There is a warning about did peer on the spec now [https://identity.foundation/peer-did-method-spec/](https://identity.foundation/peer-did-method-spec/)
  - [https://daniel-hardman.medium.com/sentries-confessionals-vaults-and-envelopes-4a58cf4f8a5a](https://daniel-hardman.medium.com/sentries-confessionals-vaults-and-envelopes-4a58cf4f8a5a)
  - original did keri impl [https://github.com/WebOfTrust/ietf-did-keri](https://github.com/WebOfTrust/ietf-did-keri)
    
    - Needs to transition to a did keri lite (subset of did keri)
    - Signify is a typescript impl that might serve as the the keri lite impl
  - Newer than even AIP3.0. KERI and DIDComm v3.0 (likely)
  - Link to Daniel’s GUT presentation:
