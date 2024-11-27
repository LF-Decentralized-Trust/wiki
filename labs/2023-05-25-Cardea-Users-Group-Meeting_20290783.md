1. [Hyperledger Labs](index.html)
2. [Hyperledger Labs Home](Hyperledger-Labs-Home_20283400.html)
3. [Cardea](Cardea_20290619.html)
4. [2023 Cardea Meetings](2023-Cardea-Meetings_20294370.html)

# Hyperledger Labs : 2023-05-25 Cardea Users Group Meeting

Created by Helen Garneau, last modified by Ry Jones on May 25, 2023

## **Summary**

**![](attachments/20290783/20294395.jpg?height=250)**

#### **On Today's Call:**

- **Review:**  New Community Group connection instructions (calendar etc), review of project goals, upcoming speaker series
- **Presentation**: Serhat Pala, Partner, Cross Ocean Ventures: Workplace Drug Testing

**Connection Info**

The call takes place over Zoom: [https://zoom.us/j/99592925086?pwd=UlpLU2pJeGMvVmljM3JHUmNkZ0FqUT09](https://zoom.us/j/99592925086?pwd=UlpLU2pJeGMvVmljM3JHUmNkZ0FqUT09)

### **Date**

25 May 2023 9am PT/ 10am MT/ 12pm ET

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit our Code of Conduct: [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

All activities should be conducted in accordance with the [Antitrust Policy found here](http://www.linuxfoundation.org/antitrust-policy).

## **Attendees**

- Keela Shatzkin, Ken Ebert, Ry Jones, Helen Garneau, Serhat Pala, Elisabeth Green, Heather Dahl, James Schulte, Mike Ebert, Simon Nazarenko, Steve Davis, Tim Spring, Trevor Butterworth, Will Groah, Bhaskar Ram

## **Announcements:**

- 6/8 Meeting:  Presentation from Sarah Samis, VP of Public health Products and Platforms of GCOM

## **Agenda:**

- - Transitioning to Hyperledger
    
    - Calendar transition
      
      - 2nd&amp;4th Thursdays for now will continue
    - Groups io: [https://lists.hyperledger.org/g/labs](https://lists.hyperledger.org/g/labs)
      
      - Helen is admin
    - Notes/Materials
      
      - Old notes and materials have been transitioned to the wiki page
      - Can track notes real time
    - Zoom/Meeting Invites
      
      - Will transition to hyperledger zoom
      - Recordings are posted to youtube as “playlist” people can subscribe to
    - Chat
      
      - Move from slack to discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger)
      - #cardea channel under Labs
    - Blog announcing transtition to Hyperledger:
      
      - [https://www.hyperledger.org/blog/2023/05/10/cardea-a-privacy-preserving-open-source-ecosystem-for-verifying-health-data-joins-hyperledger-labs](https://www.hyperledger.org/blog/2023/05/10/cardea-a-privacy-preserving-open-source-ecosystem-for-verifying-health-data-joins-hyperledger-labs)

<!--THE END-->

- - Discussion with Serhat Pala
    
    - Covering the Basics:
      
      - Chain of Custody matters with specimen
      - Point of Service
        
        - Instant testing
          
          - These are usually screening tests not confirmatory tests
            
            - i.e. non-negative test should/could result in follow up confirmation test (due to false positives, etc)
        - Lab based/off-site
          
          - have higher sensitivity
      - Primary Specimens
        
        - Urine
        - Saliva
          
          - newer, slightly less acceptance for variety of reasons
    - Lifecycle
      
      - Pre-employment
        
        - during application process, generally after acceptance of position
        - drug testing &amp; background screening often happen together, many service providers offer both
        - Order:
          
          - Send order form to candidate for them to bring to lab
            
            - release of info to employer is likely included in onboarding paperwork **OR**
            - collection site explicitly collects the consent to release the result to the employer (ordering "provider")
          - On-site/self hosted testing (if applicable to the company type/size/setting)
        - Testing procedure
          
          - Identity proof at the site/during collection
          - Low-tech solutions today, during check-in process
          - opportunities for issues with authenticity of sample (person swap, sample tampering, etc)
        - Result
          
          - Usually never shared with the employee themselves, only the employer
          - there is usually a Medical Review Officer that determines if the result is pass/fail for the employer; "the interpreter" 
            
            - critical for cases where patient might be on medication the indicates positive result, for legal/medical reasons
            - the MRO is usually independent, contracted by either lab or 3rd party administrator (i.e. employment verification company)
          - Employer generally gets yes/no answer to control workflow, not details of the test, but may also include them
          - Transmission of data:
            
            - often incorporated into MRO system
            - HIPAA... but occasionally email might happen (hopefully encrypted!)
      - Ongoing/Event based testing
        
        - Some industries are regulated
          
          - Dept of Transportation has minimum requirements
          - State/Federal might have additional oversight of specific industries
          - Companies can layer on additional requirements as needed
        - 3rd party administrators usually manage these programs
        - Consent
          
          - Is this consent each time or once that covers the recurring/program agreement
        - Schedule is usually at random (once per year - unscheduled, or random sample of company)
          
          - timeliness to respond to request for order is important to ensure there is no tampering
    - Business Trending
      
      - Growth industry
      - Other factors
        
        - when it's hard to find employees, standards might lower to attract more people
        - similarly, tightens during economic downturns because you're more choosy for candidates (and current staff)
        - Changing landscape on legalization/decriminalization of certain individual drug use
          
          - Does not appear to decrease test rates, impact of business relationship/industry requirements, might have legal exposure for company (to test *and* not to test)
      - Economies of scale
        
        - companies would like to reduce burden on employee to streamline process, issues with ownership of result (currently with the employer)
        - the 3rd party administrators could potentially share if the service the same companies (and contracts allow)
    - Questions:
      
      - Organ Donation overlap?
        
        - donation is provided but only yes/no is passed down on whether sample is viable and a match
        - Needs more follow up
      - Is there a need for the employer to allow the employee/candidate to request the data to be shared with them (via verifiable cred)?
        
        - Yes, the result should belong to the specimen owner, especially since the use cases go way beyond just work-place testing
        - **but** it opens up a lot of questions and could result in additional issues for the employer, i.e. the result could be challenged after the result is released based on the room for interpretation.  For example, this opens up the black box for the employer to be scrutinized on their decisions/process
        - IF there is trust in the system, this may change the flow and employers would be happy to give up the cost of testing if they can trust other results
  - Future Agendas:
    
    - 6/8 Meeting:  Presentation from Sarah Samis, VP of Public health Products and Platforms of GCOM

## **Call Recording:**

[https://youtu.be/L9v-eirGso8](https://youtu.be/L9v-eirGso8)

## Attachments:

![](images/icons/bullet_blue.gif) [Cardea Speaker Card (2).jpg](attachments/20290783/20294395.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 15:07

[Atlassian](http://www.atlassian.com/)
