1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-08-08 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Ry Jones on Aug 08, 2023

## Summary:

Topics:

- Project: Hyperledger AnonCreds Rust in ACA-Py
- PRs and Other Issues
  
  - Nightly Builds
- Open Discussion

**Zoom Link**: [https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09](https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

- [https://youtu.be/GstX51UnIlE](https://youtu.be/GstX51UnIlE)
- [2023 08 08 Hyperledger Aries Cloud Agent Python Users Group transcript.txt](attachments/18506713/18518577.txt)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Project: Hyperledger AnonCreds Rust in ACA-Py
- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
  
  - Marshmallow PR [#2398](https://github.com/hyperledger/aries-cloudagent-python/pull/2398)
  - Multi-tenant – select ledger for reading/writing – [#2339](https://github.com/hyperledger/aries-cloudagent-python/pull/2339), [#2395](https://github.com/hyperledger/aries-cloudagent-python/pull/2395)
  - Nightly Builds [#2250](https://github.com/hyperledger/aries-cloudagent-python/issues/2250)
  - Pytest and Flake8 [#2400](https://github.com/hyperledger/aries-cloudagent-python/issues/2400)
- Open Discussion
  
  - OpenID4VC – issuer – make it a companion service that calls into ACA-Py vs. within ACA-Py – [Issue #2182](https://github.com/hyperledger/aries-cloudagent-python/issues/2182)
    
    - Requires adding additional public endpoints beyond the DIDComm endpoint.
    - Keeping it as a separate service that calls into ACA-Py for services – storage, signing, etc. – much like vc-authn-oidc
    - Endpoints for preparing (SD-)JWT credentials – similar to the JSON-LD endpoints we have today – sign/verify
    - Alternative – plugin, so that there is a tighter integration with calling ACA-Py utility functions
  - Code Coverage reports – we used to have a report that said exactly what percent increase/decrease on every PR - [Issue #2403](https://github.com/hyperledger/aries-cloudagent-python/issues/2403)
    
    - CodeCov – no longer being used
    - Add ticket about this
  - Okta integration
    
    - [https://github.com/bcgov/vc-authn-oidc](https://github.com/bcgov/vc-authn-oidc)
    - Look at the 2.0-development branch
  - When to stop testing with the Indy SDK? [Issue #2402](https://github.com/hyperledger/aries-cloudagent-python/issues/2402)
    
    - Time to remove those tests? Yes
      
      - Suggestion: Remove all of the tests from the PR Integration Test runs.
      - Nightly run of Indy tests – let's eliminate that as well.
    - Hypothetical: ACA-Py fix needed for using the Indy SDK
      
      - Uncomment out the tests and fix as a branch based on the 0.9.0 tag
    - Note: The chance of another Indy SDK release is very unlikely – way too much technical debt in the code base and (non-functioning) CI/CD pipeline.

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [2023 08 08 Hyperledger Aries Cloud Agent Python Users Group transcript.txt](attachments/18506713/18518577.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
