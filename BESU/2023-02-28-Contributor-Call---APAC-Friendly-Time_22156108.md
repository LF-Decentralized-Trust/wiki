1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Meetings](Meetings_22153838.html)
4. [Agendas](Agendas_22153868.html)
5. [2023 Agendas](2023-Agendas_22155942.html)

# Besu : 2023-02-28 Contributor Call - APAC Friendly Time

Created by Jason Frame, last modified by Ry Jones on Feb 28, 2023

(Meeting Link: ⁨[https://zoom.us/j/91405289771?pwd=QzA3a0ozTjVSZ0hsYzgwTm9lVDRPQT09](https://zoom.us/j/91405289771?pwd=QzA3a0ozTjVSZ0hsYzgwTm9lVDRPQT09))

APAC Friendly Time ([https://www.timeanddate.com/worldclock/converter.html?iso=20220621T010000&amp;p1=224&amp;p2=179&amp;p3=1440&amp;p4=195&amp;p5=47](https://www.timeanddate.com/worldclock/converter.html?iso=20220621T010000&p1=224&p2=179&p3=1440&p4=195&p5=47))

- 5 pm Monday Los Angeles
- 8 pm Monday New York
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
  
  - /add item/
- **Roadmap Review** 
  
  - [Besu Roadmap](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Roadmap)
- **Release updates**
  
  - [Release Rotations 2023](Release-Rotations-2023_22156045.html)
    
  - [23.1.1 proposed for March 8](https://discord.com/channels/905194001349627914/943252457063075880/1078415059493060628) - thoughts?
    
    - Ideally would include Goerli Shanghai config
    - No objections to March 8 release date
- **Work Updates**
  
  - Shanghai Epic: [https://github.com/hyperledger/besu/issues/4746](https://github.com/hyperledger/besu/issues/4746)
    
    - Ready for Sepolia and on track for mainnet
  - Work started on **EIP-6110: in-protocol deposits** by external contributor [https://github.com/hyperledger/besu/pull/5055](https://github.com/hyperledger/besu/pull/5055)
    
    - Appears to be done as part of the Ethereum Protocol Fellowship by Mikhail's mentee: [https://hackmd.io/@doPpmyH4Ta-4Yc8pq3u-ZA/BkQKSAn2s](https://hackmd.io/@doPpmyH4Ta-4Yc8pq3u-ZA/BkQKSAn2s)
    - Any reason not to include this on main using ExperimentEipsTime as a feature toggle?
      
      - Have further discussion on contributor discord
- **Other Business**
  
  - merge queue - any objections to enabling this?
    
    - the only change to how we currently work is you would have to manually squash commits on your branch PR rather than via the github UI - eg [https://stackoverflow.com/questions/25356810/git-how-to-squash-all-commits-on-branch](https://stackoverflow.com/questions/25356810/git-how-to-squash-all-commits-on-branch)
    - Sally has tested it out on a couple of repos - notes here [https://github.com/hyperledger/besu/issues/5102](https://github.com/hyperledger/besu/issues/5102) - I haven't come across any showstoppers
    - it's essentially the same as enabling auto-merge, except that any additional "merge from main" actions are automated
    - should reduce our CI spend, as well as reducing manual interventions
    - Outcome: No objections. Sally to enable it after the next release with notes on squash merge instructions
  - Final call to remove #besu-nodes Discord channel.
    
    - Previously mentioned [2022-12-06 Contributor Call - APAC Friendly Time](2022-12-06-Contributor-Call---APAC-Friendly-Time_22155940.html)
    - Discussion: [https://discord.com/channels/905194001349627914/905205502940696607/1044723284597559298](https://discord.com/channels/905194001349627914/905205502940696607/1044723284597559298)
      
      [https://discord.com/channels/905194001349627914/905205502940696607/1044756214669643856](https://discord.com/channels/905194001349627914/905205502940696607/1044756214669643856)
    - One way would be give a couple of days deprecation and ask users with outstanding questions to move them over to #besu
    - Outcome: Simon to ping Danno on concerns re: besu-nodes channel deprecation. No other objections. If objections are resolved then remove the channel.
- **Open Forum**
- **Future Topics**

**Recordings**

[**https://youtu.be/5Ek\_B-e-OAU**](https://youtu.be/5Ek_B-e-OAU)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20230228-010007\_RecordingnewChat.txt](attachments/22156108/22156119.txt "Download")

Feb 28, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

File [GMT20230228-010007\_Recording.transcript.vtt](attachments/22156108/22156120.vtt "Download")

Feb 28, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
