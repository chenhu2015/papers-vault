---
title: "GEOALIGN: Geometric Rollout Curation for Robust LLM Reinforcement Learning"
authors: ["Ting Zhou", "Zhenqing Ling", "Yiyang Zhao", "Ying Shen", "Daoyuan Chen"]
date: 2026-06-25
arxiv_id: "2606.26917"
url: "https://arxiv.org/abs/2606.26917"
score: 0.82
topics: [agentic RL, RL training, GRPO, reward model, PPO]
status: unread
---

# GEOALIGN: Geometric Rollout Curation for Robust LLM Reinforcement Learning

## Summary

GEOALIGN identifies a failure mode called directional inconsistency: within a GRPO batch, a small subset of high-reward rollouts induces representation-space preference directions that sharply disagree with the batch majority, causing high-variance and destabilizing updates. The fix is a lightweight online projector on per-rollout hidden states that concentrates reward-ordered displacement directions, detects angular outliers via deviation from a batch consensus prototype, and replaces them with stable within-prompt alternatives. Applied to both dialogue alignment and math reasoning with binary rewards, GEOALIGN improves final performance and reduces training oscillation vs. PF-PPO, PAR, PODS, and Seed-GRPO.

## Key Contributions

- Directional inconsistency identification: formal characterization of how a minority of high-reward rollouts can poison batch gradient direction in representation space
- Online latent-space projector: concentrates reward-ordered displacement directions across the batch without requiring additional inference passes
- Angular deviation detection: measures each rollout's deviation from a batch consensus prototype direction; outliers above threshold are replaced rather than down-weighted
- Forward-pass-only overhead: adds negligible compute vs. baseline GRPO

## Relevance

Extends the vault's RL optimization internals thread (RIPO: geometric fix for PPO manifold; RL-ZVP: zero-variance prompts; IGRPO: information gain branch selection) with a new geometric signal — latent-space directional consensus — as a rollout quality indicator. Where GEOALIGN differs from prior data curation work: the quality signal is not based on reward magnitude or difficulty, but on inter-rollout consistency in representation space.

## My Thoughts

<!-- Add your own notes here -->
