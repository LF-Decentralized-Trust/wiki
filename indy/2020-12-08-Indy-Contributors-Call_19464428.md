1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-12-08 Indy Contributors Call

Created by Stephen Curran, last modified on Dec 08, 2020

## Summary

Planned:

- Status of Ubuntu 20.04 18.04 work
- Status of upcoming indy-node release, Rich Schema Feature Flag, and CI/CD Progress
- Status of upcoming indy-sdk release

## Recording from the call: [20201208 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Evernym) &lt;richard.esplin@evernym.com&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio.tech) &lt;lynn@indicio.tech&gt;
- [Michael Bailey](https://lf-hyperledger.atlassian.net/wiki/people/557058:62efa9cf-9c50-4bef-a369-9e771c734f9f?ref=confluence) (Paramount Software) &lt;mbailey@paramountsoft.net&gt;
- [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) (Scoir) &lt;kgriffin@scoir.com&gt;

## Related Calls and Announcements

- TBD

## Release Status and Work Updates

- Indy Node
  
  - Next release in progress, led by this team
  - Ubuntu 20.04 18.04
- Indy SDK
  
  - Next release in progress, led by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries
- Ursa
- Evernym's next items (won't be adopting shared libraries, will probably maintain LibIndy as a fork outside of Hyperledger)
  
  1. Current releases of Indy Node and Indy SDK
  2. Remove the Sovrin Token from Sovrin MainNet.

## Meeting Topics

- Meeting schedule over Christmas and New Years? (Dec 22 and Jan 5)
  
  - Will continue with the meetings.
- Ubuntu 20.04 18.04 for Indy Node / Indy Plenum
  
  - PRs for Plenum and Node for 18.04 ready to be merged and tested
  - Confirmation on this approach? **Yes** - no objection
    
    - If we continue with Jenkins for CI/CD, we need to copy and run two versions of the pipeline one for 16.04 and 18.04
    - However, no one knows how to do this is – we're stuck.
  - **Decision**: Time to ditch Jenkins and move to GitHub Actions once and for all. It would be nice to run both, but the risk of not being able to move forward at all is a bigger concern.
    
    - New team led by Wade, Kevin and Steve McCowan will work on getting this done, with questions to the Evernym team.
    - Not discussed, but ideally, in the process of this we:
      
      - Get rid of the split plenum/node pipelines, and
      - We eliminate the use of Master, Stable and RC branches, going to just Master (Main) and PR branches in the common case; feature and fix branches if and when needed.
  - Indy Plenum PR Review - the consensus code - Any updates to status?
    
    - Brent's fix for INDY-827 (PR 1486)  - not to be merged into main until reviewed and tested by another
      
      - Decision: Will not be merged into this release because of the manual testing effort.
    - Need to accept PR 1482 - Evernym can do that.
    - What is the difference between STABLE and MASTER
      
      - Stephen to review the last call recording - couldn't find anything on the recording – still not understood.
- Request for indy-sdk release
  
  - RC branch ready to go, release notes updated, everything is almost ready to go
  - IOS 64-bit only, 32 bit being dropped
  - Jenkins pipeline for Windows is not working – locked out of the infrastructure
    
    - Wade working on cloning the VM and wire it back up - risk is that the VM has been manually updated over time, but not clear
    - The VM is a Jenkins master controlling the ledgers for testing.
  - One commit in Master Branch is not DCO signed - RESOLVED - force push into Master
  - Mac issue – 32 bit support is being dropped, 64 bit will continue to be supported
  - Rust issue – need to consider when to switch to newer version.
- Richard to put in a PR to say that indy-sdk is deprecated – discussion to follow.

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464428/19465602.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
