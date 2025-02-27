1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Quality Assurance: Tests, Strategy, Reports](22839728.html)

# Hyperledger Fabric : Hyperledger Fabric v1.2 Release Testing

Created by Tracy Kuhrt on Jan 04, 2019

On July 03, 2018, after the usual Unit Tests and merge jobs tests were executed in every repository in the hyperledger fabric project, a final set of Release Tests were triggered and executed on the released images. These included many from the fabric-samples repository: byfn, efyn with default channel, custom channel, couchdb, node chaincode on x86\_64 and s390x platforms, and fabcar, balance-transfer, fabric-ca samples on x86\_64 and mac. All worked as expected. In addition, many people contributed by running through positive and negative test scenarios with variations of these scripts. Finally, refer back to the [QA Release page](https://wiki.hyperledger.org/projects/fabric/quality_assurance "https://wiki.hyperledger.org/projects/fabric/quality_assurance") for more information about the System Verification Testing (SVT) and the daily automated regression testing that was part of the release verification. Here are the most relevant sets of tests:

- [V1.2 TOP 10 New SVT Tests](https://jira.hyperledger.org/browse/FAB-10853?filter=12248)
- [V1.2 SVT Regression test scripts initiated manually during release testing](https://jira.hyperledger.org/browse/FAB-10853?filter=12197)
- [V1.2 SVT Regression test scripts executed automatically as part of the Continuous Integration daily test suite](https://jira.hyperledger.org/browse/FAB-4683?filter=12202)

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
