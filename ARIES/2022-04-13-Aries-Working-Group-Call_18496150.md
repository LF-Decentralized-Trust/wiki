1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-04-13 Aries Working Group Call

Created by Sam Curren, last modified by Stephen Curran on Apr 13, 2022

## Summary:

- Aries CLI

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

13 Apr 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

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
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;
- Bruno Hivert &lt;bruno.hivert@idlab.org&gt;
- [Sean Bohan](https://lf-hyperledger.atlassian.net/wiki/people/634eef0301c2ff842c15f9e7?ref=confluence)  (Hyperledger) &lt;sbohan@linuxfoundation.org&gt;

## Welcome / Introductions

## Announcements

- IIW
- Cardea Demo Day April 14th 10am US/Mountain Daylight Time - Zoom Link: [https://us02web.zoom.us/j/88535183851?pwd=QTFsT3Fjc0xpT3FRek9aRkhKcHdrdz09](https://www.google.com/url?q=https%3A%2F%2Fus02web.zoom.us%2Fj%2F88535183851%3Fpwd%3DQTFsT3Fjc0xpT3FRek9aRkhKcHdrdz09&sa=D&source=calendar&ust=1649637689183751&usg=AOvVaw0C_jDLr9qmnXAQnIVL5u2r)

Release Status and Work Updates

- Aries Protocol Test Suite
- Aries Agent Test Harness
- Aries Shared:
- Aries-CloudAgent-Python
  
  - 0.7.4-rc0 released, and the final contents for 0.7.4 being discussed.
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

Aries CLI - Animo

- [https://github.com/animo/aries-cli](https://github.com/animo/aries-cli)
- [https://aries-cli.animo.id](https://aries-cli.animo.id)

Device Binding RFC

- [https://github.com/hyperledger/aries-rfcs/pull/729](https://github.com/hyperledger/aries-rfcs/pull/729)

Coordinated Update - OOB Invitations - [https://github.com/hyperledger/aries-rfcs/tree/main/features/0496-transition-to-oob-and-did-exchange](https://github.com/hyperledger/aries-rfcs/tree/main/features/0496-transition-to-oob-and-did-exchange)

- [https://discord.com/channels/905194001349627914/905206466410057728/960899454536417311](https://discord.com/channels/905194001349627914/905206466410057728/960899454536417311)

Issue #728

- [https://github.com/hyperledger/aries-rfcs/issues/728](https://github.com/hyperledger/aries-rfcs/issues/728)

Updating from unqualified DIDs to fully formed DIDs - Timo (next week)

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

Text File [chat.txt](attachments/18496150/18516156.txt "Download")

Apr 13, 2022 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18496150/18516156.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496150/18516157.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496150/18516158.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
