1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Py Maintainers Meetings](ACA-Py-Maintainers-Meetings_18506202.html)

# Hyperledger Aries : 2024-09-24 Aries Cloud Agent - Python Maintainers Meeting

Created by Stephen Curran, last modified on Sep 25, 2024

## Summary:

Topics:

- PRs, Issues
- Status: OWF Submission
  
  - Handling PyPi (\`aries\_cloudagent\`) and GHCR artifacts during the transition
- did:tdw Resolver
- Progress on other initiatives

**Zoom Link**: [https://zoom.us/j/91279968714?pwd=Yk9GVVNLOFE1cklkSk51UEZQTklOQT09](https://zoom.us/j/91279968714?pwd=Yk9GVVNLOFE1cklkSk51UEZQTklOQT09)

**Call Time**: 9:00 Pacific / 18:00 Central Europe

## Recordings From the Call:

![antitrust-policy-notice.png](https://github.com/LF-Decentralized-Trust/governance/blob/845bf277e246fa2be73be260f57b645b8aa84838/tac/meeting-minutes/images/antitrust-policy-notice.png?raw=true)

![](https://raw.githubusercontent.com/LF-Decentralized-Trust/governance/717c2020287a32594adff365c898b6bfe90d630a/tac/meeting-minutes/images/all-are-welcome.png)

LF Decentralized Trust is committed to creating a safe and welcoming

community for all. For more information

please visit the [LFDT Code of Conduct](https://lf-decentralized-trust.github.io/governance/governing-documents/code-of-conduct.html).

## Welcome, Introductions and Announcements

- Heads Up: New Zoom links for this meeting and ACA-Pug when we move to OWF

## Attendees

- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)
- Plugins: [https://plugins.aca-py.org](https://plugins.aca-py.org)
- did:tdw DIF Working Group Meeting this Thursday, Sept. 26 at 9:00 Pacific / 18:00 Central Europe, Agenda/Zoom info is: [https://hackmd.io/k4cIK9vQSlaeg2pdHE51IQ](https://hackmd.io/k4cIK9vQSlaeg2pdHE51IQ)

## Agenda

- New maintainers – Thiago and Mourits - #[3239](https://github.com/hyperledger/aries-cloudagent-python/issues/3239)
- Dealing with artifacts and naming:
  
  - Any flashes of inspiration on the name? "acapy"
  - Need an immediate update to the README to begin to announce the move and process.
  - Create a "move2owf.md" file that we will maintain with guidance about the move.
  - Repo name will be "acapy", associate repos would be "acapy-..." as in "acapy-plugins" and so on.
  - What do we rename "aries\_cloudagent" to?  Suggestion is "acapy-agent".
  - Create PR to change "things", then move to OWF, create a fork at the old location (see below) then merge the PR, then clean up.
  - Can we keep publishing to PyPi "aries\_cloudagent" after we make such a change?  Can we use an alternate name for a PyPi package?
    
    - PyPi – leave deprecation messages – warning.
    - One more release from Hyperledger with the deprecation notice.
    - Then an immediate release from OpenWallet Foundation with a new package name of "acapy-agent".
  - Assuming we can get permissions, can we keep publishing to GHCR – e.g.[ghcr.io/hyperledger/aries-cloudagent-python:py3.12-1.0.0](http://ghcr.io/hyperledger/aries-cloudagent-python:py3.12-1.0.0)
    
    - For LTS – we will keep publishing to this GHCR
    - Move the repo, create a fork using the old name, update the README to send the users to the new repo, and continue to publish PyPi and GHCR releases from the fork – which will never be merged. 
      
      - No new issues on the fork.
  - Documentation – what file should we create?  Just put it at the top of the README in screaming letters?
    
    - Document that details the change – published on https://aca-py.org
    - Discord
    - Aries Mailing List
  - Any concerns about the plugins?
    
    - Redirect should take care of a lot of this – we hope.
    - Worst case documentation, and people will have to update their deployments.
  - Any other concrete things we can do?
  - Timing:
    
    - First thing is a README update and announcements.
    - Next is a final Hyperledger Aries release.
    - PRs to prepare changes
    - Move.
- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and Issues –
  
  - #[3184](https://github.com/hyperledger/aries-cloudagent-python/pull/3184) (connection protocol – and next version number and how to document?)
    
    - Immediate release of what we have as 1.0.1 – with a deprecation notice.
      
      - Could be last Hyperledger release.
    - Merge the connection protocol PR
    - Remove Issue Credential / Present Proof v1.0 and put them into a plugin (or not?)
      
      - Indicio to remove and create a plugin
      - BC Gov to test the plugin and tweak.
    - All three will go into the subsequent release – 1.1.0 either from Hyperledger or OWF as we decide.
  - #[3246](https://github.com/hyperledger/aries-cloudagent-python/pull/3246) (multikey management)
    
    - Try to finish off, review again and merge today and include in 1.0.1.
    - #3181 – creates two routes to add a proof to a JSON document.
  - [#3243](https://github.com/hyperledger/aries-cloudagent-python/issues/3243) (in-memory wallet)
- Any thoughts on #[3240](https://github.com/hyperledger/aries-cloudagent-python/issues/3240) – extending the `--seed`  to include what DID method to use with the seed?
  
  - Conceptually – a wallet import to create the right private keys in ACA-Py to enable appropriate signing.  Know the keypair/DID in advance, but want to use it in ACA-Py.
- Progress on other initiatives:
  
  - OpenID4VCs plugin - Indicio team focus
  - Other?
- Open Discussion
  
  - Urgent request to complete did:indy support (e.g., JSON-LD VCs based on did:indy DIDs) – triggering learnings about DID handling.  [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) to assemble those learnings and share as work proceeds.

## Upcoming Meeting Topics:

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
