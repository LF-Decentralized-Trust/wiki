1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-08-16 Indy Contributors Call

Created by Stephen Curran, last modified on Aug 16, 2022

## Summary

- Update on the Indy Ubuntu 20.04 Upgrade
- Root cause of the "mixed node" problem
- Moving the AnonCreds implementation out of Indy – to where?
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)(Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Avast) &lt;richard.esplin@avast.com&gt;

[Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio, PBC) &lt;lynn@indicio.tech&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
- Indy SDK
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Progress on completing the Ubuntu upgrade.
- Update on the Indy Ubuntu 20.04 Upgrade
- Root cause of the "mixed node" problem: [Indy Node issue 1769](https://github.com/hyperledger/indy-node/issues/1769)
- Moving the AnonCreds implementation out of Indy – to where?
  
  - We previously discussed moving AnonCreds to Aries as part of aries-credx.
  - Could also be a DIF project?
- Avast (soon Norton) won't be participating in Indy going forward, at least for 2022. We intend to still participate in Hyperledger Aries. [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)won't be able to attend future meetings or follow the chat, but will try and respond to direct messages.

# Upgrade Notes

- Update on CI/CD Update and Ubuntu Upgrade 
  
  - Indy Shared GHA Repo
  - Indy-Plenum:
  - Indy-Node:
  - indy-test-automation:
  - indy-node-container:
    
    - Call time changed – 17:00 CET / 8:00 Pacific on Thursdays.
  - Indy-SDK build progress
  
  <!--THE END-->
  
  - Related work - Sovrin token-plugin repo being reworked to match indy-node/plenum.
    
    - Mostly done the code.
    - Working on the pipeline
    - Linting issues documented and being cleaned
      
      - [https://github.com/sovrin-foundation/token-plugin/issues/413](https://github.com/sovrin-foundation/token-plugin/issues/413)
- The root cause of the "Mixed Node" issue has been found – and it's not a mixed node issue.
  
  - Christian Bormann has been investigating and looks like he's figured it.
  - **Issue**: The merging of the RevRegEntry arrays into the RevReg was implemented in the past without a specified ordering. Such a merge is implemented differently between Python 3.5 and later, such that the merged array is in a different order in the 20.04 code, and so causes the root hash to be different between implementations. The result of the root hash differences is a 20.04 node as it stands today cannot join consensus.
  - Options to address the issue that were discussed:
    
    - Go back in time and add a ".sort" to the merge command.
      
      - No one admitted to having a time machine, so the idea was dismissed.
    - Rewrite history to update the existing transactions to be sorted, including updating the audit log.
      
      - Deemed highly risky and inappropriate for a blockchain-based solution.
    - Call out to a Python 3.5 program to do the merge.
      
      - Deemed to be a tech debt that must last forever.
    - Write a version of the Python 3.5. merge routine (C code) in Python to get the same order as previously. Use this from now on.
      
      - Deemed a possibility, but with the risk that the Python code would have to work on existing and future transactions.
      - A consideration here is if we can find a pattern that results in a difference in the merge outcomes, such that we think it is safe to use this approach from now on.
    - Write a version of the Python 3.5. merge routine (C code) in Python to get the same order as previously. Add a config transaction to the ledger and use the ".sort" code after the config, use the "old" code before the config.  Make sure that the Python code handles all the transactions before the config.
      
      - This seems the best option, although the logistics at upgrade time are painful.
  - Actions:
    
    - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)to take a look at the [C code here](https://github.com/python/cpython/blob/v3.5.0/Objects/setobject.c) to see about doing a Python version.
    - We should also do some searching on the web to see if others have done that.

## Future Calls

- GDPR and the right to be forgotten – mitigations and approaches.
- Dealing with Indy Node DoS attacks.

<!--THE END-->

- Status of Indy-SDK
  
  - Statement on the future of the Indy SDK: [PR 2329](https://github.com/hyperledger/indy-sdk/pull/2329)
  - Plans for future of Indy CLI (move to Indy VDR?)
  - Indy SDK in test for Indy Node (move to Indy VDR?)
  - Status of GitHub Actions for the Indy-SDK
- Indy bugs
  
  - Using GitHub tags "Good First Issue" and "Help Wanted"
  - [Node 1490](https://github.com/hyperledger/indy-plenum/issues/1490): problems with large catch-up
  - [Plenum 1506](https://github.com/hyperledger/indy-plenum/issues/1506): view change message consensus calculation error

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464601/19466213.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
