1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-04-19 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Apr 20, 2022

## Summary:

Planned Topics:

- Proposal/Discussion: Adding support for DIDComm V2/WACI to ACA-Py – led by [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence)
  
  - Homework – Please review this [proposal](https://docs.google.com/document/d/1piGZ-0FW9DWEFRetviV1Vjxv7DDkIFQDWUs38VGqZ-Y/edit?usp=sharing) and think about the issues raised
- Getting to release 0.7.4

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Chat
  
  - 08:08:48 From Peter Altmann - DIGG : I hope I can introduce myself here. I am Peter Altmann from the Swedish Agency for Digital Government. I work in the EU commission on the technical specifications for the proposed EU Digital Identity Wallet. I also work with some public sector actors in Sweden where I have used ACA-Py to develop some proof of concepts. Nice to be here!
  - 08:17:25 From Victor Martinez : DIDCOMMv2 provides a negotiation compatibility [https://identity.foundation/didcomm-messaging/spec/#negotiating-compatibility](https://identity.foundation/didcomm-messaging/spec/#negotiating-compatibility)
  - 08:19:17 From Artur Philipp : But does this offer the Option to negotiate the envolope (V1 vs V2)? A Client which only supports V1, is then probably not able to negotiate, Right?
  - 08:19:55 From Andrew Whitehead : A client that only supports V1 probably can't decode a V2 envelope at all
  - 08:22:09 From Victor Martinez : Maybe something to take into account, SICPA has started a project to introduce DIDCOMM v2 in Aries JS.
  - 08:22:40 From Victor Martinez : Some comments regarding SICPA implementation :
  - 08:22:52 From Victor Martinez : If underlying primitives computing performance is a concern:
    
    Dependency tree:
    
    Didcomm -&gt; Authlib -&gt; cryptography
    
    Cryptography relies on foreign function interfaces (FFI):
    
    for OpenSSL: [https://github.com/pyca/cryptography/tree/main/src/\_cffi\_src/openssl](https://github.com/pyca/cryptography/tree/main/src/_cffi_src/openssl)
    
    For rust code (x509 implementation): [https://github.com/pyca/cryptography/tree/main/src/rust/src](https://github.com/pyca/cryptography/tree/main/src/rust/src)
    
    Conclusion: low-level, performance-critical code is implemented in C or Rust.
  - 08:27:11 From Andrew Whitehead : Askar also contains Rust implementations of the primitives
  - 08:29:43 From Peter Strobel : Oh that's interesting, I wasn't aware a v2 connection could be established without an Out Of Band invitation!
  - 08:38:54 From Daniel Bluhm : I'll see if I can follow up with Sam on why the V3 was required and report back on the acapy channel on Discord
  - 08:44:37 From Stephen Curran : Peter Strobel — that can be done in DIDComm V1 as well. “Implicit invitations” are when a party has a DIDComm service entry in their public DID. Another party can use that without an OOB.
  - 08:46:03 From Andrew Whitehead : Not sure if it does make sense to automatically upgrade a V1 connection to V2 without rotating the DID, because the cryptography used is different
  - 08:47:26 From Andrew Whitehead : Downgrading V2 to V1 is a worse proposition

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - Aries Cloud Agent Python
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - Aries-VCR/OrgBook BC Deployment
  - Issuer Kit - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BPA - Business Partner Agent for B2B use of VCs
  - BC Wallet – based on Aries Framework JavaScript and Aries Bifold

## Agenda

- Proposal/Discussion: Adding support for DIDComm V2/WACI to ACA-Py – led by [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence)
  
  - Homework – Please review this [proposal](https://docs.google.com/document/d/1piGZ-0FW9DWEFRetviV1Vjxv7DDkIFQDWUs38VGqZ-Y/edit?usp=sharing) and think about the issues raised
- Getting to release 0.7.4 – what is needed after RC0
  
  - [PRs since Release 0.7.4-RC0](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-04-07) - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496176/18516185.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
