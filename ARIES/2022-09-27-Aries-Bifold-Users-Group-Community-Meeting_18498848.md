1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2022 Bifold Meetings](2022-Bifold-Meetings_18515892.html)

# Hyperledger Aries : 2022-09-27 Aries Bifold Users Group Community Meeting

Created by Jason Leach, last modified by James Ebert on Jan 31, 2023

## Summary

Planned Topics:

- Biometrics Implementation discussion
- React Native Upgrade
- Proof Proposals
- OCA Work Progress

## Community Meeting Policies

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

Take the opportunity to introduce yourself or organization. Let the community know what interest you have in the Bifold effort.

## Attendees

Record your attendance for posterity, and allow others may contact you if needed.

- Name (Organization) &lt;email&gt;
- James Ebert (Indicio) &lt;james.ebert@indicio.tech&gt;
- Jason Leach (Fullboar Creative) &lt;jason.leach@[fullboar.ca](http://fullboar.ca)&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- Sean Bohan (Hyperledger) &lt;sbohan@linuxfoundation.org&gt;
- Akiff Manji (Petri Dish Development) &lt;amanji@petridish.dev&gt;

## Announcements

## Deployments and Work Updates

- Biometrics - mostly done, still WIP
  
  - According to the targeted NIST Spec – you can't upgrade, you can only downgrade
  - [https://csrc.nist.gov/publications/detail/sp/800-63/3/final](https://csrc.nist.gov/publications/detail/sp/800-63/3/final)
  - Add a key check to AFJ or Indy SDK / Indy Credx
- Technical debt cleanup and documentation planned.
  
  - Improving the unit test coverage
  - Getting started documentation
  - Yarn package manager
- Initial work started on working with OCA
  
  - Aspects planned for integration
    
    - Branding
    - Credential Internationalization
    - [https://oca.colossi.network/v1.1.0-rc.html#label-overlay](https://oca.colossi.network/v1.1.0-rc.html#label-overlay)
- React Native update to 0.70.1 by Indicio.

## Agenda

- Proof Proposals
  
  - Holders requesting proofs from organizations
  - Methods:
    
    - Definition of Proof Requests in Machine Readable Governance Files
      
      - Also works in a holder to holder case
      - Can provide proofs requests as well as
      - Prototyping in Bifold would be quite beneficial at this point
        
        - Email governance or other hair-on-fire use case
      - Being spec'd at the DIF
        
        - Expression of sentiments about DIDs - who are the valid issues, verifiers, etc
        - Recognition of issuers/verifiers via credentials
        - Potential to join DIF MRG &amp; ToiP Trust Registries
      - Lots of things possible, what's in scope?
        
        - Participant identifiers:
          
          - Identification by DID
          - Identification by credential
        - Schemas
          
          - Schema for issuance
          - Schema for verification
        - Issuers of schemas
        - Approved verifiers (applicable of only some use cases)
          
          - Also schema based
        - Out of scope:
          
          - Workflows
      - DIF - Subgroup on the Claims and Credentials WG - Contact Sam Curren to get invitation details
        
        - [https://github.com/decentralized-identity/claims-credentials/blob/main/AGENDA.md](https://github.com/decentralized-identity/claims-credentials/blob/main/AGENDA.md)
      - It's better to get started and get experimenting
        
        - Aries WG – Get email Governance started
    - OCA provided proof requests
    - The organization provides a proof proposal
      
      - Could be provided by Action Menu
- React Native update to 0.70.1 by Indicio.
- VM Development Environment
  
  - Dockerized services
  - Does rely on Xcode &amp; Android SDK - Native installation process needed
  - Documentation issue
- Q/A w/Maintainers
- Review PRs.
- Review relevant issues.

## Next Meeting

- TBD

## Future Topics

- Machine Readable Governance Presentation - Mike
- How should we implement Machine Readable Governance?

## Action items

- How to move from v1 to v2 for present proof and issue credential. Will we need to deal with two different screens as both v1 and v2 are supported.
- Support OOB.

# Recording

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18498848/18516775.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498848/18516776.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498848/18516774.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
