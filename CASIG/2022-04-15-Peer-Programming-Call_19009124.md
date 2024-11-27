1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)
4. [Accounting &amp; Certification WG Peer Programming Call](19006574.html)
5. [2022 Peer Programming Call Notes Archive](2022-Peer-Programming-Call-Notes-Archive_19008759.html)

# Climate Action SIG : 2022-04-15 Peer Programming Call

Created by Si Chen, last modified by Bertrand WILLIAMSRIOUX on Apr 21, 2022

**Summary**

- Further refined data sets for the [Oil &amp; Gas Methane Emissions Reduction Project](19008903.html) to come up with the use case for the Hyperledger Global Challenge 2022.

**Use Case**

![key tight oil and shale gas regions](https://www.eia.gov/petroleum/drilling/archive/2020/12/images/dpmapv4l-wtitle_sm2.png)

We define methane and flaring emissions fro Oil &amp; Gas producers based in U.S. oil and gas basins (see image above): 

- Permian (*P*) - Texas, Nevada
- Bakken (*B*) - North Dakota, Montana
- Niobrara (*N*) - Wyoming, Colorado, ....

Each basin is assinged 2 Audited Emissions Certificates from the [NET network](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Emissions+Tokens+Network), one for methane emissions (fugitive, venting, incomplete flaring), *Bm*, *Nm*, and *Pm* and one for total methane flaring *Bf*, *Nf*, and *Pf*.  We estimate the total methane and flaring emissions, denominated in million tones of CO2e total emissions [as compiled in this spreadsheet with sources](https://docs.google.com/spreadsheets/d/1PQ2qz-P9qing_3F3BmvH6g2LA1G9BdYe/edit#gid=689160760).

Each basin is also assigned fuel production tokens for oil and natural gas (e.g., *Bo* and *Bg*) in metric tons of oil equivalent (mtoe) and billion cubic meters (bcm), respectively. We use 0.86 mtoe/bcm to convert gas to oil equivalent. Note that we have selected mtoe and bcm  in our basin examples for the year 2020 detailed in Table 1, however, oil and gas could be converted in any unit base on user preference.

Table 1: Emission and fuel production token data for select oil and gas basins in the U.S. in 2020.

*C-NFT component*

Basin

Methane, mt CO2e

*input*

Flaring, mt CO2e

*input*

Oil prod., mtoe

*output*

Gas prod., bcm

*output*

O&amp;G prod., mtoe

*(total output)*

EF methane kgCO2e/toe

*partial*

EF flaring kgCO2e/toe

*partial*

EF total,  kgCO2e/toe

*total*

Bakken, *B* *Bm* = 35.30 *Bf* = 3.17*Bo* = 60.43*Bg* = 27.94*BT* = 84.46418.037.6*Be* = 455.5Niobrara, *N**Nm* = 4.07*Nf* = 0.16*No* = 237.25*Ng* = 56.62*NT* = 81.0550.22.0*Ne* = 52.2Permian, *P**Pm* = 27.53*Pf* = 7.19*Po* = 1597.58*Pg* = 172.83*PT* = 366.5475.119.6*Pe* = 94.7

**U.S. Average**

**298.5****15.2****313.7****Global Average**

**229.9****38.7****268.5**

The data in Table 1 are used to construct Carbon Trakers Non Fungible Tokens (C-NFTs) for each basin (producer), as [introduced in this working paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4081426). The C-NFT links the methane and flaring emission tokens to the corresponding fuel production tokens, which, are assigned to each C-NFT at the closure of a audit, verification and certification processes. The C-NFT provides an anchor for the embodied flaring and venting emissions, measured as the carbon intensity or emission factors (see right rolumns in Table 1) of the oil and gas fuel tokens. 

- Permian C-NFT carbon intensity anchor point,  *Pe* = (*Pm* + *Pf*)/(*Po* +  *Pg* \*0.86 mtoe/bcm) = 94.7 kgCO2e/toe

The emission factors assigned to the C-NFT for each basin, and national and global averages reveal important information about U.S. production at the basin level. First U.S. flaring is well below global averages, and is lowest in the Niobara basin in Wyoming/Colorado. However, the majority of oil and sector waste emissions come from methane, which is more the 25 times more potent than the CO2 produced during methane flaring. U.S. methane emission factor is estimated to be 30% greater than the global average in 2020. As a result the Bakken was the most polluting basin on a per unit basis, with Niobrara achieving the lowest levels.

Note: In the original C-NFT contract fuel tokens are denominated in kgCO2e, by applying the standard scope 1 emission factor of each fuel: oil = 2.966 ton CO2e/toe; gas = 1.875 ton Co2e/kcm. As dsicussed in the call with [Si Chen](https://lf-hyperledger.atlassian.net/wiki/people/557058:c49c10c4-25bf-4187-b582-b521c3c33223?ref=confluence) we consider assigning custom units to fuel tokens used in a C-NFT. However, for consistency these should conform to the same unit, e.g., mtoe used in Table 1.

Now any fuel tokens assigned to the C-NFT, can be transferred to an energy trader or fuel consumer (e.g., via a public utility company). 

Local Gas Utility buys 1 bcm natural gas with 20% from oil company in Bakken, 20% from Niobrara and 60% from Permian. Now we can calculate the average methane emission factor of the gas supplied by the public utility.

- Local Gas methane emissions per thousand cubic-meter natural gas: (*Be*\*0.2 + *Ne*\*0.2 + *Pe*\*0.6)   = 158.36kgCO2e/toe.

More interestingly, the Local Gas Utility can acquire the following natural gas fuel tokens from each C-NFT, 0.2 bcm form *Bg* and *Ng* , and 0.6 bcm of *Pg*. These can be re-sold to consumers at a premium on the emission factor anchor. Clearly, Niabrara could seek a significant premium compared to the average emission factor of the Local Gas Utility: 52.2 vs. 158.36 kgCO2e/toe. Assuming consumers are exposed to a carbon price of 100 USD/tonCO2e, the fuel production linked to the Niabrara contract could seek a premium of up to 9.1 USD/kcm or 0.25 USD/mmtbu, roughly 10% of the Henry Hub Natural gas prices in 2020 (~2.5 USD/mmbtu).

![](plugins/servlet/confluence/placeholder/unknown-attachment)

Video 2

![](plugins/servlet/confluence/placeholder/unknown-attachment)

**Time:**

- Wednesday April 15, 2022 at 09 AM Pacific
- [Add Climate Action and Accounting SIG calls to your calendar](https://lists.hyperledger.org/g/climate-sig/ics/invite.ics?repeatid=31581)

**Dial-In Information:  \[ZOOM]**

**For this call, the call-in information is different**:

Join Zoom Meeting  
[https://zoom.us/j/93426785264?pwd=bmJOL2UxTzNHME5HTjg3c3d0QjZVdz09](https://zoom.us/j/93426785264?pwd=bmJOL2UxTzNHME5HTjg3c3d0QjZVdz09)

Meeting ID: 934 2678 5264  
Passcode: rQCq8x

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19009124/19009164.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19009124/19009163.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 13:10

[Atlassian](http://www.atlassian.com/)
