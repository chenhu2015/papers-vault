---
title: "MIRL: Mutual Information-Guided Reinforcement Learning for Vision-Language Models"
authors: ["Yin Zhang", "Jiaxuan Zhao", "Zonghan Wu", "Zengxiang Li", "Junfeng Fang", "Kun Wang", "Qingsong Wen", "Yilei Shao"]
date: 2026-05-02
arxiv_id: "2605.01520"
url: "http://arxiv.org/abs/2605.01520v1"
score: 0.84
topics: [VLM, vision-language, multimodal, RLHF, reward model, RL training]
status: unread
---

# MIRL: Mutual Information-Guided Reinforcement Learning for Vision-Language Models

## Summary

MIRL uses mutual information between generated visual descriptions and input images as a cheap pre-screening signal to allocate the RLVR sampling budget, filtering trajectories likely doomed by early visual errors before completing the full rollout. A decoupled RL training loop applies independent MI-based rewards for visual perception separately from reasoning rewards, resolving the reward blindness that prevents standard RLVR from distinguishing perception failures from reasoning failures.

## Key Contributions

- MI between generated descriptions and input images as a budget-allocation pre-screening signal
- Decoupled RL: independent MI-based rewards for visual perception vs. reasoning stages
- 70.22% average accuracy on 6 VL reasoning benchmarks, surpassing 16 complete rollouts with only 10 pre-samples + top-6 selection (25% fewer complete trajectories)
- Reward blindness in RLVR for VLMs formally identified and addressed

## Relevance

Directly answers the multimodal VLM RL carry-forward from May 28–29 with a principled solution to the perception/reasoning entanglement problem — a fresh angle distinct from rubric-based or calibration approaches seen recently.

## My Thoughts

<!-- Add your own notes here -->
