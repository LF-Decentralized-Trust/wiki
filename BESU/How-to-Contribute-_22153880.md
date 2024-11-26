1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Content Refactor](Content-Refactor_22153881.html)

# Besu : How to Contribute-

Created by Edward Evans, last modified by Felipe Faraggi on Jan 24, 2020

# Contents

- [Things to be Aware of before Contributing](#HowtoContribute--ThingstobeAwareofbeforeContributing)
  
  - [The Developer Certificate of Origin (DCO) checks](#HowtoContribute--TheDeveloperCertificateofOrigin%28DCO%29checks)
  - [Copyright and License](#HowtoContribute--CopyrightandLicense)
- [Contributing Code or Documentation](#HowtoContribute--ContributingCodeorDocumentation)
- [How to work with DCO](#HowtoContribute--HowtoworkwithDCO)
  
  - [When Committing](#HowtoContribute--WhenCommitting)
  - [When Merging](#HowtoContribute--WhenMerging)
  - [When you have a DCO failure on your PR from DCO Bot](#HowtoContribute--WhenyouhaveaDCOfailureonyourPRfromDCOBot)
  - [When you have a DCO failure on your PR from CI](#HowtoContribute--WhenyouhaveaDCOfailureonyourPRfromCI)
- [Becoming a Maintainer](#HowtoContribute--BecomingaMaintainer)

# Things to be Aware of before Contributing

Be sure to read the [contribution guidelines](https://github.com/hyperledger/besu/blob/master/CONTRIBUTING.md) for more details on searching and creating issues.

## The Developer Certificate of Origin (DCO) checks

As per section 13.a of the [Hyperledger Charter](https://www.hyperledger.org/about/charter) all code submitted to the Hyperledger Foundation needs to have a [Developer Certificate of Origin](http://developercertificate.org/) (DCO) sign-off.

This certifies that you are able to submit your contribution to our repository under the license of the repository, and for the contribution to be redistributed under that same license.

You can "sign" this certificate by including a line in the git commit of "`Signed-off-by: Legal Name <email-address>`".

## Copyright and License

As per section 13.a of the [Hyperledger Charter](https://www.hyperledger.org/about/charter) all new code submitted to the Hyperledger Foundation needs to be under the Apache License, Version 2.0.

As per section 13.c of the [Hyperledger Charter](https://www.hyperledger.org/about/charter) all new documentation submitted to the Hyperledger Foundation needs to be under the Creative Commons Attribution 4.0 International License.

You may maintain copyright to your works under these two clauses.

When you commit code please ensure you:

- put your copyright if required
- you MUST put the SPDX license header using Apache 2.0 like below. If you do not put the header in the build will fail the license header check

```
 /* SPDX-License-Identifier: Apache-2.0 */
```

# Contributing Code or Documentation

The codebase and documentation are maintained using the same "*contributor workflow*" where everyone without exception contributes changes proposals using "*pull-requests*".

This facilitates social contribution, easy testing, and peer review.

To contribute changes, use the following workflow:

01. [Fork the repository](https://github.com/PegaSysEng/besu/fork).
02. **Clone your fork** to your computer.
03. **Create a topic branch** and name it appropriately.  Starting the branch name with the issue number is a good practice and a reminder to fix only one issue in a Pull-Request (PR).
04. **Make your changes** adhering to the coding conventions described in the associated repository's `CONTRIBUTING.md`  file.  *In general a commit serves a single purpose and diffs should be easily comprehensible.  For this reason do not mix any formatting fixes or code moves with actual code changes.*
05. **Commit your changes** see [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/) article by Chris Beams and ensure there is a`Signed-off-by: Legal Name <email-address>` line in the commit to submit the code under a [Developer Certificate of Origin (DCO)](http://developercertificate.org/).
06. **Test your changes** locally before pushing to ensure that what you are proposing is not breaking another part of the software. Running the `./gradlew clean check test`  command locally will help you to be confident that your changes will pass CI tests once pushed as a Pull Request.
07. **Push your changes** to your remote fork (usually labeled as `origin`).
08. **Create a pull-request** (PR) on the Besu repository. If the PR addresses an existing Jira issue,  include the issue number in the PR title in square brackets (for example,`[PAN-2374]`).
09. **Add labels** to identify the type of your PR. *For example, if your PR is not ready to validate, add the "work-in-progress" label. If it fixes a bug, add the "bug" label.* If the PR address an existing Jira issue, comment in the Jira issue with the PR number.
10. **Ensure your changes are reviewed**. *Select the reviewers you would like to review your PR. If you don't know who to choose, simply select the reviewers proposed by GitHub or leave blank.*
11. **Make any required changes** on your contribution from the reviewers feedback.  *Make the changes, commit to your branch, and push to your remote fork.*
12. **When your PR is validated**, all tests passed and your branch has no conflicts with the target branch, you can **"squash and merge"** your PR, when doing so ensure that there is a `Signed-off-by: Legal Name <email-address>` line in the commit message to comply with [DCO](http://developercertificate.org/)  and you're done. You contributed to Besu! Thanks !

# How to work with DCO

## When Committing

You need to ensure that every commit message has a line "`Signed-off-by: Your Legal Name <your-email@address>`", and while you could add that manually every time, here are the steps to follow so the computer can add it for you:

1. Set your legal name in the git configuration:
   
   `git config user.name "Legal Name"`
2. Set your email in the git configuration:
   
   `git config user.email "email@address"`
3. Add the `-s`  or `--signoff`  to all `git commit`  invocations.
   
   1. Add a git alias:
      
      `git config --global alias.c 'commit --signoff'`and then run "`git c`" instead of "`git commit`"
   2. In IntelliJ
      
      ![](attachments/22153880/22153886.png?height=400)

## When Merging

The merge or a PR must also have a DCO so we can know the entire repository is under the associated license.

1. When Merging a Pull Request through **"squash and merge"**, include the `Signed-off-by` lines from every contributor, and add one for you as the person merging.

## When you have a DCO failure on your PR from DCO Bot

![](attachments/22153880/22153895.png?height=45)'

Click on that "Details" link and follow the instructions.

![](attachments/22153880/22153896.png?height=400)

## When you have a DCO failure on your PR from CI

On Circle CI you will see:

![](attachments/22153880/22153897.png?height=48)

On Jenkins in the full Console Output you will see:

![](attachments/22153880/22153898.png?height=64)

If this is only from CI and not from DCO Bot, then please contact a Maintainer, as it probably means that the `master` branch has a commit that does not follow DCO which will necessitate a `master` rebase.

# Becoming a Maintainer

Besu welcomes community contributions and encourages diversity in its maintainers. To become a maintainer, please read the [maintainers](https://github.com/hyperledger/besu/blob/master/MAINTAINERS.md) document in the repo before seeking sponsorship.

## Attachments:

![](images/icons/bullet_blue.gif) [Screen Shot 2019-09-17 at 10.13.13 am.png](attachments/22153880/22153886.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2019-09-17 at 8.27.56 am.png](attachments/22153880/22153895.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2019-09-17 at 8.28.18 am.png](attachments/22153880/22153896.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2019-09-17 at 12.35.45 pm.png](attachments/22153880/22153897.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screen Shot 2019-09-17 at 12.39.47 pm.png](attachments/22153880/22153898.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
