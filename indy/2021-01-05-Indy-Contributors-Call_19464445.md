1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-01-05 Indy Contributors Call

Created by Richard Esplin, last modified by Stephen Curran on Jan 05, 2021

## Summary

Planned:

- Proposal: BC Gov to contribute the [indy-shared-rs](https://github.com/bcgov/indy-shared-rs) repo to Hyperledger
- Status of indy-node CI/CD progress
- Status of upcoming indy-sdk release
- GitHub Actions for the Indy SDK

## Recording from the call: [20210105 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)  (Laniakea Health) &lt;alex@seropass.me&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio.tech) &lt;lynn@indicio.tech)
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Related Calls and Announcements

- BC Gov Open Source Bounty ($60k CDN) to add W3C Standard Verifiable Credentials with ZKP and Selective Disclosure to ACA-Py. Applications accepted through Friday [here](https://digital.gov.bc.ca/marketplace/opportunities/code-with-us/3f9f0e86-b8bf-47ee-9f3d-5b272f9ec845).

## Release Status and Work Updates

- Indy Node
  
  - Next release in progress, same content as the last release, but using a revised CI/CD process for at least indy-plenum and indy-node
- Indy SDK
  
  - Next release in progress, led by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries
- Ursa

## Meeting Topics

- **Proposal**: BC Gov to contribute the [indy-shared-rs](https://github.com/bcgov/indy-shared-rs) repo to Hyperledger
  
  - A companion repo to [indy-vdr](https://github.com/hyperledger/indy-vdr) (already contributed to Hyperledger) and [aries-askar](https://github.com/bcgov/aries-askar) (also proposed for contribution)
  - Should it by aries-shared-rs? Probably not, since it relies on anoncreds, which is an Indy concept. Usage is optional in Aries.
  - No objections to accepting the contribution.
- Indy SDK Release - [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
  
  - RC published and being tested – w00t!! – 1.16, Build 170
    
    - No tag yet – it's in the RC branch
  - Couple of weeks for community to test
  - Ubuntu and Windows tests ran successfully
  - BC Gov apps being built and tested
  - Plan is to request approval for release at the next Contributors call.
  - The mobile and Mac releases are all there.
- GitHub Actions for the Indy SDK – ABSA contribution
  
  - Community request – what is needed to replace Jenkins with this
    
    - LibIndy and postgres plugin only
    - Publish binaries for mobile only
    - Wrappers, plus some additional ones
    - A new container image based on Alpine with precompiled LibIndy and plugins.
    - Drop LibVCX, Token, Windows, RedHat, and Ubuntu
      
      - People who want this support can contribute on top of this GitHub actions  work.
    - Plan: Fork to ABSA, 2 weeks implementing GHA and then a PR to Indy
    - Default runners in GHA
      
      - But could be done with Hyperledger's Azure Pipelines if necessary.
      - Doesn't look to be needed, as the Indy Node pool is working fine in GHA.
        
        - GHA supports cached containers, so the same Indy Node image can be reused.
- Indy Node Release
  
  - Process:
    
    - Fix Jenkins so that we have a build to compare with (Evernym)
    - Setup Github Actions / Azure CI pipeline (Kevin, Wade)
    - Show that a release through Github is the same as through Jenkins
    - Start releasing from Master instead of Stable (Wade)
  - Goals (ranked):
    
    1. Release using CI / CD on GitHub Actions
    2. Update from Ubuntu 16.04 to Ubuntu 18.04 / Ubuntu 20.04
       
       1. When updating validator nodes, note that there is a bug that prevents catch up from an empty ledger. Must copy data to the new machine then catch-up.
       2. During the upgrade, it's better to have different versions of Ubuntu with same version of Indy Node then run for an extended period of time with different versions of Indy Node.
    3. New branching model to release from Master with tags
       
       1. Promote Stable to Master, then deprecate Stable
    4. Release work in Master
       
       1. Using a feature flag to prevent usage of new Rich Schemas transactions.
    5. Switch from Indy Crypto to Ursa
    6. Potential features to assist with removing token from Sovrin networks
       
       1. Stub unused ledgers from removed plugins
       2. Fees as a Node concept
  - Potential releases:
    
    - CI / CD Change, released from Stable
      
      - indy-crypto: use existing artifact
      - indy-plenum: generate from new GitHub CI / CD
      - indy-node: generate from new GitHub CI / CD
      - token-plugin: generate from Jenkins
      - sovrin-node: generate from Jenkins
      - ursa-crypto: exclude
    - Upgraded Ubuntu, release from Stable
      
      - indy-crypto: use existing artifact / release from Jenkins / exclude from release (if necessary)
      - indy-plenum: generate from new GitHub CI / CD
      - indy-node: generate from new GitHub CI / CD
      - token-plugin: generate from Jenkins/use existing artifact
      - sovrin-node: generate from Jenkins
      - ursa-crypto: excluse from release / use existing artifact (if necessary)
    - Release without Stable (move what is Master today into a branch)
      
      - Same components/sources  as previous release
    - Remove Token, released from Stable (There is not agreement this is desirable now vs. other priorities)
      
      - indy-crypto: use existing artifact
      - indy-plenum: generate from new GitHub CI / CD
      - indy-node: generate from new GitHub CI / CD
      - token-plugin: stub or exclude
      - sovrin-node: generete from Jenkins
      - ursa-crypto: exclude
    - Release New Features (merge former Master branch back to Master)
      
      - indy-crypto: exclude
      - indy-plenum: generate from new GitHub CI / CD
      - indy-node: generate from new GitHub CI / CD
      - token-plugin: stub or exclude
        
        - If necessary, could try to release with existing token-plugin
      - sovrin-node: maybe new Github CI / CD
      - ursa-crypto: existing artifacts

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464445/19465631.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464445/19465648.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
