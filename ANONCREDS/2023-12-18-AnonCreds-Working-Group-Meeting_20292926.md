1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-12-18 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Jan 05, 2024

## Summary

- Eliminating the need for an AnonCreds JSON-LD `@context`
- Aries Issue Credential and Present Proof attachment formats
- Open Discussion

## Time: 7:00 Pacific / 16:00 Central Europe Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

## Recording:

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Repositories:

- AnonCreds Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
- Any updates to the Agenda?

## Agenda

Open Issues

- Eliminating having a special \`@context\` for AnonCreds
  
  - Issue: [https://github.com/hyperledger/anoncreds-spec/issues/192](https://github.com/hyperledger/anoncreds-spec/issues/192)
  - HackMD: [https://hackmd.io/@BYJVN-mpSCe5H3eaIw7-7g/ryk4dvIIp](https://hackmd.io/@BYJVN-mpSCe5H3eaIw7-7g/ryk4dvIIp)
  - [Presentation](https://docs.google.com/presentation/d/1pVIQWoUq7mRdWwKVK20gq73LSJuyqluommw_bj_QzQU/edit?usp=sharing)
  - Discuss the updates needed to implement the changes
  - Idea: Having a commit-time "config" setting for 1.0 vs. 2.0 (or can we do better?)
  - Results documented in issue 192 (linked above)
- Aries Issue Credential / Present Proof Attachments
  
  - Current: [Indy](https://github.com/hyperledger/aries-rfcs/tree/main/features/0592-indy-attachments), [JSON-LD](https://github.com/hyperledger/aries-rfcs/tree/main/features/0593-json-ld-cred-attach) - which do we use, or should we define another that (also) handles JWTs?
  - HackMD: [https://hackmd.io/JEIOxf\_ETnaX33kTIu7YJw?view](https://hackmd.io/JEIOxf_ETnaX33kTIu7YJw?view)
  - Outcome still to be defined.  Leading proposals:
    
    - Issue either:
      
      - With RFC 0592/0771 and add handling for an extra an proof type, or
      - With the new attachment format being proposed by Timo
    - Present either:
      
      - With RFC 0592/0771 for AnonCreds presentations and RFC 0510 (DIF Presentation Exchange) for JSON-LD presentations, or
      - With RFC 0510 for both AnonCreds and JSON-LD presentations
        
        - Extending the 0510 handling for generating/verifying AnonCreds presentations by automating the finding of AnonCreds source VCs for a presentation from DIF PE data, and creating a DIF PE Submission.
          
          - Challenge: I think (to be confirmed), an AnonCreds presentation requires including an AnonCreds-format presentation request. Can that be produced?  Should it be, since the verifier already has it...
      - *NOTE*: If an AnonCreds VC is to also have a non-AnonCreds DataIntegrityProof that also has holder binding, the AnonCreds VC **MUST** have an "id" field explicitly added, and hold a DID.  We can document that.
- Chat:
  
  - 07:07:42     From Timo Glastra : what do you think of Manu's suggestion to make the cryptosuite values the same for all and hide the differences between the three in the encoded proof value metadata?
    
    07:08:38     From Timo Glastra : What about: anoncreds-vc-2023, anoncreds-vc-proof-2023, anoncreds-vp-2023
    
    07:16:15     From Andrew Whitehead : * issuanceDate becomes validFrom
    
    07:26:56     From Andrew Whitehead : "@vocab": "[https://www.w3.org/ns/credentials/issuer-dependent#](https://www.w3.org/ns/credentials/issuer-dependent)",
    
    07:31:08     From Stephen Curran : [https://hackmd.io/oTUuyaLdSL6PHGQNpPB-4g?both](https://hackmd.io/oTUuyaLdSL6PHGQNpPB-4g?both)
    
    07:32:46     From Timo Glastra : Instead of hardcoded flag, maybe we can make this an parameter to the create credential/presentation methods?
    
    07:33:04     From Timo Glastra : tbis = the hardcoded flag to switch between v1/v2
    
    07:35:27     From Timo Glastra : [https://hackmd.io/s0qKgg5VQ6WKf5cSrH7Ygw?view](https://hackmd.io/s0qKgg5VQ6WKf5cSrH7Ygw?view)
    
    07:37:02     From Andrew Whitehead : [https://hackmd.io/mpvne7noRa-Q6PVGdkS47g?view](https://hackmd.io/mpvne7noRa-Q6PVGdkS47g?view)
    
    07:39:30     From Andrew Whitehead : [https://tinyurl.com/2xbf363q](https://tinyurl.com/2xbf363q)
    
    07:45:59     From Stephen Curran : [https://docs.google.com/presentation/d/1QbB8U-6qccGb4jd47GjNAErE61AxNBa7KN7azM2LNQE/edit?usp=sharing](https://docs.google.com/presentation/d/1QbB8U-6qccGb4jd47GjNAErE61AxNBa7KN7azM2LNQE/edit?usp=sharing)
    
    07:54:10     From Timo Glastra : We were planning to use DIF PE for presentations yes
    
    08:00:44     From Timo Glastra : Current example for DIF PE: [https://hackmd.io/atAmNhg7QyOVUI\_CMsW\_-w?view#Presentation-Definition](https://hackmd.io/atAmNhg7QyOVUI_CMsW_-w?view#Presentation-Definition)
    
    08:01:06     From Timo Glastra : I'll add some more notes on how to convert between legacy and new format
    
    08:01:34     From Peter ani : Reacted to I'll add some more n... with ":thumbs-up"
    
    08:01:51     From Timo Glastra : I'm feeling quite opposed to hacking 0771 to issue multi-proof w3c credentials
    
    08:02:45     From Tim Bloomfield : I like the new format, but understand the time constraints
    
    08:02:49     From Golda Velez : @Timo Glastra we can get togther this week if you want
    
    08:02:57     From Timo Glastra : Reacted to "@Timo Glastra we can..." with :thumbs-up
    
    08:03:09     From Timo Glastra : yes might be good to get together and construct a plan
    
    08:03:14     From Golda Velez : Reacted to "yes might be good to..." with :100Percent

## Future Calls

## To Dos:

- Issue to talking about what AnonCreds verifies and what is left to the issuer to verify.
- Revocation Interval
  
  - Approach to determine if the holder used an acceptable RevRegistry – see [this Issue comment](https://github.com/hyperledger/anoncreds-spec/issues/132#issuecomment-1400856502)
  - Who calls the AnonCreds method to get the Revocation Registry from the ledger for verification
    
    - Verifier or AnonCreds?
  - To set "validation" to true/false based on the RevRegEntry timestamp in relation to the revocation interval?  [Presentation](https://docs.google.com/presentation/d/11hXNz_BKOx-ljEGj6cXB1dwnEgEBg3ocqoyR7lgZW1I/edit?usp=share_link)
  - Key points:
    
    - 1\. an RevRegEntry is “current” from the time it is written, to the time of the next RevRegEntry
    - 2\. “within the interval” is based on when a RevRegEntry is “current” (see 1.), not its timestamp.
    - 3\. AnonCreds or the Verifier (calling AnonCreds) should calculate “within interval” (using 2.) and mark verification true if the RevRegEntry used by the Prover is within the interval, else false.
      
      - Dangers:
        
        - False-Negatives: If a strict "timestamp used is between from, to" and not based on when a RevReg is "current" (per 2.), we will get "not verified" incorrectly.
        - False-Positives: If we don't do any checking of the timestamp and the interval, the holder could incorrectly use an old RevRegEntry.
    - 4\. General point: AnonCreds should return both a summary (true/false) and if false, additional data about why it was false.
  - Decision – add an optional \`at\_from\_ts\` set of entries, one per NRP, that AnonCreds can use for determining if the holder\_ts is within the Presentation Request interval.

## Action items

- Adding support for W3C Format AnonCreds to the anoncreds implementation and the spec.
- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

## W3C AnonCreds + AFJ Demo

- Aries Framework JavaScript repo: [https://github.com/DSRCorporation/aries-framework-javascript/tree/w3c-demo-poc](https://github.com/DSRCorporation/aries-framework-javascript/tree/w3c-demo-poc)
- Anoncreds-RS library, Anoncreds-NodeJs, and Anoncreds-Shared are built from the branch: [https://github.com/DSRCorporation/anoncreds-rs/tree/anoncreds-wc3-wrappers](https://github.com/DSRCorporation/anoncreds-rs/tree/anoncreds-wc3-wrappers)
  
  - Use main implementation (not included, dropping of `mapping`  and `encoding`  changes)
- Update AFJ `@hyperledger/anoncreds-nodejs`  and \`@hyperledger/anoncreds-shared\` dependencies to use locally built packages

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
