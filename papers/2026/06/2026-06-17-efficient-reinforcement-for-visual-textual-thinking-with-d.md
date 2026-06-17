---
title: "Efficient Reinforcement for Visual-Textual Thinking with Discrete Diffusion Model"
authors: ["Yoonjeon Kim", "Yuhta Takida", "Chieh-Hsin Lai", "Eunho Yang", "Yuki Mitsufuji"]
date: 2026-06-11
arxiv_id: "2606.14792v1"
url: "http://arxiv.org/abs/2606.14792v1"
score: 0.75
topics: [multimodal models, vision-language models, VLM, GRPO]
status: unread
---

# Efficient Reinforcement for Visual-Textual Thinking with Discrete Diffusion Model

## Summary

Discrete diffusion models enable efficient visual rollouts via localized editing (26.9% fewer GRPO rollout FLOPs vs autoregressive models) for interleaved visual-textual reasoning. A key finding is that joint reward assignment across text and visual segments introduces cross-modal interference; factorized reward assignment — independently assigning rewards to each modality's segment — improves by 11.2% over joint assignment and 38% over the base model, providing a practical design rule for multimodal RL training.

## Key Contributions

- Discrete diffusion as RL backbone for interleaved visual-textual reasoning: localized visual editing (not full regeneration) reduces rollout compute by 26.9% vs AR
- Cross-modal interference diagnosis: joint reward across unrelated image and text token sequences during GRPO causes modality reward misattribution
- Factorized reward assignment: independent rewards per text/vision segment as the solution; +11.2% over joint, +38% over base model
- Demonstrates that AR assumption (full-image regeneration) in visual reasoning RL is not necessary and costly

## Relevance

The factorized reward assignment finding is a direct practical extension of AT-RL (Jun 14), which showed that ~15% of MLLM tokens are high visual-textual anchors and that RL on those anchors alone outperforms full-token RL. AT-RL solves the same cross-modal interference by selecting tokens selectively; this paper solves it by assigning rewards independently per segment — two orthogonal operations on the same underlying problem of cross-modal RL interference in MLLMs.

## My Thoughts

<!-- Add your own notes here -->
