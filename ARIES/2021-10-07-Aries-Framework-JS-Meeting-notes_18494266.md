1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-10-07 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Jakub Koci on Oct 07, 2021

Planned Topics:

- AFJ Mediation
- Issues and PRs
- AMA

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence)  (Indicio) &lt;james.ebert@indicio.tech&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
- Animo has won eSSIF Lab Grant to build Aries Mobile SDK - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://drive.google.com/file/d/1t9_XljI9rvFrgvNVM7ymxFae3Xo0Nhvx/view?usp=sharing)
  
  - AIP 2.0
  - BBS+, JSON-LD
  - Shared components (Aries Askar, Indy CredX, Indy VDR)

## Agenda

- Record the meeting
- Welcome &amp; Introductions
- AFJ Mediation Architecture
  
  - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1q_rB3YCAHi2h9HgVC-MhWg9PqEEn1bDD/edit?usp=sharing&ouid=116426574400293992845&rtpof=true&sd=true)
  - What do we need in AFJ/at a protocol level 
    
    - Pickup protocol
    - Plugable persistence of messages
    - Database for indy storage
    - HTTP vs WebSockets
  - What do we need outside of AFJ
    
    - Redis
    - Push-notifications
- Issues &amp; PRs
  
  - [feat(core): support image url in invitations](https://github.com/hyperledger/aries-framework-javascript/pull/463)
  - [feat(core): support multiple indy ledgers](https://github.com/hyperledger/aries-framework-javascript/pull/474)
    
    - Should we prefer a self-certifying DID on a non-production ledger over a non-self-certifying DID on a production ledger?
- Expose wallet API
- AMA

## Open Issues

- [Finish getting started guides in documentation](https://github.com/hyperledger/aries-framework-javascript/issues/338) !!! Stephen &amp; Mostafa
- [Add support for receiving and proving revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/349) - James
- Loading ledger asynchronously - reduce the time it takes when receiving a credential
- How to handle the case without an internet connection
- [Add support for RFC 0035: Problem Report](https://github.com/hyperledger/aries-framework-javascript/issues/58) - both adopted into other protocols and initiating it as a standalone protocol
- [wallet import and export](https://github.com/hyperledger/aries-framework-javascript/issues/175)
- Add demos on how to use AFJ as issuer/holder/verifier (like sample mediator)
- Machine-readable governance frameworks
- Action menu
- [Add support for verifying revocable indy credentials](https://github.com/hyperledger/aries-framework-javascript/issues/350)
- [Allow invitations to use public DID](https://github.com/hyperledger/aries-framework-javascript/issues/84)
- [Add support for RFC 0434: Out-of-Band](https://github.com/hyperledger/aries-framework-javascript/issues/344) - Priority (Connection reuse)
- [Add support for RFC 0023: DID Exchange](https://github.com/hyperledger/aries-framework-javascript/issues/345)
- [Add support for 0453: Issue Credential v2](https://github.com/hyperledger/aries-framework-javascript/issues/352)

## Meeting Notes

## Future topics

- React Native testing
- Support for Deno
  
  - Although it's not our focus right now, it should be possible in the long term.
  - First, we need to analyze if the following dependencies will work in Deno or what we need to do to make it work:
    
    - indy-SDK
    - native dependencies (file system, transport protocols like HTTP or WebSockets, ...)
    - other dependencies in package.json
- Monorepo dependencies
  
  - TypeScript types

**Meeting recording:**

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18494266/18515605.txt "Download")

Oct 07, 2021 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
