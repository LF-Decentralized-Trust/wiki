1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2023 Bifold Meetings](2023-Bifold-Meetings_18517232.html)

# Hyperledger Aries : 2023-07-04 Aries Bifold Users Group Community Meeting

Created by Jason Leach, last modified on Jul 04, 2023

## Summary

Planned Topics:

- Bifold Update;
- Planned Work;
- Discussion of Issues or PRs

## Community Meeting Policies

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

Take the opportunity to introduce yourself or organization. Let the community know what interest you have in the Bifold effort.

## Attendees

Record your attendance for posterity, and allow others may contact you if needed.

- - Name (Organization) &lt;email&gt;
  - [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar Creative / Government of BC) &lt;jason.leach@[fullboar.ca](http://fullboar.ca)&gt;
  - [Mostafa Youssef](https://lf-hyperledger.atlassian.net/wiki/people/5c6dd5f88a38a065324b668a?ref=confluence) &lt;mostafa.youssef@ontario.ca&gt;
  - [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) &lt;alberto@instnt.org&gt;

## Announcements

- AFJ 0.4.0 Merged
- OCA 1.0.0 Published
- Aries to OWF (join the conversation (Wednesdays at 7AM/PT)
- Bifold used for NFC demonstration by an Org (cool demo to open a door)

## Agenda

- Bifold update
  
  - Fixed bugs, lots of testing, more bugs;
  - Next sprint, TBD;
  
  <!--THE END-->
  
  - Looking to get React Native 0.72.x and we will explore expo modules;
  - Updates to automated workflow (proof / credentials) Ref. [PR 868](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/868)
  - Mobile verifier, moving from connectionless to ephemeral connections.
    
    - Will watch for the \`[aries.vc](http://aries.vc).verifier.once\` goal code;
    - Ephemeral connections are a concept, they require a normal connection but the goal code will indicate it should be deleted;
    - We wan to keep the QR code consistent and less dense.
- Backup &amp; Restore 
  
  - AyanWorks is looking to implement backup and restore;
  - Will hide it behind a feature flag because its a sensitive subject for teams working with high-assurance VCs;
