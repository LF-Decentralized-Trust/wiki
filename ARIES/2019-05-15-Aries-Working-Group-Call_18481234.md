1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2019 Aries Working Group Meetings](2019-Aries-Working-Group-Meetings_18511496.html)

# Hyperledger Aries : 2019-05-15 Aries Working Group Call

Created by Sam Curren, last modified by Nathan George on Jul 15, 2020

## Summary:

Credential Based Access Use Case

Aries RFC Process

## Date

15 May 2019

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

NameOrganizationEmail[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)Cloud Compass/BC Govswcurran@cloudcompass.caSam CurrenSovrin Foundationsam@sovrin.orgTroy RondaSecureKeytroy.ronda@securekey.comTobias LookerMattrtobias.looker@mattr.globalPaul KnowlesDativapaul.knowles@dativa.comDuane JohnsonMedici Land Governancedujohnson@mediciland.comKen EbertSovrin Foundationken@sovrin.orgKyle Den HartogMattrindy@kyledenhartog.com[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)Sovrin Foundation[daniel.bluhm@sovrin.org](mailto:daniel.bluhm@sovrin.org)

[Oskar van Deventer](https://lf-hyperledger.atlassian.net/wiki/people/5ea015018e58680c1ff449d6?ref=confluence)

TNO[oskar.vandeventer@tno.nl](mailto:oskar.vandeventer@tno.nl)

 Alexander Blom

Bloqzone [alexander.blom@bloqzone.com](mailto:alexander.blom@bloqzone.com) Helen GarneauSovrin Foundation

[helen@sovrin.org](mailto:helen@sovrin.org)

[Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)

Sovrin Foundation[adam@sovrin.org](mailto:adam@sovrin.org)Albert SolanaValidated Id[albert.solana@validatedid.com](mailto:albert.solana@validatedid.com)Tomislav MarkovskiStreetcredtmarkovski@gmail.comGary de BeerSAFBCdibbs.za@gmail.comCody MaceAnonyome Labscmace@anonyome.com

[Nader Helmy](https://lf-hyperledger.atlassian.net/wiki/people/5a8b44640e6608334b4676eb?ref=confluence)

Danube Technader.helmy@danubetech.comAudrius Ramoska123c Consultingaudrius@123c.euAlexi FalquierSpaceman IDalexis@spaceman.idMarkus SabadelloDanube Techmarkus@danubetech.comDaniel HardmanEvernymdaniel.hardman@evernym.comGeorge AristySecureKey Technologiesgeorge.aristy@securekey.comRobert MitwickiLab10 Collectiverobert@lab10.coopNathan GeorgeKivanathang@kiva.org

## Announcements

- Aries announced at Consensus in NY

## Agenda

ItemWhoNotesCredential Access Use CaseStephen Curran

Aries RFC Process

Selection of DID Comms Related RFCs for Ratification

Sam Curren

[https://github.com/hyperledger/aries-rfcs/pull/2](https://github.com/hyperledger/aries-rfcs/pull/2)

bring over did comms related HIPEs (v1, under the knowledge that the conversation is continuing)

--- stuff we didn't get to below ---

Credential Exchange Protocol UpdateStephen Curran  
DIDCom over XMPP - new draft HIPE

Oskar van Deventer (TNO)

Alexander Blom (Bloqzone)

[https://github.com/Oskar-van-Deventer/indy-hipe/tree/didcom-over-xmpp/text/didcom-over-xmpp](https://github.com/Oskar-van-Deventer/indy-hipe/tree/didcom-over-xmpp/text/didcom-over-xmpp)

Purpose: have DIDCom messages traverse firewalls.

Discussion

-Use DID in userpart of XMPP address for better privacy?

-Fast XMPP service endpoint rotation for even more privacy?

 Peer DID discussion - updateOskar, Daniel, Kyle

 Current status:

• Understanding Peer DID (Oskar): [https://docs.google.com/document/d/1SgKvuG7u0r5UkaDRnnkQmnarVylCx5VF5y0eIyV-I6Y](https://docs.google.com/document/d/1SgKvuG7u0r5UkaDRnnkQmnarVylCx5VF5y0eIyV-I6Y)  
• Pairwise to N-Wise (Daniel): [https://docs.google.com/document/d/1BjYdivGQ9GxIz9CJ2ymNvMA68uHZm8bFOTyCHDmziOU](https://docs.google.com/document/d/1BjYdivGQ9GxIz9CJ2ymNvMA68uHZm8bFOTyCHDmziOU)  
• Use cases for n-wise (Daniel): [https://docs.google.com/document/d/17wn4zah37ATGXClWfbvTu07v\_YmkDgQfGEWhBiROZBo](https://docs.google.com/document/d/17wn4zah37ATGXClWfbvTu07v_YmkDgQfGEWhBiROZBo)  
• Peer-DID based microledger (Oskar): [https://docs.google.com/presentation/d/1VwVWGMjbTR51HPFx1\_k4Pe1hHBDnpPa-qGuzJN5UFUw](https://docs.google.com/presentation/d/1VwVWGMjbTR51HPFx1_k4Pe1hHBDnpPa-qGuzJN5UFUw)

Result will be likely set of PRs to [Peer DID](https://github.com/openssi/peer-did-method-spec), and possibly other HIPEs

Open Discussion

## Next Week

Review of DID Comms Related RFCs

## Future Topics

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20190515-190242\_Indy-Agent.txt](attachments/18481234/18511535.txt "Download")

May 16, 2019 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Participant log

![](attachments/18481234/18511516.jpg)

## Attachments:

![](images/icons/bullet_blue.gif) [Participants.jpg](attachments/18481234/18511516.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [GMT20190515-190242\_Indy-Agent.txt](attachments/18481234/18511535.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481234/18511536.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481234/18511534.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
