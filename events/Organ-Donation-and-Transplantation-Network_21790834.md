1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Challenges](Challenges_21792347.html)
4. [Hyperledger Challenge 2022](Hyperledger-Challenge-2022_21792351.html)
5. [Ideate Challenge](Ideate-Challenge_21792356.html)
6. [Submissions](Submissions_21790825.html)

# Community Events : Organ Donation and Transplantation Network

Created by Sanjay Kumar K, last modified on Mar 15, 2022

(Work in progress. Will finish in next 2-3 days) 

***Innovation Tagline:**  DLT to increase accessibility and coordination*

**Project Keywords:**  #fabric #optn #organDonation #organTransplantation #verifiableCredentials #ssi #socialImpact

## Project Members

1. [Sanjay Kumar K](https://lf-hyperledger.atlassian.net/wiki/people/712020:4596d4f6-e466-487c-8427-9db51c8989d2?ref=confluence)

## Project Description *(no more than 1,000 words including graphics)*

Two separate solutions are proposed for two different problems.

1. A Hyperledger Fabric network will be created. Inside the network, multiple channels will be created i.e each channel will create a  subnetwork of Organ Procurement and Transplantation Network ( OPTN). These channels will be interoperable. The architecture and working of each channel will be determined based on the need and rules of a particular jurisdiction on how to design the OPTN i.e which organizations will form the channel, what rules will be coded into chaincode, which entities should be given permission to perform transactions.  The idea behind this is to increase accessibility by increasing the number of organizations that parallelly serve different entities and these organizations collectively form a subnetwork with a shared ledger/state for better coordination, communication, and governance.  Multiple OPTN can communicate i.e interchannel communication to further increase coordination, accessibility decision making, and governance.
2. Organ donation consented will be represented and presented in form of "Verifiable Credential (VC)". Each donor will carry donation consent in his phone and this consent can be cryptographically verified using an SSI ledger in which "Credential Definition" of the "Verifiable credential was defined". The verification will reveal 
   
   1. Which organization collected the consent from the donor and issued the donation consent in form of VC
   2. The donor who gave the consent.
   3. The data in the VC, which could be blood type or health status etc
   4. The data in the VC is in its original form as it was when issued and the same data is presented.

## **Problem**

There are three related problems that need different solutions.

1. Centralized Organ Procurement and Transplantation Network (OPTN).
   
   1. Solution: Different Organisations can collectively maintain the network (decentralization).
2. Siloed Transplant Coordination Network.
   
   1. Solution: Different OPTN sub networks can communicate to have better-coordinated action.
3. Non-interoperable silos manage the organ donation consent given by donors. 
   
   1. Solution: Using Verifiable Credentials to represent different claims which can be efficiently verified while protecting privacy.

#### **Centralized Organ Procurement and Transplantation Network.**

Current In the **USA**, a single nonprofit organization called United Network For Organ Sharing maintains and govern the database

1. which stores: 
   
   1. National transplant waiting list, matching donors to recipients.
   2. Maintaining the database that contains all organ transplant data for every transplant event that occurs in the U.S.
2. Which runs the algorithm to decide who gets the organ based on the database and contacts the patient's hospital.

Different entities who interact with the OPTN database are

1. Organ Procurement Organisations (OPOs): These organizations procure organs from the donors and add the details to the database.
2. HLA Labs: These labs perform tests on organs and add the lab reports of organs to the database.
3. Patients: Register themselves on the waiting list.
4. Hospitals: UNOS will contact the hospital of a patient if a suitable organ is found for a patient.

#### **Siloed  Transplant Coordination Network**

Currently, in **India**, different organizations at different levels maintain the ledger of the transplant waiting list and the list of organs available. Some states follow 3 tier network and some states like Maharastra adopt 4 tier network for transplant coordination. 

NOTTO:  National Organ and Tissue Transplant Organisation 

ROTTO: Regional  Organ and Tissue Transplant Organisation 

SOTTO:  State  Organ and Tissue Transplant Organisation 

![](attachments/21790834/21792668.png?width=661)

The lower-level organization collects data of patients and donated organs, and then they allocated organs to patients based on the policies, the details of patients, details of organs, and details of transplantation are sent to the higher-level organization. The higher-level organization helps in increased accessibility to patients to the pool of available organs and because the harvested organs are short-lived, it crucial for better and timely coordination to prevent the wastage of organs.

The advantage of tier structure is it improves accessibility as there are lower-level organizations that are dedicated to particular regions, thus different organizations parallelly serve the different regions. 

The disadvantage of tier structure is it decreases coordination because there are multiple ledgers and these ledgers are maintained on a siloed database, the problem it generates in coordination are 

1. Centralized Database. It's hard for different authorities to independently maintain the same exact data in the same order i.e data synchronization is hard. This limits multiple higher-level organizations to maintain and govern the same state collectively.  The problems this creates are:   
   
   1. Single Point of failure: If the database of the organization or authority is destroyed then coordination won't happen until it's been restored or recreated.
   2. Limited Accessibility: The organ matching will be only performed between the pool of organs it has and the patient on the waiting list. This is highly inefficient.
   3. Lack of Transparency: Organ Matching or the algorithm to find the suitable recipient is done privately. This process is not open to inspection.
2. Data Transfer: The data is transferred from lower-level organizations to higher-level organizations. This creates: 
   
   1. Loss of data Provence: The data in the higher-level organizations won't reflect all the details as it was added in the lower-level organizations, this, in turn, reduces the accountability.
   2. Non-Determinism: If data are stored in different formats at different various levels then the database at the higher-level organization will be inconsistent and may run the risk of result giving wrong data.

At present, there is a challenge between building a system with both accessibility and greater coordination. 

Solution: Using Hypereldger Fabric we can build networks with greater accessibility and coordination. 

#### **Non-Interoperable Silos Manage the Organ Donation Consent.**

"In 2020, the organ donation rate in Spain was 37people per million people", Spain has the highest rate of organ donation for the past 3 decades, this success is attributed to its system of "opt-out" or "presumed consent", which means that every individual is presumed to consent to organ donation even if they have never registered as a donor. 

Currently, In India and elsewhere there are multiple organizations that collect consent from the donor and store this consent in their database. 

Donors are classified into two types living donor and deceased donor. The deceased donor is usually those who are brain dead. where donor's organs are working but there is no brain functioning, these donors are kept alive in ICU until organs are harvested. Braindead could be the result of a road accident. 

When a person meets ancient and is declared braindead at the hospital, the consent for donation comes from the conversation between hospital staff and the donor's family. If the family doesn't reach a consensus on donation then the organs won't be extracted even if the donor has given prior consent to some organization. The prior consent of the donor is not recognized because of 

1. Lack of coordination between consent collecting organizations and hospitals.
2. Lack of trust in the consent collecting organizations.
3. Lack of authentication mechanism prevents consent collecting organizations to prove that the particular donor has given consent to them.

Because it's hard to coordinate and prove that the donor has given consent,  countries like Netherland, Spain, Colombia, etc have passed an "opt-out" or "presumed consent"  law. 

But this law is hard to pass in diverse and big countries like India, plus this may erode trust in hospitals as it could create a bad perception that hospitals will extract organs without consent.  Brazil introduced the "opt-out" law in 1997 and it was abolished in 1998 because of growing distrust in the medical system of the country. 

The proposed solution is to use "Verifiable Credential" to represent donation consent, which is stored in the donor's phone and can be cryptographically verified. 

## **Solution**

A network will be created using Hyperledger Fabric and multiple channel/subnetworks will be created for each OPTN under different jurisdictions and based on requirements. An identity metasystem or an SSI ledger will be either be created inside the network as a subnetwork or a third-party identity metasystem network like "Indicio" or "Sovrin" will be used or different entities and organizations can use multiple SSI identity metasystems to issue Verifiable Credentials and we aim to design our project to process VC from multiple SSI networks. 

![](attachments/21790834/21793028.png?height=250)

Verifiable Credentials will be used for 

1. Processing of Medical Records.  In UNOS, every 9 minutes a patient is added, processing and storing a huge volume of medical data would result in an increase in overhead cost, and not storing and non-processing of data at different decentralized nodes would create a potential for manipulation of organ allocation for transplantation.
2. Donation Management. 
   
   1. Portable and Cryptographically verifiable donation permit Issued by NGO: Hospitals can directly communicate with the donor and cryptographically verify that donor has given consent and consent was collected and donation permit was issued by authorized organization.
   2. Authentication of Donor: Cryptographically the donor can authenticate his identity to NGO that issues a donation permit, the NGO can build upon this identity and issues donation consent against this identity. Further, the donor can authenticate himself cryptographically to any verifier of donation permit. This would be useful for small NGOs that cannot spend resources to contact or integrate with identity issuers to authenticate the donors but the limitation to this is the identity that will be used by donors to authenticate to NGO will have to be trusted and accepted by all so the verifier accepts it too and will also have to have the capability to prove the ownership.
   3. Guardianship Authorization and management. Sometimes the donor may not be in condition to share his donation consent and so the donor will need a guardian who in the donor's place would present the donation permit and authorize hospitals to harvest the donor's organ.

![](attachments/21790834/21793034.png?height=400)

                              Donation Permit Issuance to Donor By NGO

![](attachments/21790834/21793032.png?height=400)

                          Authentication of Donor Using Existing Identity Issued

![](attachments/21790834/21793035.png?height=400)

                               Guardianship Management

**Minimum Viable Product**

### ![](attachments/21790834/21792991.png?height=400)

We will create a Hyperledger Fabric network with 

1. Sample OPTN channel with three organizations will be created,
   
   1. each of these organizations will serve one particular type of entity to prove the benefits of decentralization and how it will help in better
      
      1. accessibility
      2. coordination
      3. decision making
      4. governance
   2. Private Data Collection will be implemented between these entities to show privacy mechanisms can be added to protect sensitive data.
2. Identity metasystem channel: Will write chanicode to implement SSI Ledger. The NGOs will write the credential definitions to issue donation consent as Verifiable Credential to the donors (off-chain). The format of VC will be JWT and in the future, AnonCreds format will be used.

### Accomplishment and Team

[Sanjay Kumar K](https://lf-hyperledger.atlassian.net/wiki/people/712020:4596d4f6-e466-487c-8427-9db51c8989d2?ref=confluence) 

Help Needed in:

1. Domain Knowledge of Organ Transplantation and Donation
2. Production Level deployment of Hyperledger Fabric Project
3. Mentoring on Hyperledger Fabric
4. Mentoring on SSI
5. Frontend
6. Mobile App developer

### Project Plan

Will develop the prototype and this will serve as POC for the above-discussed functionalities. Will demo this to concerned authorities in  Karnataka Health Department who oversee the SOTTO. I work in "Centre For Smart Governance" which was formed by Karnataka Government to develop software for government departments. I will ask my organization to help me coordinate with the health department of Karnataka so I could build OPTN for Karnataka according to its needs and requirements.  We will later design OPTN for different jurisdictions based on their requirements. 

Will onboard NGOs those that collect donation consent, will develop an SSI mobile wallet, or would use existing SSI wallet for donors to store donation permits issued by NGOs. 

### Reference

## Attachments:

![](images/icons/bullet_blue.gif) [image2022-2-9\_21-38-15.png](attachments/21790834/21792667.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-2-9\_21-39-31.png](attachments/21790834/21792668.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-2-9\_21-39-31.jpg](attachments/21790834/21792896.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [image2022-3-15\_19-18-2.png](attachments/21790834/21792991.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-3-16\_1-55-20.png](attachments/21790834/21793028.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-3-16\_2-4-7.png](attachments/21790834/21793032.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-3-16\_2-6-3.png](attachments/21790834/21793034.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-3-16\_2-9-11.png](attachments/21790834/21793035.png) (image/png)

Document generated by Confluence on Nov 26, 2024 16:16

[Atlassian](http://www.atlassian.com/)
