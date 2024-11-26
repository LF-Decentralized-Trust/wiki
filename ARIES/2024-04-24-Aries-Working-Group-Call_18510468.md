1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-04-24 Aries Working Group Call

Created by Sam Curren, last modified by Stephen Curran on Apr 24, 2024

## Summary:

- Service Endpoints
- Mediation

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

## Date

24 Apr 2024 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

move ![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Instnt) &lt;james@instnt.org&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio) &lt;kim@indicio.tech&gt;
- [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) (Entidad) &lt;jorge@entidad.io&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence)  (Anonyome Labs) &lt;smccown@[a](http://anonyome.com)nonyome.com&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
- Frameworks:
  
  - Aries Cloud Agent Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: [https://aca-py.org](https://aca-py.org)
    
    - ACA-Py has deprecated the Connection, Issue Credential v1, and Present Proof v1 protocols. They haven't been scheduled for removal yet and there's a plan to move the protocol implementations to plugins so people who need a little bit more life support have an opportunity but the intent is for the plugins to be eventually phased out as well.
  - Credo [https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts/discussions/1586#discussioncomment-7815973), Meetings: [Credo Meetings](Framework-JS-Meetings_18482467.html)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
  - Picos as of pico-engine version 1.3.0 natively use DIDComm v2 ([https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md](https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md))
- Mobile:
  
  - Bifold Wallet -- [https://github.com/openwallet-foundation/bifold-wallet](https://github.com/openwallet-foundation/bifold-wallet)
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
- [aries-endorser-service](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries Akrida](https://github.com/Indicio-tech/aries-akrida) - Load Testing DIDComm based protocols

## Discussion Topics

- IIW Recap
  
  - DIDComm
  - DIDComm OpenID
  - DIDs as Identifier Metasystem
- Also, MessagePickup/Delivery during Live Mode Mediation - [https://github.com/decentralized-identity/didcomm.org/pull/105](https://github.com/decentralized-identity/didcomm.org/pull/105)
- Removing Indy SDK from ACA-Py – is it time?
- Unqualified DIDs Update
  
  - Where are we?

## Other Business

## Future Topics

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
