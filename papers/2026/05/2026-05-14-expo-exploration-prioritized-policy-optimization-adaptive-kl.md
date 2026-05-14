---
title: "expo: Exploration-prioritized policy optimization via adaptive KL regulation and Gaussian curriculum sampling"
authors: ["Mingxiong Lin", "Zhangquan Gong", "Maowen Tang"]
date: 2026-05-14
arxiv_id: "2605.09923"
url: "https://arxiv.org/abs/2605.09923"
score: 0.85
topics: [GRPO, PPO, RL training, agentic RL, RLHF]
status: unread
---

# expo: Exploration-prioritized policy optimization via adaptive KL regulation and Gaussian curriculum sampling

## Summary

GRPO has two understudied inefficiencies: its fixed KL coefficient overconstrains exploration when the policy needs large updates, and uniform question sampling ignores signal informativeness. EXPO adds two lightweight plug-in modules: Accuracy-Conditioned adaptive KL that relaxes the penalty as needed, and Gaussian curriculum sampling that prioritises moderately-difficult problems which provide the most informative gradient signals. Both modules improve GRPO's sample efficiency and final performance on mathematical reasoning benchmarks.

## Key Contributions

- Identifies fixed KL penalty as a structural bottleneck: prevents exploration during phases that require large policy deviations
- Accuracy-Conditioned adaptive KL: dynamically adjusts the regularisation strength based on current policy accuracy
- Gaussian curriculum sampling: selects training problems whose difficulty follows a Gaussian centered on the model's current ability
- Both modules are plug-in compatible with existing GRPO/RLVR training stacks

## Relevance

Complements the GRPO efficiency work (VCRL variance-curriculum from May 13, AdaCuRL from May 13) but targets two different GRPO inefficiencies: the KL penalty design (algorithmic) and the sampling distribution (data). The adaptive-KL angle is new to the digest and directly relevant to the core RL training interest.

## My Thoughts

<!-- Add your own notes here -->
