1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-04-30 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on May 01, 2024

## Summary:

Topics:

- Release Planning:
  
  - 0.12.1
- PR Merges for pending 1.0.0
- Adding Support in ACA-Py for DIDComm v2
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

## Attendees

- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc / BC Gov) &lt;wade@neoterictech.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (Quartech / BC Gov) &lt;emiliano.sune@quartech.com&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Status of ACA-Py 0.12.1
  
  - Release 0.12.1rc1 available – any issues found?
  - Potential issue – the "holder\_did" / "entropy" issue – [Issue 2923](https://github.com/hyperledger/aries-cloudagent-python/issues/2923)
    
    - Limited to the AnonCreds in W3C VCDM Format code?
  - Anything else to add?
- Once 0.12.1 is out – ready for 1.0.0rc4?
  
  - Include the tenant authorization changes?
  
  <!--THE END-->
  
  - Wait for the drop Indy SDK to be ready to merge?
  - AnonCreds RS PRs – finally!
- Main Topic: Adding DIDComm v2 Support to ACA-Py – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) 
  
  - Uses DMP: [https://github.com/Indicio-tech/didcomm-messaging-python](https://github.com/Indicio-tech/didcomm-messaging-python)
  - [https://github.com/frostyfrog/didcomm-v2-test-util](https://github.com/frostyfrog/didcomm-v2-test-util)
  - [https://github.com/Indicio-tech/aries-cloudagent-python/tree/feat/didcommv2-proof-of-concept](https://github.com/Indicio-tech/aries-cloudagent-python/tree/feat/didcommv2-proof-of-concept)
  - Diff: [https://github.com/hyperledger/aries-cloudagent-python/compare/main...Indicio-tech:aries-cloudagent-python:feat/didcommv2-proof-of-concept](https://github.com/hyperledger/aries-cloudagent-python/compare/main...Indicio-tech:aries-cloudagent-python:feat/didcommv2-proof-of-concept)
- ED25519 2020 Verification of JSON-LD Signatures
  
  - Can issue the credentials
  - When trying to verify – looking for the old style (2018) format – needs to be update
    
    - Verification is failing because decoding the public key incorrectly – wrong key, looking for base58 key, should be looking for multi-base.
    - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) does real time debugging and identifies the problem.  Cool!
      
      - Likely here: [https://github.com/hyperledger/aries-cloudagent-python/blob/3892e8cfa8fbe7cccc5d20f2e80762ef67bc5a66/aries\_cloudagent/vc/ld\_proofs/crypto/wallet\_key\_pair.py#L62-L73](https://github.com/hyperledger/aries-cloudagent-python/blob/3892e8cfa8fbe7cccc5d20f2e80762ef67bc5a66/aries_cloudagent/vc/ld_proofs/crypto/wallet_key_pair.py#L62-L73)
  - Decoding is likely in ACA-Py
- VCDM 2.0 – need to add support for that.
  
  - Be able to receive/process 2.0 and 1.1
  - Flag at issue time to send 1.1 or 2.0?
  - Discussion for tomorrow at Aries Working Group call to discuss the new vc-di attachment format.
  - How to manage the transition from the current JSON-LD vs using the VC-DI attachment format?
    
    - How to retain backwards compatibility?
    - How to use the new VC-DI attachments.
    - Importance – using ACA-Py with VC-API – see this issue: [https://github.com/w3c-ccg/vc-api/pull/382](https://github.com/w3c-ccg/vc-api/pull/382)
- Open Discussion

## Upcoming Meeting Topics:

## Future Topics

- Formal test plan
  
  - We go through a process of release candidates but we often still end up discovering bugs after releases are out
  - Daniel to create an issue to start a discussion

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
