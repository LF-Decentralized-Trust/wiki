1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Quality Assurance: Tests, Strategy, Reports](22839728.html)

# Hyperledger Fabric : Getting Started with Fabric CI

Created by Tracy Kuhrt, last modified by Brett Logan on Dec 17, 2019

# ***THIS PAGE IS OUT OF DATE AND BEING UPDATED. FABRIC AND ITS REPOSITORIES HAVE MIGRATED TO GITHUB FOR SCM AND AZURE PIPELINES FOR CI***

### Contributors

NameEmailJessica Wagantall[jwagantall@linuxfoundation.org](mailto:jwagantall@linuxfoundation.org)Ramesh Thoomu[rameshbabu.thoomu@gmail.com](mailto:rameshbabu.thoomu@gmail.com)Scott Zwierzynski[scottz@us.ibm.com](mailto:scottz@us.ibm.com)Vijay Punugubati[Vijay.Punugubati@ibm.com](mailto:Vijay.Punugubati@ibm.com)Brett T Logan[brett.t.logan@ibm.com](mailto:brett.t.logan@ibm.com)

## Summary

The Hyperledger Fabric (and associated) projects utilize various tools and workflows for continuous project development. This documentation will assist you in getting started with using these tools and understanding the workflow(s) our contributors use while working with the Fabric CI infrastructure.

### Finding Help on Hyperledger CI

Welcome to the Hyperledger Fabric community! We are excited that you want to contribute to the Continuous Integration/Release Engineering efforts. You're in the right place to get started. In the event that you need additional assistance, We encourage you to engage with our CI contributors via the following channels:

