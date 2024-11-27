1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-09-29 Indy Contributors Call

Created by Stephen Curran, last modified on Sep 29, 2020

## Summary

Planned:

- Continue the Indy Release Planning Meeting

## The call recording is available here: [20200929 Indy Contributors Call Recording](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) (Hyperledger) &lt;rjones@linuxfoundation.org&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Himangshu Pan (Klizo Solutions) &lt;himangshu@klizos.com&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence) (Evernym) &lt;brent.zundel@evernym.com&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence) (Laniakea Health) &lt;alex@laniakeahealth.com&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio.tech) &lt;lynn@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Related Calls and Announcements

- [IIW](https://internetidentityworkshop.com/) Oct 20-22 (will be held online)

## Release Status and Work Updates

- Indy Node
  
  - Next release in process
- Indy SDK
  
  - Team at ABSA is considering a different architecture [https://github.com/AbsaOSS/libvcx/commits/master](https://github.com/AbsaOSS/libvcx/commits/master) - likely to become an Aries repo with libvcx removed from indy-sdk
  - Next Release Timing TBD
  - Libindy on IOS Challenges: XCode 11 has a change in it to the simulator name ("-sim" added to the name) – prevents Libindy to running on the simulator - building for Sim/Linking for platform running on.
    
    - [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) investigating and looking for collaborators.  Follow ups on indy channel on RC.
      
      - GitHub Actions now has iOS builders - does this help?
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

- Future of LibVCX:
  
  - ABSA proposal:
    
    [https://lists.hyperledger.org/g/indy/topic/proposal\_to\_move\_absa\_libvcx/77033698?p=,,,20,0,0,0::recentpostdate/sticky,,,20,2,0,77033698](https://lists.hyperledger.org/g/indy/topic/proposal_to_move_absa_libvcx/77033698?p=%2C%2C%2C20%2C0%2C0%2C0%3A%3Arecentpostdate%2Fsticky%2C%2C%2C20%2C2%2C0%2C77033698)
  - Deprecate from Indy-SDK
  - Move to Aries: Aries-VCX / Aries-Rust-VCX? aries-vcx-rs
  - Proposal: move to Aries quickly, but wait to deprecate from Indy-SDK until the new repo is stable.
    
    - Add a note Indy-SDK letting people know about the new repo.
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) to continue discussion on a new release of indy-plenum and indy-node - from this meeting: [2020-09-17 Special: Planning Next Indy Node Release](19464402.html)
  
  - Process flow [summary](https://docs.google.com/presentation/d/1iYIIlkZUcgfVh8SvrzQXPgPyUUNubgUAomTTpcJ9J_Q/edit#slide=id.p)
  
  <!--THE END-->
  
  - Additional goal of this effort – eliminate the difference between stable and master at the time the release is made
- Status:
  
  - Replace indy-crypto with ursa – complete?
    
    - Wade has reviewed it, build and testing pass
    - Need a review from someone - Sergey K - hoping to finish this week. Renata on vacation.
  - Rich schema work to be accepted with the Rich Schema transactions feature flagged off – complete?
    
    - Volunteer for implementing feature flag? Alex has volunteered. Plan – Alex to do plan/Evernym to arrange review call.
- To be discussed:
  
  - Ubuntu 20.04
    
    - Cam started it and got it running on Ubuntu 18.04. PRs submitted, more packages need to be assessed and updated.
    - Biggest challenge is dealing with CI / CD: we need to move to GitHub Actions first.
  - Migrate from Jenkins to GitHub Actions
  - Other work merged
  - PRs to be merged
  - CI/CD updates - next week

## Future Calls

Next call:

- Request made by [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) to discuss PR from [Indy-HIPE 0161 - Generic Token](https://github.com/hyperledger/indy-hipe/pull/160)
- CI/CD Progress
- Indy Plenum PRs

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464404/19465495.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
