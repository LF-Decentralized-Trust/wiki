1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-01-19 Indy Contributors Call

Created by Stephen Curran, last modified on Jan 19, 2021

## Summary

Planned:

- Status of indy-node CI/CD progress
- Status of upcoming indy-sdk release
- GitHub Actions for the Indy SDK

## Recording from the call: [20210119 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Richard Esplin (Evernym) &lt;richard.esplin@evernym.com&gt;
- Robin Klemens (DB Systel GmbH) &lt;Robin.Klemens@deutschebahn.com&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)  (Laniakea Health) &lt;alex@seropass.me&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - Next release in progress, same content as the last release, but using a revised CI/CD process for at least indy-plenum and indy-node
- Indy SDK
  
  - Next release in progress, led by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - donated to Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa

## Meeting Topics

- Indy SDK Release - [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
  
  - RC published and being tested – w00t!! – 1.16, Build 170
    
    - No tag yet – it's in the RC branch
  - Ready for release?
- Indy Node Release
  
  - Process:
    
    - Fix Jenkins so that we have a build to compare with (Evernym)
    - Setup Github Actions / Azure CI pipeline (Kevin, Wade)
      
      - Plenum CI – unblock some of the tests – PR this morning
      - Node CI portion - complete
      - Node CD progress - being worked on, working on the tests in Kevin's repo
      - Plenum CD side – Ian has started to work on that, but not much to report yet.
      - Issue:
        
        - Build containers are used in the flows – currently in Wade or Kevin's personal repo.
          
          - How to manage the images and where to put them?  Push the images to Hyperledger's Docker Hub, or GitHub Packages. Wade to check on this, leaning to Hub.
          - Base core CI and images are from Hyperledger and are from 16.04 at this point – which is appropriate for our first goal.
          - Question is who else is using those.  Kevin to check with Ry on that.
    - Show that a release through Github is the same as through Jenkins
    - Start releasing from Master instead of Stable (Wade)
  - Goals (ranked):
    
    1. Release using CI / CD on GitHub Actions
    2. Update from Ubuntu 16.04 to Ubuntu 18.04 / Ubuntu 20.04
       
       1. When updating validator nodes, note that there is a bug that prevents catch up from an empty ledger. Must copy data to the new machine then catch-up.
       2. During the upgrade, it's better to have different versions of Ubuntu with same version of Indy Node then run for an extended period of time with different versions of Indy Node.
       3. PR in flight for Ubuntu 18.04 with some debate as to whether it is complete or not. Some suspect that getting that PR completed vs. getting to 20.04 is the same effort.
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
  - Conversation about documenting the new branching model for Indy.
    
    - It isn't currently documented.
    - [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) 's understanding of the current plan:
      
      - 1\. Create a branch with everything in Master
      - 2\. Revert Master back to the last release from Stable
      - 3\. Merge everything from Stable into Master
      - 4\. Then merge from the branch that used to be Master back into Master
      - This will probably happen over multiple releases.
      - Then going forward, each release will come from Master with a release Tag that could be used to create a branch if needed.
    - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) 's goal for branching – slightly different from Richard's:
      
      1. Rename Master to Main
      2. Set Main to be the contents of Stable -- identical to the last release of Indy Node (same for plenum).
      3. Evolve from there, starting with the Ubuntu upgrade.
      4. Only add things from the "old Main" as needed -- e.g. indy-crypto to ursa-crypto.
         
         1. Anything that was not in Stable as of Aug. 30 would have to be re-added as PR.
         2. Rational for that is that there wasn't too much in that, with the main content being Rich Schema, which is generally considered to be obsolete in the community.
    - Where should it be documented?
      
      - Historically, we have released Indy and Sovrin simultaneously, so the documentation on the current branching model is here:
        
        [https://github.com/sovrin-foundation/sovrin/blob/master/docs/release.md](https://github.com/sovrin-foundation/sovrin/blob/master/docs/release.md)
        
        and here:
        
        [https://github.com/sovrin-foundation/sovrin/blob/master/docs/acceptance.md](https://github.com/sovrin-foundation/sovrin/blob/master/docs/acceptance.md)
        
        It would be good to move the Indy specific stuff into the Indy repos describing the new branching model (releases from tags in Master).
        
        Traditionally, the stable branch was needed to coordinate builds of Indy and the Sovrin Token. But we expect that to go away quickly. And Indy development has slowed, so Master should be more stable.

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464453/19465662.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
