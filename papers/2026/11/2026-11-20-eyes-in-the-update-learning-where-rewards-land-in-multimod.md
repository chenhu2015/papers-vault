---
title: "Eyes in the Update? Learning Where Rewards Land in Multimodal Reasoning"
authors: ["Lixuan He", "Tianzhe Chu", "Shulin Tian", "Shikang Zheng", "Feng Chen", "Yi Ma"]
date: 2026-11-17
arxiv_id: "2611.22438v1"
url: "http://arxiv.org/abs/2611.22438v1"
score: 0.86
topics: [multimodal models, vision-language models, VLM, reinforcement learning, reward model]
status: unread
---

# Eyes in the Update? Learning Where Rewards Land in Multimodal Reasoning

## Summary

Gaze-RL redistributes trajectory-level reward in multimodal RL by computing a latent reward landing field from internal cross-modal geometry and local predictive uncertainty, assigning larger update weight to positions that are both visually anchored and decision-bearing while keeping the field mean-one so total rollout credit is preserved. Requires no process supervision, auxiliary perception modules, or architectural changes, and improves both Qwen2.5-VL and InternVL3.5 across broad image and video benchmarks.

## Key Contributions

- Latent reward landing field derived from internal cross-modal geometry — no external annotator or auxiliary model required
- Mean-one constraint preserves total rollout credit while reallocating it toward visually grounded, decision-bearing positions
- Architecture-agnostic: tested on two different VLM backbones (Qwen2.5-VL, InternVL3.5) without modification
- Explicitly addresses the sparsity/unevenness of visual evidence use inside multimodal RL trajectories

## Relevance

Extends the credit assignment theme from the multi-turn OPSD cluster (RIPPLE's stage-decomposed credit, EMPO's effect-marginal credit) into the multimodal domain — the first entry in the vault addressing intra-trajectory reward redistribution for VLMs specifically. The cross-modal geometry framing is a genuinely new mechanism not present in any prior entry.

## My Thoughts

<!-- Add your own notes here -->
