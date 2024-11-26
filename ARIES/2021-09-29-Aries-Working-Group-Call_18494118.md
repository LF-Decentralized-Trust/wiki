1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2021 Aries Working Group Meetings](2021-Aries-Working-Group-Meetings_18514540.html)

# Hyperledger Aries : 2021-09-29 Aries Working Group Call

Created by Sam Curren on Sep 28, 2021

## Summary:

- Work updates
- Automated Data Agreement - Jan
- Once again review [https://github.com/hyperledger/aries-rfcs/pull/697](https://github.com/hyperledger/aries-rfcs/pull/697) in the context how this can be should be done.
- UX of Invitations
- Open Discussion (as time permits)

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

29 Sep 2021 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

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

## Welcome / Introductions

## Announcements

- [IIW](https://internetidentityworkshop.com/) (online) Oct 12-14
- did indy work starting - did-indy-method channel on Hyperledger chat, [indy did method](https://github.com/hyperledger/indy-did-method) repo, [published spec](https://hyperledger.github.io/indy-did-method/)
- Aries SDK for React Native 
  
  - [https://gitlab.grnet.gr/essif-lab/infrastructure\_3/animo-solutions](https://gitlab.grnet.gr/essif-lab/infrastructure_3/animo-solutions)
- Findy Agent – open source code: [https://findy-network.github.io/](https://findy-network.github.io/)
  
  - Lots of interesting things to be found there. Checkout the travelogue blog piece.
  - Test set and test harness added to Aries agent
- Swiss- Discussion paper on the target vision for an e-ID: 
  
  - [https://www.bj.admin.ch/dam/bj/en/data/staat/gesetzgebung/staatliche-e-id/diskussionspapier-zielbild-e-id.pdf.download.pdf/diskussionspapier-zielbild-e-id.pdf](https://www.bj.admin.ch/dam/bj/en/data/staat/gesetzgebung/staatliche-e-id/diskussionspapier-zielbild-e-id.pdf.download.pdf/diskussionspapier-zielbild-e-id.pdf)
- GlobaliD - 'Code with me' proposal for native mobile aries frameworks. Information and reward details [here](https://docs.google.com/document/d/1v9_DhHvT5ahMEwV0eHxkVck5knN7cCde6MKlKuNxgt4/edit#heading=h.bl43zjnuoqpk)
  

Release Status and Work Updates

- Aries Protocol Test Suite
- Aries Agent Test Harness
  
  - Expanding the VC format tests
- Aries Shared:
  
  - Aries Shared: Fully functional branch in ACA-Py that uses the shared libraries, not indy-sdk
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    - indy-shared-rs - [https://github.com/hyperledger/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
    - aries-askar (storage): [https://github.com/hyperledger/aries-askar](https://github.com/andrewwhitehead/aries-askar)
- Aries-CloudAgent-Python
  
  - AIP 2.0 work going on
    
    - DIF Presentation Exchange to be merged this week
- Aries-Framework-Go (Troy) #aries-go
  
  - [2020-11-03 Meeting Notes](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2020-11-03+Framework+Go+Weekly+Planning)
  - BBS+ Verifiable Credentials implemented using pure Go. [Example](https://github.com/hyperledger/aries-framework-go/blob/ac94a47/pkg/doc/verifiable/credential_ldp_test.go#L450).
    
    - Next tasks: interop testing against Mattr implementation and selective disclosure capabilities.
  - Working on adding remote encrypted storage capability - with a default implementation of DIF Secure Data Storage - Encrypted Data Vaults.
    
    - Encrypted Data Vault (EDV) from DIF SDS spec format has been implemented. Works as an encryption wrapper to underlying storage providers.
    - DIF EDV/SDS REST client is in progress. Docker image will support configuring EDV endpoint as wallet storage.
  - Remote KMS support is in progress. Docker image will support configuring remote KMS.
  - Created repo to handle pluggable go framework components such as Indy VDR: [https://github.com/hyperledger/aries-framework-go-ext](https://github.com/hyperledger/aries-framework-go-ext)
    
    - MySQL and CouchDB components moved to ext repo.
    - New contributions of MongoDB and RabbitMQ support to the ext repo.
- Aries Mobile Agent React Native
- Aries-SDK-Ruby (Jack)
- Aries-Framework-DotNet (Tomislav)
- Aries-Toolbox
  
  - Connections Update Complete
  - ACA-Py Toolbox Plugin updated to support ACA-Py 5.3
  - Dependency Updates
  - Converted to a web application by HCF - repo [https://github.com/thclab/aries](https://github.com/thclab/aries)
- Aries-SDK-Java
- Aries-Framework-JavaScript
  
  - New [aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext) repository for extensions
    
    - New package @aries-framework/rest as a rest wrapper around AFJ
  - Work going on for automatic multi indy ledger support
- Rich Schemas and W3C Verifiable Credentials (Brent &amp; Ken)
- Aries-MobileAgent-Xamarin (Aries MAX)
- Pending contributions from GlobalID:
  
  - indy-sdk PR for IOS
  - indy-sdk-android
  - Aries Framework IOS (Swift)
  - Aries Framework Android (Kotlin)
- Ursa

## Notes:

IHAN Blueprint: [https://media.sitra.fi/2018/12/22091907/ihan-blueprint-2-5.pdf](https://media.sitra.fi/2018/12/22091907/ihan-blueprint-2-5.pdf) Services Section 3.5

Reference about fat protocol: [https://www.usv.com/writing/2016/08/fat-protocols/](https://www.usv.com/writing/2016/08/fat-protocols/)

ACDC vs World: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/spreadsheets/d/1Bh1nt8DWfIVgOj1-Oubx1BjINt_t0rgBJae1IfwyQQg/edit#gid=0)

Data Agreement:

- [https://kantarainitiative.org/download/7902/](https://kantarainitiative.org/download/7902/)
- [https://github.com/decentralised-dataexchange/automated-data-agreements/tree/main/docs](https://github.com/decentralised-dataexchange/automated-data-agreements/tree/main/docs)
- [https://www.iso.org/standard/80392.html](https://www.iso.org/standard/80392.html)
- Demo: [https://igrant.io/data4travel.html](https://igrant.io/data4travel.html)

## Discussion Topics

- UX of Invitations
  
  - [https://hackmd.io/QuB3EUxtTMOQEmzhqufC6g](https://hackmd.io/QuB3EUxtTMOQEmzhqufC6g)
  - Data in Invitations
- Deep Linking
  
  - [https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0268-unified-didcomm-agent-deeplinking/README.md](https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0268-unified-didcomm-agent-deeplinking/README.md)
- Forget Me RFC
  
  - [https://github.com/hyperledger/aries-rfcs/pull/697](https://github.com/hyperledger/aries-rfcs/pull/697)
- Open Discussion

## Other Business

## Future Topics

- Next Meeting
- Daniel Hardman - n-wise protocols (not next week, perhaps 2 weeks)
- ux - wallet interactions with machine readable governance files, what UI do we want, and how do we support that? (stephen curran, pending topic)
- Other:
  
  - Where should we document interoperability results (AIP 1.0)? A page in this wiki space?
  - Hubs vs Agents
    
    - [https://www.hyperledger.org/blog/2019/07/23/rhythm-and-melody-how-hubs-and-agents-rock-together](https://www.hyperledger.org/blog/2019/07/23/rhythm-and-melody-how-hubs-and-agents-rock-together)
  - Status and future of wallet query language
  - DID Resolution W3C and Sam's concerns: [https://github.com/hyperledger/aries-rfcs/issues/130](https://github.com/hyperledger/aries-rfcs/issues/130)
  - Connectionless
  - KERI - deep dive / transaction family / Notary groups /

## Action items

- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)  Bring on the next call information about how ACDC address problems of JSON-LD serialization of RDF

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18494118/18515567.txt "Download")

Sep 29, 2021 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18494118/18515567.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494118/18515568.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494118/18515566.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
