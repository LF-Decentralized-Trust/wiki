1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-11-03 Aries Framework JS Meeting notes

Created by Moritz Schlichting, last modified on Nov 03, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Moritz Schlichting](https://lf-hyperledger.atlassian.net/wiki/people/617fa696bcb5740068dd4a60?ref=confluence) (Animo Solutions) &lt;moritz@animo.id&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call
  
  - Discussion on Push Notifications
  - Removed ACK Fail - [https://github.com/hyperledger/aries-rfcs/pull/727](https://github.com/hyperledger/aries-rfcs/pull/727)
    
    - Relevant issue in AFJ: [https://github.com/hyperledger/aries-framework-javascript/issues/1074](https://github.com/hyperledger/aries-framework-javascript/issues/1074)
- DIDComm v2 Adoption
  
  - Where are we?
  - What would help?
  - Comments welcome on s[preadsheet](https://docs.google.com/spreadsheets/d/15noWiG_zhhUpornhrZm9cLEjQ1aa6z9qgJgPCaaIbtY/edit?usp=sharing) for important DIDComm v2 considerations/attributes
  - Discussion welcome in the d[iscord channel](https://discord.com/channels/905194001349627914/1032736844053483621)
  - Join the discord or reach out to [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence)
- IIW is coming up - [https://internetidentityworkshop.com](https://internetidentityworkshop.com/)
  
  - November 15 - 17

## Agenda

- Record the meeting
- 0.3.0 release
  
  - Write migration guide like [https://aries.js.org/guides/updating/versions/0.1-to-0.2](https://aries.js.org/guides/updating/versions/0.1-to-0.2)
  - Plan
    
    - Write migration guide → need to wait for complete changelog
    - Make 0.3.0 release
  - Extensions updates
    
    - Hooks → Bifold (BCGov/Indicio/Community)
    - Rest → Animo
- Decline issuance / proof request PR - [https://github.com/hyperledger/aries-framework-javascript/pull/1014](https://github.com/hyperledger/aries-framework-javascript/pull/1014)
- Post 0.3.0
  
  - Shared Components (0.4.0)
  - JSON-LD credential issuance/verification (0.3.x)
  - Ledger Agnostic AnonCreds – related to shared components (0.4.0/0.5.0)
  - Type aware eslint rules (after JSON-LD issuance/verification, incremental)
  - Slimming down core (incrementally)
    
    - extract into separate package and depend on the separate package from core → remove in next major release

## Meeting Notes

- Failures in Aries Agent Test Harness
  
  - [https://allure.vonx.io/api/allure-docker-service/projects/findy-b-javascript-f-dotnet/reports/384/index.html](https://allure.vonx.io/api/allure-docker-service/projects/findy-b-javascript-f-dotnet/reports/384/index.html)
  - [https://allure.vonx.io/api/allure-docker-service/projects/findy-b-javascript/reports/383/index.html](https://allure.vonx.io/api/allure-docker-service/projects/findy-b-javascript/reports/383/index.html)
- Performance issues multi-use invitation vs single-use invitation (using AFJ mediation)
  
  - Might this be related to v1 vs v2
- OpenID connect  integration  with AFJ? (offline)
- Push on shared components
- URGENT!: How can we get [https://github.com/hyperledger/aries-framework-javascript/pull/795](https://github.com/hyperledger/aries-framework-javascript/pull/795) merged as soon as possible
  
  - It's costs maintenance overhead for Mike (Richardson)
- MIgration guide:
  
  - Please follow the guide
  - Either:
    
    - Open issues if things are missing in [https://github.com/hyperledger/aries-javascript-docs](https://github.com/hyperledger/aries-javascript-docs/pull/74) OR
  - Or:
    
    - Comment on the PR [https://github.com/hyperledger/aries-javascript-docs/pull/74](https://github.com/hyperledger/aries-javascript-docs/pull/74)

## Future topics

Next Week:

- Shared components how to finish asap
- Mikes PR merge
- potentially multi vs single use invite performance

Future Topics:

- React Native testing
- Monorepo dependencies
  
  - TypeScript types

<!--THE END-->

- ACA-py and AFJ performance/scale documentation
- Mike's modularization, etc documentation
- Open ID Connect for Issuance/Verification
  
  - [https://openid.net/specs/openid-4-verifiable-credential-issuance-1\_0.html](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html)
  - [https://github.com/bcgov/vc-authn-oidc](https://github.com/bcgov/vc-authn-oidc)
- Hyperledger fabric and Aries wrapper new updates

**Meeting recording:**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499725/18516975.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
