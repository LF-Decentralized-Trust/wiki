1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2022 Meetings: AnonCreds Working Group](20295016.html)

# Hyperledger AnonCreds : 2022-11-07 AnonCreds Rust Working Group Meeting

Created by Stephen Curran, last modified on Nov 07, 2022

## Summary

- Ledger Agnostic AnonCreds [Project Plan](https://github.com/orgs/hyperledger/projects/16)
  
  - Who is doing what?
- Backwards compatibility testing
- Maintainers List
- Future Meetings Schedule
- Open Discussion

Recording of Call: [dummyfile.txt](#)

## Notices:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Timo Glastra) &lt;timo@animo.id&gt;

[Victor Martinez](https://lf-hyperledger.atlassian.net/wiki/people/557058:73fff461-39df-4cc9-85d1-7b8a65773bee?ref=confluence) (Víctor Martínez) &lt;victor.martinez@sicpa.com&gt;

[Darko Kulic](https://lf-hyperledger.atlassian.net/wiki/people/712020:9f029ed1-ec22-4d0e-9393-683c31a4fa36?ref=confluence) (Darko Kulic) &lt;darko.kulic@sicpa.com&gt;

[Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

## AnonCreds Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - IIW -- Nov 15-17, Mountain View, Calif.
    
    - Suggestions for what to do at IIW
- Updates to the Agenda

## Agenda

- Ledger Agnostic AnonCreds [Project Plan](https://github.com/orgs/hyperledger/projects/16)
  
  - Discussed, add a couple of things. Some items were claimed.
- Backwards compatibility testing
  
  - Tasks created and taken by Timo to look at ACA-Py and AFJ and the effort to bring in the anoncreds-rs artifacts such that we can start to use them.
  - Agreed that all peer-to-peer interactions/data structures should look the same, with the exception of the format of the IDs in the objects
  - We need to have an AnonCreds Methods registrar/resolver interface in the ACA-Py and AFJ codebases, similar to where we are with DIDs.
    
    - This is to enable the ledger-specific calls based on what the Aries Framework is configured to do for writing, or the resolution of AnonCreds IDs received.
  - For integration testing in Aries Frameworks and AATH: we'll wait until we're further along in producing artifacts before we move into integration testing.
  - Unit tests:
    
    - Keep building them (of course!)
    - There are many commented out tests – mostly because the Indy-SDK had access to an indy-wallet, and many of the tests assume that. We should add an in-memory wallet instance to enable activating those tests.
    - Task added to "uncomment" as many tests as possible and that make sense has been added.
- Maintainers List
  
  - Reviewed and for now we are happy with the list. The process is in place for
- Future Meetings Schedule
  
  - Decision not to set a weekly/biweekly call. Instead, we'll go async first (Github, Discord), but strongly encourage Devs/Maintainers to call a meeting to address when async will taking too long.
  - Always an option to have a discussion during or immediately after an AnonCreds spec meeting (Monday 7:00 Pacific / 16:00 Central Europe)
- Wrappers:
  
  - Would be nice to have generated wrappers if they are of sufficient quality and consistent with the Rust model (which may not be possible). Stephen to talk to [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence)about what generated wrappers would be like to see if the rest of the Devs are supportive.
  - Keep wrappers in the repo or have them as a separate repo?
    
    - Argument to keep them in – we can make them a GHAction test to be working before merges – more likely to keep them up to date – and we can produce release artifacts in-sync with tags.
    - Argument to move them out – unmaintained wrappers become a burden and they make releasing features harder. Having them in a separate repo can make them easier to update (although that should really not be the case as long as we have active, engaged maintainers).
    - Proposal:
      
      - Keep core, active wrappers in, with GHA tests and artifact generation/publishing.
      - Keep existing, but non-core (no active maintainers) in separate repos
      - Have a process for moving a wrapper out of the main repo, and for moving a repo into the main repo.
        
        - Mostly tied around the number of active devs contributing to the wrappers and the roadblocks for releases because of slow wrapper maintainers
- Open Discussion

## Future Calls

## To Dos:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/20291570/20295036.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
