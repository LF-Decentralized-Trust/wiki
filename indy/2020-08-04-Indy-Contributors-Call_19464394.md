1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-08-04 Indy Contributors Call

Created by Richard Esplin, last modified by Stephen Curran on Aug 04, 2020

## Summary

Planned:

- Plans for next Indy Node release
- Contributions needed on Indy Node
- Preparations/pre-work for the Indy Interop-athon

## The call recording is available here: [20200804 Indy Contributors Call](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- Identity Implementer Working Group call ([Wiki Page](https://lf-hyperledger.atlassian.net/wiki/display/IWG/Identity+WG+Implementers+Call)) - every 2nd Thursday
- Join Us: Indy Interop-athon Virtual Conference - Sept. 1, 2 - [Indy Interop-a-thon - Making "Network of Networks" Real](https://lf-hyperledger.atlassian.net/wiki/spaces/II/overview)

## Release Status and Work Updates

- Indy Node
  
  - Timing TBD:
- Indy SDK
  
  - Significant changes in LibVCX
  - Team at ABSA is considering a different architecture
    
    [https://github.com/AbsaOSS/libvcx/commits/master](https://github.com/AbsaOSS/libvcx/commits/master)
  - Release Timing TBD
- Indy Monitoring - [https://github.com/bcgov/indy-node-monitor](https://github.com/bcgov/indy-node-monitor)
  
  - Improvements to the JSON output
    
    - Anonymous mode (no node\_monitor DID needed)
    - Error/Warning Summary section added
      
      - Not accessible (either mode)
      - Unreachable Nodes warning
      - Freshness check
    - Remove docker info from output - pure JSON from ./run.sh script
- Indy/Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
    - aries-credx
    - Aries Secure Storage initiatives:
      
      - Working on some low-level rust crates necessary for supporting Storage
  - Ursa
    
    - BBS+, Revocation work 2.0 work
    - Current Release: 0.3.4 is ready.

## Meeting Topics

- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) Who is going to lead releasing Indy Node? We have a backlog of fixes that need to go out.
  
  - Especially: [https://github.com/hyperledger/indy-node/security/advisories/GHSA-wh2w-39f4-rpv2](https://github.com/hyperledger/indy-node/security/advisories/GHSA-wh2w-39f4-rpv2) (needed by end of August)
    
    [https://github.com/hyperledger/indy-node/pull/1604](https://github.com/hyperledger/indy-node/pull/1604)
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) Other "easy" Indy Node contributions needed
  
  - Sovrin Jenkins isn’t public due previous security problems, need to move to GitHub Actions
    
    [https://github.com/hyperledger/indy-node/pull/1605/](https://github.com/hyperledger/indy-node/pull/1605/)
  - Ledger bugs
    
    - ledger crash if more than F nodes are out-of-consensus:
      
      [https://github.com/hyperledger/indy-plenum/issues/1488](https://github.com/hyperledger/indy-plenum/issues/1488)
    - new node can take other nodes out of consensus:
      
      [https://sovrin.atlassian.net/browse/SN-18](https://sovrin.atlassian.net/browse/SN-18)
  - PRs that need small fixes to be accepted.
    
    [https://github.com/hyperledger/indy-node/pull/865](https://github.com/hyperledger/indy-node/pull/865)
    
    [https://github.com/hyperledger/indy-node/pull/948](https://github.com/hyperledger/indy-node/pull/948)
    
    [https://github.com/hyperledger/indy-node/pull/1409](https://github.com/hyperledger/indy-node/pull/1409)
  - Update to Ubuntu 20.04
    
    [https://jira.hyperledger.org/browse/INDY-2186](https://jira.hyperledger.org/browse/INDY-2186)
    
    [https://github.com/hyperledger/indy-node/pull/1443](https://github.com/hyperledger/indy-node/pull/1443)
    
    [https://github.com/hyperledger/indy-plenum/pull/1332](https://github.com/hyperledger/indy-plenum/pull/1332)
- Preparation for the initial topics at the Indy Interop-athon - [Indy Interop-athon - Making "Network of Networks" Real](https://lf-hyperledger.atlassian.net/wiki/spaces/II/overview)
  
  - Current support for Fully Qualified DIDs in Indy SDK: [https://github.com/hyperledger/indy-sdk/blob/master/CHANGELOG.md#1120---2019-10-08](https://github.com/hyperledger/indy-sdk/blob/master/CHANGELOG.md#1120---2019-10-08)

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464394/19465451.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
