---
title: "EmoAgent-R1: Towards Multimodal Emotion Understanding with Reinforcement Learning-based Dynamic Agent Specialization"
authors: ["Lihuang Fang", "Yuchen Zou", "kebing Jin", "Jinghui Qin"]
date: 2026-07-28
arxiv_id: "2607.21013"
url: "https://arxiv.org/abs/2607.21013"
score: 0.80
topics: [GRPO, multimodal models, VLM, RL training, RLAIF, reward model]
status: unread
---

# EmoAgent-R1: Towards Multimodal Emotion Understanding with Reinforcement Learning-based Dynamic Agent Specialization

## Summary

Introduces P-GRPO (Progressive GRPO), which combines group-based relative advantages with PMI-inspired progressive token-level modulation to transform GRPO's sparse binary outcome rewards into fine-grained step-level learning signals, directly addressing the uniform credit assignment pathology. EmoAgent-R1 applies P-GRPO in a two-step agentic workflow (agent selection + agent specialization) for multimodal emotion recognition, demonstrating stronger emotion reasoning and improved optimization stability versus baseline GRPO.

## Key Contributions

- P-GRPO: combines standard GRPO group-based relative advantages with PMI-inspired progressive token-level modulation
- Transforms sparse binary outcome rewards into fine-grained step-level signals within the GRPO framework without changing its core group structure
- Two-step agentic workflow: cold-start with synthetic CoT + routing data, then RL with dynamic agent specialization based on perceived emotion source
- Improved GRPO optimization stability demonstrated on multimodal emotion recognition benchmarks

## Relevance

P-GRPO is the first information-theoretic approach (PMI-based) to the uniform credit assignment problem that Dark Room (Jul 25) identified as a GRPO structural pathology — where z-score normalization treats all tokens uniformly. While Dark Room proposed the variance-profile criterion for reward signal design and STAPO (Jul 26) uses normalized entropy for step-level gradient allocation, P-GRPO uses PMI to identify which tokens should receive stronger gradient signals within GRPO's normalization, partially addressing Gap #16.

## My Thoughts

<!-- Add your own notes here -->