1. [#ci-pipeline](https://chat.hyperledger.org/channel/ci-pipeline "https://chat.hyperledger.org/channel/ci-pipeline") channel on Rocket.Chat (For general continuous integration discussions)
2. [#fabric-ci](https://chat.hyperledger.org/channel/fabric-ci "https://chat.hyperledger.org/channel/fabric-ci") channel on Rocket.Chat (For fabric continuous integration discussions)
3. [#infra-support](https://chat.hyperledger.org/channel/infra-support "https://chat.hyperledger.org/channel/infra-support") channel on Rocket.Chat (For general infrastructure discussions)
4. Send an email to the [fabric@lists.hyperledger.org](mailto:fabric@lists.hyperledger.org) mailing list
5. Contact [helpdesk@hyperledger.org](mailto:helpdesk@hyperledger.org) for any infrastructure support

## Getting Started with Fabric CI

The Fabric CI environment is comprised of two parallel deployments of the [Jenkins CI](https://jenkins-ci.org/ "https://jenkins-ci.org/") system:

- Jenkins Production, located at [https://jenkins.hyperledger.org/](https://jenkins.hyperledger.org/ "https://jenkins.hyperledger.org/")
- Jenkins Sandbox, located at [https://jenkins.hyperledger.org/sandbox/](https://jenkins.hyperledger.org/sandbox/ "https://jenkins.hyperledger.org/sandbox/")

**Note:** You will notice that both the Jenkins production instance and the Jenkins sandbox instance are both accessible from the same URL, though the sandbox instance is accessed at **/sandbox**.

For more information on how to use the sandbox, use the documentation in [https://github.com/hyperledger/ci-management/blob/master/Sandbox\_Setup.md](https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md "https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md")

### Hyperledger Fabric projects on CI

The table below indicates all of the Hyperledger Projects that are built, tested, verified, and released using the Jenkins CI infrastructure:

ProjectRepositorycello[https://gerrit.hyperledger.org/r/#/admin/projects/cello](https://gerrit.hyperledger.org/r/#/admin/projects/cello)ci-management[https://gerrit.hyperledger.org/r/#/admin/projects/ci-management](https://gerrit.hyperledger.org/r/#/admin/projects/ci-management)fabric[https://gerrit.hyperledger.org/r/#/admin/projects/fabric](https://gerrit.hyperledger.org/r/#/admin/projects/fabric)fabric-baseimage[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-baseimage](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-baseimage)fabric-ca[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-ca](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-ca)fabric-chaincode-java[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-chaincode-java](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-chaincode-java)fabric-chaincode-node[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-chaincode-node](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-chaincode-node)fabric-chaincode-evm[https://gerrit.hyperledger.org/r/admin/repos/fabric-chaincode-evm](https://gerrit.hyperledger.org/r/admin/repos/fabric-chaincode-evm)fabric-chaintool[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-chaintool](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-chaintool)fabric-samples[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-samples](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-samples)fabric-sdk-go[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-go](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-go)fabric-sdk-java[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-java](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-java)fabric-gateway-java[https://gerrit.hyperledger.org/r/admin/repos/fabric-gateway-java](https://gerrit.hyperledger.org/r/admin/repos/fabric-gateway-java)fabric-sdk-node[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-node](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-node)fabric-sdk-py[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-py](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-py)fabric-sdk-rest[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-rest](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-sdk-rest)fabric-test[https://gerrit.hyperledger.org/r/#/admin/projects/fabric-test](https://gerrit.hyperledger.org/r/#/admin/projects/fabric-test)

### Jenkins Dashboard

On the Jenkins dashboard, a list of all Jenkins jobs required to build, test, verify and release each of the Hyperledger Fabric projects is organized and displayed in separate views. For example, the **Fabric** [view](https://jenkins.hyperledger.org/view/fabric/ "https://jenkins.hyperledger.org/view/fabric/") displays each of the jobs related to the fabric project.

Here, all of the Jenkins jobs for testing the Fabric project are displayed. The Jenkins jobs are displayed in a table, and indicates:

- **Status** - the status of the most recently executed job,
- **Name** - the name of the job
- **Last Success** - the last successful run of the job
- **Last Failure** - the last failed run of the job
- **Last Duration** - indicates the length of time the last job took to run

### Jenkins Job Types

Continuing with the **Fabric** project example, the jobs list contains multiple jobs required to accurately build, test, and verify the [Hyperledger Fabric](https://gerrit.hyperledger.org/r/#/admin/projects/fabric) project. The job types for the **Fabric** project are as follows

```
* Verify
  * Unit Tests (performs make linter, make unit-tests)
  * Integration Tests (performs integration tests)
  * Documentation changes (Builds the documentation and ship it to nexus log server)
```

You can check the RTD format of you patch set documentation build here [https://logs.hyperledger.org/production/vex-yul-hyp-jenkins-3/fabric-docs-build-x86\_64/](https://logs.hyperledger.org/production/vex-yul-hyp-jenkins-3/fabric-docs-build-x86_64/)&lt;build\_number&gt;/html

ex: [https://logs.hyperledger.org/production/vex-yul-hyp-jenkins-3/fabric-docs-build-x86\_64/2058/](https://logs.hyperledger.org/production/vex-yul-hyp-jenkins-3/fabric-docs-build-x86_64/2058/)

```
* Merge
   * End-to-End (performs node-sdk e2e, java-sdk e2e, byfn-eyfn tests)
   * Unit-Tests
```

**IMPORTANT NOTE: Although many of the job types listed above are common across all Hyperledger Fabric projects, the list indicated above is specific to the Hyperledger Fabric project. Different projects will have different job types based on their individual build/test/release requirements.**

### Common Job Types

There are several Jenkins job types that are common across **most** Hyperledger Fabric projects. In some cases, you may/may not see all of the common job types in every project. This is heavily dependent on the needs of the Hyperledger Fabric project. That said, let's take a look at each of the most common jobs:

### Verify Jobs

Verify jobs are triggers when a **"patchset-created-event"** is triggered in gerrit. All verify jobs are depends on the patchset parent commit and patchset commit. That tells, verify jobs run on the parent commit on which developer submitted patch not on the latest master code.

### Merge Jobs

Merge jobs triggers when a **“change-merged-event”** event is triggered in gerrit. In all the merge jobs, Jenkins clones the latest master code and perform the tests, unlike verify jobs.

### Release Jobs

Release jobs are triggered after a **“ref-updated-event”** is created in each of the Fabric repositories targeted for release. Release jobs are intended to create to publish docker images, binaries and publish npm modules. For more information regarding the release process, refer to this [Release Process Document](https://github.com/hyperledger/ci-management/blob/master/docs/Release_Process.md#release-process-document).

### Support for varying Architectures

With most job types, the Jenkins build jobs are broken down further to build, test, and release the Hyperledger Fabric projects with support for varying CPU architectures. They include:

- x86\_x64
- s390x (No support beyond 2.0)

### Support for varying test types

Additionally, with most job types, you will notice the Jenkins jobs are further isolated to include a number of test types. Those include:

- End-to-End
- BYFN-EYFN \[byfn, eyfn with (default, custom, CouchDB, node lang chaincode, java lang chaincode, raft.)]
- Fabcar
- Unit Tests
- Smoke/Functional/Performance/Release tests ( More functional tests from the fabric-test repository)

For more information on what each of these test types is used for, refer to the [Hyperledger fabric CI Overview](https://ci-docs.readthedocs.io/en/latest/) documentation.

### CI-Management Repo

The [ci-management repo](https://github.com/hyperledger/ci-management "https://github.com/hyperledger/ci-management") hosts the CI job definitions for all of the Hyperledger Fabric projects integrated with Jenkins. Each job configuration is written in YAML format and built with the [Jenkins Job Builder (JJB)](https://docs.openstack.org/infra/jenkins-job-builder/ "https://docs.openstack.org/infra/jenkins-job-builder/") tool.

### Writing Jenkins Job Definitions

Much of the work inside of Fabric CI involves the creation or modification of Jenkins job definitions. To get a better understanding of how to write Jenkins job definitions, start with reading through the [JJB Job Definitions](https://docs.openstack.org/infra/jenkins-job-builder/definition.html "https://docs.openstack.org/infra/jenkins-job-builder/definition.html") documentation.

### Jenkins Sandbox

ref: [https://github.com/hyperledger/ci-management/blob/master/Sandbox\_Setup.md](https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md "https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md")

When creating or modifying Jenkins job definitions, it is important to know whether or not your job definitions work prior to adding them to the production Jenkins instance. This is why Hyperledger Fabric has provided a [Jenkins Sandbox](https://jenkins.hyperledger.org/sandbox/ "https://jenkins.hyperledger.org/sandbox/") instance, allowing you to test your Jenkins job definitions. To use the Jenkins sandbox, read through the [Sandbox Setup](https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md "https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md") process, which explains how to install Jenkins Job Builder (JJB), as well as testing, updating, and triggering jobs on the Jenkins Sandbox.

### Contributing to Fabric CI

Contributing to the Fabric CI process starts with identifying tasks to work on, and bugs to be fixed. The [JIRA](https://jira.hyperledger.org/ "https://jira.hyperledger.org") site provided by the Hyperledger Community is where to find these items. To narrow down tasks and bugs that are directly related to Fabric CI, use the following URLs:

JIRA filterURLfabric-ci[https://jira.hyperledger.org/issues/?filter=11500](https://jira.hyperledger.org/issues/?filter=11500)

### Comment Phrases to trigger failed jobs

Trigger builds through comments to a commit/change:

Re-verification/trigger of builds is possible in Jenkins by entering any of the below comment phrases as a comment to the Gerrit patch set. To do so, follow the below process:

**Step 1**: Open the failed Gerrit patch set

**Step 2**: Click on **Reply** and type the below comment phrases based on the project and click **Post**

CI jobs listen to the below comment phrases for each fabric project:

**fabric:**

Verify JobsCommentMerge JobsCommentfabric-verify-build-checks-x86\_64Run VerifyBuild/VerifyBuildfabric-merge-x86\_64remerge-xfabric-verify-unit-tests-x86\_64.Run UnitTestfabric-merge-end-2-end-x86\_64remerge-e2e fabric-verify-integration-tests-x86\_64Run IntegrationTestFor all merge jobsremergefabric-docs-build-x86\_64Run DocsBuild

**fabric-ca**:

Verify JobsCommentMerge JobsCommentfabric-ca-verify-x86\_64reverify-xfabric-ca-merge-x86\_64remerge-xfabric-ca-verify-fvt-x86\_64reverify-fvtfabric-ca-merge-fvt-x86\_64remerge-fvtfabric-rtd-verify-jobrecheckfabric-merge-end-2-end-x86\_64remerge-e2e For all verify jobsreverifyFor all merge jobsremerge

**fabric-sdk-java**:

Verify JobsCommentMerge JobsCommentfabric-sdk-java-master-verify-x86\_64reverify-xfabric-sdk-java-master-merge-x86\_64remerge-xfabric-sdk-java-master-verify-1.4-x86\_64reverify-1.4fabric-sdk-java-master-merge-1.4-x86\_64remerge-1.4fabric-sdk-java-release-1.4-verify-x86\_64reverify-xfabric-sdk-java-release-1.4-merge-x86\_64remerge-xFor all verify jobsreverifyFor all merge jobsremerge

**fabric-chaincode-node**:

**fabric-baseimage:**

Verify JobsCommentMerge JobsComment{project}-verify-x86\_64reverify-x{project}-merge-x86\_64remerge-x{project}-verify-s390xreverify-z{project}-merge-s390xremerge-zFor all verify jobsreverifyFor all merge jobsremerge

All other repositories use any of the below comment phrases

**fabric-samples                                   fabric-chaincode-java                      fabric-sdk-go**

**fabric-sdk-node                                 fabric-chaincode-evm                      fabric-sdk-py**

**fabric-gateway-java                         fabric-test**

Verify JobsCommentMerge JobsComment{project}-verify-x86\_64reverify or reverify-x{project}-merge-x86\_64remerge or remerge-x

### Troubleshooting - Failing CI Jobs

For an overview of CI Processes, refer to the FAQ, below.

If you are a developer having difficulty obtaining that green checkmark consistently from hyperledger-jobbuilder because your merge job or verify job fails, then \*create a bug* in Jira to start the process rolling to fix the problem for everyone in the community!

1. Take a look at why your patchset is failing verification. If it seems unrelated to your patchset changes, then…
2. Examine console logs for other patchsets build failures occurring in [Fabric Project builds](https://gerrit.hyperledger.org/r/#/q/status:open). Confirm if any others are seeing build failures with the same symptoms. If so, then…
3. Find out if a bug exists already for your problem. The first place to look is the list of open [CI\_Failure bugs](https://jira.hyperledger.org/browse/FAB-9207?filter=12103). Next, [SEARCH Fabric Issues](https://jira.hyperledger.org/browse/STL-1128?jql=) for your error strings symptoms. If no bug exists for your problem, then…
4. [CREATE a bug](https://jira.hyperledger.org/secure/CreateIssue!default.jspa "https://jira.hyperledger.org/secure/CreateIssue!default.jspa") with severity = 'Highest' and label = 'ci\_failure', and set the appropriate component for triage. Squads regularly review their components bug lists.
5. Alert the community by reaching out to [#fabric-ci](https://chat.hyperledger.org/channel/fabric-ci "https://chat.hyperledger.org/channel/fabric-ci") channel (or [#infra-support](https://chat.hyperledger.org/channel/infra-support "https://chat.hyperledger.org/channel/infra-support") channel, if the issue pertains to network latency issues, such as FAB-7971), where you may find help and discussions of similar topics. For more info, see the CI FAQs, below.

### Frequently Asked Questions

Below is a table that shows you where to find the most informative resources for the most frequently asked questions about Fabric CI.

QuestionResource**Which Fabric projects are currently using CI?**[hyperledger\_fabric\_projects\_on\_ci](http://hyperledger_fabric_projects_on_ci)**What is the process used to build, test, and release Fabric projects?**[https://ci-docs.readthedocs.io/en/latest/](https://ci-docs.readthedocs.io/en/latest/)**Where is the Jenkins CI for Hyperledger Fabric?**[https://jenkins.hyperledger.org/](https://jenkins.hyperledger.org/ "https://jenkins.hyperledger.org/")**Where is the sandbox installation of Jenkins CI for Hyperledger Fabric?**[https://jenkins.hyperledger.org/sandbox](https://jenkins.hyperledger.org/sandbox "https://jenkins.hyperledger.org/sandbox")**Where can I found out more about each of the Jenkins jobs used to build, test, and release Hyperledger Fabric projects?**[https://github.com/hyperledger/ci-management](https://github.com/hyperledger/ci-management "https://github.com/hyperledger/ci-management")**How do I write Jenkins job definitions for use with Hyperledger Fabric projects?**[https://docs.openstack.org/infra/jenkins-job-builder/definition.html](https://docs.openstack.org/infra/jenkins-job-builder/definition.html "https://docs.openstack.org/infra/jenkins-job-builder/definition.html")**How should I test my Jenkins job definitions for use by the Fabric CI process?**[https://github.com/hyperledger/ci-management/blob/master/Sandbox\_Setup.md](https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md "https://github.com/hyperledger/ci-management/blob/master/Sandbox_Setup.md")**I want to find Fabric CI related tasks to work on. Where should I go?**[https://jira.hyperledger.org/issues/?filter=11500](https://jira.hyperledger.org/issues/?filter=11500)**I have questions about Fabric CI. Where should I go for help?**[https://chat.hyperledger.org/channel/ci-pipeline](https://chat.hyperledger.org/channel/ci-pipeline "https://chat.hyperledger.org/channel/ci-pipeline")

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
