1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2022 Bifold Meetings](2022-Bifold-Meetings_18515892.html)

# Hyperledger Aries : 2022-10-11 Aries Bifold Users Group Community Meeting

Created by James Ebert, last modified on Oct 11, 2022

## Summary

Planned Topics:

- Fork Maintenance Strategy Discussion
- OCA in Bifold

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
- Sam Curren (Indicio) &lt;sam@indicio.tech&gt;
- Lance Byrd (RootsID) &lt;lance.byrd@rootsid.com&gt;
- Clecio Varjao (Gov. of BC) &lt;clecio.varjao@gov.bc.ca&gt;

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
  
  - iOS Sleep/Lock Crash (ZMQ) - [https://github.com/hyperledger/aries-mobile-agent-react-native/issues/469](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/469)

## Agenda

- Bifold Fork Management Strategy Discussion - Sam
  
  - At least 2 orgs maintaining "forks" of Bifold to ship applications
  
  <!--THE END-->
  
  - Is there guidance on how to best stay close to Hyperledger Bifold Main
  - What are the strategies here?
  - Other questions
    
    - Bifold as a fork – very hard to keep things together (contribution becomes hard to stay in sync)
    - Contribution after the fact – figure out what to contribute, create a PR, rebase if needed, etc
  - Android &amp; iOS folders are fairly specific to the individual app, etc
    
    - Tool or generator to scaffold a Bifold app - Lance love this
  - "Fork" – not meaning going away from Bifold. Eventually an org will need to make deviations from Bifold, such as brand/color changes, logos, navigation
    
    - *Not* "Fork and Forget"
    - "Close Fork"
  - Modularization - Contributing on a component-basis would be easier
    
    - We also need something for someone to start from – defaults
    - Framework – how to manage screens, components, navigation, etc
      
      - Peer dependencies are a mess in React Native
      - Library vs Framework
        
        - Framework is in control and manages things
        - Library has re-usable pieces that an end developer can use
          
          - Does AFJ fill this role?
          - Bifold fills a valuable role in the community – fully featured application, an example
          - How do we make it the easiest for people to contribute back to Bifold – not a launchpad but rather a ship
    - Navigation stack is a bit of a mess
      
      - Very business-case centric
      - Components could be passed a callback that handles navigation (meaning the end-developer/app can handle it)
      - This could be a boundary line – a component doesn't do
  - Collaboration between organizations
  - "It would be easier to contribute if..."
  - Is React Native the right place? – Yes, for today
  - Technical Process for managing forks
    
    - BCWallet – Bifold is set up as a Git Submodule
- OCA in Bifold (followup from the Aries WG)
  
  - Draft PR for an API
    
    - Issues running in Bifold
    - Goal is to just get started, using layers, configuration, etc. May need to refactor
- Timing of first credential issue
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

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18499145/18516829.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499145/18516830.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499145/18516828.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
