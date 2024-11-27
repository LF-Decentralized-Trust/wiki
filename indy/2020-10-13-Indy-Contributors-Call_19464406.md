1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-10-13 Indy Contributors Call

Created by Stephen Curran, last modified on Oct 13, 2020

## Summary

Planned:

- Discussion - Release Rich Schema or not
- Indy HIPE - Generic Token
- Release Status Update

## The call recording is available here: [202021013 Indy Contributors Call Recording](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)  (Laniakea Health) [alex@laniakeahealth.com](mailto:alex@laniakeahealth.com)
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) ([Indicio.tech](http://Indicio.tech)) [lynn@indicio.tech](mailto:lynn@indicio.tech)
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) wade.barnes@shaw.ca
- [Himangshu Pan](https://lf-hyperledger.atlassian.net/wiki/people/5ca13e399a000c1180954e0a?ref=confluence) (Klizo Solutions) [himangshu@klizos.com](mailto:himangshu@klizos.com)
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;[smccown@anonyome.com](mailto:smccown@anonyome.com)f&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- [IIW](https://internetidentityworkshop.com/) Oct 20-22 (will be held online)

## Release Status and Work Updates

- Indy Node
  
  - Next release in process
- Indy SDK
  
  - Team at ABSA is considering a different architecture [https://github.com/AbsaOSS/libvcx/commits/master](https://github.com/AbsaOSS/libvcx/commits/master) - likely to become an Aries repo with libvcx removed from indy-sdk
  - Next Release Timing TBD
  - Wrapper for IOS and Android from GlobalID to be donated
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
  
  - Update to validator-status script to include public IP addresses of nodes – thanks [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)and [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)
- Indy/Aries Shared Libraries
  
  - Current status: creating a branch of ACA-Py with these components and without indy-sdk
  - Indy Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
  - Aries Shared:
    
    - aries-credx
    - aries-askar - Aries Storage - [https://github.com/andrewwhitehead/aries-askar](https://github.com/andrewwhitehead/aries-askar)
- Ursa

## Meeting Topics

- New Indy HIPE - [Generic Token](https://github.com/hyperledger/indy-hipe/tree/master/text/0161-generic-token)
  
  - Question: define a payment interface, or include a generic token plugin?
    
    - Could make the Sovrin token generic:
      
      [https://github.com/sovrin-foundation/token-plugin](https://github.com/sovrin-foundation/token-plugin)
      
      [https://github.com/sovrin-foundation/libsovtoken](https://github.com/sovrin-foundation/libsovtoken)
    - Do we need Hyperledger TSC approval to include token code in Hyperledger?
    - Vote: 8 Yes, 0 No, 4 abstain
- Should Rich Schema be released or not?
  
  - Vote:
    
    - Yes to release what is on Main today (including Rich Schema) **after** the feature flag is added
    - No to make Main match what is the current release today and carry forward from there.
  - Vote results:
    
    - Yays: 4
    - Nays: 1
    - Abstains: 1
- Release Status:
  
  - Replace indy-crypto with ursa – build failing, [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)investigating
  - CI/CD Progress being made (yay!)

## Future Calls

Next call:

- Indy Plenum PRs

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464406/19465497.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464406/19465505.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
