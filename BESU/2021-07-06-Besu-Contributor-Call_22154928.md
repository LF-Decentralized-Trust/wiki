1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Meetings](Meetings_22153838.html)
4. [Agendas](Agendas_22153868.html)
5. [2021 Agendas](2021-Agendas_22154808.html)

# Besu : 2021-07-06 Besu Contributor Call

Created by Matthew Wright, last modified on Jul 08, 2021

(Meeting Link: ⁨[https://consensys.zoom.us/j/95691099798](https://www.google.com/url?q=https%3A%2F%2Fconsensys.zoom.us%2Fj%2F95691099798&sa=D&source=calendar&ust=1621094747216000&usg=AOvVaw0DzE1ZLz6VqnubaLGDkBoj))

EMEA/AMER Friendly Time -  1500 UTC ([https://www.timeanddate.com/worldclock/converter.html?iso=20201012T150000&amp;p1=224&amp;p2=179&amp;p3=1440&amp;p4=195&amp;p5=47](https://www.timeanddate.com/worldclock/converter.html?iso=20201012T150000&p1=224&p2=179&p3=1440&p4=195&p5=47))

- 8 AM Tuesday San Francisco
- 11 AM Tuesday New York
- 3 PM Tuesday UTC
- 5 PM Tuesday Paris/Berlin
- 1 AM Tuesday Brisbane

**Agenda**

- **Housekeeping**
  
  - Antitrust notice - [https://www.linuxfoundation.org/antitrust-policy/](https://www.linuxfoundation.org/antitrust-policy/)
  - This meeting is being recorded
  - Please Mute unless speaking
  - If you have a question use the raise hand feature
- **General Announcements**
- **Release updates**
  
  - **London PR with Mainnet block # on ETH1 Specs Repo (Rai)** 
    
    - Waiting to get merged - then we will have what we need to release with mainnet block # for London
    - We could be releasing Besu 21.7.0 (July 7th, 2021) if all goes well with the block number proposed to the eth1-specs repo
  - **Ropsten consensus issue release also needs to be merged in (Rai)**
    
    - Rai - Issue: When base fee was low, we weren't calculating delta properly
    - Justin - It's a trivial fix
  - **Clients are aiming to have releases with mainnet block number before [allcoredevs](https://github.com/ethereum/pm) this Friday (Rai)**
- **Work Updates**
  
  - **ETH 66 (Rai - WIP)**
    
    - [https://github.com/hyperledger/besu/issues/2210](https://github.com/hyperledger/besu/issues/2210)
  - **Issue for Bonsai (Rai)**
    
    - [https://github.com/hyperledger/besu/pull/2492](https://github.com/hyperledger/besu/pull/2492)
  - **Improvements to transaction pool (Justin)**
    
    - Expected to make it into the release (Besu 21.7.0)
    - [https://github.com/hyperledger/besu/pull/2505](https://github.com/hyperledger/besu/pull/2505)
  - **Ping pong serialization issue** 
    
    - Transaction pool changes
    - If you flood the transaction pool
    - Increasing the size of the transaction pool, so the maximum allowable dev p2p message as 10mb - increasing the size of the pool, to prevent malicious transactions
    - Transaction mempool has been low in memory and isn't affected too much
    - Might make it into release besu 21.7.0
  - **External to maintainers of Besu are interested in contributing to state expiry using Besu**
  - **Working on getting Besu snaps ready** 
    
    - Work on code hashes
- **Other Business** 
  
  - **Want to contribute? Here are some resources!** 
    
    - [**Start Here**](Start-Here_22154335.html)
    - **Good First [Issues](Issues_22154243.html)**
    - **[Start a convo with us](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Rocket+Chat) on Rocketchat**
    - [**Technical Roadmap (where to support)**](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Roadmap)
- **Open Forum**
- **Future Topics**
  
  - London to fork August 5th - to discuss on next AMER/ APAC contributor cal

**\*\*Recording will be added here after the call**

[https://consensys.zoom.us/rec/share/euHSlQ2VkMQO6vI7DLb\_JnEM1hpmGHLORAtYjSB5C1KmSYb-m3Y-y5WObhKp2CWA.cpbm7M6p8iBjhwi9](https://consensys.zoom.us/rec/share/euHSlQ2VkMQO6vI7DLb_JnEM1hpmGHLORAtYjSB5C1KmSYb-m3Y-y5WObhKp2CWA.cpbm7M6p8iBjhwi9) 

Passcode: y5#9RmEC

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
