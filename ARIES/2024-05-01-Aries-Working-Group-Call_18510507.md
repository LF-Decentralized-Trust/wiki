1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2024 Aries Working Group Meetings](2024-Aries-Working-Group-Meetings_18518997.html)

# Hyperledger Aries : 2024-05-01 Aries Working Group Call

Created by Stephen Curran, last modified on May 01, 2024

## Summary:

- The new VC-DI Attachment Format for issuing credentials
- Aries RFCs PRs – Changing RFC Statuses
- Initial progress on DIDComm v2 in ACA-Py
- Brief Overview of did:tdw

## Zoom: [https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09](https://zoom.us/j/93803916577?pwd=UWdLSTJ2b0kvZTRyc1hZTUdQQ3ZFZz09)

## Recording:

## Date

01 May 2024 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

move ![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Instnt) &lt;james@instnt.org&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Implementations:
  
  - Aries Cloud Agent Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: [https://aca-py.org](https://aca-py.org)
    
    - ACA-Py 0.12.1 released today.
    - 1.0.0 is next – merges of waiting PRs pending, and tagging of release candidate will happen Real Soon Now.
    - Next up: Completing AnonCreds in W3C VCDM, DIDComm v2 support, [Trust DID Web](https://github.com/bcgov/trustdidweb) (did:tdw) support.
  - Credo [https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts/discussions/1586#discussioncomment-7815973), Meetings: [Credo Meetings](https://wiki.openwallet.foundation/display/CREDO/Meeting+notes)
  - Bifold Wallet -- [https://github.com/openwallet-foundation/bifold-wallet](https://github.com/openwallet-foundation/bifold-wallet) Meetings: [Bifold Meetings](https://wiki.openwallet.foundation/display/BIFOLD/Meeting+notes)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
  - Picos as of pico-engine version 1.3.0 natively use DIDComm v2 ([https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md](https://github.com/Picolab/pico-engine/blob/master/packages/pico-engine/README.md))
- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
- [aries-endorser-service](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries Akrida](https://github.com/Indicio-tech/aries-akrida) - Load Testing DIDComm based protocols

## Discussion Topics

- The vc-di attachment – [RFC 809](https://hyperledger.github.io/aries-rfcs/latest/features/0809-w3c-data-integrity-credential-attachment/), [proposed changes in PR 828](https://github.com/hyperledger/aries-rfcs/pull/828)
  
  - Briefly discussed, but the PR submitter was not there and so didn't make progress. Perhaps next week.
- Adding the ["stalled" RFC Status](https://github.com/hyperledger/aries-rfcs/pull/827) and reclassifying PRs – see [Spreadsheet](https://docs.google.com/spreadsheets/d/1Dnp6qg4RZkdvC7G7izoPmHeWRk9S0mB7qKiwjWkaOJQ/edit?usp=sharing) summarizing the proposed changes.
  
  - Goal is to make the [published Aries RFCs](https://hyperledger.github.io/aries-rfcs/latest/) easier to use.
  - Published Aries RFCs [To Do list](https://github.com/hyperledger/aries-rfcs/issues/825) – Help welcome!
  - Progress:
    
    - Went through the spreadsheet, touching on each RFC with a proposed change of status, the purpose and reason for the change.
    - Identified a set (marked "Review") that are to be looked at before changing the status
    - Agreed that the next steps are:
      
      - Remove the ones to be reviewed from a change.  A new PR will be added that proposes any changes to the status of those RFCs, if needed.
      - Add the additional status changes proposed by [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) to the PR.
      - Merge the PR at that point.
  - We also looked again at the [published Aries RFC site](https://hyperledger.github.io/aries-rfcs/latest/) and the [to do list of things](https://github.com/hyperledger/aries-rfcs/issues/825) to make the site better.
- Update: Adding DIDComm v2 Support to ACA-Py – First Impressions
  
  - Link – ACA-Py branch with DIDComm v2 changes: [https://github.com/hyperledger/aries-cloudagent-python/compare/main...Indicio-tech:aries-cloudagent-python:feat/didcommv2-proof-of-concept](https://github.com/hyperledger/aries-cloudagent-python/compare/main...Indicio-tech:aries-cloudagent-python:feat/didcommv2-proof-of-concept)
  - Link - New DIDComm Utilities Library: [https://github.com/Indicio-tech/didcomm-messaging-python](https://github.com/Indicio-tech/didcomm-messaging-python)
  - Initial Progress - added code to ACA-Py to receive and unpack a DIDComm V2 message.
  - Best approach to the overall implementation still being fleshed out.
- Trust DID Web – did:tdw – brief overview based on this [presentation](https://docs.google.com/presentation/d/1PHo16asyceRiNKN7UkV8BSmtWtN6Wp3A6_9MV0IQ2jg/edit?usp=sharing) used at IIW
  
  - An enhancement to did:web that provides a web-based DID Method with a verifiable history, authorized updates and portability (and more!) to a DID Method that has an implementation that is less than 1000 LOC in Typescript.

## Other Business

## Future Topics

## Action items

## Call Recording:

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
