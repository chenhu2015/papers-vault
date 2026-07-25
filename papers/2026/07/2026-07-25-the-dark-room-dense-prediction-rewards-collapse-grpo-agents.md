---
title: "The Dark Room in the Reward Channel: Dense Prediction Rewards Collapse GRPO-Trained LLM Agents -- and What Actually Works"
authors: ["Yu Wang"]
date: 2026-07-23
arxiv_id: "2607.21273v1"
url: "http://arxiv.org/abs/2607.21273v1"
score: 0.85
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# The Dark Room in the Reward Channel: Dense Prediction Rewards Collapse GRPO-Trained LLM Agents -- and What Actually Works

## Summary

Dense per-step prediction rewards under GRPO cause a 'dark room' pathology on ALFWorld: prediction accuracy converges to 1.0 while task success collapses to 0, and annealing cannot rescue it. The root cause is GRPO's std normalization: in all-fail groups the z-scored advantage is invariant to the shaping coefficient, so bounded rewards become unbounded gradient pressure. Removing std normalization recovers baseline parity from the same reward, while switching signal delivery from the reward channel to an auxiliary-loss channel gains ~20 points over reward-channel methods.

## Key Contributions

- Dark room pathology: GRPO + dense prediction reward drives every run to degenerate absorbing state (prediction accuracy 1.0, task success 0, episode length pinned at horizon) on Qwen3-1.7B/4B/8B on ALFWorld
- Root mechanism: in all-fail groups, z-scored advantage is invariant to shaping coefficient — bounded rewards become unbounded pressure regardless of scale or annealing
- Variance-profile criterion: dense signals whose within-group variance decays by mastery are structurally safe for z-scoring; signals that do not decay will cause pathological amplification
- Signal-delivery matrix: auxiliary-loss channel beats reward channel by ~20 points; shuffled-gold placebo matches true-gold in the loss channel, showing the gap comes from channel, not label quality

## Relevance

The variance-profile criterion is the first principled account of which dense signals are safe to use with GRPO — previously this was purely empirical. The Dark Room failure mode helps explain why so many dense reward attempts in agentic RL fail unpublishably: any prediction-style dense reward whose signal strength doesn't decay as the policy masters the behavior will pathologically amplify under z-scoring. This connects to Clip-Low/Clip-High (Jul 24, entropy collapse from clipping) and the GRPO entropy collapse thread: both identify structural artifacts in GRPO normalization that compound with the reward signal. The auxiliary-loss channel finding also retroactively explains why TRACE (today) works: TRACE's frozen reference model log-prob is not injected as a reward but is derived offline and used to shape the per-step advantage — it sidesteps the all-fail group amplification by computing the value outside the GRPO normalization loop.

## My Thoughts

<!-- Add your own notes here -->
