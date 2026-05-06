---
title: "Dynamic Token Compression for Efficient Video Understanding through Reinforcement Learning"
authors: ["Shida Wang", "YongXiang Hua", "Zhou Tao", "Haoyu Cao", "Linli Xu"]
date: 2026-03-27
arxiv_id: "2603.26365v1"
url: "https://arxiv.org/abs/2603.26365v1"
score: 0.80
topics: [GRPO, VLM, vision-language, multimodal, RL training]
status: unread
---

# Dynamic Token Compression for Efficient Video Understanding through Reinforcement Learning

## Summary

SCORE (Surprise-augmented token COmpression via REinforcement learning) learns an adaptive token-compression policy for video VLMs using a group-wise RL scheme with a split-advantage estimator inspired by GRPO. The policy network is conditioned on a surprise-augmented state incorporating inter-frame residuals to capture temporal dynamics and motion saliency, trained via two-stage curriculum from static pseudo-videos to real dynamic videos. SCORE achieves a 16× prefill speedup while preserving 99.5% of original performance at 10% token retention on diverse video understanding benchmarks.

## Key Contributions

- Surprise-augmented state representation: inter-frame residuals make temporal dynamics and motion saliency explicit for the compression policy
- Group-wise RL with split-advantage estimator: GRPO-inspired training for a non-standard (compression) policy
- Two-stage curriculum: pseudo-video pretraining → real dynamic video fine-tuning for stable RL convergence
- 16× prefill speedup at 10% token retention with 99.5% performance preservation

## Relevance

Novel application of GRPO-style group-wise RL to an efficiency task (token compression) rather than a reasoning task — demonstrates that the RL training framework generalises beyond accuracy-focused objectives. The curriculum approach mirrors DEEP-GRPO's pivot-state resampling in spirit: both address the exploration problem in RL training by staging the difficulty of the training distribution.

## My Thoughts

<!-- Add your own notes here -->
