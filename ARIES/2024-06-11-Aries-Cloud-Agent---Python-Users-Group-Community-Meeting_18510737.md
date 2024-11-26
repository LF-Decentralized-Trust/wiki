1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-06-11 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Sean Bohan on Jun 25, 2024

## Summary:

Topics:

- PRs and Issues
- 1.0.0 Progress
- Open Discussion

## **Recording:**

## **Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- Emiliano Sune (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Open [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) – as of writing this, none are ready to be merged
  
  - Pagination is ready for review, but needs more tests
  - DIDComm v2 needs more test
  - Rest are in "Draft", "Changes Requested" or have failing tests.
  - What is needed for 1.0.0?
- Open [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues):
  
  - Anything hot that should be addressed before 1.0.0rc0?
    
    - Perhaps: [3020](https://github.com/hyperledger/aries-cloudagent-python/issues/3020), [3018](https://github.com/hyperledger/aries-cloudagent-python/issues/3018), [3016](https://github.com/hyperledger/aries-cloudagent-python/issues/3016), [2999](https://github.com/hyperledger/aries-cloudagent-python/issues/2999), [2998](https://github.com/hyperledger/aries-cloudagent-python/issues/2998)
    - Necessary, I think: [2993](https://github.com/hyperledger/aries-cloudagent-python/issues/2993)
- Getting Consensus on this issue:
  
  - Discussion: Considering dropping BBS Signature support for now?
  - Issue: The current BBS Library does not have an Arm artifact, so we can support Mac M1 (etc.) devices natively.
    
    - Request for help in upgrading from BBS Library supplier (MattrGlobal) has not been answered.
    - Impact – almost unusable on a Mac right now.
  - Options:
    
    - Create Docker images that don't have BBS SIgnatures Signatures included, and provide guidance on install time changes needed to add it.
      
      - Kind of like a plugin – deployers must explicitly add BBS vs. expecting to be there.
      - Variation: Multiple tags – e.g. one with a different tag for "with BBS" and "without BBS".
        
        - What goes in the current tag, what goes in the version with the new tag?
    - Switch to another implementation?
      
      - Multiple, non-interoperable implementations.  It's not clear which one to switch to.
    - **\*\*THE "CORRECT" OPTION – BUT MORE WORK\*\*** Move current implementation to a plugin
      
      - Allows those using it (is there anyone?) to use the plugin.
      - This is the pattern we are moving to – removing from core.
      - Allows for other implementations in the same pattern.
    - Drop the support for now.
      
      - The "next gen" BBS signatures implementations are coming – wait for them and add back then.
  - Comments from chat:
    
    - 08:50:41     From Daniel Bluhm : I have the same question as Patrick; if it's not getting used or is pretty far out of spec, is it worth going through the effort of keeping it going?
    - 08:50:51     From Colton Wolkins : #4 drops it completely, instead of allowing it as an option (from my understanding)
    - 08:52:45     From Daniel Bluhm : Plugin-ifying would probably require the most development effort to execute
    - 08:53:07     From Daniel Bluhm : There are some hacky spots to support BBS keys that would need to be addressed
    - 08:56:43     From Daniel Bluhm : We've been able to work around it for our development focus for those on my team using M\*, though it is a frequent headache still. Just not blocking.
    - 08:57:53     From Colton Wolkins : Isn't it by running the containers in amd64 mode or something like that?
    - 08:57:54     From Emiliano Suñé : *"We've been able to work around it for our development focus for those on my team using M\*, though it is a frequent headache still. Just not blocking"*. Do you have tips/recommendations we may want to include in the docs in the meantime for this? I usually happen to switch to using arm64 right after I forgot what I did the time before to get it working...
    - 08:58:46     From Emiliano Suñé : If you are running the image you can specify the platform, but if you are developing (i.e.: devcontainer) it will complain about the architecture when installing dependencies in the first place since the proper binaries are not available
    - 09:00:07     From Colton Wolkins : I don't have a Mac, so I can't 100% vouch for this, but I'm seeing this export internally @Emiliano Suñé : export DOCKER\_DEFAULT\_PLATFORM=linux/amd64
    - 09:00:08     From Colton Wolkins : \[This is an encrypted message]
    - 09:00:14     From Daniel Bluhm : We haven't gotten into the habit of using devcontainers (yet) at least but yeah, it's that platform flag that we use, specifying linux/amd64
- Official Releases
  
  - Pradeep to put in a PR with his suggestion for LTS handling.
- AnonCreds Rust Revocation Issue in ACA-Py – status - [`Anoncreds` Revoking one credential of many of the same type fails proof](https://github.com/hyperledger/aries-cloudagent-python/issues/2934)
- Issues with revocation registry rotation
- Open Discussion

## Upcoming Meeting Topics:

## Future Topics

- Formal test plan
  
  - We go through a process of release candidates but we often still end up discovering bugs after releases are out
  - Daniel to create an issue to start a discussion

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
