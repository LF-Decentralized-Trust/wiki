1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-11-10 Indy Contributors Call

Created by Stephen Curran, last modified on Nov 23, 2020

## Summary

Planned:

- Indy Plenum PR Review
- Status of upcoming indy-node release, Rich Schema Feature Flag, and CI/CD Progress
- Status of upcoming indy-sdk release
- Update on Indy DID Method Specification progress

## The call recording is available here: [20201110 Indy Contributors Call Recording](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio.tech) &lt;lynn@indicio.tech&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)  (Laniakea Health) &lt;alex@laniakeahealth.com&gt;

## Related Calls and Announcements

- TBD

## Release Status and Work Updates

- Indy Node
  
  - Next release in progress, led by a team
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
- Evernym's next items (over next two months should have more people on the project, but most will be new)
  
  1. Remove the Sovrin Token from Sovrin MainNet.
  2. Having LibIndy use Indy-VDR-Aries, or using Indy-VDR-Aries directly.
  3. Migrating the LibIndy wallet to an Aries wallet and addressing performance concerns.
  4. Revocation 2.
     
     1. Mattr has  some new thinking on this.
  5. Make progress on Rich Schemas and BBS+ signatures.
     
     In addition, we want to support releases of Indy Node and Indy SDK that are being organized by the community.

## Meeting Topics

- Indy Plenum PR Review - the consensus code 
  
  - Brent's fix for INDY-827 (PR 1486)  - not to be merged into main until reviewed and tested by another
  - Need to accept PR 1482 - Evernym can do that.
  - What is the difference between STABLE and MASTER?
  - Arrange a meeting to get the CI/CD done, or perhaps merge the code bases to enable a single pipeline.
- Indy Node Release Status Updates:
  
  - Replace indy-crypto with ursa-crypto – build failing, [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) investigating.
    
    - PR to fix, but there is a dependency to indy-plenum in order to proceed.
  - [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence) is implementing the Rich Schema feature flag ([Pull Request found here](https://github.com/hyperledger/indy-node/pull/1626))
    
    - Reviewed and changes suggested
  - CI/CD Progress being made (awesome!!)
    
    - PyTest tags added – not yet merged – in draft.  Need to make sure that every test has a mark on it.  Some tests may be lost until the tags are added. Merge after that check.
      
      - Need a review and approvals.
      - One failing test – 33,000 lines of output, which breaks the test output handler. Figuring out how to fix that.
        
        - auth test case
    - Github Actions on a branch for CI – running and working, but need to keep them running in parallel to current method before moving forward.
    - GitHub Actions for CD still to be done. Volunteers?
- Request for indy-sdk release
  
  - Driver – restrictions on predicates
    
    - LibVCX not planned as part of this
  - Driver - (Evernym) fixes to indy-sdk and libvcx
  - Driver - Stable release before wrapping Aries Shared Libraries (and deprecating components)
  - Plan: mid-November release
    
    - Review what has been merged already
    - Knowledge transfer from Evernym team to Ian, Wade, others on how to tag, build and release - call to be setup this week. Sergey M. - Friday at 6AM Pacific
    - Join Zoom Meeting (Friday 6am pacific time)
      
      [https://us02web.zoom.us/j/88652458257?pwd=Z2xmdFpQbVBFTThWTVlOYm9ieitwUT09](https://www.google.com/url?q=https%3A%2F%2Fus02web.zoom.us%2Fj%2F88652458257%3Fpwd%3DZ2xmdFpQbVBFTThWTVlOYm9ieitwUT09&sa=D&source=calendar&usd=2&usg=AOvVaw2c-wlGFiIHIsOMl5g66pdu)
      
      Meeting ID: 886 5245 8257
      
      Passcode: 534767
    - Possible resources – UBC Students if there are things that can be done.
  - iOS wrapper - can we include this in the release? Latest:
    
    - Drop 32-bit (no issue there)
    - Follow instructions - doing build from scratch  – works fine, but link fails iosarch64 binaries not found (arm versions).
      
      - Issue - libsodium, SSL, ZMQ installation via homebrew; Mac binaries installed, not universal or iOS. Must install them manually - build and package. Some prebuilt ones can be installed via homebrew. Instructions need to be added - questionable source.
      - Need to decide if people should build it themselves or install via the pre-built or from a package manager (CocoaPods)  Update the instructions one way or the other.
      - Produce artifacts that can be put on CocoaPods package manager.
  - [https://github.com/hyperledger/indy-sdk/issues/2249](https://github.com/hyperledger/indy-sdk/issues/2249)
- Progress: Indy DID Method (did:indy) Specification - Meetings: [Indy DID Method Specification - Hyperledger Indy - Hyperledger Confluence](https://lf-hyperledger.atlassian.net/wiki/display/indy/Indy+DID+Method+Specification)
- Request from Hyperledger – reach out to HL Staff to help getting some contributors – has been successful in the past – **can anyone step up from the project to drive that from the project side**?  Contact [Marta Piekarska-Geater](https://lf-hyperledger.atlassian.net/wiki/people/5e73630546571b0c3da79b94?ref=confluence)

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464416/19465560.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
