---
title: "Beyond Entropy: Self-Diagnostic Multi-Role Token Optimization for Video Reasoning"
authors: ["Yudong Han", "Yong Wang", "Zaiquan Yang", "Liang Lin", "Chongyang Tao", "Xiangxiang Chu", "Liyuan Pan"]
date: 2026-10-02
arxiv_id: "2610.03400"
url: "https://arxiv.org/abs/2610.03400"
score: 0.82
topics: [multimodal models, vision language models, VLM, RL training]
status: unread
---

# Beyond Entropy: Self-Diagnostic Multi-Role Token Optimization for Video Reasoning

## Summary

DyCPO addresses token-level credit assignment in VLM RL by constructing a multi-role dependence metric that separates visual exploration tokens from answer-relevance tokens, avoiding the over-reliance on entropy heuristics that extends reasoning length without improving accuracy. Its key novelty is self-diagnostic counterfactual signals derived from the model's own successful and failed rollouts, allowing the optimization objective to co-evolve with the policy rather than using static counterfactual priors. Consistent improvements over entropy-based and static-counterfactual baselines are demonstrated on video reasoning and general video understanding benchmarks.

## Key Contributions

- Multi-role dependence metric: a single token receives a joint score over visual-exploration and answer-relevance roles, balancing how much to encourage exploration vs. suppress it in favour of decisive reasoning
- Self-diagnostic counterfactual: counterfactual signals are derived from the model's own successful and failed rollouts rather than static priors, enabling co-evolution of the credit signal with the policy
- Filler token suppression: explicitly penalises tokens that are exploration-only without answer relevance (known cause of length inflation)
- Applied to video reasoning: addresses the unique challenge that visual tokens can dominate high-entropy heuristics and mislead credit assignment in multimodal settings

## Relevance

Adds a 6th entry to the VLM RL credit assignment thread (prior: TPAE importance, persistence-aware verifiability, TTRSD sensitivity, TTIQ joint grounding, SAVOR reliability). DyCPO's self-diagnostic co-evolution angle connects directly to RewardWeaver (Oct 8) — both adapt their credit/reward signal to the current policy state rather than using a fixed signal, but DyCPO does so at the token level within a single rollout rather than at the training-stage level.

## My Thoughts

<!-- Add your own notes here -->
