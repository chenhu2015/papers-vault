---
title: "When Every Rollout Fails: Splicing Learner-Conditioned Options into Long-Horizon Agent RL"
authors: ["Haowen Hou", "Yicheng Liu", "Zhen Huang", "Jiaqi Wang"]
date: 2026-11-25
arxiv_id: "2611.34777"
url: "https://arxiv.org/abs/2611.34777"
score: 0.90
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# When Every Rollout Fails: Splicing Learner-Conditioned Options into Long-Horizon Agent RL

## Summary

SPLICE addresses the all-fail group problem in GRPO-style RLVR on long-horizon agent tasks: when every trajectory in a group scores zero, there is no reward-based policy gradient. Rather than supplying complete solutions from a stronger model, SPLICE inserts a proposal model that selects a splice point in a failed trajectory and generates bounded options (hierarchical RL primitives) from that point, then estimates each option's value via current-policy continuations and trains on the best local targets. Evaluated on SWE-bench Verified and BrowseComp-Plus, SPLICE outperforms GRPO and full-trajectory guidance baselines by 2.8–9.8 percentage points, raising GRPO's graduation rate on initially failed SWE tasks by 10.8pp.

## Key Contributions

- Identifies all-fail groups as the central failure mode of GRPO/RLVR on long-horizon tasks where every sampled trajectory receives zero reward
- Introduces options-based local training targets: a proposal model splices into a failed trajectory, generates bounded options, and values them via current-policy continuations
- Avoids the full-trajectory off-policy problem of stronger-model guidance while remaining computationally cheaper
- Outperforms GRPO and full-trajectory baselines on two hard long-horizon benchmarks (SWE-bench Verified, BrowseComp-Plus)

## Relevance

Directly extends the long-horizon agentic RL failure modes thread (RLVB, PROVE, FALCA) with a concrete GRPO fix for the all-fail case, using hierarchical options to inject local credit signal where outcome reward is absent. The proposal-model splice mechanism is a practical alternative to the full-trajectory strong-model guidance that was the standard prior approach.

## My Thoughts

<!-- Add your own notes here -->
