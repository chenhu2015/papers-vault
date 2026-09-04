---
title: "VIG: Visual Information Gain as a Reward Signal for Multimodal Chain-of-Thought Compression"
authors: ["Wen Luo", "Xiaohan Yi", "Xiaotao Huang", "Liqun Huang"]
date: 2026-09-04
arxiv_id: "2608.21883v2"
url: "http://arxiv.org/abs/2608.21883v2"
score: 0.83
topics: [VLM, multimodal, vision-language, GRPO, reward model, agentic RL]
status: unread
---

# VIG: Visual Information Gain as a Reward Signal for Multimodal Chain-of-Thought Compression

## Summary

VIG proposes an information-theoretic GRPO reward that scores each multimodal reasoning token by how much the image reduces its predictive uncertainty, computed online from two forward passes (with and without image) of the same policy — no reference chains, annotations, or auxiliary reward models required. Applied to Qwen3-VL-Thinking (2B/4B/8B), VIG consistently improves the accuracy-efficiency trade-off across six multimodal benchmarks by raising visual information density in the CoT. This opens a new reward-signal axis for VLM RL: grounding quality per token rather than outcome correctness or step-level structure.

## Key Contributions

- Information-theoretic per-token GRPO reward: each token scored by I(image; token | context) computed from two forward passes of the same model
- No reference chains, external annotations, or auxiliary reward models — fully self-supervised signal derivable from standard VLM forward pass
- Consistent accuracy-efficiency improvement across six multimodal benchmarks and three Qwen3-VL-Thinking model sizes (2B/4B/8B) plus R1-Onevision-Bench
- New framing: efficient multimodal reasoning = raising visual information density, not imposing length budget

## Relevance

VIG adds a sixth axis to the VLM RL design map (reward signal, advantage estimator, rollout tree efficiency, environment model, rollout diversity — now plus grounding density reward). It is structurally adjacent to StructReward (Sep 02) — both densify the GRPO reward signal — but from a different angle: StructReward uses step-sequence alignment to provide dense process rewards for structured tasks; VIG uses mutual information with the visual input to provide per-token grounding rewards for multimodal tasks. The two are potentially composable: a VLM RL training objective that jointly maximizes step-alignment reward (StructReward) and visual grounding density (VIG) remains an open question.

## My Thoughts

<!-- Add your own notes here -->
