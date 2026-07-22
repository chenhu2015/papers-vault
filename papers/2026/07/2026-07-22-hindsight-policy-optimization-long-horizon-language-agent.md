---
title: "From Outcomes to Actions: Leveraging Hindsight for Long-Horizon Language Agent Training"
authors: ["Zishang Jiang", "Tingyun Li", "Jinyi Han", "Xinyi Wang", "Sihang Jiang", "Yizhou Ying", "Xiaojun Meng", "Jiansheng Wei", "Jiaqing Liang", "Yanghua Xiao"]
date: 2026-06-28
arxiv_id: "2607.16257"
url: "https://arxiv.org/abs/2607.16257"
score: 0.83
topics: [agentic RL, LLM agent, reinforcement learning, RLHF]
status: unread
---

# From Outcomes to Actions: Leveraging Hindsight for Long-Horizon Language Agent Training

## Summary

Hindsight Policy Optimization (HPO) addresses the high-variance credit assignment problem in long-horizon LLM agent interactions by projecting both the current policy distribution and a hindsight distribution (derived from observed outcomes) into a shared intent space, then extracting policy gradient signals from the Wasserstein distance between them. Aggregating semantically similar states and actions in intent space yields a bounded-variance estimator that improves policy performance more stably than trajectory-level baselines. HPO is theoretically grounded and empirically demonstrates more stable improvement on complex long-horizon LLM agent tasks compared to standard RL baselines.

## Key Contributions

- Intent space projection: maps current policy and hindsight distribution into a shared latent semantic space, aggregating similar (state, action) pairs into clusters
- Wasserstein distance between intent projections provides a geometrically meaningful, low-variance policy gradient signal that distinguishes actions by their semantic effect on outcomes
- Bounded-variance estimation proof via semantic aggregation: similar states/actions that would otherwise contribute independent noisy gradient terms are consolidated
- Addresses the long-horizon distinguishability problem: different actions at the same intermediate state map to different intent clusters, providing finer-grained credit than episode-level return

## Relevance

Directly complements BPO (today) in the agentic RL credit assignment thread. Where BPO reduces variance by sharing structural prefixes in a sandboxed rollout tree, HPO reduces variance by projecting into a semantic intent space — the two approaches target variance from different sources (prefix redundancy vs. semantic conflation). The Wasserstein distance signal connects to the information geometry thread (Fisher-Rao in DyCo-RL, Riemannian PPO-Clip in RIPO/Value-Gradient Hypothesis): all three papers use geometric distances in transformed spaces to improve gradient signal quality, but at different levels (attention/token, policy manifold, and intent/semantic space, respectively).

## My Thoughts

<!-- Add your own notes here -->
