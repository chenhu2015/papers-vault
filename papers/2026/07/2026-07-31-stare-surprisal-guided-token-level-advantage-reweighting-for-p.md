---
title: "STARE: Surprisal-Guided Token-Level Advantage Reweighting for Policy Entropy Stability"
authors: ["Haipeng Luo", "Qingfeng Sun", "Songli Wu", "Can Xu", "Wenfeng Deng", "Han Hu", "Yansong Tang"]
date: 2026-07-31
arxiv_id: "2606.19236"
url: "https://arxiv.org/abs/2606.19236"
score: 0.85
topics: [agentic RL, RL training, GRPO, reward model]
status: unread
---

# STARE: Surprisal-Guided Token-Level Advantage Reweighting for Policy Entropy Stability

## Summary

STARE conducts a first-order gradient analysis of GRPO's entropy dynamics and identifies an advantage-surprisal four-quadrant structure: per-token entropy variation decomposes into trajectory advantage times an entropy sensitivity function over the next-token distribution, yielding a near-criticality property that motivates token-selective credit assignment. It identifies entropy-critical token subsets via within-batch surprisal quantiles, selectively reweights their effective advantages, and incorporates a target-entropy closed-loop gate for stable training. Outperforms DAPO by 4-8% on AIME24/25 across model scales from 1.5B to 32B and three task families including multi-turn tool use.

## Key Contributions

- First-order gradient analysis decomposing GRPO's per-token entropy variation into advantage × entropy-sensitivity, proving a near-criticality property that explains entropy collapse
- Surprisal-based token identification: within-batch surprisal quantiles select entropy-critical token subsets for selective advantage reweighting
- Target-entropy closed-loop gate maintains policy entropy within a stable band, preventing both collapse and explosion
- Validated at 1.5B–32B scale across Short CoT, Long CoT, and Multi-Turn Tool Use task families

## Relevance

STARE is the fourth distinct instantiation of the entropy-as-structural-signal pattern in Gap #12: STAPO (normalized entropy for neglect-prone steps) → O²-CritiCuRL (multi-rollout frequency for critical steps) → TAO-RL (entropy bonus at post-tool-call tokens) → STARE (surprisal quantiles for entropy-critical tokens). Critically, STARE is the first to provide a formal gradient-level analysis proving *why* entropy-based token selection works: the advantage-surprisal decomposition shows that tokens with high surprisal are exactly the tokens where entropy is most sensitive to the advantage signal. This retroactively grounds all four instances in a single theoretical principle.

## My Thoughts

<!-- Add your own notes here -->
