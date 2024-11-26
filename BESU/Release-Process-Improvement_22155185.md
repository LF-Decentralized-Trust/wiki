1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Releasing](Releasing_22154097.html)
5. [Archive](Archive_22154100.html)

# Besu : Release Process Improvement

Created by Justin Florentine, last modified on Jan 18, 2022

Goals:

- Remove dependency on any proprietary build tools.
- Require at least 2 people to approve a release.
- Reduce possibility for error during the build process.
- Continue CalVer version numbering scheme.
- Improve artifact publication security.

## Status Quo

Besu currently does branch based release strategy, using a proprietary tool developed by ConsenSys.  Regardless of the branch being released from, a new release branch is created and pushed to origin.  This triggers an additional (arguably unnecessary) build PR for the merge back to the “releasing branch” (master, release-&lt;calver&gt;, etc).  It also forces a “quiet period” where we do not / cannot merge to the branch-to-release.  The branch based flow also submits an additional post-release PR to merge the next project version property (so that build artifacts are &lt;next-calver&gt;-SNAPSHOT).  

This process requires at least 2 contributors to complete the release process because 2 rounds of PR approvals are necessary to proceed.  The requirement for more than one person to participate is an important feature of this process which we want to preserve.

Overall, the branch flow requires 3 CI builds and 2 PR approvals to complete a release.  It seems that this flow was built to support quarterly releases, but was generalized for regular releases also.

While there does exist a proprietary tool by ConsenSys that can be used to facilitate the release, it is not necessary. The simplest possible release process under the current status quo would look like:

1. Preparing release source:
   
   1. For a point release from a release branch (21.10.7 is the example used below):
      
      1. Make a source branch containing all the commits to be released, rooted on previous release commit.
      2. Open a PR into the previous release, causing it to be tested by CI. This can and should happen in advance of the release for team review. Hopefully this is the hardest part of the process.
      3. Add a final commit, that changes the version to the next one being released, usually just removing SNAPSHOT.
   2. release from mainline
      
      1. Make a release branch which points to the commit on main to be released.
      2. Add a final commit, that changes the version to the next one being released.
