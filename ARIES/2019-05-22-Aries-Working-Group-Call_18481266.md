1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2019 Aries Working Group Meetings](2019-Aries-Working-Group-Meetings_18511496.html)

# Hyperledger Aries : 2019-05-22 Aries Working Group Call

Created by Sam Curren, last modified on May 23, 2019

## Summary:

Aries RFC Status

Credential Exchange Update and Discussion, including flow variations for 'advanced' cases (payment, zkps, etc.) and 'simple' cases (ask for credential, get credential).

Return-Routing / Endpointless Agents Discussion

## Date

22 May 2019

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

NameOrganizationEmailStephen CurranCloud Compass/BC Govswcurran@cloudcompass.caAlexander BlomBloqzonealexander.blom@bloqzone.com

[Oskar van Deventer](https://lf-hyperledger.atlassian.net/wiki/people/5ea015018e58680c1ff449d6?ref=confluence)

TNO - Techruptionoskar.vandeventer@tno.nl

[George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)

SecureKey Technologiesgeorge.aristy@securekey.comTroy RondaSecureKey Technologiestroy.ronda@securekey.comAlbert SolanaValidated Idalbert.solana@validatedid.comTobias LookerMattrtobias.looker@mattr.globaljonnycrunch  
jonnycrunch@me.comSam CurrenSovrin Foundationsam@sovrin.orgPaul KnowlesDativapaul.knowles@dativa.comSteve McCownAnonyome Labssmccown@anonyome.comVipin Bharathandlt.nycvip@dlt.nycMichael LodderSovrin Foundationmike@sovrin.orgOliver TerbuuPort / ConsenSysoliver.terbu@consensys.netSpencer HolmanEvernymspencer.holman@evernym.comBobbi MuscaraLedger AcademyBobbi@LedgerAcademy.comAudrius Ramoska123c Consultingaudrius@123c.euKyle Den HartogMattrindy@kyledenhartog.comAlexi FalquierSpaceman IDalexis@spaceman.idNader HelmyDanube Technader.helmy@danubetech.com

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)

Sovrin Foundationdaniel.bluhm@sovrin.org

## Announcements

## Agenda

ItemWhoNotesAries RFC UpdateSam Curren[https://github.com/hyperledger/aries-rfcs/blob/master/index.md](https://github.com/hyperledger/aries-rfcs/blob/master/index.md)Credential Exchange Protocol UpdateStephen Curran[https://docs.google.com/presentation/d/14CuMJcWx-Lx6lsQsRRGy5rARgdoTUKiUV-tcfTFn1bw](https://docs.google.com/presentation/d/14CuMJcWx-Lx6lsQsRRGy5rARgdoTUKiUV-tcfTFn1bw/edit?usp=sharing)Agents without EndpointsSam Curren[https://hackmd.io/p/r1bQfCMTE#/](https://hackmd.io/p/r1bQfCMTE#/)-- meeting ended here --

DIDCom over XMPP - new draft HIPE

Oskar van Deventer (TNO)

Alexander Blom (Bloqzone)

[https://github.com/Oskar-van-Deventer/indy-hipe/tree/didcom-over-xmpp/text/didcom-over-xmpp](https://github.com/Oskar-van-Deventer/indy-hipe/tree/didcom-over-xmpp/text/didcom-over-xmpp)

Purpose: have DIDCom messages traverse firewalls.

Discussion

-Use DID in of XMPP address for better privacy?

-Fast XMPP service endpoint rotation for even more privacy?

Peer DID UpdatesOskar, Daniel, Kyle

Current status:

• Understanding Peer DID (Oskar): [https://docs.google.com/document/d/1SgKvuG7u0r5UkaDRnnkQmnarVylCx5VF5y0eIyV-I6Y](https://docs.google.com/document/d/1SgKvuG7u0r5UkaDRnnkQmnarVylCx5VF5y0eIyV-I6Y)  
• Pairwise to N-Wise (Daniel): [https://docs.google.com/document/d/1BjYdivGQ9GxIz9CJ2ymNvMA68uHZm8bFOTyCHDmziOU](https://docs.google.com/document/d/1BjYdivGQ9GxIz9CJ2ymNvMA68uHZm8bFOTyCHDmziOU)   
• Use cases for n-wise (Daniel): [https://docs.google.com/document/d/17wn4zah37ATGXClWfbvTu07v\_YmkDgQfGEWhBiROZBo](https://docs.google.com/document/d/17wn4zah37ATGXClWfbvTu07v_YmkDgQfGEWhBiROZBo)  
• Peer-DID based microledger (Oskar): [https://docs.google.com/presentation/d/1VwVWGMjbTR51HPFx1\_k4Pe1hHBDnpPa-qGuzJN5UFUw](https://docs.google.com/presentation/d/1VwVWGMjbTR51HPFx1_k4Pe1hHBDnpPa-qGuzJN5UFUw)

Result will be likely set of PRs to [Peer DID](https://github.com/openssi/peer-did-method-spec), and possibly other HIPEs

Open Discussion

## Next Week

## Future Topics

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20190522-190638\_Aries-WG-C.txt](attachments/18481266/18511560.txt "Download")

May 23, 2019 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Participants

![](attachments/18481266/18511546.png?height=250)

## Attachments:

![](images/icons/bullet_blue.gif) [image2019-5-22\_21-6-12.png](attachments/18481266/18511546.png) (image/png)  
![](images/icons/bullet_blue.gif) [GMT20190522-190638\_Aries-WG-C.txt](attachments/18481266/18511560.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481266/18511558.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481266/18511559.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
