---
title: "ICRL: Learning to Internalize Self-Critique with Reinforcement Learning"
authors: ["Jianbo Lin", "Xiaomin Yu", "Yi Xin", "Yifu Guo", "Zhuosong Jiang", "Zhongqi Yue", "Weishi Wang", "Heqing Zou", "Chengwei Qin", "Hui Xiong"]
date: 2026-05-20
arxiv_id: "2605.15224v1"
url: "http://arxiv.org/abs/2605.15224v1"
score: 0.87
topics: [agentic RL, GRPO, reward model, LLM agent, RL training]
status: unread
---

# ICRL: Learning to Internalize Self-Critique with Reinforcement Learning

## Summary

ICRL jointly trains a solver and critic from a shared backbone, with the critic rewarded based on the solver's subsequent performance gain—incentivizing actionable rather than superficial feedback. A distribution-calibration re-weighting ratio selectively transfers critique-guided improvements to critique-free mode, preventing solver dependence on external critique at test time. On Qwen3-4B/8B, ICRL achieves +6.4 points over GRPO on agentic tasks and +7.0 on mathematical reasoning, with an 8B critic matching 32B baselines at substantially fewer tokens.

## Key Contributions

- Joint solver+critic training from shared backbone: critic reward tied to solver's post-critique performance gain
- Distribution-calibration re-weighting: bridges the gap between critique-conditioned and critique-free distributions
- Role-wise group advantage estimation: stabilizes joint optimization across the two asymmetric roles
- Learned 8B critic achieves parity with 32B external critics while using far fewer tokens per step

## Relevance

This extends the self-improvement thread (today's query 2) with a principled RL mechanism. Unlike SPIRAL/self-play (May 15, adversarial) or SDAR (May 16, distillation), ICRL does cooperative critic-solver RL with explicit distribution alignment—directly relevant to the GRPO + reward model + agentic RL core interests. The efficiency result (8B ≈ 32B critic) is particularly actionable for cost-efficient agentic pipelines.

## My Thoughts

<!-- Add your own notes here -->
