1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2023 Bifold Meetings](2023-Bifold-Meetings_18517232.html)

# Hyperledger Aries : 2023-03-28 Aries Bifold Users Group Community Meeting

Created by James Ebert, last modified by Alexander Shenshin on Apr 13, 2023

## Summary

Planned Topics:

- Mediator Issues Review

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
  - [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
  - [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) (Instnt, Inc.) &lt;alberto@instnt.org&gt;
  - [Mostafa Youssef](https://lf-hyperledger.atlassian.net/wiki/people/5c6dd5f88a38a065324b668a?ref=confluence) (Ontario Gov) &lt;mostafa.youssef@ontario.ca&gt;
  - [Clecio Varjao](https://lf-hyperledger.atlassian.net/wiki/people/557058:f9e1bfa2-a82c-4b68-85ee-627507d593d9?ref=confluence)  (Government of BC) &lt;clecio.varjao@gov.bc.ca&gt;
  - [Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) (DSR) &lt;artem.ivanov@dsr-corporation.com&gt;
  - [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) (DSR Corporation) &lt;alexander.shenshin@dsr-corporation.com&gt;

## Announcements

IIW – April 18- 20

## Agenda

- Mono-repo re-org PR (really close) - [https://github.com/hyperledger/aries-mobile-agent-react-native/pull/641](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/641)
- Mediator Issues Review - Akiff / Clecio
  
  - Mediator w/ACA-Py
    
    - Slow, first time connects, dropped messages
    - Overall instability as ACA-Py running as a mediator
    - Not able to run as a high-availability instance
  - [https://github.com/fullboar/mediator-test-script](https://github.com/fullboar/mediator-test-script)
    
    - ACA-Py 0.8.0 (using RC0)
      
      - ACA-Py 0.8.0 fully released 2 weeks ago
      - Encountered issues with the upgrade migration scripts
  - Was going to try spinning up AFJ as mediator
  - Monitoring is a key thing missing from the mediator
    
    - Needs to be in the routing level
  - Timeouts on connecting to the mediator
    
    - Not consistent – more prominent during the startup
  - ACA-Py – low CPU resource can throttle and doesn't actually do a lot due to thread switching
    
    - Increase resources significantly to address
  - Pickup v2 protocol Live Mode development
    
    - Not happening as of right now – Clecio
  - Maybe we can aggregate in the aries-mediator-service
    
    - [https://github.com/hyperledger/aries-mediator-service/issues](https://github.com/hyperledger/aries-mediator-service/issues)
  - People running mediators
    
    - Alberto - Running ACA-Py mediator
      
      - 95% of the time it's okay – issues especially at the startup of the agent
    - Indicio - Running ACA-Py mediator w/Pickup Plugin
  - Tasks:
    
    - Monitoring script development
      
      - Ontario Upgrade Testing could be adapted to do this potentially
    - Update ACA-Py mediator to 0.8.0
      
      - Ontario report significant performance improvements
- Updating the Node version
  
  - Why do we need an upper limit?
  - #675 - remove upper limit
- Artem – Mobile Verifier Demo
- Update to AFJ 0.4.x;
- Creating an AFJ [mediator](https://github.com/hyperledger/aries-mediator-service) to keep alongside the ACA-py version;
- First work on new repo design will be to break out OCA into an NPM package.

## Next Meeting

## Future Topics

- Indy ledger namespaces
- Machine Readable Governance Presentation - Mike
- How should we implement Machine Readable Governance?
- Bifold architecture - what's next?

## New Action Items

- Jason to come up with a road map for upgrading to RN 0.7x.y for next meeting.
- Jason to create or move Issue for verifier developer feature in Bifold.
- Jason to add Codecov report / bot to repo as a PR check.
  
  - Consider adding CodeQL from Github to find issues (security or otherwise)

<!--THE END-->

- Jason to create a draft maintainers file as PR for community review.
  
  - Ref. [https://github.com/hyperledger/anoncreds-spec/blob/main/MAINTAINERS.md](https://github.com/hyperledger/anoncreds-spec/blob/main/MAINTAINERS.md)

<!--THE END-->

- Need to update Sovrin genesis file and check network availability.
- Fetch genesis transaction as part of a build step.
- Understand if the wallet can update the genesis transaction in the field (post build).
- Problem with pick-up plugin (pickup v2) with mediators. The first message is dropped.
- Clecio will help update ZMQ in indy and give a new build to James.
- James to present some architecture ideas at the next Bifold meeting.

# Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18503637/18517856.txt "Download")

Mar 28, 2023 by [James Ebert](/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18503637/18517856.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503637/18517857.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503637/18517855.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
