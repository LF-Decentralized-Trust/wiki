1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-05-03 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Char Howland on May 03, 2022

## Summary:

Planned Topics:

- Getting to release 0.7.4
- Aries Endorser Service – a new repo [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- Connections and Authentication in Aries

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Chat: 
  
  - 08:24:10 From Timo Glastra : In addition to the allow list for connections, having an allow list for dids would also be useful (in an application we're building we do it based on did)
  - 08:29:51 From Colton Wolkins : Will take a deeper look into what's there and what the requirements currently are. Thank you for starting the project!
  - 08:34:12 From Colton Wolkins : My biggest concern with authentication is a problem that Discord has with their QR Code system. I look forward to see how everything pans out in the future
  - 08:41:07 From Paul Wenzel : [https://github.com/hyperledger/aries-cloudagent-python/issues/1743](https://github.com/hyperledger/aries-cloudagent-python/issues/1743)
  - 08:46:09 From Fabio Tagliaferro : The JSON-LD Credentials in ACA-Py tutorial lacks the Present Proof section [https://github.com/hyperledger/aries-cloudagent-python/blob/main/JsonLdCredentials.md#present-proof](https://github.com/hyperledger/aries-cloudagent-python/blob/main/JsonLdCredentials.md#present-proof)
    
    In case, I would be happy to contribute to improve the tutorial with the missing section
    
    This could be an alternative to follow [https://github.com/hyperledger/aries-cloudagent-python/blob/main/demo/AliceWantsAJsonCredential.md](https://github.com/hyperledger/aries-cloudagent-python/blob/main/demo/AliceWantsAJsonCredential.md)
    
    But I found it confusing with some endpoints that I cannot find in a non-demo ACA-py agent
    
    Namely: /issue-credential-2.0/send-offer and /request-presentation-2.0/request-proof
    
    In the meanwhile, could you please link some useful resources to use the BBS+ credential for a verifiable presentation?
  - 08:51:29 From Colton Wolkins : I'm not 100% certain if revocation entries are endorsed ATM. I'd have to double check
  - 08:53:10 From Ian Costanzo : It’s configurable by ledger
  - 08:53:48 From Ian Costanzo : By default the tails file location and the original accumulator has to be endorsed, but when crews are revoked and the updated accumulator is written that doesn’t need to be endorsed
  - 08:54:03 From Wade Barnes : Currently on most networks rev\_reg\_entries do not need to be endorsed, however there is nothing stopping a network from enforcing the rule, so we've decided to have the ability to send all transactions through an endorser.
  - 08:54:29 From Colton Wolkins : Right x3
  - 08:55:01 From Colton Wolkins : I just don't remember seeing signatures on the Revocation records the last time I was playing with Author/Endorser

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)(Indicio) &lt;colton@indicio.tech&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - Aries Cloud Agent Python
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - Aries-VCR/OrgBook BC Deployment
  - Issuer Kit - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BPA - Business Partner Agent for B2B use of VCs
  - BC Wallet – based on Aries Framework JavaScript and Aries Bifold
  - Traction

## Agenda

- Getting to release 0.7.4 – what is needed after RC1
  
  - [PRs since Release 0.7.4-RC1](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-04-28) - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- Aries Endorser Service – a new repo [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
- Connections and Authentication in Aries
- Dealing with the issues of a failure to access a tails server when needed
  
  - For provers – they can cache the tails file to reduce the need to contact the tails service
  - For issuers it's trickier as you (currently) have to write the ledger transaction and then upload the tails files
    
    - If you can't write to the tails file, it's too late.
    - Per @ianco Best thing to do is write the tails file first, then write to the ledger.
      
      - Further mitigations – use multiple tails file servers and fallback to other ones when needed.
      - Even possible – when a tails file write fails, host the tails file on the ACA-Py instance – and let the site Admin know that was done...
  - Other solution – replace the current revocation method with a new one that doesn't need tails files...

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496306/18516237.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
