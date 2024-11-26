1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-04-02 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Patrick St-Louis on Apr 02, 2024

## Summary:

Topics:

- Status Update did:peer and AFJ Interop – where we are
- Status ACA-Py 0.12.0
- Status Update AnonCreds RS
- Cleanup of Invitations for Reuse and did:peer:2/4 usage
- Open Discussion

## **Zoom Link**: [https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09](https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09)

## **Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

- IIW coming up April 16-18.
  
  - Thread in Hyperledger Discord on IIW.
- Identity Working Group – this Thursday [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) on ecosystem building

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) (DTLab-LabCN/Open Security and Identity inc.) &lt;patrick.st-louis@opsecid.ca&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Status Updates:
  
  - AnonCreds RS in ACA-Py
    
    - PRs for AnonCreds+CredX concurrently – after the 0.12.0 release
    - Upgrade script – complete.
  - did:peer and AFJ Interop
    
    - Connection reuse for did:peer:2/4
- Status of ACA-Py 0.12.0
  
  - Additional PRs to go into the release? Yes – list: 
    
    - PR 2862
    - Issue [2859](https://github.com/hyperledger/aries-cloudagent-python/issues/2859)
  - Another update – missing verification method in VC-DI.
  - Additional concepts? No
- Status of ACA-Py 1.0.0 Release:
  
  - Checklist [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/2753), labelled [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3A1.0.0) and [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20label%3A1.0.0)
    
    - Other issues/PRs to be added?
    - PR 2860 - handling authorization to update base/tenant wallet.
  - Should we wait on the AnonCreds RS work?
  - LTS Considerations per [Aries RFC 0799 Long Term Support](https://github.com/hyperledger/aries-rfcs/tree/main/concepts/0799-long-term-support)
  - Other considerations?
- Logging for Tenants - [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) is working on this.
  
  - Trying to refactor it a bit – goal is to make it multi-tenant
  - Any ideas on thoughts on making it easier/cleaner?
  - First time – change every instance of logger being used – painful change.
    
    - Should be able to configure it without changing every instance.
    - Use the logging interface and inject something about the tenant.
  - Should the multi-tenant be separated from the single-tenant logging?
- Should we switch to "mutli-tenancy" always – where the current non-multi-tenant is simply multi-tenant with just one tenant.
  
  - Reduce complexity, reduce branches in code.
  - Once Indy SDK support is dropped, it will be easier since Askar is inherently like that.
  - Interesting differences in approaches, both of which are viable:
    
    - Traction – independent controllers one per traction tenant.
    - Single controller – that manages each of the tenants.
- DISCUSS: When to officially drop support for the Indy SDK?
- How to transition to did:indy?
- Vulnerability in an OpenSSH dependency library disclosed last Friday
  
  - Long time GitHub contributor tried to push a remote execution – in xz-utils - bleeding edge version, but caught before it got to the major distributions.
  - Reminder to stay on the lookout for dependencies and vulnerabilities

## Upcoming Meeting Topics:

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
