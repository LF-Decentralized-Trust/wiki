1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Challenges](Challenges_21792347.html)
4. [Hyperledger Challenge 2022](Hyperledger-Challenge-2022_21792351.html)
5. [Ideate Challenge](Ideate-Challenge_21792356.html)
6. [Submissions](Submissions_21790825.html)

# Community Events : Anonymous social login plugin

Created by Dr.-Ing. Roman Zoun, last modified on Mar 02, 2022

***Innovation Tagline:**  (decentralization of central Identity Provider)*

**Project Keywords:**  #decentralization #SSI #SelfSovereignIdentity #web3 #untrackable #Metaverse #DID

**We start our journey from the market and the customer side, check out our customer research results in Appendix section.**

## Project Members

1. Roman Zoun [Dr.-Ing. Roman Zoun](https://lf-hyperledger.atlassian.net/wiki/people/712020:bcf67673-b87e-4a91-8af0-f27bbc9e5642?ref=confluence) → Lead (Marketing, Dev: Aries, Spring boot, Angular)
2. Michel Sahli [Michel Sahli (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5f0edafb1a26ad0014394305?ref=confluence) → First Dev Lieutenant (Aries, Spring boot, Angular)
3. Thomas Eppler [Thomas Eppler](https://lf-hyperledger.atlassian.net/wiki/people/557058:4fb046d9-8e2c-4973-a963-2469aa25e686?ref=confluence) → User Excitement Officer (Understand the market, Inventive thinking, asking the right questions)
4. Manuel Forster [Manuel Forster](https://lf-hyperledger.atlassian.net/wiki/people/557058:ebbdaae0-d512-4a45-b3f8-c0d37ff6344e?ref=confluence) → Genious IT Sculpter (Aries, Spring boot, Angular)

## Project Description *(no more than 1,000 words including graphics)*

**What we usually do:** I registered myself on Linux foundation using Linkedin and now I got an advertisement for training on the Linux foundation platform. So I used an identity and I paid with my behavior.

**What we want to make possible:** We want to show there is another way! Imagine "login with google," and google will never know you did it. We introduce an anonymous social login plugin for digital services to allow users to use the secure way to onboard and register using third party login, without notifying them about it. Our goal is to wake the privacy awareness in users and tell the world that social login can be anonymous and the data collected by them shouldn't be collected. Additionally, the user will have a passwordless Identity manager in his hand, no forgotten passwords anymore. Stop "login with google", start "login without google". 

![](attachments/21792483/21792815.png?height=250)

### list of abbreviations

- **OIDC** - OpenID Connect allows Clients to verify the identity of the End-User based on the authentication performed by an Authorization Server, as well as to obtain basic profile information about the End-User in an interoperable and REST-like manner. OpenID Connect allows clients of all types, including Web-based, mobile, and JavaScript clients, to request and receive information about authenticated sessions and end-users. The specification suite is extensible, allowing participants to use optional features such as encryption of identity data, discovery of OpenID Providers, and session management, when it makes sense for them.
- **IDP** - Identity Provider s a system entity that creates, maintains, and manages identity information for [principals](https://en.wikipedia.org/wiki/Security_principal "Security principal") and also provides authentication services to relying applications within a federation or distributed network. Identity providers offer user authentication as a service. Relying party applications, such as web applications, outsource the user authentication step to a trusted identity provider

### Problem

1. Onboarding processes are established on nearly every online service using social login via OIDC This is easy, but involves a central identity provider such as LinkedIn Facebook google etc, see this page of hyperledger foundation:
   
   ![](attachments/21792483/21792484.png?height=250)
2. The current solution is user friendly and everyone love to use it, mostly with an two factor authentication, which involves often the mobile phone and a password.
3. The social login is integrated in the process like start-button on windows desktop, but every time I use it, the central identity provider notice this and can learn more about the behavior of the user. For example, I logged in here using linkedIn, so LinkedIn will provide me some advertisement around Linux foundation.
4. And if I'm not logged in in LinkedIn, I need to login again, which means I need to know my password
5. **Summary of Problems**:
   
   1. User's behavior is tracked in the current services, which makes the user to a product of social identity provider!
   2. Users need to remember too many passwords!

→ To strengthen the statement **we did Market Research to this topic: check the Appendix below**

Summary of the client research: Since the goal is to be accepted by the market and leverage hyperledger projects on the market, we started your journey with a market research. We can clearly show the needs of the market as a result of online research and from a customer survey. First, we research the web and publications about security and hyperledger projects and it came out, that overall the need for secure communication and secure exchange of personal data exists, especially in not trackability of activities and preventing personal data storage and the risk of data breaches. 

Besides this, we prepared a survey to find out features of our customers, the users, with the highest importance and lowest satisfaction value. This brings insights and high opportunity to our topic. Furthermore, we asked in the survey afterwards for the best features. From this we defined the top 4 List of the features in the topic Login, Accounts and personal data security:

1. **knowing which organization is sharing your data with whom else**
2. **you have transparency about which personal data you have shared with which organization/website.**
3. **that you can log into websites on the computer with biometric features (fingerprint, FaceID, ...) without having to enter a password**
4. **you can decide and control who can see your personal data (name, email, date of birth etc.)\***

The result is the top 4 wished features:

1. **that you can define who can see your personal data**
2. **that you can \*log into \*websites particularly \*comfortably and easily\***
3. **that you can see in an overview which of your personal data is used by whom**
4. **knowing which organization \*is sharing your data with whom else\***

### Solution

In the beginning we will tackle the feature "you have transparency about which personal data you have shared with which organization/website." and "you can decide and control who can see your personal data (name, email, date of birth etc.)" and "that you can log into websites on the computer with biometric features (fingerprint, FaceID, ...) without having to enter a password". During the hackathon, we will bring a solution or concept, together with hyperledger mentor and community, to solve the feature "knowing which organization is sharing your data with whom else". So we implement the second and third position from our customer research for the hackathon, and will provide a concept to solve the Top1 feature together with hyperledger community during the hackathon using methods from "inventive thinking". 

1. Provide a service which combines the usual social login onboarding, without the central IDP get your behavior. We introduce the Social verifiable credential, a service where a user login once, and issue his social account as verifiable credentials in his wallet. In addition, we introduce a simple OIDC SSI verifier to include the social login as verifiable credentials easy into your service.
2. The user have then a passwordless social identity, because the whole account is in your wallet
3. We introduce a easy auth server using SSI configured for the social accounts, that can be used for Login on every plattform.
4. Our solution doesn't include any central IDP, no databases for storing the data and is easy to integrate to your service, as configuration for docker-compose, kubernetes AWS, Azure, Google Cloud ...
   
   1. alternatively we plan to use zapier for easy integration, like trinsic
   2. Our goal is decentralize, so verey service provider need to add his own verifier but we provide the easiest way to do it
5. **Minimum Implementation goal**:
   
   1. As minimum is an issuer with the social login via central IDP. The verifier is not needed in the beginning, since a lot of products can solve this (trinsic, esatus, ...)

### Accomplishment and Team

- Roman Zoun [Dr.-Ing. Roman Zoun](https://lf-hyperledger.atlassian.net/wiki/people/712020:bcf67673-b87e-4a91-8af0-f27bbc9e5642?ref=confluence) → Lead (Marketing, Dev: Aries, Spring boot, Angular)
  
  - OIDC dev
  - aries AIP1 jedi
  - Springboot investor
  - angular friend
  - inventive thinker
  - marketing executer
- Michel Sahli [Michel Sahli (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5f0edafb1a26ad0014394305?ref=confluence) → First Dev Lieutenant (Aries, Spring boot, Angular)
  
  - OIDC knight
  - Security Boss
  - aries AIP2 expert
  - Springboot fabricator
  - angular padawan
  - applied researcher
- Thomas Eppler [Thomas Eppler](https://lf-hyperledger.atlassian.net/wiki/people/557058:4fb046d9-8e2c-4973-a963-2469aa25e686?ref=confluence) → User Excitement Officer
  
  - Digital Identity Researcher
  - Innovation Client Research Expert
  - Lecturer for Innovation Methodologies
  - metaverse mesmer
  - early digital identity adopter
- Manuel Forster [Manuel Forster](https://lf-hyperledger.atlassian.net/wiki/people/557058:ebbdaae0-d512-4a45-b3f8-c0d37ff6344e?ref=confluence) → Genious IT Sculpter (Aries, Spring boot, Angular)
  
  - Architecture
  - aries AIP1
  - Springboot guru
  - DevOps expert
  - angular lover

### Project Plan

#### Milestone 1 - Define Data Governance and Architecture

- Define schemas,
  
  - Google Verifiable Credetnial schema
  - Facebook Verifiable Credetnial schema
  - Twitter Verifiable Credetnial schema
  - ...
- Define Architecture
  
  - Plattform, Issuer, verifier, communication
  - **Important!!! No database because no data will be stored!**

#### Milestone 2 - Implementing a Plattform includes social identity provider authentication

- implement platform with at least one social login (first google, then facebook, twitter, linkedIn, Apple, GitHub WeChat, amazon, etc),
  
  - Spring Security Client with google IDP configuration

#### Milestone 3 - Implementing a service to issue the data from identity provider as verifiable credential to a wallet

- implement self-issuer service, which means the user see his data after login and then can issue it to his wallet (Evernym/lissi/trinsic/esatus),
  
  - Spring Backend
  - Spring Webhook, Aries cloud wallet for issuing and communication with user wallet
  - Angular frontend

#### Milestone 4 - Marketing about out awesome plattform

- Start marketing for OIDC-Verifier and easy tutorials how to integrate with videos, twitter, with help of hyperledger
  
  - Some Ideas for marketing
    
    - Target Services: Create Video describing architecture and how central idp is working
    - Target users: Create funny sketches how would it be if your wife/mama/dad would be like central IDP and know everytime you check in in a hotel or a bar or club
    - Target Services: Create Architecture Video for decentralization of central IDP and the service still can save the data in the service, and for the service it doesn't have any negative aspects
    - Target users: Same funny video how with the wife/mama/dad, but this time she only knows, you go to a friend, but doesn't know what you did next
  - Share via twitter, tiktok etc

#### Milestone 5 - Implement a verifier, which allows OIDC authentication via SSI and the Credentials defined in Milestone 1 and issued by milestone 2 and milestone 3

- implement OIDC-verifier with configuration for the credential definition ids of the social login
  
  - Spring athorization server + Spring Webhook + Aries cloud wallet
  - configured on credential definition ids of the Verifiable credentials that are implemented on the platform
  - Login page is QR code with proof request for this
- implement different ops configs, for Premis, Cloud, Proxy etc

#### Appendix

Support from ssi product provider

- If a product provider give us access to their technology for free, we will use it and be much faster.
- Trinsic, Lissi, Animo Solutions provide verifier, that can be used as verifier, too

### Risk

Risk

- The risk is, that no one will integrate the OIDC-Verifier, because of the effort and no users on market (chicken egg problem)
  
  - We reduce the risk by providing a lot of tutorials and support to integrate the OIDC verifier
  - OIDC-Verifier is free, and we say that other products of trinsic, esatus, evernym can be used here
  - we need good short pitch videos that we can spread over social media - see milestone 4
- Another risk, is that users will not use it, because no services offer it (chicken egg problem)
  
  - We need at least on hyperledger/linux foundation the possibility to login with it, then we will make marketing to show the data privacy benefits for the user
  - hope it begins with some enthusiasts but will scale later to everyone
  - Since this is something that users get into SSI, we are sure, we get marketing support of SSI companies and enthusiasts
  - we need good short pitch videos that we can spread over social media - see milestone 4
- another risk is the scalability of user access, what if it goes to the moon, we are not sure about the scalability of the aries wallet
  
  - we just hope hyperledger community and some SSI product providers support us for production ready deployment of cloud wallet
- Another Risk is that one social provider blocks us
  
  - Limit risk by instant marketing reactions around this, and starting petitions, and ask all known GPDR data protection auditors to look at this...and we can say, that tracking user is not needed and should be punished by GPDR...we can't do other things
  - Add positive feedback/marketing to providers who accept this for publicity and privacy of their customers and negative about the ones who blocks our platform

# Appendix

## Market Web Research

We research companies why how they see the future of login and identity management with following results:

"Self-sovereign identities (SSI) are digital identities that are managed in a decentralized manner. This technology allows users to self-manage their digital identities without depending on third-party providers to store and centrally manage the data"

\[[https://www.bosch.com/stories/self-sovereign-identities](https://www.bosch.com/stories/self-sovereign-identities)]

"Self-sovereign identity (SSI) is a term used to describe the digital movement that recognizes an individual should own and control their identity without the intervening administrative authorities. SSI allows people to interact in the digital world with the same freedom and capacity for trust as they do in the offline world."

\[[https://sovrin.org/faq/what-is-self-sovereign-identity/](https://sovrin.org/faq/what-is-self-sovereign-identity/)]

"By 2022, Gartner predicts that 60% of large and global enterprises, and 90% of midsize enterprises, will implement passwordless methods in more than 50% of use cases — up from 5% in 2018."

\[[https://www.gartner.com/smarterwithgartner/embrace-a-passwordless-approach-to-improve-security](https://www.gartner.com/smarterwithgartner/embrace-a-passwordless-approach-to-improve-security)]

"There are serious concerns about any kind of centralized Identity Providers (IdPs) as used in many areas of our daily life (e.g. in social logins). In the digital age our personal information is stored on computer systems. Databases store millions of records that are hosted on servers or in data centers which often belong to private companies. This probably sensitive information is stored centrally and is thus often at risk from data theft by hackers."

\[[https://www.switch.ch/export/sites/default/about/innovation/.galleries/files/SWITCHInnovationLab\_IDAS.pdf](https://www.switch.ch/export/sites/default/about/innovation/.galleries/files/SWITCHInnovationLab_IDAS.pdf)]

"Self-Sovereign Identity (SSI) is a game changer in the area of digital identities. It allows a decentralized management of identities while giving back control to their owner. It solves core privacy problems existing in centralized and federated identity models and offers new ways of using identities (e.g. user accounts) and official documents (e.g. diplomas) in the form of verifiable credentials."

\[[https://www.adnovum.ch/en/incubator/innovation\_initiatives/self\_sovereign\_identity.html](https://www.adnovum.ch/en/incubator/innovation_initiatives/self_sovereign_identity.html)]

"In a world of changing privacy regulations, identity theft, and online anonymity, identity is a precious and complex concept. Self-Sovereign Identity (SSI) is a set of technologies that move control of digital identity from third party “identity providers” directly to individuals, and it promises to be one of the most important trends for the coming decades."

\[Self-Sovereign Identity - Decentralized digital identity and verifiable credentials, May 2021, ISBN 9781617296598]

Overall, it seems the need for secure communication and secure exchange of personal data is a need.

## Our own Customer Research: Survey

We asked people around the world, about our idea and identity management overall. About the importance and satisfaction around our topic.

So we asked following features (1 not important/satisfied - 5 super important/satisfied):

IndexFeatureAvg ImportanceAvg SatisfactionAyour personal data (name, email, password, date of birth, etc.) are only stored with you and not somewhere in a "cloud" or with a provider.\*3.1764705882.471Byou can decide and control who can see your personal data (name, email, date of birth etc.)\*4.1764705882.765Cyou can confirm individual attributes of yourself (e.g. "Yes, I'm over 18 years old") without having to show all the detailed data (e.g. full date of birth)\*3.2941176472.353Dyou can obtain a service with an advantage (e.g. cheaper price) if you provide data about yourself\*2.3529411762.118Eyou have transparency about which personal data you have shared with which organization/website.\*4.1176470592.059Fto know how long which organization stores your data\*3.4117647062.235Gknowing which organization is sharing your data with whom else4.1176470591.765Hto know exactly to what extent a login service (e.g. Facebook, Google) tracks your activities across different websites in order to send you targeted advertising\*3.5294117651.882Iyou can decide for yourself what online services (e.g. Facebook) you use often store or evaluate about you - i.e. what you like, do, are, have\*3.3529411761.941Jthat you can log into websites on the computer with biometric features (fingerprint, FaceID, ...) without having to enter a password3.8235294122.647

We clearly see that the feature "knowing which organization is sharing your data with whom else" has the highest importance and less satisfaction. 

![](attachments/21792483/21792789.png?height=250)

*G and E have the highest importance value and the least satisfaction value,  
so they indicate the strongest opportunities for innovation!*

*B has the strongest importance value, but a slightly higher satisfaction value,  
so this indicates a hygiene requirement, which so or so is expected by users!*

**So results are following top 4 features** 

1. **knowing which organization is sharing your data with whom else**
2. **you have transparency about which personal data you have shared with which organization/website.**
3. **that you can log into websites on the computer with biometric features (fingerprint, FaceID, ...) without having to enter a password**
4. **you can decide and control who can see your personal data (name, email, date of birth etc.)\***

We asked for wished features and got following results:

FeatureAnswersAthat all your personal data is only \*stored with you (locally)\*25%Bthat you can define \*who can see your personal data\*40%Cthat you can \*confirm individual attributes of yourself \*(e.g. "Yes, I am over 18 years old") without having to show all the detailed data10%Dthat you have an \*advantage* (e.g. lower price) \*if you provide your data\*15%Ethat you can see in an overview \*which of your personal data is used by whom\*35%Fthat you can see in an overview \*how long who is storing your data\*5%Gknowing which organization \*is sharing your data with whom else\*30%Hto see as an overview which of your \*online activities* the login services (like Google, Facebook etc) are \*tracking regarding across different websites\*15%Ithat you can \*determine* which of your \*personal data are stored by online services \*which you use often15%Jthat you can \*log into \*websites particularly \*comfortably and easily\*35%KOther5%

**The result is the top 3 wished features:**

1. **that you can define who can see your personal data**
2. **that you can \*log into \*websites particularly \*comfortably and easily\***
3. **that you can see in an overview which of your personal data is used by whom**
4. **knowing which organization \*is sharing your data with whom else\***

## Attachments:

![](images/icons/bullet_blue.gif) [image2022-1-24\_17-36-28.png](attachments/21792483/21792484.png) (image/png)  
![](images/icons/bullet_blue.gif) [LoginWithout.png](attachments/21792483/21792815.png) (image/png)  
![](images/icons/bullet_blue.gif) [Picture123213213.png](attachments/21792483/21792789.png) (image/png)

Document generated by Confluence on Nov 26, 2024 16:16

[Atlassian](http://www.atlassian.com/)
