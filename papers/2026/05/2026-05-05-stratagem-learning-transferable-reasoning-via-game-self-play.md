---
title: "Stratagem: Learning Transferable Reasoning via Trajectory-Modulated Game Self-Play"
authors: ["Xiachong Feng", "Deyi Yin", "Xiaocheng Feng", "Yi Jiang", "Libo Qin", "Yangfan Ye", "Lei Huang", "Weitao Ma", "Qiming Li", "Yuxuan Gu", "Bing Qin", "Lingpeng Kong"]
date: 2026-04-20
arxiv_id: "2604.17696v1"
url: "http://arxiv.org/abs/2604.17696v1"
score: 0.78
topics: [reinforcement learning, agentic RL, RL training]
status: unread
---

# Stratagem: Learning Transferable Reasoning via Trajectory-Modulated Game Self-Play

## Summary

Stratagem addresses the key failure mode of game self-play for LLMs—patterns learned remain anchored in game-specific semantics and fail to transfer—by introducing a Reasoning Transferability Coefficient (RTC) that selectively reinforces trajectories exhibiting abstract, domain-agnostic reasoning. A complementary Reasoning Evolution Reward incentivizes progressive reasoning development, preventing contextual stasis where static game contexts fail to grow the model's capabilities. The dual mechanism produces substantial improvements on math, general reasoning, and code generation benchmarks, with especially strong competition-level mathematics gains.

## Key Contributions

- Reasoning Transferability Coefficient (RTC): identifies and selectively reinforces trajectories with domain-agnostic, transferable reasoning patterns
- Reasoning Evolution Reward: incentivizes increasing reasoning complexity over training to prevent stagnation
- Demonstrates that game self-play can generalize to math and code when transfer is explicitly targeted
- Human evaluation confirms both components contribute independently to transferable reasoning

## Relevance

Addresses exploration and generalization in RL training for LLMs—a thread running through DEEP-GRPO, HeRL, and PolicySplit from earlier digests. Stratagem is the first to specifically target the transfer problem in game self-play, making it a useful complement to those exploration strategies.

## My Thoughts

<!-- Add your own notes here -->
