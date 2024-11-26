1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2019 Aries Working Group Meetings](2019-Aries-Working-Group-Meetings_18511496.html)

# Hyperledger Aries : 2019-06-12 Aries Working Group Call

Created by Sam Curren, last modified on Jun 13, 2019

## Summary:

Kantara Privacy Control Panel, uPort Message Flow Demonstration, Indy Catalyst Agent as Aries Agent Codebase

## Note: This call is Recorded. Recordings posted at the bottom of the page.

## Date

12 Jun 2019

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

[Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Attendees

NameOrganizationEmail[Tobias Looker](https://lf-hyperledger.atlassian.net/wiki/people/712020:6b4b9e75-c537-4af4-b498-bd8e8b96dc37?ref=confluence)Mattrtobias.looker@mattr.global

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

Cloud Compass Computing/BC Govswcurran@cloudcompass.ca[George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)SecureKey Technologiesgeorge.aristy@securekey.com

[Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence)

Evernymdaniel.hardman@evernym.com

[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Mattrkyle.denhartog@mattr.global

[Oliver Terbu](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b0b89c4-350c-41f9-9260-1ef40f38fec7?ref=confluence)

uPort / ConsenSysoliver.terbu@consensys.net

[Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)

Sovrin Foundationadam@sovrin.orgAndrew HughesITIM Consulting[andrewhughes3000@gmail.com](mailto:andrewhughes3000@gmail.com)

[Albert Solana Berengué](https://lf-hyperledger.atlassian.net/wiki/people/70121:0b2fa4b3-a9eb-4eb8-b319-d96c4647750d?ref=confluence)

Validated Idalbert.solana@validatedid.com

[Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence)

Evernymbrent.zundel@evernym.com

[Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)

Sovrin Foundationsam@sovrin.orgMike RichardsonStarlingsGlobalemerysolutions@yahoo.co.uk

[Lohan Spies](https://lf-hyperledger.atlassian.net/wiki/people/557058:955e8187-8218-4b8d-a771-c2c1bf9b4c9e?ref=confluence)

DIDxlohan.spies@didx.xyz[Drummond Reed](https://lf-hyperledger.atlassian.net/wiki/people/70121:f3a4c542-f887-49b3-aac9-7374b4da8e1d?ref=confluence)Evernym &amp; Sovrin Foundation[drummond.reed@evernym.com](mailto:drummond.reed@evernym.com)Ken EbertSovrin Foundationken@sovrin.org

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence)

Anonyome Labssmccown@anonyome.comNader HelmyDanube Technader.helmy@danubetech.comMoushmi BanerjeeNutanix[moushmi.banerjee@nutanix.com](mailto:moushmi.banerjee@nutanix.com) @rchristmanAnonyome Labsrchristman@anonyome.comLine Kofoedbloqzoneline.kofoed@bloqzone.com

[Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)

Lab10 Collectiverobert@lab10.coop

## Announcements

- BC Gov is interested in collaborating with groups working on Mobile Agents that could be ready for a live implementation at the end of the summer. Contact [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence).
- Community project: Aries RFCs - [process to move HIPES](https://docs.google.com/document/d/1BKLR6lmjuwmHrYldNELijddJYi43IJByBXSMQgIHSYM/edit?usp=sharing); RFCs that have been moved [concepts](https://github.com/hyperledger/aries-rfcs/tree/master/concepts) / [features](https://github.com/hyperledger/aries-rfcs/tree/master/features) / [pull requests](https://github.com/hyperledger/aries-rfcs/pulls).
- Aries-sdk-* Repos Created: [https://github.com/hyperledger?utf8=%E2%9C%93&amp;q=aries-sdk&amp;type=&amp;language=](https://github.com/hyperledger?utf8=%E2%9C%93&q=aries-sdk&type=&language=)
- #aries-sdk on chat.hyperledger.org
- Javascript Agent Framework kickoff discussion - June 18th 9AM MDT (3PM UTC)

## Agenda

ItemWhoNotesWelcome / Introductions

Kantara Privacy Control Panel (20 min)Andrew Hughes  
uPort Message Flow Overview (15min)

[Oliver Terbu](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b0b89c4-350c-41f9-9260-1ef40f38fec7?ref=confluence)

[![](attachments/thumbnails/18481360/18511616)](attachments/18481360/18511616.pdf)

more infos on encryption:   
[https://github.com/uport-project/specs/blob/develop/messages/encryption.md](https://github.com/uport-project/specs/blob/develop/messages/encryption.md)

Indy Catalyst Agent as Aries Agent Python Candidate (30 min)

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

Presentation: [https://docs.google.com/presentation/d/1SeGmyt7BIZRw-XDHR2NcmxJSZ2g7-tZPoBaBZ7-Jt8I/edit?usp=sharing](https://docs.google.com/presentation/d/1SeGmyt7BIZRw-XDHR2NcmxJSZ2g7-tZPoBaBZ7-Jt8I/edit?usp=sharing)

Non-repudiable signatures demo (10 min)

[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Open Discussion

## Next Week

- Making meetings more productive: [Tobias Looker](https://lf-hyperledger.atlassian.net/wiki/people/712020:6b4b9e75-c537-4af4-b498-bd8e8b96dc37?ref=confluence)and [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)
  
  - Starting an Asia-Pacific friendly meeting
  - Starting an US / Europe friendly meeting (off-week from Indy Working Group)
  - Keeping meetings focused on action: work reports and release planning
- Architecture of Aries / Indy (split between libaries and libindy): [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)

## Future Topics

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20190612-190218\_Aries-WG-C.txt](attachments/18481360/18511640.txt "Download")

Jun 13, 2019 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [uport-aries.pdf](attachments/18481360/18511616.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [image2019-6-12\_23-9-30.png](attachments/18481360/18511633.png) (image/png)  
![](images/icons/bullet_blue.gif) [GMT20190612-190218\_Aries-WG-C.txt](attachments/18481360/18511640.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481360/18511638.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481360/18511639.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
