1. [Hyperledger Labs](index.html)
2. [Hyperledger Labs Home](Hyperledger-Labs-Home_20283400.html)
3. [Cardea](Cardea_20290619.html)
4. [2023 Cardea Meetings](2023-Cardea-Meetings_20294370.html)

# Hyperledger Labs : 2023-12-14 Cardea Users Group Meeting

Created by Keela Shazkin, last modified on Dec 14, 2023

## **Summary**

**Cardea Lab- Project Overview  
Second Thursday of every month:**   
Join us for an overview of the project and learn more about the future path of Cardea.  
9:00am to 10:00am  
(UTC-07:00) Pacific Time - Los Angeles

[https://zoom.us/j/91386616588?pwd=MGorZEY1V25XWkJ4dzIxT3JydWVjZz09](https://zoom.us/j/91386616588?pwd=MGorZEY1V25XWkJ4dzIxT3JydWVjZz09)

#### **On Today's Call:**

- **Agenda:**  
  
  - New Cardea use cases &amp; workflows
  - Future white paper

14 Sep 2023 9am PT/ 10am MT/ 12pm ET

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit our Code of Conduct: [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

All activities should be conducted in accordance with the [Antitrust Policy found here](http://www.linuxfoundation.org/antitrust-policy).

## **Attendees**

- Keela Shatzkin, Ken Ebert, Trevor Butterworth, Steve Davis, Simon Nazarenko, Mike Ebert, Helen Garneau

## **Announcements:**

- Next meeting: 
  
  - December 28 cancelled due to holidays/new year
  - January 11 next meeting

## **How to Stay in touch:**

- - - Calendar transition
      
      - 2nd&amp;4th Thursdays for now will continue
    - Groups io: [https://lists.hyperledger.org/g/labs](https://lists.hyperledger.org/g/labs)
      
      - Helen is admin
    - Zoom/Meeting Invites
      
      - Recordings are posted to youtube as “playlist” people can subscribe to
    - Chat
      
      - Move from slack to discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger)
      - #cardea channel under Labs

## **New Meeting Introductions:**

## **Meeting Notes/Discussion:**

- Workflows:
  
  - Patient safety and privacy/security
  - New patient workflow
    
    - Initial minimal placeholder record via web or phone (large percentage non-technical)
      
      - Issue a credential with minimal information? (re-issue later with more complete data)
      - Not always possible at this stage, but valuable to issue the credential as early as possible to avoid errors and duplication. Also increases security and efficiency of check-in.
    - Update and complete the patient information
      
      - Remotely prior to visit
      - In-office:
        
        - Paper form on a clipboard
        - iPad
      - Add image of the patient
      - Health insurance
      - Health history
      - Issue patient identity credential via QR code on web, email, SMS, in-office poster, displayed on-screen, invitation from the governance, carrier pigeon.
        
        - Simon pointed out concerns about SMS formatting &amp; where you go next in the UX/workflow
  - Schedule a new appointment workflow
    
    - Present Patient credential to front desk
    - Front desk pulls up chart
    - Select an appointment time/location
    - (optional) Message appoint to app  via DIDComm, SMS, email
    - (optional) Issue an appointment credential, especially useful for referrals
  - Check in for an appointment
    
    - Present Patient credential to front desk
    - (optional) Confirm patient information; revoke old credential &amp; issue updated Patient credential
    - Check in
  - Be seen by clinical staff (being called back from the waiting room)
    
    - Staff calls you back
    - Present patient credential
    - Image from patient credential matched to patient face by staff visually or via camera/image recognition
    - Avoids fraud (switching insured for another person) or errors (Bob2 is treated instead of Bob1)
    - Could also re-check cred (or connection DID) with each staff coming/going from room- may not be necessary if chart is present/open
    - With each new staff person that interacts with the patient, either connection or credential can be used to ensure the correct chart is being used.
  - Telehealth
    
    - This is for an existing patient (prior identity proofing happened in office). New patients require identity proofing and are more complex and will be considered in the future.
    - Present Patient credential to web UI
    - The caregiver is connected to the correct patient chart
    - web UI initiates the telehealth connection either via video meeting or telephone call.
- Credential Draft/critical data points
  
  - Picture/Identity binding

**Call Recording:** 

Document generated by Confluence on Nov 26, 2024 15:07

[Atlassian](http://www.atlassian.com/)
