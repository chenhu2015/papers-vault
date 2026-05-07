---
title: "Reward-Decomposed Reinforcement Learning for Immersive Video Role-Playing"
authors: ["Miao Wang", "Yuling Shi", "Yijiang Li", "Yeheng Chen", "Xiaodong Gu", "Bin Li", "Bo Gao", "Yaduan Ruan"]
date: 2026-05-06
arxiv_id: "2605.04733"
url: "https://arxiv.org/abs/2605.04733"
score: 0.80
topics: [multimodal, VLM, GRPO, vision-language, reinforcement learning]
status: unread
---

# Reward-Decomposed Reinforcement Learning for Immersive Video Role-Playing

## Summary

EBM-RL (Eye-Brain-Mouth Reinforcement Learning) decomposes GRPO training for video-grounded dialogue into three structured phases—visual perception, internal reasoning, and spoken answer—enforced by four complementary rewards including CLIP-based scene-text alignment and a perceptual-cognitive uplift reward. Without any fine-tuning, EBM-RL generalises zero-shot to out-of-domain VideoQA benchmarks, outperforming larger frontier VLMs.

## Key Contributions

- Structured [perception]-[think]-[answer] generation decomposition enforced during GRPO training, grounding dialogue in visual cues before reasoning
- Four complementary rewards: CLIP scene-text alignment, perceptual-cognitive reward (likelihood of reference response given perceive+think), answer accuracy, dense format reward
- Zero-shot VideoQA generalisation without fine-tuning, outperforming larger VLMs on out-of-domain benchmarks
- Open-source dataset for video-grounded role-playing dialogue

## Relevance

Continues the video VLM RL thread from May 6 (SDRL, EVA, SCORE) with a reward-decomposition angle; structured CoT + multi-reward GRPO is directly relevant to the multimodal RL and VLM topics. The zero-shot VideoQA generalisation result reinforces the pattern that RL-trained VLMs generalise beyond their training domain.

## My Thoughts

<!-- Add your own notes here -->
