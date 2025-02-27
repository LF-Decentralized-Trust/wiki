1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Py Maintainers Meetings](ACA-Py-Maintainers-Meetings_18506202.html)

# Hyperledger Aries : 2024-03-12 Aries Cloud Agent - Python Maintainers Meeting

Created by Stephen Curran, last modified on Mar 11, 2024

## Summary:

Topics:

- PRs
- Issues
- Release 1.0.0
- Adding support in ACA-Py for AnonCreds in W3C Format
- OOB Invitations Supporting Peer DIDs and Connection Reuse
- Upgrading Wallet Types

**Zoom Link**: [https://zoom.us/j/91279968714?pwd=Yk9GVVNLOFE1cklkSk51UEZQTklOQT09](https://zoom.us/j/91279968714?pwd=Yk9GVVNLOFE1cklkSk51UEZQTklOQT09)

**Call Time**: 9:00 Pacific / 18:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
  
  - 2824 - ready?
  - 2816 - did rotate - ready?
  - 2748 - status?
    
    - Discussion about ACA-Py support DID Exchange v1.1, v1.0, both.
- [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
- Adding support in ACA-Py for AnonCreds in W3C Format – update from[Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- OOB Invitations Supporting Peer DIDs and Connection Reuse – update on implementation
- Upgrading Wallet Types – update on implementation
- Release 1.0
- Open Discussion

## Upcoming Meeting Topics:

## Future Topics

- Sonar Cloud - is this actually working? Add issue to take a look – perhaps Wade or Jason Syrotuck.
- OpenAPI - Indicio is doing post processing on the OpenAPI file, because what is in the repo is not especially useful.
  
  - too many values being marked as optional – especially on receipt of results from the Admin API.
  - multiple use of the schema – technically they are optional in other places, but not in the OpenAPI
  - Response schemas aren't enforced allowing for returned values to differ
- Code coverage reports on ACA-Py

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
