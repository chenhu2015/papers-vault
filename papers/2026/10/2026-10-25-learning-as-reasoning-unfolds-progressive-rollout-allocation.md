---
title: "Learning as Reasoning Unfolds: Progressive Rollout Allocation for Efficient Reinforcement Learning"
authors: ["Heyang Jiang", "Henry Liu", "Baharan Mirzasoleiman"]
date: 2026-10-25
arxiv_id: "2607.22002v1"
url: "http://arxiv.org/abs/2607.22002v1"
score: 0.85
topics: [RL training, GRPO, reinforcement learning, agentic RL]
status: unread
---

# Learning as Reasoning Unfolds: Progressive Rollout Allocation for Efficient Reinforcement Learning

## Summary

VIGOR proposes variance-guided online rollout allocation for RLVR: instead of a fixed budget per example, it starts with few rollouts and iteratively adds more to examples with the highest group reward variance. Theoretically, reward variance controls gradient magnitude under RLVR, and the closed-form speedup over GRPO grows with refinement rounds under Pareto-distributed variance. Reaches target accuracy with up to 2.3× fewer rollouts on math and 1.49× fewer rollouts on coding.

## Key Contributions

- Variance-guided adaptive rollout allocation — start small, iteratively add to highest group reward variance examples
- Theoretical result: reward variance controls gradient magnitude under RLVR; closed-form speedup ratio derived under Pareto-distributed variance
- 2.3× fewer rollouts to reach target math accuracy; 1.49× fewer rollouts on coding with 3.4 point improvement in pass rate
- No pre-rollout filtering overhead — allocation decision is made progressively within a batch

## Relevance

Directly extends the IsoCompute rollout allocation thread (Oct 24) from a prescriptive compute-optimal framing to a principled adaptive-allocation framing grounded in gradient theory. VIGOR's variance signal plays the same role as IsoCompute's sharpening/coverage dichotomy but derives it online from observed reward variance rather than from problem difficulty priors.

## My Thoughts

<!-- Add your own notes here -->
