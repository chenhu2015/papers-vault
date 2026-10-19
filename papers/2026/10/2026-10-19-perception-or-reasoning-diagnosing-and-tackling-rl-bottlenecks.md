---
title: "Perception or Reasoning? Diagnosing and Tackling Reinforcement Learning Bottlenecks in VLMs"
authors: ["Zeyuan Yang", "Zhuohao Chen", "Jiaben Chen", "Yao Zhang", "Maohao Shen", "Chuang Gan"]
date: 2026-10-19
arxiv_id: "2610.21380v1"
url: "http://arxiv.org/abs/2610.21380v1"
score: 0.84
topics: [VLM, GRPO, multimodal, RL training, agentic RL, reward model]
status: unread
---

# Perception or Reasoning? Diagnosing and Tackling Reinforcement Learning Bottlenecks in VLMs

## Summary

PARA (Perception and Reasoning Attribution) diagnoses whether a given VLM–benchmark pair is bottlenecked by perception or reasoning headroom, finding that current RL exploits reasoning gaps far more effectively than perceptual gaps. Motivated by this, GRAD (Group-Relative Attention Distillation) directly guides weaker rollouts' visual attention using the best rollout in each GRPO group, consistently improving performance across two model scales and seven benchmarks while complementing existing RL methods.

## Key Contributions

- PARA diagnostic: measures remaining perceptual vs reasoning headroom per model–benchmark pair
- Key finding: RL gains correlate with reasoning headroom but are weaker for perceptual headroom
- GRAD: group-relative attention distillation using best rollout's attention to supervise weaker rollouts
- Validated across 4 VLMs, 17 benchmarks; GRAD complements existing RLVR methods

## Relevance

Connects to the VLM RL credit assignment thread (VGPO/MAPO/CapPO) — GRAD is a sixth mechanism for visual grounding in RL, using inter-rollout attention distillation within a GRPO group. The PARA attribution framework also provides a diagnostic tool for understanding why the temporal visual forgetting thread kept returning 0 results: the field may have fragmented into perception-specific vs reasoning-specific RL improvements.

## My Thoughts

<!-- Add your own notes here -->
