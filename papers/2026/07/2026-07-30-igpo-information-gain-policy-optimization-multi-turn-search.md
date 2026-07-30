---
title: "Information Gain-based Policy Optimization: A Simple and Effective Approach for Multi-Turn Search Agents"
authors: ["Guoqing Wang", "Sunhao Dai", "Guangze Ye", "Zeyu Gan", "Wei Yao", "Yong Deng", "Xiaofeng Wu", "Zhenzhe Ying"]
date: 2026-07-30
arxiv_id: "2510.14967v2"
url: "http://arxiv.org/abs/2510.14967v2"
score: 0.85
topics: [agentic RL, RL training, GRPO, LLM agent, reward model]
status: unread
---

# Information Gain-based Policy Optimization: A Simple and Effective Approach for Multi-Turn Search Agents

## Summary

IGPO models each multi-turn interaction as an incremental process of acquiring information about the ground truth, defining turn-level rewards as the marginal increase in the policy's probability of producing the correct answer — the same IG principle later used by CIGPO (Jul 29) but published earlier (October 2025) and applied to multi-turn search agents. Unlike process-reward approaches requiring external models or Monte Carlo estimation, IGPO derives intrinsic rewards directly from the model's own belief updates and combines them with outcome supervision for dense reward signals. Outperforms strong RL baselines on in-domain and out-of-domain benchmarks with higher accuracy and improved data efficiency.

## Key Contributions

- Defines turn-level IG as marginal increase in the policy's probability of producing the correct answer per turn — intrinsic reward requiring no external reward model
- Addresses three critical issues in multi-turn RL with sparse rewards: advantage collapse, lack of fine-grained credit assignment, and poor sample efficiency
- Combines IG intrinsic rewards with outcome-level supervision into dense reward signals trainable with standard GRPO
- Demonstrates generalization: outperforms baselines on both in-domain and out-of-domain multi-turn benchmarks

## Relevance

IGPO is the October 2025 precursor to CIGPO (Jul 29, 0.87), which uses the same per-turn IG concept extended to multi-turn retrieval with reference model log-likelihood as the belief estimator. IGPO's formulation — marginal increase in P(correct answer) per turn — is the original instantiation of what the Jul 29 digest identified as a "turn-level decomposition of Progress Advantage." This places IGPO as the foundational paper in the IGPO → InfoReasoner (Jan 2026) → InfoPO (Feb 2026) → CIGPO (Jul 2026) sequence of IG-based multi-turn credit assignment methods.

## My Thoughts

<!-- Add your own notes here -->
