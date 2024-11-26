1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-10-20 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Oct 20, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) (Animo Solutions) &lt;berend@animo.id&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence)&lt;a@2060.io&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Make contributions to Bifold easier
  - Connectivity issues (have been reported on Bifold and AFJ sides)
    
    - AFJ Issue: [https://github.com/hyperledger/aries-framework-javascript/issues/1048](https://github.com/hyperledger/aries-framework-javascript/issues/1048)
    - Bifold Issue: [https://github.com/hyperledger/aries-mobile-agent-react-native/issues/367](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/367)
- Aries Call
  
  - How to solve the agent behind a firewall issue that can't connect to a ledger?
  - cleaned up open PRs
  - [Fall IIW 2022](https://internetidentityworkshop.com/) - Un-Conference, [November 15-17](https://www.eventbrite.com/e/internet-identity-workshop-iiwxxxv-35-2022b-tickets-368643531727) - San Francisco, CA
- Timeline and roadmap for DIDComm v2 support
  
  - ACA-Py, AFJ, AATH
  - Looking for people who are interested in this effort → reach out to [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) he can add you to the Discord cohort
  - Discord thread [https://discord.com/channels/905194001349627914/1032662111307960453](https://discord.com/channels/905194001349627914/1032662111307960453)

## Agenda

- Record the meeting
- 0.3.0 release
  
  - Write migration guide like [https://aries.js.org/guides/updating/versions/0.1-to-0.2](https://aries.js.org/guides/updating/versions/0.1-to-0.2)
  - AATH integration
    
    - [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence)will do his best, with the help or [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence)
  - Plan
    
    - Release 0.2.5
    - Merge inconsistencies PR
    - Merge 0.3.0-pre into main
      
      - triggers 0.3.0-alpha.0 release → test it out!
      - Animo, Indicio will test
    - Trigger 0.3.0 changelog PR
    - Write migration guide → need to wait for complete changelog
    - Make 0.3.0 release
  - Extensions updates
    
    - Hooks → Bifold (BCGov/Indicio/Community)
    - Rest → Animo
- Indy SDK React Native
  
  - Crash in newer RN versions
  - [https://github.com/hyperledger/aries-mobile-agent-react-native/issues/469](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/469)
  - options
    
    - create new build for indy-sdk with libzmq 4.3.0+
    - use shared components
      
      - we could start with only indy-vdr
    - use indy-vdr-proxy
- Decline issuance / proof request PR - [https://github.com/hyperledger/aries-framework-javascript/pull/1014](https://github.com/hyperledger/aries-framework-javascript/pull/1014)
- Post 0.3.0

## Meeting Notes

## Future topics

Next Week:

- Indy SDK React Native crash

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

[video1897399618.mp4](#)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
