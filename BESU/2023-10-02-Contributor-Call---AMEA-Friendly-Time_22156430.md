1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Meetings](Meetings_22153838.html)
4. [Agendas](Agendas_22153868.html)
5. [2023 Agendas](2023-Agendas_22155942.html)

# Besu : 2023-10-02 Contributor Call - AMEA Friendly Time

Created by Matt Nelson (Deactivated), last modified by Simon Dudley on Oct 09, 2023

**Agenda**

- **Housekeeping**
  
  - Antitrust notice - [https://www.linuxfoundation.org/antitrust-policy/](https://www.linuxfoundation.org/antitrust-policy/)
  - This meeting is being recorded
  - Please Mute unless speaking
  - If you have a question use the raise hand feature
- **General Announcements**
  
  - Logo Discussion - ![](https://cdn.discordapp.com/attachments/1013884740845174855/1158428053953851533/besu_logo_mockup.jpg?ex=651c35b2&is=651ae432&hm=e91390047f1c9b4c3b3b72f20d2c308a2332096a49bddf2a670215012300a26b&)
    
    - No issues among maintainers - looks fine
- **Release updates**
  
  - NOTE docs release [process change](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Documentation+release+process) for docusaurus - requires a PR (not just a github release)
  - 23.7.x series - trialling releasing from a release branch per - (RFC) [Reprise: Release Candidates from Main For Every Release](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Reprise%3A+Release+Candidates+from+Main+For+Every+Release)
    
    - (Incorporates both [Proposal: Quarterly releases from main by default](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Proposal%3A+Quarterly+releases+from+main+by+default) AND [Proposal: Avoid Cherry-Picked Releases](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Proposal%3A+Avoid+Cherry+Picked+Releases))
    - (from Simon) This did not work well for 23.7.3-RC, hopefully Gary has enough context to discuss the issues, but the main ones were:
      
      - Carrying out the release was complicated and error prone: cherry picking still needed to happen even though it was a release from main - it *could* be scripted BUT...
      - There's a manual part of the process where we have to work out from which commit to start the cherry-pick.
      - Discord thread: [https://discord.com/channels/905194001349627914/943252457063075880/1153922976736104449](https://discord.com/channels/905194001349627914/943252457063075880/1153922976736104449)
    - NOTES ON CALL:
      
      - Good:
        
        - Can merge to main
        - Good squash/commit history
        - Can easily abort release candidates that fail and does not create candidate docker images that users may pick up by accident
      - Bad:
        
        - Different SHAs for cherry picks, more fraught history
        - Need admin to disable branch protection rules for new release branches
      - Only Gary and Simon have used this release process
      - Human required process needs to identify which SHA commit we start the release from
      - Need work around automation and process itself
      - 23.10.0 -
        
        - Should take this into the automation realm → iterating on scripts for release automation
      - Fabio would like to try this process on next release
      - We will pilot this release process before making it official - perhaps in 24.1.0
  - 23.7.3-RC release update from Ameziane - [Memory usage investigations on 23.7.3-RC](Memory-usage-investigations-on-23.7.3-RC_22156403.html)
    
    - PLAN FROM CALL: 
      
      - Check with Danno RE required release timeline for Swirld's Labs
        
        - If needed within a week: cherry pick on 23.7.3 for a .4 release
        - Otherwise, include in 23.10.0 and begin burn-in on Friday after code freeze
  - Enterprise Releases proposal - [https://docs.google.com/document/d/1oeI2fq3jBYFyQHj4kHb1OemAzI1L6DRudkEtZRSYabM/](https://docs.google.com/document/d/1oeI2fq3jBYFyQHj4kHb1OemAzI1L6DRudkEtZRSYabM/)  - NOTES BELOW: 
    
    - Starting point → Release candidate is cut and socialized with ALL contributor groups
    - RCs can be tested within any organizations environment and with their own testing suite and then results are socialized
      
      - Socializing RCs for parties in the #besu-release channel
      - Normal time-bound is Friday → Wed/Thurs of the following week
      - Agreement on results can pause a release → This is probably where we need the most consensus among maintainers
    - Extension of acceptance tests for private / permissioned chains ?
    - Need to iron out what process may be used for private chains (Kaleido action item, perhaps)
    - Need to ensure we are marrying up use-case distributions work discussed previously (modularity) with an interim strategy here
    - Consider docker and kubernetes setups and other cloud environments, perhaps
  - Defaults:
    
    - Snap, Bonsai, and Archive
    - Private networks do care about these features and will need to understand what will be the impact to their networks
- **Work Updates**
  
  - Cancun
    
    - devnet 9 - already started, besu is contributing with a minor stake. encountering proposal problems still being debugged.
    - hive tests relevant to devnet 9 are all passing but 4, 1 of those is pending update from test authors.
- **Other Business**
  
  - [Proposal: Discord Server Pub/Priv Channel Split](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=22156351) - unanimous at this stage for the "besu enterprise" channel name
    
    - "besu-enterprise" as a great name for private/enterprise use-cases
    - Landed on two recommendations in Matt N's comment on the proposal above
  - [\[ACCEPTED\] DEBUG Log Improvement Proposal](22156212.html) - reminder about this one, looking for feedback. If no major objections will make it a policy and continue submitting PRs to make our current logging conform.
- **Open Forum**
  
  - /add item/
- **Future Topics**
  
  - /add item/

**Recordings**

Playlist: [https://www.youtube.com/playlist?list=PL0MZ85B\_96CHpqsKmljUK8HB98wK67RjC](https://www.youtube.com/playlist?list=PL0MZ85B_96CHpqsKmljUK8HB98wK67RjC)

Document generated by Confluence on Nov 26, 2024 13:00

[Atlassian](http://www.atlassian.com/)
