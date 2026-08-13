---
title: "Self-Supervised On-Policy Distillation for Reasoning Language Models"
authors: ["Zhiquan Tan", "Yinrong Hong"]
date: 2026-08-13
arxiv_id: "2605.17497"
url: "https://arxiv.org/abs/2605.17497"
score: 0.79
topics: [agentic RL, GRPO, RL training, LLM agent, RLHF]
status: unread
---

# Self-Supervised On-Policy Distillation for Reasoning Language Models

## Summary

SSOPD converts GRPO-style rollout groups into dense process supervision by distilling the shortest correct completion (a self-generated witness of how the policy can succeed) into prefixes of the longest wrong completion (persistent failure requiring correction), requiring no external teacher or privileged solution traces. A stopping-time view motivates the shortest-correct/longest-wrong selection rule, and a prompt-level frontier weight concentrates auxiliary loss where correct and wrong branches coexist. Improves over GRPO in all 9 model-benchmark settings on AIME 2024/2025 and HMMT 2025, surpassing the solution-conditioned OPSD baseline by 0.8 points on Qwen3-8B.

## Key Contributions

- Intra-group correct-wrong contrast as dense process supervision without external traces or teacher models
- Stopping-time view motivating shortest-correct/longest-wrong selection rule as finite-group approximation to editing persistent failures toward fast-success actions
- Prompt-level frontier weight concentrating auxiliary loss where correct and wrong branches coexist in the same rollout group
- Surpasses solution-conditioned OPSD baseline (+0.8 pts on Qwen3-8B); improves GRPO in all 9 model-benchmark settings

## Relevance

SSOPD introduces **intra-group self-distillation** as a new mechanism for dense process supervision — complementary to the vault's external-teacher OPD thread (Guided-OPD, FutureBridge-OPD, RP-OPSD, VAD, CFPO, SOD). Where existing mechanisms use an external teacher to supervise student rollouts, SSOPD uses the correct completion from the same rollout group as a self-generated teacher — the policy IS its own supervisor. The frontier weight (active only when correct and wrong branches coexist) directly addresses the all-correct/all-fail problem that parallels GRPO's all-fail filtering (Gap #16 thread). This is an 8th mechanism for Gap #20's multi-level teacher supervision, now extended to self-supervised sources.

## My Thoughts

<!-- Add your own notes here -->
