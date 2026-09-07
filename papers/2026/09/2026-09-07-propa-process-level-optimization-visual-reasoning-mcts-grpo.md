---
title: "PROPA: Toward Process-level Optimization in Visual Reasoning via Reinforcement Learning"
authors: ["Yanbei Jiang", "Chao Lei", "Yihao Ding", "Krista Ehinger", "Jey Han Lau"]
date: 2026-09-07
arxiv_id: "2511.10279v1"
url: "https://arxiv.org/abs/2511.10279"
score: 0.80
topics: [multimodal models, vision language models, VLM, GRPO, reward model, reinforcement learning, RL training]
status: unread
---

# PROPA: Toward Process-level Optimization in Visual Reasoning via Reinforcement Learning

## Summary

PROPA integrates MCTS with GRPO to generate dense process-level rewards at each intermediate reasoning step without human annotations, resolving the cold-start problem by interleaving GRPO updates with SFT on both successful and failed trajectories. A Process Reward Model (PRM) is further trained to guide inference-time search, aligning test-time search with the training signal. Across seven benchmarks and four VLM backbones, PROPA achieves up to 17% in-domain and 21% out-of-domain gains over SFT- and RLVR-based baselines.

## Key Contributions

- MCTS-generated dense process-level rewards without human annotation — addresses the annotation bottleneck of StructReward and similar dense-reward methods in VLM RL
- Interleaved GRPO+SFT training: cold-start via SFT on MCTS trajectories (both successes and failures), then alternating RL updates maintain stability
- PRM trained on MCTS trajectory data, enabling inference-time search aligned with training signal
- Seven benchmarks and four VLM backbones: up to 17% in-domain, 21% out-of-domain improvement over SFT- and RLVR-based baselines

## Relevance

PROPA closes the VIG+StructReward for general VLM reasoning open gap from a different angle than DARS (Sep 06, image editing) and MSRL (Sep 05, chart-to-code): rather than using heuristic structured rewards (StructReward principle) or visual information gain (VIG principle), PROPA uses MCTS to discover which reasoning steps are process-level correct, enabling annotation-free dense rewards for general visual reasoning tasks (math, science, open-ended QA). The interleaved GRPO+SFT curriculum also parallels SCALECUA Frontier Sampling's insight that curriculum-aware training allocation is key to stable long-horizon RL.

## My Thoughts

<!-- Add your own notes here -->
