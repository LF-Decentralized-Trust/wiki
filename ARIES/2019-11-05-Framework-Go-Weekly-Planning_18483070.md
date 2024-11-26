1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-11-05 Framework Go Weekly Planning

Created by Rolson Quadras, last modified on Nov 05, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

05 Nov 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)  (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) (SecureKey) &lt;troy.ronda@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- DIDExchange Rest API - Integrate Action events with webhooks [#579](https://github.com/hyperledger/aries-framework-go/issues/579)- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- DIDExchange Rest API - Support for AcceptExchangeRequest API [#549](https://github.com/hyperledger/aries-framework-go/issues/549)- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- DIDExchange Rest API - Return ConnectionID [#537](https://github.com/hyperledger/aries-framework-go/issues/537)- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Add/verify signature in exchange response [#24](https://github.com/hyperledger/aries-framework-go/issues/24) ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Support for public did in request message([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Remove transientStore from did exchange service [#687](https://github.com/hyperledger/aries-framework-go/issues/687)  - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- DIDExchange - Transient v Permanent Data store [#622](https://github.com/hyperledger/aries-framework-go/issues/622) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Allow injectable transient storage [#672](https://github.com/hyperledger/aries-framework-go/issues/672) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Concurrency failure in bdd-test [#649](https://github.com/hyperledger/aries-framework-go/issues/649) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Fix service endpoint in create invitation response (Complete) [#572](https://github.com/hyperledger/aries-framework-go/issues/572) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- RestAPI - Get label value in CreateInvitation [#552](https://github.com/hyperledger/aries-framework-go/issues/552) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Grooming stories for issue-credential epic [#663](https://github.com/hyperledger/aries-framework-go/issues/663) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Compute the sendVerKey for sending response [#353](https://github.com/hyperledger/aries-framework-go/issues/353) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence))
- State Refactoring [#677](https://github.com/hyperledger/aries-framework-go/issues/677) closed [#679](https://github.com/hyperledger/aries-framework-go/issues/679) In progress.  ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
  
- Set the Legacy pack/unpack implementation as the default [#632](https://github.com/hyperledger/aries-framework-go/pull/632) ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence))
- Refactor Keys structure in KMS [#596](https://github.com/hyperledger/aries-framework-go/issues/596) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )
- Introduce protocol client implementation [#657](https://github.com/hyperledger/aries-framework-go/issues/657) (work in progress) (@Andrii Soluk)
- Verifiable Credential follow-up issues [#586](https://github.com/hyperledger/aries-framework-go/issues/586), [#514](https://github.com/hyperledger/aries-framework-go/issues/514) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

## Grooming updates (from the previous week)

## Design discussion

- [0.1.1 Overview](Framework-Go-v0.1.1_18482004.html)
- WebAssembly and C Bindings ([Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence))
  
  - Folders:
    
    - cmd/aries-c (generates C callable shared objects and archives).
    - cmd/aries-wasm (generates Web Assembly).
    - pkg/binding/c/didexchange (C exports for DIDExchange Client).
    - pkg/binding/wasm/didexchange (WASM exports for DID Exchange Client).
    - (and so forth).
  - Testing strategy:
    
    - BDD
      
      - WASM in browser. GoLang can drive remote browser: [https://github.com/sclevine/agouti](https://github.com/sclevine/agouti) (as can similar JS BDD frameworks).
      - WASM outside browser. Load in GoLang as a wrapper client OR rewrite BDD tests in external language (JS).
      - C outside browser. Load in GoLang as a wrapper client OR rewrite BDD tests in external language (JS).
    - Unit Test
      
      - C bindings - should be able to test exported functions directly as normal Go unit tests.
      - WASM bindings
        
        - The pre-transformed test functions should be testable as normal Go unit tests.
        - TBD: the JS function transformer (if needed).
        - Probably need to mock browser functions (IndexedDB, ...).
  - PoCs:
    
    - [https://github.com/troyronda/aries-framework-go/tree/wasm](https://github.com/troyronda/aries-framework-go/tree/wasm)
    - [https://github.com/troyronda/aries-framework-go/tree/c](https://github.com/troyronda/aries-framework-go/tree/c)

## Milestone progress

- TBD

## Other business

- [https://didcom.org](https://didcom.org) is now used as the prefix for message types (replaces did:sov:....)
- FYI: [https://github.com/hyperledger/aries-rfcs/tree/master/concepts/0289-toip-stack](https://github.com/hyperledger/aries-rfcs/tree/master/concepts/0289-toip-stack)
- FYI: [https://github.com/hyperledger/aries-framework-go/issues/694](https://github.com/hyperledger/aries-framework-go/issues/694) (latest linter fixes)

## Future topics

- TBD

## Action items

- Groom discrepancies in rest api

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
