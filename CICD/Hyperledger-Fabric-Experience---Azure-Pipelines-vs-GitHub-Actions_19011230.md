1. [CI/CD](index.html)
2. [Sovrin resource migration](Sovrin-resource-migration_19011213.html)

# CI/CD : Hyperledger Fabric Experience - Azure Pipelines vs GitHub Actions

Created by Stephen Curran, last modified on Apr 03, 2020

I'll start by introducing myself, I'm [Brett Logan (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/712020:70fd36cb-f719-40fc-993c-9c3f644b7f10?ref=confluence) , I'm part of the Fabric team at IBM. Together Ry and I migrated everything that sits on Azure Pipelines today. I also manage the day-to-day DevOp's operations of all of Fabric repos with regards to AZP, Artifcatory, GitHub Actions, and general GitHub. I'm going to spew some information here on AZP and GHA on the why you might choose one over the other, and some of the stuff we have in the pipeline with AZP (we have a pretty good relationship with the AZP product management team, so we get to Beta test a lot of features and know they are coming long before most of the general public does)

The benefit of GitHub actions is that it is integrated directly into the repository, and you can generally perform operations on the repository that you can’t perform on it using Azure Pipelines, for example you add triggers for specific comments to trigger certain GitHub actions. Actions have a wealth of easily accessible information about the PR that you don’t easily have access to in AZP.

The downside to GitHub actions is that on their open source (free) tier, you are limited to 15 jobs running in parallel at once. The size of the VM’s is also limited to 2vCPU/4GB, which is extraordinarily small for most of our compute and memory intensive use cases (though they do get recycled after each job, so you always start with a fresh VM). They do have the option of bringing your own VM’s, but unlike Jenkins’s, you cannot have dynamic slaves (ones that are created at the start of a job and destroyed at the end of the job) so you have to manage the clean up of your systems after every test run. We spoke with the GHA team at the All Thing’s Open conference last April, and their enterprise play for dynamic build agents will be entirely kubernetes. They have no intention of bringing dynamic VM-based build agents, only bring your own k8s cluster and they will manage the pod lifecycle.

AZP has many of the same initial limitations on their open source (free) tier. For open source projects, they limit you 10 parallel jobs per organization (though they are giving us 40 for free). The VM’s are the same size, 2vCPU/4GB. and are recycled after each job. You can also bring your own static build agents, but again you have to manage cleaning them up after each job. AZP’s enterprise play is going to be both Kubernetes and VM-based dynamic build agents. We are currently performing beta tests for the AZP team on their VM-based dynamic build agents. With this you can select any VM size and image (or create your own image) in the Azure cloud, and they will manage the lifecycle of these VM’s for you (recycling them after each job so you have a fresh VM). With this you can get access to GPU-enabled VM’s as well as specialized hardware Azure has, like Intel SGX-enabled hardware. While we do have to pay for these resources, we can use Azure spot instances to get ridculously cheap hardware (a 4vCPU/16GB spot instance costs $39/mo as opposed to its reserved instance pricing of $213/mo, and since they are dynamically managed, i.e., not running 24/7 the costs are incredibly small, a fleet of 10 VM’s would likely cost less than $100/mo).

Enterprise Artifactory supports pretty much any package type you can image (and also a generic type for storing any generic artifact, like a tarball), and is much easier to manage than Nexus. We have an enterprise account under “[hyperledger.jfrog.io](http://hyperledger.jfrog.io)” and things like docker repos get really nice dns entries automatically when you create new repos, such as, “[hyperledger-fabric.jrog.io/fabric-peer:latest](http://hyperledger-fabric.jrog.io/fabric-peer:latest)” making it much easier to manage URL endpoints.

BinTray is the enterprise release distribution. It differs from Artifactory in that it is a worldwide CDN for business critical applications. Artifactory is hosted out of a single multi-zone datacenter. So for items you need located as close to the source as possible, BinTray is the choice. For artifacts that can handle small amounts of latency, Artifactory is the way to go. We do pay by the GB for both BinTray and Artifactory, though we are working on getting an opensource exemption for Artifactory which will gives us unlimited storage and bandwidth for free. BinTray will always cost money.

I'll also add, you can use GHA and AZP in conjunction, i.e., we use GHA to perform repo level checks, like verifying DCO and comment on PR's with instructions on how to fix PR's missing a DCO signoff, or adding labels to issues and having them automatically merged.

My opinion is, AZP is the best bet for your application if you need agents larger than 2vCPU/4GB

We also get enterprise support with AZP (with 24/7 support and less than 4 hour initial contact), and have direct lines of contact with the Product Management team. We don't have any of that with GHA.

You also have access to MacOS, Windows, Linux, iOS and Android build in AZP. The MacOS builds are limited to their 2vCPU/4GB size, but they are on the 40 agent free tier, so there is no cost to use them, and you can add your own static MacOS agents

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
