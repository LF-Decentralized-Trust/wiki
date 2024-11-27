1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)
4. [Accounting &amp; Certification WG Peer Programming Call](19006574.html)
5. [2021 Peer Programming Call Notes Archive](2021-Peer-Programming-Call-Notes-Archive_19006679.html)

# Climate Action SIG : 2021-04-26 Peer Programming Call

Created by Robin Klemens, last modified by Si Chen on Apr 26, 2021

**Planned**:

- Consumer Disclosures WG and DAO
  
  - We'll talk about implementing the Consumer Disclosures WG's sustainability scoring (see presentation on the [wiki page](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Consumer+Disclosure+WG)) and the governance of the [DAO](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/DAO+Project).
- Identity Solutions
  
  - How to implement an identity solution for the blockchain accounting applications using Hyperledger Indy, Aries, and TrustID.  We have an approved mentorship for [integrating TrustID,](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Implement+Client+Side+Security+for+Climate+SIG+Fabric+Application) Kamlesh has also gotten one approved for [integrating Fabric and Aries](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Hyperledger+Fabric+-+Hyperledger+Aries+Integration+to+support+Fabric+as+Blockchain+ledger), and Robin has been doing a lot of work with Indy lately -- so this should be a very good discussion.
  - Good resources to get started with the tools and frameworks of Hyperledger for Self Sovereign Identity (SSI) solutions
    
    - A curated list of self-sovereign identity resources - [https://github.com/animo/awesome-self-sovereign-identity](https://github.com/animo/awesome-self-sovereign-identity)
    - High-level process flow with a mobile app: (6min) [https://www.youtube.com/watch?v=bZrWAsD42-I](https://www.youtube.com/watch?v=bZrWAsD42-I)
    - Hyperledger Indy and Plenum. Plenum is the consensus protocol used in Indy: (33min) [https://www.youtube.com/watch?v=bZrWAsD42-I](https://www.youtube.com/watch?v=bZrWAsD42-I)
    - Hyperledger Indy, Aries, and Ursa in the TOIP stack: (65min) [https://www.youtube.com/watch?v=FfuhlF9ZYPM](https://www.youtube.com/watch?v=FfuhlF9ZYPM)
    - Hyperledger Aries Cloudagent Python - architectural deep dive: (81min) [https://www.youtube.com/watch?v=FXTQEtB4fto](https://www.youtube.com/watch?v=FXTQEtB4fto)

**Summary:**

We went through the [DAO](DAO_19007052.html) voting scheme and discussed how to implement it with the Consumer Disclosure WG's sustainability scoring.  [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence) helped make a couple of important improvements to prevent vote gaming: the maker of a proposal can only stake a fixed number of voting tokens on the proposal; there is a limited (4 hour window) for canceling and withdrawing your vote, and there is a fee for it; and makers of successful proposals get a 50% bonus to encourage them to make more helpful proposals. 

Then (starting at 55 minutes into the recording below) we discussed [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)'s [mentorship for integrating Fabric and Aries](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Hyperledger+Fabric+-+Hyperledger+Aries+Integration+to+support+Fabric+as+Blockchain+ledger) and ours for [integrating TrustID for client side security](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Implement+Client+Side+Security+for+Climate+SIG+Fabric+Application).  We discussed how Aries could be used to store decentralized identities (DIDs) on Fabric instead of on Indy, if TrustID could be used to authenticate with private keys in the Metamask wallet, and how to integrate them together.  

**Recording:**

**![](plugins/servlet/confluence/placeholder/unknown-attachment)**

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

**Time:**

- Monday, April 26, 2021 at 09 AM Pacific
- [Add Climate Action and Accounting SIG calls to your calendar](https://lists.hyperledger.org/g/climate-sig/ics/invite.ics?repeatid=31581)

**Dial-In Information:  \[ZOOM]**

You can join either from your computer or from your phone:

- From computer: [https://zoom.us/j/6223336701?pwd=dkJKdHRlc3dNZEdKR1JYdW40R2pDUT09](https://zoom.us/j/6223336701?pwd=dkJKdHRlc3dNZEdKR1JYdW40R2pDUT09)
- From phone: +1(855)880-1246 (toll free US number) or view [International numbers](https://zoom.us/u/bAaJoyznp)
- Meeting ID: 622 333 6701

## Attachments:

![](images/icons/bullet_blue.gif) [casig\_presentation\_jan2021.png](attachments/19007304/19007306.png) (image/png)  
![](images/icons/bullet_blue.gif) [casig\_osclimate\_feb9.png](attachments/19007304/19007305.png) (image/png)  
![](images/icons/bullet_blue.gif) [3.png](attachments/19007304/19007310.png) (image/png)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007304/19007307.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007304/19007308.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007304/19007309.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007304/19007311.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007304/19007332.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 13:10

[Atlassian](http://www.atlassian.com/)
