1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)
5. [Identity Mixer Support for both Fabric Gateway SDK for Java and Fabric Gateway Client API for Java](Identity-Mixer-Support-for-both-Fabric-Gateway-SDK-for-Java-and-Fabric-Gateway-Client-API-for-Java_21958367.html)

# Hyperledger Mentorship Program : Project Plan - Identity Mixer Support for both Fabric Gateway SDK for Java and Fabric Gateway Client API for Java

Created by kamlesh nagware, last modified by . Kavin on Dec 22, 2022

## **Abstract**

Idemix (Identity Mixer) is a cryptographic protocol suite, which provides strong authentication as well as privacy-preserving features such as **anonymity**, the ability to transact without revealing the identity of the transactor, and **unlinkability**, the ability of a single identity to send multiple transactions without revealing that the transactions were sent by the same identity. More details here - [https://hyperledger-fabric.readthedocs.io/en/release-2.2/idemix.html](https://hyperledger-fabric.readthedocs.io/en/release-2.2/idemix.html)

Currently, **Fabric Gateway SDK for Java** and **Fabric Gateway Client API for Java** doesn't have support to use an Idemix Identities for transactions doing in Hyperledger Fabric. The objective of this mentorship program is to give support to store Idemix Identities in a Wallet and be able to use the same to invoke and query the transaction in a Hyperledger Fabric Network.

## **Mentors**

Name

Time zone

Discord ID

Email ID

### Kamlesh Nagware

ISTknagware#6976  kamlesh.nagware@gmail.com

**Mentee**

Name

Time zone

Discord ID

Email ID

### Kavin Arumugam

ISTKArumugam#1934a.kavin24@gmail.com

Communication channel:  Discord+ Github

**Hyperledger Fabric Repositories involved in this project:** 

- [Fabric SDK for Java](https://github.com/hyperledger/fabric-sdk-java)
- [Fabric Gateway SDK for Java](https://github.com/hyperledger/fabric-gateway-java)
- [Fabric Gateway Client API for Java](https://github.com/hyperledger/fabric-gateway)

## **Deliverables**

- Ability to store Idemix Identity in a Wallet by using Fabric SDK for Java &amp; Fabric Gateway SDK for Java.
- Ability to use Idemix Identity in a Fabric Gateway Client API for Java.
- Ability to use the Stored Idemix Identity from a Wallet to fire transactions to the Hyperledger Fabric Network using Fabric Gateway SDK for Java and be able to invoke &amp; query the transaction by signing it using Fabric Gateway Client API for Java.
- Demonstrate the usage of Identity Mixer Identity by using both Fabric Gateway SDK for Java and Fabric Gateway Client API for Java.

## **Implementation**

- **Fabric SDK for Java:
  
  Goal:** Return Identity Mixer Identity as an Encoded String so that it can be stored in a Wallet.
  
  **Code:** [https://github.com/KarthikKavinA/fabric-sdk-java/commit/5593dd7fcbcd6b22dfb1b387e603e09f2f18cfa9](https://github.com/KarthikKavinA/fabric-sdk-java/commit/5593dd7fcbcd6b22dfb1b387e603e09f2f18cfa9)
  

<!--THE END-->

- **Fabric Gateway SDK for Java:
  
  Goal:** Add an implementation to store an Identity Mixer Identity in a Wallet.
  
  **Code:** [https://github.com/KarthikKavinA/fabric-gateway-java/commit/75c0250034151729abb1089790ea07d1722a4f8b](https://github.com/KarthikKavinA/fabric-gateway-java/commit/75c0250034151729abb1089790ea07d1722a4f8b)
  
- **Fabric Gateway Client API for Java:** (Strongly recommended for applications using Fabric V2.4 and later)
  
  **Goal:** Provide Identity Mixer Identity Signing Capabilities and using the same to invoke &amp; query the transaction
  
  **Code:** [https://github.com/KarthikKavinA/fabric-gateway/commit/75cd65c722ce0bd777e74d658995641aac2b294a](https://github.com/KarthikKavinA/fabric-gateway/commit/75cd65c722ce0bd777e74d658995641aac2b294a)

<!--THE END-->

- **Demo Application for using Idemix Identity in Fabric
  
  Code:** [https://github.com/KarthikKavinA/fabric-idemix-identity-demo](https://github.com/KarthikKavinA/fabric-idemix-identity-demo)

## **Final Project Presentation**

- [**https://docs.google.com/presentation/d/1vWsWKz\_pPhFu3oGbS2sXwFC\_YdpwcGqe/edit?usp=sharing&amp;ouid=115402957320744570442&amp;rtpof=true&amp;sd=true**](https://docs.google.com/presentation/d/1vWsWKz_pPhFu3oGbS2sXwFC_YdpwcGqe/edit?usp=sharing&ouid=115402957320744570442&rtpof=true&sd=true)

## **Milestones**

**Eval 1:**

- Ability to store Idemix Identity in a Wallet by using Fabric SDK for Java &amp; Fabric Gateway SDK for Java.

**Eval 2:**

- Ability to use the Stored Idemix Identity from a Wallet to fire transactions to the Hyperledger Fabric Network using Fabric Gateway SDK for Java.

**Eval 3:**

- Ability to use Idemix Identity in a Fabric Gateway Client API for Java.
- Able to invoke &amp; query the transaction by signing it using Fabric Gateway Client API for Java.

**Eval 4:**

- Demonstrate the usage of Identity Mixer Identity by using both Fabric Gateway SDK for Java and Fabric Gateway Client API for Java.

## **Timeline**

Dates

Tasks/Plan

Status

**June 1 - June 14**

- Attend Hyperledger Mentorship Program 2022 Onboarding Meeting
- Mentor &lt;&gt; Mentee - Intro
- Introduction to Hyperledger Fabric and its SDKs
- Short Study on Membership Service Provider (X509 &amp; Idemix) in Fabric
  

Done**June 15 - June 28**

- Introduction to Identity Mixer
- Actors involved in Idemix Flow &amp; How to use in Fabric
- Discussion about Project Plan with Mentor and Defining the Timelines, Milestones and Deliverables

Done

**June 29 - July 12**

- Install Prerequisites and Bring up &amp; play with the sample Fabric Network
- Setting Up and Configuring the network to fit for Idemix Usage
- Identification of Basic flow for using Identity Mixer in Fabric

Done**July 13 - July 26**Basic Flow Test of Idemix Usage in Fabric:

1. Issuer - Fabric CA
   
   1. By default, Fabric CA is configured to issue Idemix Credentials
2. Verifier - IdemixMSP in Channel Configuration
   
   1. Creating &amp; Specifying Idemix MSP in "configtx.yaml"
   2. Generate Idemix Organization MSP Definition using "configtxgen" in form of JSON
   3. Updating Channel Configuration to update Idemix Organization MSP by Existing Organization Admin (with necessary approvals)
3. User - From CLI (now) / Java SDK (later)
   
   1. Generate Idemix Credential for an User with Idemixgen Tool but with "Fabric CA Idemix Credentials"
   2. Export Necessary ENV Variables.
   3. Submit a Transaction to Network using an "idemix" User

Done**July 27 - Aug 9**

- Read the First Time Contributor Guidelines
  
  ( [https://hyperledger-fabric.readthedocs.io/en/latest/github/github.html](https://hyperledger-fabric.readthedocs.io/en/latest/github/github.html) )
- Setting up the development environment for fabric-sdk-java &amp; fabric-gateway-java
- Get the Basic Understanding of fabric-sdk-java
- Add an API in fabric-sdk-java to get the Serialized Idemix Enrollment
- Build &amp; Test the SDK

Done**Aug 10 - Aug 23**

- Get the Basic Understanding of fabric-gateway-java
- Implementation of an Idemix Identity Provider
- Modification in the Gateway Implementation to add an Idemix Identity Provider
  
  (Currently, it is hardcoded to use only x509 Identity Provider)
- Modification of Identity Providers in Wallet Implementation
- Build and Test the SDK

Done**Aug 24 - Sept 6**

- Write a Code to submit a transaction to the network by selecting an Idemix Identity from a Wallet using fabric-java-sdk &amp; fabric-gateway-java repository

Done**Sept 7 - Oct 4**

- Execute the samples from fabric-samples with Fabric v2.4+ for better understanding
- Setup the development environment for Fabric Gateway Client API for Java
- Create Fork, Clone the SDK to local and build it.
- Go through the Fabric Gateway Client API for Java

Done**Oct 5 - Nov 1**

- Lift the Identity Mixer Implementation from fabric-sdk-java
- Fit the Identity Mixer Implementation into fabric-gateway
- Implement the Hash Implementation to generate digest of messages by providing the complete messages to send for Idemix Signing Implementation
- Update to v1.1.2 to fix an issue with the Transaction ID when a non-default hash implementation is supplied

Done**Nov 2 - Dec 19**

- Build the fabric-gateway sdk and test it
- Create newIdemixSigner() function to specify in the signing implementation to sign messages sent to the network
- Create newIdemixIdentity() function to specify the Identity Mixer Client Identity to connect to the network
- Create a sample code to demonstrate the usage of Idemix Identity using Fabric Gateway SDK for Java &amp; Fabric Gateway Client API for Java

Done

## **Discussions &amp; Clarifications**

- [**https://discord.com/channels/905194001349627914/946761626072277002**](https://discord.com/channels/905194001349627914/946761626072277002)
- [**https://discord.com/channels/905194001349627914/943089887589048350/945341135977582642**](https://discord.com/channels/905194001349627914/943089887589048350/945341135977582642)
- **[https://discord.com/channels/905194001349627914/1052794417917984788](https://discord.com/channels/905194001349627914/1052794417917984788)**
  

## **Project Result**

## **Demo Video**

- [**https://drive.google.com/file/d/1\_Ii\_cfiHSRMUdmNW-bPGUqqk96htGoly/view?usp=sharing**](https://drive.google.com/file/d/1_Ii_cfiHSRMUdmNW-bPGUqqk96htGoly/view?usp=sharing)

## **Demo Application**

- [**https://github.com/KarthikKavinA/fabric-idemix-identity-demo**](https://github.com/KarthikKavinA/fabric-idemix-identity-demo)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21958819/21967198.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
