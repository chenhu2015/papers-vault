---
title: "VICT: Verifier-Instrumented Credit Tracing for Long-Horizon LLM Agent Reinforcement Learning"
authors: ["Pengcheng Li", "Zhengyang Zhang", "Dongxu Zhang", "Sui Huang", "Shaohua Ma"]
date: 2026-08-28
arxiv_id: "2608.28128v2"
url: "http://arxiv.org/abs/2608.28128v2"
score: 0.88
topics: [agentic RL, RL training, GRPO, RLHF, LLM agent]
status: unread
---

# VICT: Verifier-Instrumented Credit Tracing for Long-Horizon LLM Agent Reinforcement Learning

## Summary

VICT shifts credit assignment from rollout-side inference to verifier-side tracing: it extracts executable or evidence-backed atoms from the terminal verifier and traces them back to actions through dependency-valid proof edges, redistributing group-relative advantage only along those edges. The method preserves the original terminal reward and changes only the training-time advantage tensor, requiring no learned critic, process labels, branch rollouts, or inference-time verifier access. On ALFWorld and WebShop, VICT substantially improves over outcome-only training and achieves strong performance alongside recent fine-grained credit methods.

## Key Contributions

- Verifier-side credit tracing via executable/evidence-backed atoms + dependency-valid proof edges
- Preserves original terminal reward; changes only the training-time advantage tensor
- No learned critic, process labels, branch rollouts, or inference-time verifier access required
- Abstains when evidence is incomplete or ambiguous, avoiding noisy credit injection

## Relevance

VICT occupies a distinct niche in the hindsight credit redistribution space: unlike TRIAL (trajectory relabeling), T-STAR (step-level hindsight), TASPO (task-anchored process supervision), and CRISP (critical-step perception), VICT derives credit structure from the verifier's own internal decomposition rather than from the rollout. This makes it verifier-coupled rather than rollout-coupled — the closest analog to T-STAR's hindsight approach but operating on verifier structure rather than outcome labels. Together with GACA (NLL-based granularity) and CRISP (critical-step selection), VICT adds a third non-rollout credit signal, further closing the "where does fine-grained credit come from?" question.

## My Thoughts

<!-- Add your own notes here -->
