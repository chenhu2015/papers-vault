---
title: "Agon: Competitive Cross-Model RL with Implicit Rival Grading of Reasoning"
authors: ["Vladislav Beliaev"]
date: 2026-09-04
arxiv_id: "2607.07690v1"
url: "http://arxiv.org/abs/2607.07690v1"
score: 0.79
topics: [GRPO, reinforcement learning, reward model, RLHF, RLAIF, agentic RL]
status: unread
---

# Agon: Competitive Cross-Model RL with Implicit Rival Grading of Reasoning

## Summary

Agon replaces GRPO's outcome-only reward with implicit rival grading: two models of similar strength alternately draft and read each other's solutions to the same problem, earning reward for out-solving the rival that has seen their work — so reasoning quality is judged implicitly during training with no process labels or reward model. At inference the pair deploys as a two-stage cascade (drafter + reader), doubling GRPO's pass@1 on DeepMath (roughly 8× the gain of an untrained Mixture-of-Agents) and replicating on competitive-programming code across Qwen3 and Gemma 4. Agon provides a self-improving training signal that avoids reward hacking and scales with model capability rather than with annotation cost.

## Key Contributions

- Implicit rival grading: reasoning quality evaluated without process labels by training each model to out-solve a rival that has seen its work
- Two-stage cascade inference: drafter produces a solution, reader answers after reading the draft — the inference pattern mirrors the training dynamic
- 2× GRPO pass@1 improvement on DeepMath hard split; ~8× gain over untrained Mixture-of-Agents baseline
- Generalizes across competitive programming and two model families (Qwen3, Gemma 4)

## Relevance

Agon addresses a gap left open by the entire Sep GRPO improvement stack (MaxPO, OTB, StructReward, NC-GRPO): all five optimize the policy given a fixed reward signal, while Agon replaces the reward signal itself with a dynamic, capability-matched implicit signal. This is structurally complementary to LLM-jury (Sep 04) — both replace static reward models with multi-model inference-time signals — but Agon bakes the multi-model structure into training rather than using it only at test time. The combination of Agon's rival-grading training signal with NC-GRPO's latent-space rollout diversification remains unexplored.

## My Thoughts

<!-- Add your own notes here -->
