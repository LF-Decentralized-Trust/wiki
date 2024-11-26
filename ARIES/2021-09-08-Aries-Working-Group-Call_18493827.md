1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2021 Aries Working Group Meetings](2021-Aries-Working-Group-Meetings_18514540.html)

# Hyperledger Aries : 2021-09-08-Aries Working Group Call

Created by Robert Mitwicki, last modified on Sep 12, 2021

## Summary:

- Work updates
- Questions Review of the DID core spec on W3C
  
  - Comment from Mozilla [https://lists.w3.org/Archives/Public/public-new-work/2021Sep/0000.html](https://lists.w3.org/Archives/Public/public-new-work/2021Sep/0000.html)
  - Apple (object with changes): [https://lists.w3.org/Archives/Member/w3c-archive/2021Aug/0663.html](https://lists.w3.org/Archives/Member/w3c-archive/2021Aug/0663.html)
    
    Mozilla (principled objection): [https://lists.w3.org/Archives/Public/public-new-work/2021Sep/0000.html](https://lists.w3.org/Archives/Public/public-new-work/2021Sep/0000.html)
    
    Google (object with changes): [https://lists.w3.org/Archives/Member/w3c-archive/2021Aug/0588.html](https://lists.w3.org/Archives/Member/w3c-archive/2021Aug/0588.html)
    
    MS (supportive with suggested improvements for future): [https://lists.w3.org/Archives/Member/w3c-ac-forum/2021JulSep/0076.html](https://lists.w3.org/Archives/Member/w3c-ac-forum/2021JulSep/0076.html)
    
    Amazon (no plans to support but no objections): [https://lists.w3.org/Archives/Member/w3c-archive/2021Aug/0069.html](https://lists.w3.org/Archives/Member/w3c-archive/2021Aug/0069.html)
  - [https://w3c.github.io/did-rubric/](https://w3c.github.io/did-rubric/)
- Unpacking KERI
- Open Discussion (as time permits)

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

08 Sep 2021 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (Organization) &lt;email&gt;
- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence) &lt;robert.mitwicki@humancolossus.org&gt;
- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) &lt;sam@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) &lt;smccown@anonyome.com&gt;
- @Keith Smith &lt;bksmith@us.ibm.com&gt;

## Welcome / Introductions

## Announcements

- [IIW](https://internetidentityworkshop.com/) (online) Oct 12-14
- [https://github.com/kiva/indy-diem](https://github.com/kiva/indy-diem)
- did indy work starting - did indy channel on hyperledger chat, indy did method repo
- Aries SDK for React Native

## Related Calls

- Previous Aries Working Group B calls
- ACDC - see [ACDC (Authentic Chained Data Container) Task Force](https://wiki.trustoverip.org/display/HOME/ACDC+%28Authentic+Chained+Data+Container%29+Task+Force) at ToIP for more info.
- [Input and Semantic WG at ToIP](https://wiki.trustoverip.org/display/HOME/Inputs+and+Semantics+Working+Group)
- DIF DIDComm WG Call: [Rolling Agenda](https://docs.google.com/document/d/1BpTm5SmgfOJcEsXfizO0ZmH1r7imTJDGKudAZtYsm0M/edit).
- Indy contributors call
  
  - SSI and internet of things
- Indy DID Specification - Spec. is complete and the finalization in process - [HackMD Document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw) is the latest version – moving to SpecUp in GitHub Real Soon Now
- [2021-09-9 : Identity Implementers WG Call](https://lf-hyperledger.atlassian.net/wiki/spaces/IWG/pages/18252055/2021-09-9+Identity+Implementers+WG+Call): Jim StClair ([Lumedic.io](http://lumedic.io/)) will present an overview of how SSI technologies are progressing through ISO/TC 307 to become a part of ISO standards.

## Release Status and Work Updates

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

## RFC Progress

## Other Business

## Future Topics

- Next Meeting
- Other:
  
  - Where should we document interoperability results (AIP 1.0)? A page in this wiki space?
  - Hubs vs Agents
    
    - [https://www.hyperledger.org/blog/2019/07/23/rhythm-and-melody-how-hubs-and-agents-rock-together](https://www.hyperledger.org/blog/2019/07/23/rhythm-and-melody-how-hubs-and-agents-rock-together)
  - Status and future of wallet query language
  - DID Resolution W3C and Sam's concerns: [https://github.com/hyperledger/aries-rfcs/issues/130](https://github.com/hyperledger/aries-rfcs/issues/130)
  - Connectionless
  - KERI - deep dive / transaction family / Notary groups /

## Action items

## Call Recording

  File Modified

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18493827/18515512.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18493827/18515511.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
