1. [Hyperledger Labs](index.html)
2. [Hyperledger Labs Home](Hyperledger-Labs-Home_20283400.html)
3. [Cardea](Cardea_20290619.html)
4. [2023 Cardea Meetings](2023-Cardea-Meetings_20294370.html)

# Hyperledger Labs : 2023-09-28 Cardea Users Group Meeting

Created by Helen Garneau, last modified by Keela Shazkin on Sep 28, 2023

## **Summary**

#### **On Today's Call:**

- **Review:**  New use cases

**Connection Info**

The call takes place over Zoom: [https://zoom.us/j/96010412250?pwd=enF1allFcThVYkNuTGw1cTRpVkpQQT09](https://zoom.us/j/96010412250?pwd=enF1allFcThVYkNuTGw1cTRpVkpQQT09)

### **Date**

28 Sep 2023 9am PT/ 10am MT/ 12pm ET

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit our Code of Conduct: [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

All activities should be conducted in accordance with the [Antitrust Policy found here](http://www.linuxfoundation.org/antitrust-policy).

## **Attendees**

- Keela Shatzkin, Ken Ebert, Trevor Butterworth, Steve Davis, Elisabeth Green, Mike Ebert

## **Announcements:**

## **Agenda:**

- - Identity Management use cases
    
    - Reducing human error/time on registration
      
      - Some data points still require checking/validation (i.e. last name, insurance, etc)
      - Could really reduce the re-collection of core data points (name, phone, race/ethnicity, etc)
      - Implementation Ideas:
        
        - Issuer
          
          - Health System (big hospital)
            
            - MRN is more consistent over time
          - Payer
            
            - Private
            - Public 
              
              - Often the data is sourced from the state and can be stale
            - Churn of payers
              
              - Typically annual (with private)
              - With eligibility changes (with public)
          - Source of data:
            
            - Drivers license
            - State identity card
            - Current hospital data
            - Ancillary services issued identity credential
        - Verifier
          
          - Health System
            
            - Returning patient
            - Avoid fuzzy name lookups to reduce duplication of persons
          - Ancillary services: Labs, pharmacies, clinics, private practices
            
            - Inheriting demographics
            - Discrete link to hospital record (with MRN)
          - MPI services
          - Credit services
          - University health care systems
          - Long term care facilities
      - Benefits
        
        - Reduced fraud for payers and health systems
          
          - ER, bait and switch (a covered patient presents at the desk, but a second person goes in for care)
        - User experience
        - In value based care, getting credit for services rendered or steps taken or reduction of patient health risk.
        - Patient access to their records (secure access) or to correctly identify records from another provider.
    - Helping maintain patient identity in low-structure use cases
    - Bridging clinical to social care with common patient identifiers
    - Reducing dependency on algorithmic matches to bridge identity proofed patient to fuzzy medical record link
      
      - Having a better ID to create better record in the first place
      - Could have definitive match rather than fuzzy
        
        - MRN and name, or more robust medical record- both have value
    - Next Steps
      
      - Boil down the idea(s)
      - Name it!
  - Future Agendas:
    
    - Finalize white paper
      
      - 10/12 meeting (v2.1)
