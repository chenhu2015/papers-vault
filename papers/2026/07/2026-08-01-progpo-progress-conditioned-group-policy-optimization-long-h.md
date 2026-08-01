---
title: "Progress-conditioned Group Policy Optimization for Long-Horizon Agentic Tasks"
authors: ["Kaibing Yang", "Guangfeng Cai", "Shengtian Yang", "Shuo He", "Yu Li", "Mengyi Liu", "Pengwei Chen", "Jun Xu", "Lei Feng"]
date: 2026-07-22
arxiv_id: "2607.22724"
url: "https://arxiv.org/abs/2607.22724"
score: 0.86
topics: [agentic RL, GRPO, LLM agent]
status: unread
---

# Progress-conditioned Group Policy Optimization for Long-Horizon Agentic Tasks

## Summary

ProGPO diagnoses a 'credit trap' in long-horizon group-based policy optimization: all-failed rollout groups provide no outcome-based gradient, allowing repeated low-effect actions to dominate the high-probability policy region and perpetuate failure. ProGPO breaks this loop by activating first-visit observation coverage exclusively within all-failed groups, assigning higher relative advantages to trajectories that visit more novel states—since reaching new observations is a prerequisite for eventual task success. Evaluated on ALFWorld and WebShop with Qwen2.5-1.5B/7B, with particularly large improvements on hard tasks.

## Key Contributions

- **Credit trap diagnosis**: formalizes the self-reinforcing failure loop in long-horizon GRPO — all-failed groups + action repetition → no correction signal → more repetition
- **Conditional progress signal**: first-visit observation coverage activated *only* within all-failed rollout groups; does not interfere with outcome-reward-driven learning when at least one rollout succeeds
- **State novelty as proxy**: higher relative advantage for trajectories visiting more new observations, grounded in the observation that new-state coverage is a structural prerequisite for task success
- Consistent SoTA improvements on ALFWorld and WebShop for both 1.5B and 7B Qwen2.5 models, with the largest gains concentrated on the hardest task splits

## Relevance

Constitutes the seventh distinct approach to Gap #16 (GRPO all-fail group problem), complementary to TAO-RL (Jul 30, explicit group filtering) — where TAO-RL removes degenerate groups entirely to avoid negative gradient signal, ProGPO provides an alternative reward signal *within* all-failed groups that enables learning to continue rather than stalling; these two approaches address complementary failure regimes (TAO-RL: remove corrupted signal, ProGPO: replace it with a proxy).

## My Thoughts

<!-- Add your own notes here -->
