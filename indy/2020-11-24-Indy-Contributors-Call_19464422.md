1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-11-24 Indy Contributors Call

Created by Stephen Curran, last modified by Kevin Griffin on Nov 29, 2020

## Summary

Planned:

- Status of Ubuntu 20.04 work
- Status of upcoming indy-node release, Rich Schema Feature Flag, and CI/CD Progress
- Status of upcoming indy-sdk release

## The call recording is available here: [20201124 Indy Contributors Call Recording](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio.tech) &lt;lynn@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)  (Laniakea Health) &lt;alex@laniakeahealth.com&gt;
- [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) (Scoir) &lt;kg@scoir.com&gt;

## Related Calls and Announcements

- TBD

## Release Status and Work Updates

- Indy Node
  
  - Next release in progress, led by this team
  - Ubuntu 20.04
- Indy SDK
  
  - Next release in progress, led by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
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
- Evernym's next items (won't be adopting shared libraries, will probably maintain LibIndy as a fork)
  
  1. Current releases of Indy Node and Indy SDK
  2. Remove the Sovrin Token from Sovrin MainNet.
  3. Revocation 2.
     
     1. Mattr has  some new thinking on this.
  4. Make progress on Rich Schemas and BBS+ signatures.

## Meeting Topics

- Ubuntu 20.04 for Indy Node / Indy Plenum
  
  - Now likely highest priority - release is needed as soon as possible
    
    - Ursa wants to deprecate their builds for Ubuntu 16.04
    - Backported packages that are probably not needed any longer:
      
      [https://repo.sovrin.org/deb/pool/xenial/stable/](https://repo.sovrin.org/deb/pool/xenial/stable/)
  - [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) has been looking at this.
    
    - Moving forward – can anyone help Steve with this effort?
      
      - Cam from Kiva?  Someone from Evernym?
  - Previous efforts
    
    - [https://github.com/hyperledger/indy-node/pull/1443](https://github.com/hyperledger/indy-node/pull/1443)
    - [https://github.com/hyperledger/indy-plenum/pull/1332](https://github.com/hyperledger/indy-plenum/pull/1332)
  - Learning about CI / CD
    
    - [https://github.com/hyperledger/indy-node/blob/master/docs/source/ci-cd.md](https://github.com/hyperledger/indy-node/blob/master/docs/source/ci-cd.md)
    - 
      
      (start at minute ~23.5)
      
      Describes: 
      
      Error rendering macro 'jira' : null
    - 
      
      (start at minute ~11.5)
    - Build and packaging scripts are here:
      
      [https://github.com/hyperledger/indy-plenum/tree/master/build-scripts/ubuntu-1604](https://github.com/hyperledger/indy-plenum/tree/master/build-scripts/ubuntu-1604)
      
      [https://github.com/hyperledger/indy-node/tree/master/build-scripts/ubuntu-1604](https://github.com/hyperledger/indy-node/tree/master/build-scripts/ubuntu-1604)
- Indy Plenum PR Review - the consensus code - Any updates to status?
  
  - Brent's fix for INDY-827 (PR 1486)  - not to be merged into main until reviewed and tested by another
    
    - Decision: Will not be merged into this release because of the manual testing effort.
  - Need to accept PR 1482 - Evernym can do that.
  - What is the difference between STABLE and MASTER
    
    - Stephen to review the last call recording
  - Arrange a meeting to get the CI/CD done, or perhaps merge the code bases to enable a single pipeline.
    
    - Plenum PR created
    - One test is failing – likely not because of the CI/CD – failed previously
    - Plan is to get this done entirely
- Indy Node Release Status Updates:
  
  - Replace indy-crypto with ursa-crypto – build failing, [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) investigating.
    
    - PR to fix, but there is a dependency to indy-plenum in order to proceed.
    - Still stuck on indy-plenum
  - [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence) is implementing the Rich Schema feature flag ([Pull Request found here](https://github.com/hyperledger/indy-node/pull/1626))
    
    - New PR needed because first not based to Master branch – take 2 coming soon.
    - Alex K is working on this
  - CI/CD Progress being made (awesome!!)
    
    - Paused – indy-plenum will go first and work will resume here
    - PyTest tags added – not yet merged – in draft.  Need to make sure that every test has a mark on it.  Some tests may be lost until the tags are added. Merge after that check.
      
      - Need a review and approvals.
      - One failing test – 33,000 lines of output, which breaks the test output handler. Figuring out how to fix that.
        
        - auth test case
    - Github Actions on a branch for CI – running and working, but need to keep them running in parallel to current method before moving forward.
    - GitHub Actions for CD still to be done. Volunteers?
- Request for indy-sdk release
  
  - RC branch ready to go, release notes updated, everything is almost ready to go
  - Problem: IOS branch is not building.  What do we do?
    
    - Sergey has a PR that seemed to work, and build is in progress for that.
    - If so – Master to RC and we're good to go.
    - Could drop IOS, but we'd really rather not do that.
    - Point people: Sergey, Ian, Steve McCowan, Wade
  - One commit in Master Branch is not DCO signed.
    
    - Someone manually bypassed the DCO which allowed us to proceed – a very bad practice.
      
      - Separate issued – Ry to be asked if that button can be turned off.
    - Fixed in the RC branch – not touched in the Master Branch
    - How to address in the Master Branch?
    - Ian, Wade and Ry to discuss.
  - Should we release now or get more features in?
    
    - No one requested more be added
  - Should this be the last indy-sdk release?
    
    - Evernym would like to free up the team to do other things, so would like to know if more effort is to be put into the indy-sdk?
- Progress: Indy DID Method (did:indy) Specification
  
  - Meetings: [Indy DID Method Specification - Hyperledger Indy - Hyperledger Confluence](https://lf-hyperledger.atlassian.net/wiki/display/indy/Indy+DID+Method+Specification)
- Request from Hyperledger – reach out to HL Staff to help getting some contributors – has been successful in the past – **can anyone step up from the project to drive that from the project side**?  Contact [Marta Piekarska-Geater](https://lf-hyperledger.atlassian.net/wiki/people/5e73630546571b0c3da79b94?ref=confluence)

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464422/19465571.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
