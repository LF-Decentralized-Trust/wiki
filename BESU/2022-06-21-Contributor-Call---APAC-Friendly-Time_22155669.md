1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Meetings](Meetings_22153838.html)
4. [Agendas](Agendas_22153868.html)
5. [2022 Agendas](2022-Agendas_22155133.html)

# Besu : 2022-06-21 Contributor Call - APAC Friendly Time

Created by Helen George, last modified by Ry Jones on Jul 14, 2022

(Meeting Link: ⁨[https://zoom.us/j/91405289771?pwd=QzA3a0ozTjVSZ0hsYzgwTm9lVDRPQT09](https://zoom.us/j/91405289771?pwd=QzA3a0ozTjVSZ0hsYzgwTm9lVDRPQT09))

APAC Friendly Time ([https://www.timeanddate.com/worldclock/converter.html?iso=20220621T010000&amp;p1=224&amp;p2=179&amp;p3=1440&amp;p4=195&amp;p5=47](https://www.timeanddate.com/worldclock/converter.html?iso=20220621T010000&p1=224&p2=179&p3=1440&p4=195&p5=47))

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
  
  - /Add item/
- **Roadmap Review -** [Besu Roadmap](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Roadmap)
- **Release updates**
  
  - 22.4.3 complete [https://github.com/hyperledger/besu/releases/tag/22.4.3](https://github.com/hyperledger/besu/releases/tag/22.4.3)
  - Next planned release is 22.7.0-RC1 scheduled for 29 June (Danno) [Release Rotations 2022](Release-Rotations-2022_22155268.html)
    
    - Should we release off main branch - discussion to happen on discord
- **Work Updates**
  
  - Code Audit starting 24 June
    
    - Primary focus is the engine APIs for Eth Merge
    - Nothing for you to do unless directly asked
  - Java 17 Migration
    
    - Status: Yellow
      
      - Possibly move to 22.10.0 release
    - All issues are mostly Build/CircleCI/testing related, not code related.
      
      - LGTM only supports up to Java 14 - [https://lgtm.com/help/lgtm/java-extraction](https://lgtm.com/help/lgtm/java-extraction)
        
        - CodeQL looks to be a successor project
      - CodeQL is having module issues (probably fixable)
      - latest JDK docker image is not Java 18, and upgrading to Java 18 requires new LTS of ubunutu, which is not signed yet
        
        - We could drop the "latest" variant.  It doesn't auto update and it is out of date.
      - testWindows is using he wrong JDK
      - TLSContextFactoryTest doesn't have the proper TLS libraries
        
        - Same with AcceptanceTests and org.hyperledger.besu.tests.acceptance.bft.pki.PkiQbftAcceptanceTest
- **Other Business**
  
  - Maintainers to update mainnet activity. Details to be shared on discord.
- **Metrics Review -** [Linux Foundation Project Besu Insights](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard;quicktime=time_filter_3Y)
- **Open Forum**
  
  - GitHub issue discussion started from [Nicolas Massart](https://lf-hyperledger.atlassian.net/wiki/people/70121:5502de36-6082-4606-81f5-4fd4f51016ab?ref=confluence)
    
    - [writing a quick proposal](Make-Besu-questions-easy-to-find-and-answer_22155653.html)
    - Post reminder on discord
- **Future Topics**
  
  - /Add item/

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20220621-010324\_Recording.txt](attachments/22155669/22155727.txt "Download")

Jul 14, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

File [GMT20220621-010324\_Recording.transcript.vtt](attachments/22155669/22155730.vtt "Download")

Jul 14, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true&isFromPageView=true)

File [GMT20220621-010003\_Recording.transcript.vtt](attachments/22155669/22155731.vtt "Download")

Jul 14, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description

[Download All](/wiki/download/all_attachments?pageId=22155669 "Download all the latest versions of attachments on this page as single zip file.")

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20220621-010324\_Recording.txt](attachments/22155669/22155727.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22156991.txt) (video/mp4)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22156953.txt) (audio/mp4)  
![](images/icons/bullet_blue.gif) [GMT20220621-010324\_Recording.transcript.vtt](attachments/22155669/22155730.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [GMT20220621-010003\_Recording.transcript.vtt](attachments/22155669/22155731.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22156952.txt) (audio/mp4)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22156990.txt) (video/mp4)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22155732.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22155729.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22155733.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/22155669/22155728.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 13:00

[Atlassian](http://www.atlassian.com/)
