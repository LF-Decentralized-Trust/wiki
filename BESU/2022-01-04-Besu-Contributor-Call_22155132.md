1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Meetings](Meetings_22153838.html)
4. [Agendas](Agendas_22153868.html)
5. [2022 Agendas](2022-Agendas_22155133.html)

# Besu : 2022-01-04 Besu Contributor Call

Created by Francesco Andreoli, last modified by Grace Hartley (Deactivated) on Jan 03, 2022

(Meeting Link: ⁨[https://consensys.zoom.us/j/94665568300](https://consensys.zoom.us/j/94665568300)[⁩]()) 

APAC/AMER Friendly Time -  0100UTC ([https://www.timeanddate.com/worldclock/converter.html?iso=20210913T010000&amp;p1=224&amp;p2=179&amp;p3=1440&amp;p4=195&amp;p5=47](https://www.timeanddate.com/worldclock/converter.html?iso=20210913T010000&p1=224&p2=179&p3=1440&p4=195&p5=47))

- 6 pm Monday Los Angeles
- 9 pm Monday New York
- 1 am  Tuesday UTC
- 3 am Tuesday Paris/Berlin
- 11 am Tuesday Brisbane

**Agenda**

- **Housekeeping**
  
  - Antitrust notice - [https://www.linuxfoundation.org/antitrust-policy/](https://www.linuxfoundation.org/antitrust-policy/)
  - This meeting is being recorded
  - Please Mute unless speaking
  - If you have a question use the raise hand feature
- **General Announcements**
  
  - outreach from finance re versioning info - [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence) has some info, and will share confidentially so we can address
- **Release updates**
  
  - Release process in general, plan for diversifying who can make a release.([Justin Florentine](https://lf-hyperledger.atlassian.net/wiki/people/712020:71871f91-9632-4415-9d78-780eb53fd275?ref=confluence) )
    
    - How many maintainers required to sign off on a release? Two maintainers are required because every commit has to have a reviewer.
  - GAR-E - what does it still need to reduce friction? - currently GAR-E is proprietary. Outside maintainers currently need to use a checklist and do it manually.
  - What role (if any) does CircleCI have in releasing?
  - Pros to tag based release:
    
    - Reduces friction, improves release time by about 50%
  - Cons: Objections to tag-based release
    
    - doesn't have immutable metadata - tags can be moved
    - one person can run a release - this should be prevented currently by branch protection
  - *Next Steps: Team to work through what is the scope of an ideal release solution and then see what solutions (tag based or otherwise) would work. Send note in RocketChat to understand who can volunteer to put this document together.*
- **Work Updates**
  
  - Static code analysis ([Justin Florentine](https://lf-hyperledger.atlassian.net/wiki/people/712020:71871f91-9632-4415-9d78-780eb53fd275?ref=confluence))
    
    - Example output here: [https://sonarcloud.io/dashboard?id=hyperledger-cicd\_besu](https://sonarcloud.io/dashboard?id=hyperledger-cicd_besu)
    - Can we get it to run for non-maintainers (uses a restricted context)
    - Can we get the coverage output combined across reference tests, acceptance tests, unit tests
  - Chat platform - Matrix/Rocketchat discussion
    
    - discussions are happening ([Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence))
  - Vert.x upgrade - complete
- **Other Business** 
  
  - Discussion re having community zoom used to ensure that meetings can be recorded
- **Open Forum**
  
  - Recap of conversations from prior two Besu contributor calls re EF incentive program
    
    - *Action Item: Share links/add links here to Incentive Program proposals so easily findable*
  - Ideas for Community Building:
    
    - Having all contributors join monthly Contributor call.
      
      - Additional item/option: Should we think about having 3 separate times a month.
      - *Next Step: Share proposed time changes in RocketChat to get feedback.*
    - Public roadmap on wiki covered in monthly contributor call needs to be up to date
    - Discord chat channel moving forward. Targeting to make a decision in January because that would bring Besu to Ethereum
    - Regular call to catch up with all Besu contributors not recorded
    - Leverage LFX analytics on Besu to review at top of contributor calls to see time to review on pull request and other metrics.
    - Next Steps: Grace to own following up on these community ideas.
  - Inactivity clause for moving maintainers to emeritus status - the [current guide](https://github.com/hyperledger/besu/blob/main/MAINTAINERS.md) says a quarter of inactivity. Do we want to extend that? 6 months? Longer? 
    
    > &gt; A general measure of inactivity will be no commits or code review comments for one reporting quarter, although this will not be strictly enforced if the maintainer expresses a reasonable intent to continue contributing.
    
    - Proposal to update two reporting quarters from emeritus or potentially consider having "quorum" with them, they don't get voting rights.
  - Future direction of Besu
    
    - some thoughts from [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence) - [Besu 2022 Vision](Besu-2022-Vision_22155167.html)
      
      - *Action: Share the document in the RocketChat for broader feedback from group. Gary to add some context around the rollups execution.*

**View recording:**

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

File [Besu 2022-01-04.transcript.vtt](attachments/22155132/22155181.vtt "Download")

Jan 03, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [Besu 2022-01-04.txt](attachments/22155132/22155183.txt "Download")

Jan 03, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