2. PR opened from the source into either a release or main branch, when merged, that is the signal to deploy the artifacts. The release/main branch is run through the CI process.  Example [https://github.com/hyperledger/besu/pull/3278](https://github.com/hyperledger/besu/pull/3278)
3. Let that build, and the branch name will allow the `publish` job to run. Artifacts should be pushed to the following places:
   
   1. tarfile - [https://hyperledger.jfrog.io/ui/native/besu-binaries/besu/21.10.7/besu-21.10.7.tar.gz](https://hyperledger.jfrog.io/ui/native/besu-binaries/besu/21.10.7/besu-21.10.7.tar.gz)
   2. zipfile - [https://hyperledger.jfrog.io/ui/native/besu-binaries/besu/21.10.7/besu-21.10.7.zip](https://hyperledger.jfrog.io/ui/native/besu-binaries/besu/21.10.7/besu-21.10.7.zip)
4. During the `dockerPublish` job, the docker image is built and tagged with this release number.
   
   1. docker image - [https://hub.docker.com/layers/hyperledger/besu/21.10.7/images/sha256-a984a8ed88931530ebe3cab02c3f1ce928c5821e8d59ad3c897a5a6e111058b8?context=explore](https://hub.docker.com/layers/hyperledger/besu/21.10.7/images/sha256-a984a8ed88931530ebe3cab02c3f1ce928c5821e8d59ad3c897a5a6e111058b8?context=explore)
5. Theoretically, the release is done, and the versioned artifacts have been released and are all publicly available. For instance, any docker stacks running something like Watchtower, will detect a new latest build and deploy it.
6. Releaser publicizes the release by [drafting a release on the github project page](https://github.com/hyperledger/besu/releases).
   
   1. Release is named after the version number.
   2. The Changelog from the Changelog file in source control is pasted into the description.
   3. Direct links to the .tar and .zip are included, as well as the corresponding SHA-256 hashes for each binary.
      
      - **PROBLEM**: if the releaser doesn't download the artifacts from the right section of artifactory (which is [https://hyperledger.jfrog.io/artifactory/besu-binaries/besu/),](https://hyperledger.jfrog.io/artifactory/besu-binaries/besu/%29,) but instead used the /ui/native/... URLs from artifactory, curl will return the intermediate hash pages and your hashes will be all wrong.
7. This will trigger even more reactions from interested automation. For instance, beaconchain watches for these releases, and sends out notifications to users who want to be updated.
8. Documentation is released - this is already tag based!
   
   1. [https://lf-hyperledger.atlassian.net/wiki/display/BESU/Documentation+release+process](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Documentation+release+process)
   2. [https://github.com/hyperledger/besu-docs/releases/tag/21.10.7](https://github.com/hyperledger/besu-docs/releases/tag/21.10.7)
   3. creating the release in github, creates the tag, which triggers the release and deployment of docs to [readthedocs.org](http://readthedocs.org)
9. Homebrew release
   
   1. releaser updates besu.rb in [https://github.com/hyperledger/homebrew-besu](https://github.com/hyperledger/homebrew-besu) to the latest calver of the artifact, and corresponding hash.
   2. PR is opened into main.
   3. Once approved and merged, the tap is considered updated, and homebrew users will now get the configured version on update.

## Perfect Scenario

Any 2 authorized individuals (TBD) can inspect a proposed release candidate, and upon approval the binary goes unchanged into the GitHub release page, and any other supported artifact distribution systems.

- Releaser has easy to find changelog to review.
- Releaser has easy to find PR that shows changes from previous release for closer inspection.
- Immutability of release metadata?
- Documentation changes?
- One-click-execution?
- Audit trail?

## Proposal 1: Tag Based Releases

The idea for this was stolen from the Teku project at ConsenSys. Tag releases are commit based rather than branch HEAD based.  When releasing from master, there is no branch management, PRs or approval required to release.  There will be a single build of the release tag by circle-ci.  The release process is hands-off and automated all the way up to the release on github.  This is a substantial time savings and much lower friction compared to the branch based release strategy.

### Pros:

1. Super low friction, a release is triggered by the application of a tag, and CI does the rest.
2. Can target any branch.
3. Allows possibility of using an existing binary built for the commit the tag is at.

### Cons:

1. A single contributor can do a release since there are no PR approvals required.  This is a concerning issue that must be solved, since a single contributor could ‘go rogue’.
2. Metadata of the release (the tag itself) is mutable and could be moved around the underlying repository history.
3. The semantic meaning of the release must be encodable in the tag itself.
4. Does not allow for differences between a snapshot and a release artifact. The artifact released would ALSO exist as a development snapshot.

### Deficiencies compared to status quo.

The status-quo logic “recognizes” a release branch by naming convention and increments the artifact version correctly for release candidates and final versions.  Also the branch flow deletes the long-lived release branch upon release of a final quarterly (x.y.0) release  The tag flow does not have any provision for quarterly or release candidate flows.  IMO, this can be worked around manually by the deployer, or quarterly release behavior could be added as a config to the tag flow without too much effort.

The primary post-deployment difference between the existing tag and branch based release flows is snapshot versioning for interim builds.  The existing tag flow does not push a subsequent PR to change the release version to &lt;calver&gt;-SNAPSHOT at the end of the process.  While this means that an additional contributor is not necessary for post-deployment, it also means that interim builds will have a common or static name like \`besu-develop\`.  This is an artifact of the no-PR approach of this release flow.  Again I think this is not terribly difficult to add as a configurable behavior to the existing tag flow.  Alternatively, we could invest effort into a dynamic version calculation build function, though the mechanism for determining the current snapshot version is not straightforward when we are not on a tagged commit. 

## Proposal 2: Gradle Release Process

This process would be more like a Maven release process. Release approvers approve a specific commit, and that is run through a build task that adjusts the version number, and then re-runs CI to produce the release artifact. The diff between the release artifact and the commit it is sourced from should only show the new embedded release metadata; usually GAV (Group, Artifact, Version) coordinates and any build timestamps.

### Pros:

1. Immutable build metadata, embedded in the release artifact.
2. Can target any branch.

### Cons:

1. Requires logic in build tools.
2. Requires release branches, which are the only place that release version numbers exist. These may have value for near-future hotfixes to a published version, but will definitely need to be pruned over time.
3. Security becomes a CI concern, instead of something we trust GitHub with by using branch permissions.

## Proposal 3: Circle CI Based Release

This process would separate out any release related functions from our current CI job defined in CircleCI. Since anyone can manipulate the CircleCI job on their branch, we would need to limit its capabilities, perhaps only allowing it to deploy to snapshot repositories. Then a new job could be created that handles all the release activities, and it could depend on multiple approvals or whatever mechanics we need to ensure there are no solo releases.

### Pros:

1. Releases are as secure as a specific job in CircleCI is.
2. Developer control over day to day CI process is retained.
3. CircleCI already knows how to manage secrets required for deployment.
4. Mutability of the build and its metadata is under our control, and our options are anything we can script a CI agent to run.

### Cons:

1. Releases are as secure as a specific job in CircleCI is.
2. Dual approval mechanism would have to be researched.
3. Development and maintenance of the release specific job becomes a separate, non Besu-maintainer handled concern.

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
