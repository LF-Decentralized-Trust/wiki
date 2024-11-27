1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)
4. [Accounting &amp; Certification WG Peer Programming Call](19006574.html)
5. [2021 Peer Programming Call Notes Archive](2021-Peer-Programming-Call-Notes-Archive_19006679.html)

# Climate Action SIG : 2021-07-19 Peer Programming Call

Created by Robin Klemens, last modified by Si Chen on Jul 19, 2021

**Summary:**

- [Pritam Singh](https://lf-hyperledger.atlassian.net/wiki/people/70121:3f6d9be4-62e2-4d6c-a3ae-b43ec2ba2d9a?ref=confluence)reviewed the cactus integration.  He showed how the Request Manager could lock Fabric data while transactions are being created on the Ethereum network.  The Request Manager is a separate chain code which will call the utility emissions chain code to execute the steps, and while it does so the Fabric emissions records are locked so they cannot be updated by another service.
- [Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence) showed using Fabric with SoftHSM2 to enroll admin and users.  SoftHSM2 simulates a  Hardware Security Module.  It is configured with a label ("ForFabric") and a PIN, which is then used inside of Fabric to call the HSM.  However, this may not be the correct workflow of using an actual HSM.
- At the end of the call, we decided to look at an actual HSM workflow to determine how to integrate with it.  [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)suggested this [Fabric HSM example](https://github.com/hyperledger/fabric-test/tree/main/regression/hsm) and also this example on [delegating cryptographic operations to Hashicorp Vault](https://stackoverflow.com/questions/64636337/hyperledger-fabric-how-to-delegate-cryptographic-operations-to-hashicorp-vault).
- [Elisabeth Green](https://lf-hyperledger.atlassian.net/wiki/people/712020:5b417990-5e6e-4737-8337-1a1cc470388b?ref=confluence)made a feature request at the end of the call:
  
  - Request for feature: Does the system record the time of emission? How does the system verify the parameters of the request? May the system be used to deny a request that is trying to offset freshly-extracted carbon? Say, keep the requester account locked until the code verifies that the carbon emissions are timestamped at an earlier date? Does it plan for a proposed policy to disqualify from offsetting new fossil fuel use? For example, the contract would refuse a request to offset fossil fuel extracted/used after Overshoot Day each year. Global Greens Ambassador and former Parliamentary Leader and Senator for Tasmania, Christine Milne spoke on a video a few days ago. She is planning to help negotiate policy at COP 26 and has the following need. We should distinguish between legacy carbon use, which is past emissions, which may be offset, and newly-extracted or burned carbon, which is prohibited from offsetting. There has to be a way to verify that sequestered carbon is staying in the ground or is not offset.
  - My response here is that:
    
    - The system does record the time of the emissions.
    - The current system is designed for a trusted auditor to record emissions on a Fabric ledger.  Therefore, it is up to the user, who is the trusted auditor, to verify the parameters of all the requests.  This could be modified to work in use cases where an independent verification is done as well.
    - The use case you describe, not allowing carbon emissions after a date to be offset, is not a standard one.  I would not recommend making that a feature of the open source code base, so that it is as flexible as possible to support a range of use cases.  Then individual groups could modify to support the use cases they need.

**Recording:**

**![](plugins/servlet/confluence/placeholder/unknown-attachment)**

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

**Time:**

- Monday, July 19, 2021 at 09 AM Pacific
- [Add Climate Action and Accounting SIG calls to your calendar](https://lists.hyperledger.org/g/climate-sig/ics/invite.ics?repeatid=31581)

**Dial-In Information:  \[ZOOM]**

You can join either from your computer or from your phone:

- From computer: [https://zoom.us/j/6223336701?pwd=dkJKdHRlc3dNZEdKR1JYdW40R2pDUT09](https://zoom.us/j/6223336701?pwd=dkJKdHRlc3dNZEdKR1JYdW40R2pDUT09)
- From phone: +1(855)880-1246 (toll free US number) or view [International numbers](https://zoom.us/u/bAaJoyznp)
- Meeting ID: 622 333 6701

## Attachments:

![](images/icons/bullet_blue.gif) [3.png](attachments/19007933/19007936.png) (image/png)  
![](images/icons/bullet_blue.gif) [casig\_osclimate\_feb9.png](attachments/19007933/19007938.png) (image/png)  
![](images/icons/bullet_blue.gif) [casig\_presentation\_jan2021.png](attachments/19007933/19007939.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2021-07-20 20-33-12.png](attachments/19007933/19007978.png) (image/png)  
![](images/icons/bullet_blue.gif) [Fabric HSM Identity.jpg](attachments/19007933/19008007.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [Fabric HSM Identity (1).jpg](attachments/19007933/19008034.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [client.svg](attachments/19007933/19008043.svg) (image/svg+xml)  
![](images/icons/bullet_blue.gif) [client.png](attachments/19007933/19008044.png) (image/png)  
![](images/icons/bullet_blue.gif) [client.jpg](attachments/19007933/19008045.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [Screen Shot 2021-07-29 at 6.55.25 PM.png](attachments/19007933/19008071.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2021-07-29 at 7.00.52 PM.png](attachments/19007933/19008072.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2021-07-29 at 7.09.39 PM.png](attachments/19007933/19008073.png) (image/png)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007933/19007934.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007933/19007942.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007933/19007940.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007933/19007941.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007933/19007937.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19007933/19007935.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 13:10

[Atlassian](http://www.atlassian.com/)
