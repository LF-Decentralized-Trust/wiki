1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)

# Hyperledger Iroha : General Profiling for improving Iroha2 TPS

Created by Sam H Smith, last modified on Jul 13, 2022

  Status

DECIDED 

Stakeholders[Aleksandr Petrosyan](https://lf-hyperledger.atlassian.net/wiki/people/61d89051567cb70070009dbb?ref=confluence) [Marin Versic](https://lf-hyperledger.atlassian.net/wiki/people/6155483078e5e40070229a80?ref=confluence)OutcomeProfiling is needed. Will be done with kubernetes.Due dateOwner[Sam H Smith](https://lf-hyperledger.atlassian.net/wiki/people/603ff7a5197724011360f09f?ref=confluence)

## Background

CPU time and memory cost money. Faster software is better because it can *do more* with the same hardware. Adding new functionality is only useful so long as users are able to use it. Performance enables more use. It is therefore important that start focusing on improving iroha2 performance. We expect that a significant performance increase is possible and achievable.

## Problem

### Informed decisions require metrics

With good data and metrics it is easy to make good engineering decisions. We want to improve iroha2's performance. Therefore, we want performance data, we want TPS numbers. But it can't be just any data, it must be accurate. An optimization might benefit performance on a developers own machine but be a regression in the real world use case. If the data is inaccurate our decisions will be too. Good metrics are therefore paramount.

### Death by a thousand cuts

Currently the iroha2 codebase suffers from general slowness. Slowness that is very hard to pin down to any particular place in the codebase. In april, Aleksandr Petrosyan spent 3 weeks trying to debug what he thought was a deadlock, turns out it was just iroha2 being so slow it was hard to tell the difference. There is no obvious bottle neck we can address. Everything is slow, so any optimization increases TPS only slightly, because the rest of the codebase is still slow post optimization. We can make things better but it will require iterated small percentage improvements, most of which will not have a visible impact on TPS. Even though we cannot use metrics to decide what change is good. They are still useful in making sure we have not made things worse. If you know that you haven't introduced a regression in performance you can refactor and simplify with confidence. This will allow us to do necessary optimization/simplification faster.

## Solution

### Regular profiling

I will be regularly performing TPS benchmarks on a benchmark stand, created by DevOps. This will allow the iroha2 core team consistent insight into how code changes are affecting performance. I will establish a baseline TPS for the LTS release. That way we can make sure all our codebase simplications are improvements and not regressions. Some of this work can be handled by devops once the routine has been established.

In terms of what changes we should make. There are a few key patterns we need to clean up in my opinion.

- The first is synchronous/asyncronous code. In many places we have async functions whose only purpose is to asynchronously call another function. It is not uncommon for chains of these functions to be 3 or 4 calls. This code executes synchronously. Therefore it should be written like normal singlethreaded synchronous rust code.

<!--THE END-->

- The second pattern to be changed are "call and response" actor messages. We currently send node internal messages and await their responses. The thing to realise about this pattern is that we are doing exactly what asynchronous functions were invented to do. Except here we call ten times the amount of asynchronous functions than we need to. We heap allocate memory in order to create a oneshot channel and do lots of other pointless work. Node internal call and response messages should simply be asynchronous functions.

There are many more things such as these yet to be discovered. I am confident we can achieve shockingly good results compared to today. The question is simply how quickly we will get there. Either way performance testing and profiling is essential.

### Decisions

Simply put, we need to start profiling. Otherwise we won't be able to improve performance.

Anton is working on scripts for us to deploy iroha2 on kubernetes. This is tracked by issue, [https://app.zenhub.com/workspaces/iroha-v2-60ddb820813b9100181fc060/issues/hyperledger/iroha/2450](https://app.zenhub.com/workspaces/iroha-v2-60ddb820813b9100181fc060/issues/hyperledger/iroha/2450).

Once this is done I can gather performance data regularly as mentioned above.

### Alternatives

### Concerns

There is a concern that time spent optimizing will not be fruitful. Or that the feature requirements will change so that the optimization work is made redundant.

### Assumptions

We have assumed iroha2 is only using 1-2 % of the machine's performance.

### Risks

## Additional Information

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
