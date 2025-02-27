1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2022 Bifold Meetings](2022-Bifold-Meetings_18515892.html)

# Hyperledger Aries : 2022-10-25 Aries Bifold Users Group Community Meeting

Created by Jason Leach, last modified on Oct 25, 2022

## Summary

Planned Topics:

- OCA Work Progress
- Biometrics updates
- Bugs

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

- Name (Organization) &lt;email&gt;
- Jason Leach (Fullboar Creative, Corp. / BC Gov) &lt;jason.leach@fullboar.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence)(AffinitiQuest) &lt;warren@affinitiquest.io&gt;

## Announcements

- None.

## Deployments and Work Updates

- Biometrics - done, can now toggle in settings
- Technical debt cleanup and documentation planned.
  
  - Rename source folders PR In
  - Will add more tickets to the GitHub repo.
- Minor update to AFJ

## Agenda

- Bug in first credential (delayed).
  
  - Join Discord for more info on the conversation;
  - Alberto tested pickup protocol v2 (issue still exists);
  - May need to patch agent to force a response (AFJ). The response is not being sent and may be leaving the connection in an uninit state;
  - Noted in the logs (mediator) that connection is not setup;
  - Will continue to debug. Next step to patch AFJ as per above to force connection response.
- Move to yarn.
- React Native Upgrade status (Indecio)
  
  - WIP. Jason will contact James / Ryan for a status update.

## Next Meeting

- Get an update on RN 0.70.0 update;
- Report on mediator connection bug;
- Jason to do a demo on how to customize Bifold (override screens);
- Using Android API 31 as base (upgraded from API 30);
- AFJ 0.3.0 alpha out - update to Bifold shortly after release of non-beta.
- Warren:
  
  - NFC or BT Integration;
  - Deep linking;
  - Status of OOB.

## Future Topics

- Machine Readable Governance Presentation - Mike
- How should we implement Machine Readable Governance?

## Action items

- How to move from v1 to v2 for present proof and issue credential. Will we need to deal with two different screens as both v1 and v2 are supported.
- Support OOB.

# Recording

- Not available for this call.

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
