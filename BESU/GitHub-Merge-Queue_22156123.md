1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Archive (Dev)](22154818.html)

# Besu : GitHub Merge Queue

Created by Sally MacFarlane, last modified on Mar 22, 2023

**Update -** disabled ~ Mar 17 2023

Issues found

- still runs all the checks (including GHA) again even if the queue is empty [https://github.com/orgs/community/discussions/46757?sort=top#discussioncomment-4912738](https://github.com/orgs/community/discussions/46757?sort=top#discussioncomment-4912738)
- GH enforcing the max 20 runners at once limit, which they never did before
- hence PRs were being silently removed from the queue (GHA not reporting status) and no benefit was being gained from the queue

**Update** - enabled on Mar 13 2023. DCO required adjusting as per [https://github.com/hyperledger/besu/pull/5207](https://github.com/hyperledger/besu/pull/5207). 

Essentially this works the same as enabling auto-merge, except that any additional "merge from main" actions are automated.

**Impacts on current workflow**

- once the merge queue is enabled, it's a requirement - so all PRs will be merged via the queue.
- to add your PR to the merge queue, you need to click the green "merge when ready" button" just as you would click the "enable auto-merge" button
- "squash merge commits" is done automatically
  
  - with the commit message = PR title (full commit details still available in the PR)
  - so if you want to edit the commit message, you'll need to do this locally on your branch prior to adding it to the merge queue - eg [https://stackoverflow.com/questions/25356810/git-how-to-squash-all-commits-on-branch](https://stackoverflow.com/questions/25356810/git-how-to-squash-all-commits-on-branch)
- avoiding unnecessary merge conflicts - think about inserting into a sensible place in the changelog, rather than appending to the end by default
- when there's a merge conflict, the PR with the conflicts gets kicked out of the merge queue and manual intervention is required - same as if you had enabled "auto-merge"

Discussion in Feb 28 contributor call on enabling the merge queue [2023-02-28 Contributor Call - APAC Friendly Time](2023-02-28-Contributor-Call---APAC-Friendly-Time_22156108.html) after 23.1.1 release

Note - it's part of "branch protection" - so you turn it on for specific branch protection rules.

This feature is still in beta - discussion [https://github.blog/changelog/2023-02-08-pull-request-merge-queue-public-beta/](https://github.blog/changelog/2023-02-08-pull-request-merge-queue-public-beta/)

Link to Besu merge queue (when enabled) would be [https://github.com/hyperledger/besu/queue/main](https://github.com/hyperledger/besu/queue/main)

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
