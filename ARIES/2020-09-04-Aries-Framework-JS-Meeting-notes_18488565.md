1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2020 AFJ meetings](2020-AFJ-meetings_18513105.html)

# Hyperledger Aries : 2020-09-04 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by shonjs on Sep 11, 2020

## Date

04 Sep 2020

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) (Animo) &lt;karim@animo.id&gt;
- [Ajay Jadhav](https://lf-hyperledger.atlassian.net/wiki/people/557058:4c9b11a5-2616-4abe-af94-bbc11c984654?ref=confluence) (AyanWorks) &lt;ajay@ayanworks.com&gt;
- [shonjs](https://lf-hyperledger.atlassian.net/wiki/people/557058:b2736d63-185c-457c-88a1-e84b63da434d?ref=confluence)
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)

## Agenda

- Record the meeting
- Squash and merge commit message
- Tests throw WalletInvalidHandle because afterAll function (that deletes wallet) is called before tests are finished
  
  - I think this is because outbound subject transporter and outbound transporter in general return when the message is send. But the other agent still has to process the whole message. However jest sees it as "oh the promise is resolved, the test is finished".
- How to handle auto accept
  
  - local config → stored with connection record on creation
  - global config → stored with connection record on creation?

## Meeting Notes

- everyone aware of agent running after jest tests resolve. 
  
  - [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) will either create issue or document this.
- auto accept connections logic
  
  - local config is stored with connection record, global config not
  - local config takes precedence over global config
- using AFJ inside a react native application
  
  - Indy.framework is currently not built for simulator
  - Building Indy.framework from the core does not work at the moment
  - there are issues with building iOS targets in libindy. 
    
    - [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) and [Ajay Jadhav](https://lf-hyperledger.atlassian.net/wiki/people/557058:4c9b11a5-2616-4abe-af94-bbc11c984654?ref=confluence)  will work out issues
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) making progress on issue credential protocol
  
  - credential-offer merged
  - now working of credential request
  - hopefully next week finished, maybe two weeks
- colleague of [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)could maybe work on present proof protocol
- Question if AFJ could work in deno?
  
  - Probably not. Deno doesn't work with NPM / NodeJS packages.
  - do we want to integrate with deno?
    
    - abillity to use rust with deno
    - better security?
    - performance not sure

## Future topics

- State machines

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18488565/18514103.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18488565/18514116.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18488565/18514115.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18488565/18514104.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
