---
title: "Granularity-Adaptive Credit Assignment for Long-Horizon LLM Agent Reinforcement Learning"
authors: ["Taoran Liang", "Yang Liu", "Shang Luo", "Yingguang Yang", "Rongrong Zhang", "Yingzong Min", "Yulin Huang", "Jianshen Zhang", "Yongzhi Qi", "Kefu Xu", "Congjing Ran", "Bin Pan", "Bin Chong"]
date: 2026-10-06
arxiv_id: "2609.12424v2"
url: "https://arxiv.org/abs/2609.12424"
score: 0.92
topics: [agentic RL, RL training, reward model]
status: unread
---

# Granularity-Adaptive Credit Assignment for Long-Horizon LLM Agent Reinforcement Learning

## Summary

GACA proposes critic-free granularity-adaptive credit assignment that mixes episode- and step-level credit for each decision by computing a per-token NLL criticality score within the trajectory. The score reflects how context-dependent the step-level credit estimate is and determines the mixture weight without additional rollouts or model evaluations. Across ALFWorld and WebShop with 1.5B and 7B backbones, GACA achieves the highest reported mean success rates among compared methods.

## Key Contributions

- Per-token NLL criticality score computed from rollout log-probabilities, reusing existing rollout data with no extra cost
- Score-dependent mixture between episode-level and step-level advantage that is derived analytically (lower bound on preferred step-level weight)
- Critic-free design — no separate value network, no additional training rollouts or model evaluations
- State-of-the-art on ALFWorld and WebShop at both 1.5B and 7B scale vs. GRPO, SHARPO, SDAR, and StepOPSD

## Relevance

GACA is the 13th entry in the step-credit cluster and directly addresses the episode-vs-step granularity trade-off that AdaStep (shrinkage via signal-to-variance decomposition) targets from a statistical angle. While AdaStep asks "when is a step-credit estimate statistically reliable," GACA asks "how much should each decision weight step-level vs. episode-level credit" — the two designs are orthogonal and potentially composable as a meta-layer. The per-token NLL criticality score is a new signal type in the cluster: unlike SHARPO's teacher-student log-prob gap (comparing to a reference model), GACA's NLL score is trajectory-internal (normalised within rollout), requiring no reference model or auxiliary annotator.

## My Thoughts

<!-- Add your own notes here -->
