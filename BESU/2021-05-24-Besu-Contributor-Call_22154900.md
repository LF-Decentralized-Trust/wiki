1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Meetings](Meetings_22153838.html)
4. [Agendas](Agendas_22153868.html)
5. [2021 Agendas](2021-Agendas_22154808.html)

# Besu : 2021-05-24 Besu Contributor Call

Created by Matthew Wright, last modified on May 24, 2021

(Meeting Link: ⁨[https://consensys.zoom.us/j/94665568300](https://consensys.zoom.us/j/94665568300)[⁩]()) 

APAC/AMER Friendly Time -  0100UTC ([https://www.timeanddate.com/worldclock/converter.html?iso=20201013T010000&amp;p1=224&amp;p2=179&amp;p3=1440&amp;p4=195&amp;p5=47](https://www.timeanddate.com/worldclock/converter.html?iso=20201013T010000&p1=224&p2=179&p3=1440&p4=195&p5=47))

- 6 pm Monday Los Angeles
- 9 pm Monday New York
- 1 am  Tuesday UTC
- 3 am Tuesday Paris/Berlin
- 11 am Tuesday Brisbane

**Agenda**

- Housekeeping
  
  - Antitrust notice - [https://www.linuxfoundation.org/antitrust-policy/](https://www.linuxfoundation.org/antitrust-policy/)
  - This meeting is being recorded
  - Please Mute unless speaking
  - If you have a question use the raise hand feature
- General Announcements
  
  - A few contributors and maintainers from ConsenSys will be at the global forum
  - Grace is facilitating panel on use-cases on Besu, Lucas is hosting Besu demo
  - Danno presenting Bonzai demo, Goerli demo, Ethereum layer 2 related to Hyperledger
  - Hyperledger Besu certification survey results are in!
  - Working on Rocketchat bridge to ConsenSys Discord
  - Working on global Meetups to cross-promote on Hyperledger &lt;&gt; BUIDL network
- Release updates
  
  - New Release: Besu 21.1.6 
    
    - [https://github.com/hyperledger/besu/releases/tag/21.1.6](https://github.com/hyperledger/besu/releases/tag/21.1.6)
- Work Updates
  
  - Non-technical contributors to become maintainers
    
    - Restrictions for maintainers that are non-technical can be recognized
    - Vijay and Sajida have been added as maintainers based on their product leadership
    - We should do a poll in Rocketchat for: (1) what is stopping you from contributing to Besu (2) why are you deterred from contributing to Besu?
    - Could we incentivize contributors to create more tutorials in a repo for the community? We have quorum-quickstart-dev, but could there be more developer tools for demonstrating privacy/permissioning upon deployment (we need more contributors!)
  - Experimental Bonsai trie benchmark results
    
    - Karim update: Took over Bonsai work since Danno left
    - Since March 20, we had two mainnet nodes syncing
    - 1TB vs .5 TB without Bonsi trie improvements
    - Force node without pruning - 12TB
    - 50% improvement in storage usage with bonsai enhancements
  - Post Rayonism update
    
    - Rayonism went well!
    - Besu as an execution client was the most stable execution client; top performer!
    - On Nocturne testnet, we did some things with type transactions, but had very little to do
    - We integrated with Teku/Prysm/Lighthouse (couldn't get Nimbus up in time)
    - Had really good results with all four on the second trial
    - Working on getting Besu broader adoption as an execution environment; de facto execution engine for Teku
    - Antoine to assist Gary with Rayonism work (consult)
    - Next -&gt; 
      
      - No new testnet
      - Withdrawal and partial withdrawal work
      - ETH1 hardfork will need to happen for next steps
  - ETC
    
    - Magneto hard fork
    - Antoine is close with ETC and working on mining improvements using Besu 
      
      - Besu support for pool methods (reject list, blacklist IPs), more open issues in Github
    - Besu is an ideal client for ETC miners but requires some improvements/ fixed issues
  - 1559 update
    
    - Getting close - London configs are in testnets
    - Doing work with Dimitry and Ari on reference tests
    - Besu is only ETH1 client that does RPC tests right now
    - Transaction pool modification code is getting difficult to follow
    - Refactoring code so we can optimize
    - Karim is working on late breaking update
    - Code freeze right now
    - Getting everything under the wire for first testnet release June 2nd
    - All things aside: great shape!
- Other Business 
  
  - Technical Steering Committee 
    
    - New mandate: Must transition off Master branch to Main branch
    - Deadline: End of Q2
    - Chupacabra is working on this issue
    - Consider removing other barriers for contributors
      
      - [https://www.hyperledger.org/blog/2021/01/26/removing-barriers-to-contribution-with-inclusive-language](https://www.hyperledger.org/blog/2021/01/26/removing-barriers-to-contribution-with-inclusive-language)
  - Project Management
    
    - Currently on Open CI
      
      - Issues:
        
        - PRs from external contributors is difficult
    - Github actions is new target from Hyperledger/ Linux Foundation
- Open Forum
- Future Topics
  
  - Next Besu quarterly report to TSC is scheduled for June 24th

**\*\*Recording will be added here after the call**

[https://consensys.zoom.us/rec/share/Udlzjm7VAPAqTNsQ-IhHQtFXEYmeFYcPYQ6LAc-fYyinOUS2XOUlgwj-AwjxeNmG.KuZ3yfTA9MBY52rn](https://consensys.zoom.us/rec/share/Udlzjm7VAPAqTNsQ-IhHQtFXEYmeFYcPYQ6LAc-fYyinOUS2XOUlgwj-AwjxeNmG.KuZ3yfTA9MBY52rn) 

Passcode: 4p6^Vd=n

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
