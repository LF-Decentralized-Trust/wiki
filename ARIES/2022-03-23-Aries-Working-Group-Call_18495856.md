1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-03-23 Aries Working Group Call

Created by Sam Curren, last modified by Philippe Foucault on Apr 13, 2022

## Summary:

- DID Exchange Signatures
- DID Auth Pre-Credential

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

23 Mar 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence)(IDLab) &lt;regis.eloi@idlab.org&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@mcn.gouv.qc.ca&gt;

## Welcome / Introductions

## Announcements

- IIW
- [2022-03-24 : Identity Implementers WG Call](https://lf-hyperledger.atlassian.net/wiki/spaces/IWG/pages/18252073/2022-03-24+Identity+Implementers+WG+Call) (9am MDT / 3pm UTC):  Keela Shatzkin (Shatzkin Systems, Inc.) on Cardea and the March 17th Cardea Interop-a-thon
- Hyperledger Summer of Docs (Google Funded) - adding documentation to open source projects - Deadline March 25th (Friday)
  
  - [https://docs.google.com/forms/d/e/1FAIpQLSehVjMLUjnoPgS8kX4ErpE76N-KWc3AgrCyCxe7bRrtDm6tew/viewform?resourcekey=0-GIaZX6zeX6zvB58FARfOHQ](https://docs.google.com/forms/d/e/1FAIpQLSehVjMLUjnoPgS8kX4ErpE76N-KWc3AgrCyCxe7bRrtDm6tew/viewform?resourcekey=0-GIaZX6zeX6zvB58FARfOHQ)

Release Status and Work Updates

- Aries Protocol Test Suite
- Aries Agent Test Harness
- Aries Shared:
- Aries-CloudAgent-Python
  
  - Starting on an 0.7.4 Release
  - Looking into the high priority issues/PRs
- Aries-Framework-Go (Troy) #aries-go
  
  - Working on support for DIDComm v2, Credential Manifest, OOB v2 and v3 credential protocols (for DIDComm v2)
  - [RFC 700](https://github.com/hyperledger/aries-rfcs/pull/700) to enable web wallets
- NEW [aries-service-mediator](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries Mobile Agent React Native
- Aries-CloudAgent-Pico
- Aries-SDK-Ruby (Jack)
- Aries-Framework-DotNet (Tomislav)
- Aries-Toolbox
- Aries-SDK-Java
- Aries-Framework-JavaScript
  
  - Working on 0.2.0 release
    
    - Issue Credential / Present Proof v2
    - OOB / DIDExchange
    - Holder revocation with revocation notifications support
  - Started working on JSON-LD and BBS+ credential support
  - Started working on writing a wrapper for Indy VDR for React Native
- Rich Schemas and W3C Verifiable Credentials (Brent &amp; Ken)
- Aries-MobileAgent-Xamarin (Aries MAX)
- Ursa

## Notes:

## Discussion Topics

DID Exchange Signatures

- [PR 725](https://github.com/hyperledger/aries-rfcs/pull/725) - Remove Request Signatures
- [Issue 717](https://github.com/hyperledger/aries-rfcs/issues/717) - inline peer did without signatures
- Needs details about signatures in Response
  
  - Connection Protocol [Response Section](https://github.com/hyperledger/aries-rfcs/blob/main/features/0160-connection-protocol/README.md#2-connection-response) (for reference)
  - DID Exchange Protocol [Response Section](https://github.com/hyperledger/aries-rfcs/tree/main/features/0023-did-exchange#2-exchange-response) (for reference)
  - Needs details about which key (kid in jws) to use, and how to verify
  - Problem: This verifies a DID Doc, but not necessarily the DID
    
    - This is complicated with Peer DID Method 2 usage, where there is no separate attached DID Doc in the Response
  - How to handle a non-ed25519 key passed as key agreement key in the oob invitation?

DID Auth Pre-Credential - Timo 

- [https://hackmd.io/2gbdFFO3QAC83nRDhqcEBQ](https://hackmd.io/2gbdFFO3QAC83nRDhqcEBQ)
- To prove DID ownership when issuing a jsonld credential.

## Other Business

## Future Topics

- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18495856/18516067.txt "Download")

Mar 23, 2022 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18495856/18516067.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18495856/18516068.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18495856/18516066.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
