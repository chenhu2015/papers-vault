---
title: "Granularity-Adaptive Credit Assignment for Long-Horizon LLM Agent Reinforcement Learning"
authors: ["Taoran Liang", "Yang Liu", "Shang Luo", "Yingguang Yang", "Rongrong Zhang", "Yingzong Min", "Yulin Huang", "Jianshen Zhang", "Yongzhi Qi", "Kefu Xu", "Congjing Ran", "Bin Chong"]
date: 2026-09-11
arxiv_id: "2609.12424v1"
url: "http://arxiv.org/abs/2609.12424v1"
score: 0.90
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Granularity-Adaptive Credit Assignment for Long-Horizon LLM Agent Reinforcement Learning

## Summary

GACA introduces granularity-adaptive credit assignment for long-horizon LLM agent RL, using step-level NLL as an uncertainty-based criticality proxy to blend step-level and episode-level GRPO advantage estimates. High-NLL pivotal transitions receive fine-grained credit while routine low-NLL steps receive episode-level broadcast, with a risk decomposition proving that modulation improves over fixed mixing under positive directional alignment. On ALFWorld and WebShop, GACA outperforms both GRPO and GiGPO at 1.5B and 7B scales.

## Key Contributions

- State-dependent credit granularity: NLL criticality proxy computed from existing rollouts (no learned critic, no branch rollouts)
- Per-step blending weight that grows with NLL, shifting from episode-level to step-level advantage at above-average NLL
- Exact risk decomposition showing modulation improves over fixed mixing under positive directional alignment
- Error-projection analysis characterizing when mixing adds value beyond scalar uncertainty reweighting

## Relevance

GACA extends the long-horizon credit assignment thread (GiGPO, CRISP, CANOPY) by making granularity state-dependent rather than fixed, and derives the first theoretical justification for the mixing decision using NLL as a universal criticality signal. This is a direct successor to GiGPO and a complement to CRISP's step-selection approach: CRISP selects which steps are critical (binary), GACA continuously modulates granularity (soft blend) — together they bound the design space for non-dense per-step credit.

## My Thoughts

<!-- Add your own notes here -->
