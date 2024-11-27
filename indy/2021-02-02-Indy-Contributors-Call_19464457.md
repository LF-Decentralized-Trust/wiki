1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2021 Meeting Notes](2021-Meeting-Notes_19465630.html)

# Hyperledger Indy : 2021-02-02 Indy Contributors Call

Created by Richard Esplin, last modified by Stephen Curran on Feb 02, 2021

## Summary

Planned:

- Status of indy-node CI/CD and Ubuntu upgrade
- Status of upcoming indy-sdk release and follow up issues
- Hyperledger help toward adding contributors
- HIPEs for plugin helpers

## Recording from the call: [20210202 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) (Scoir) &lt;kg@scoir.com&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Evernym) &lt;richard.esplin@evernym.com&gt;
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence) (Laniakea Health) &lt;alex@seropass.me&gt;
- [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) (DB Systel GmbH) &lt;robin.klemens@deutschebahn.com&gt;
- [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) (Hyperledger) &lt;rjones@linuxfoundation.org&gt;
- [David Boswell](https://lf-hyperledger.atlassian.net/wiki/people/70121:0a14f738-3039-421f-a6a9-a83d19f23227?ref=confluence) (Hyperledger)
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Ryan Marsh](https://lf-hyperledger.atlassian.net/wiki/people/557058:45ceb1ce-c3dd-4f33-9fef-f7aade227711?ref=confluence)(Evernym) &lt;ryan.marsh@evernym.com&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence)
    
    - Indy Node CI - [https://github.com/hyperledger/indy-node/pull/1622](https://github.com/hyperledger/indy-node/pull/1622) (Awaiting review) [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) 
      
      - DONE w00t! Alex K to review (Monday), Renata (perhaps earlier) and Sergey looked at it.
      - Does not remove Jenkins still required – just adds GHA as optional – move to swapping those
      - Broad consensus that we should accept the PRs, and improve them over time instead of waiting for thorough review.
    - Indy Plenum CI - [https://github.com/hyperledger/indy-plenum/pull/1505](https://github.com/hyperledger/indy-plenum/pull/1505) (WIP) [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) Wrapping up, almost DONE - confident
      
      - Similarly happy to accept PRs quickly.
    - Indy Plenum CD - [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) - First pass done, clean up in process
    - Indy Node CD - need clarification around rocket chat comments
      
      - Which system tests are the right ones? "Just run PyTest" says Alex
      - How to run system tests?
      - Should we remove since deprecated tests and scripts?
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) (help from [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) / [Ryan Marsh](https://lf-hyperledger.atlassian.net/wiki/people/557058:45ceb1ce-c3dd-4f33-9fef-f7aade227711?ref=confluence) )
    
    - Work needed
      
      - Python 3.8 upgrade
      - Reviewing pinned dependencies
      - Indy SDK upgrade?
    - Create a branch for collaborating, then a single PR to merge to Master / Main
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
    
    - Documenting plan (HIPE?)
    - Merging Stable to Master
    - Rename Master to Main
    - Releasing what is currently in Master
    - Evernym can help merge and test.
- Indy SDK
  
  - Next release in progress, led by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
    
    - Proposal: Ready to release? Yes
      
      - Standard testing done
      - Tested with all BC Gov apps
      - Question: Issue with account to PyPi?  Has that been resolved?
        
        - Hyperledger has ownership of the accounts, with secrets in GitHub repo, but need to check that it is still possible to publish from Jenkins
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - donated to Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa

## Meeting Topics

- Status of Indy Node (et. al) CI/CD and Ubuntu upgrade
  
  - Sovrin needs:
    
    - Next release should be 16.04 only, and (more or less) exactly as currently in production so we can verify the CI/CD process by a doing "a few nodes at a time" upgrade.
    - The Ubuntu upgrade must interoperate with the then-current 16.04 release, so that we can organize the "one node at a time" Steward OS upgrades.
    - Richard: Could be cheaper to do more QA on fewer releases.
- Hyperledger support for finding new contributors
  
  - [Contribution Campaigns](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns)
  - Hyperledger could plan a developer recruitment marketing campaign for some point this year.
    
    - Example: [Blockchain Automation Framework lab](https://lf-hyperledger.atlassian.net/wiki/spaces/labs/pages/20283434/Blockchain+Automation+Framework+lab)
    - [https://lfanalytics.io/projects/hyperledger%2Findy/dashboard](https://lfanalytics.io/projects/hyperledger%2Findy/dashboard)
    - Good project would be new Indy DID method
- HIPEs for helpers to remove plugins: [PR 162](https://github.com/hyperledger/indy-hipe/pull/162)
  
  - Freeze ledgers
  - Fees in Indy

## Future Calls

Next call:

- HIPEs for helpers to remove plugins: [PR 162](https://github.com/hyperledger/indy-hipe/pull/162)
  
  - Freeze ledgers
  - Fees in Indy
- New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  
  - Documenting plan (HIPE?)
  - Merging Stable to Master
  - Rename Master to Main
  - Releasing what is currently in Master
  - Evernym can help merge and test.

Future:

- Status of Indy-SDK release
  
  - Statement on the future of the Indy SDK: [PR 2329](https://github.com/hyperledger/indy-sdk/pull/2329)
  - Plans for future of Indy CLI (move to Indy VDR?)
  - Indy SDK in test for Indy Node (move to Indy VDR?)
  - Status of GitHub Actions for the Indy-SDK
- Indy bugs
  
  - Using GitHub tags "Good First Issue" and "Help Wanted"
  - [Node 1490](https://github.com/hyperledger/indy-plenum/issues/1490): problems with large catch-up
  - [Plenum 1506](https://github.com/hyperledger/indy-plenum/issues/1506): view change message consensus calculation error
- Hyperledger campaign to recruit additional developers.

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464457/19465697.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
