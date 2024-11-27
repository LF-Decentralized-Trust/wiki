1. [Hyperledger Labs](index.html)
2. [Hyperledger Labs Home](Hyperledger-Labs-Home_20283400.html)
3. [Cardea](Cardea_20290619.html)
4. [2023 Cardea Meetings](2023-Cardea-Meetings_20294370.html)

# Hyperledger Labs : 2023-06-08 Cardea Users Group Meeting

Created by Helen Garneau, last modified by Ry Jones on Jun 08, 2023

## **Summary**

![](attachments/20290801/20294400.jpg?height=250)

#### **On Today's Call:**

- **Review:**  New Community Group connection instructions (calendar etc), review of project goals, upcoming speaker series
- **Presentation**: Sarah Samis, VP Public Health Products and Platforms, GCOM

**Connection Info**

The call takes place over Zoom: **[https://zoom.us/j/97575630290?pwd=di9hNThXSXNhRVhkak1heXVGblM5Zz09](https://zoom.us/j/97575630290?pwd=di9hNThXSXNhRVhkak1heXVGblM5Zz09)**

### **Date**

08 Jun 2023 9am PT/ 10am MT/ 12pm ET

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit our Code of Conduct: [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

All activities should be conducted in accordance with the [Antitrust Policy found here](http://www.linuxfoundation.org/antitrust-policy).

## **Attendees**

- Keela Shatzkin, Ry Jones, Helen Garneau, Sarah Samis, Ivan, Mike Ebert, Simon Nazarenko, Steve Davis, Tim Spring, Trevor Butterworth

## **Announcements:**

- Next meeting: 6/22

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

- - Introductions
    
    - Keela Shatzkin
    - Ry Jones
    - Helen Garneau
  - Discussion &amp; Presentation with Sarah Samis &amp; Ivan
    
    - GCOM, state and local government IT services company, work with most/many states across US
      
      - Vital Records issuance and management
      - digital identity solutions using verifiable credentials
    - Vital Records community goal:
      
      - pilot level digital certificate issuance by 2026
    - Vital Records overview
      
      - a form of identity credentials, used for a range of verifications of other critical documents, i.e. driver's license
      - Issued at local/state level, NOT federal level
        
        - 57 agencies (some states have more than 1, plus US territories
        - each STATE has laws the specify how these things should be collected and managed
      - Most other countries have vital records at national/federal level
    - User/community
      
      - ![](attachments/20290801/20294405.png?height=250)
      - State and Local jurisdiction staff
      - Providers who enter data
        
        - birth data
        - death data
      - End User/public requesting data
        
        - includes clearing house integrations
      - ![](attachments/20290801/20294406.png?height=250)
    - There are timeline requirements for providers to submit the data, especially timely death reporting
    - Use Cases:
      
      - Who's qualified to submit vital stats records, Medical Certification
        
        - Issuer: ED department (who oversees medical licensing)
        - Holder: Licensed medical certifier
        - Verifier: Health Department
        - Discussion
          
          - May require adjustments to state law if there are mandates on identity verification, to ensure verifiable creds meet/satisfy these requirements
          - Could be used to manage login to the reporting system
          - Supports the submission cycle
      - Birth Use Case: Public/Person requesting their record
        
        - Issuer: Dept of Health
        - Holder: person/parent
        - Verifier: Local school district
        - Discussion
          
          - Verifiable creds would help make enrollment easier and would be more secure by use of the ED systems
            
            - School could provider registration QR code
          - Supports selective disclosure
            
            - i.e. school district only needs to verify age for grade eligibility
          - Paper forms:
            
            - Long form includes ALL data including a lot of medical and family based data
            - Short form is more limited, but still may include more than what's needed for school
          - Children born to non-citizen parents have a really hard time getting birth certificates
          - There is a major value in being able to revocate access when needed
            
            - 18th birthday
            - Emancipated Minors
            - Amendments and Corrections, ease of revoke and reissue
      - Death Use Case:
        
        - Issuer: Dept of Health
        - Holder: Relative
        - Verifiers: Government, Private sector (titles, life insurance), 3rd party to Government
        - Discussion
          
          - WHY people died is considered super sensitive data point
            
            - can be managed by selective disclosure
          - Longer times for delivery can cause delays
    - WILL need tools to help interoperate because there WILL be deviation in the standards
- - **Questions:**
    
    - Why are these not free?
      
      - Fees help cover the operating costs
      - There are special fraud protection paper requirements that also add costs
      - special cases may require a lot more investigation/vetting which requires staffing &amp; resources
    - VitalCheck
      
      - software product provided by LexisNexis, this is contracted with local governments
      - MOST states are live with public/private partnership
    - How close is birth certificate to becoming verifiable credentials?
      
      - Since this is foundational document.... and sometimes we need to MAIL this to agencies, etc, how close is this to becoming real?
      - We think this is on the horizon, there is a lot of interest, NAPHSIS conference is investigating.  Some states are laying foundation laws for digital identity (Utah, Michigan, etc)
        
        - some drivers licenses and passports ARE already digitized, partially because they NEED to be more mobile, so they came first
          
          - This could help leapfrog the use case for birth certificates because the path is being paved and barriers are being reduced
        - There is a significant use case, could help with other state/government program enrollments
    - Technical formats?
      
      - Focus isn't on the tech detail yet, but rather the general goal of digitizing the data
      - There hasn't been a rallying around a single tech answer yet.
        
        - There is a risk for state based deviations here... but there is federal role to help fund and encourage states to move in certain directions... the carrot to drive toward consistency
  - White paper Update
- - Future Agendas:
    
    - Next meeting: 6/22

## **Call Recording:**

[https://youtu.be/IdvTBG9wtYw](https://youtu.be/IdvTBG9wtYw)

[2023 06 08 Cardea Lab - chat](attachments/20290801/20294407.txt)

## Attachments:

![](images/icons/bullet_blue.gif) [Cardea Speaker Card (2).jpg](attachments/20290801/20294399.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [Cardea Speaker Card-2.jpg](attachments/20290801/20294400.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [image-2023-6-8\_12-15-45.png](attachments/20290801/20294405.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-6-8\_12-25-31.png](attachments/20290801/20294406.png) (image/png)  
![](images/icons/bullet_blue.gif) [2023 06 08 Cardea Lab - Project Overview.chat.txt](attachments/20290801/20294407.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 15:07

[Atlassian](http://www.atlassian.com/)
