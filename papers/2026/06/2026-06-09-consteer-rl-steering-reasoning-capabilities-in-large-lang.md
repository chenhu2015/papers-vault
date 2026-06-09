---
title: "ConSteer-RL: Steering Reasoning Capabilities in Large Language Models via Confidence-Aware Reinforcement Learning"
authors: ["Qing Miao", "Yiming Zhao", "Jing Yang", "Chenxi Liu", "Yuehai Chen", "Yuewen Liu", "Shaoyi Du", "Badong Chen"]
date: 2026-06-09
arxiv_id: "2606.08088"
url: "https://arxiv.org/abs/2606.08088"
score: 0.73
topics: [reinforcement learning, RL training, GRPO, reward model, PPO]
status: unread
---

# ConSteer-RL: Steering Reasoning Capabilities in Large Language Models via Confidence-Aware Reinforcement Learning

## Summary

ConSteer-RL integrates token-level confidence signals derived from model log-probabilities into GRPO training via a confidence-aware reward that penalizes overconfident errors while reinforcing correct confident reasoning. This simple augmentation to the GRPO framework achieves 2.3–4.0% average improvements across model scales on reasoning benchmarks, addressing the sparse binary reward limitation of standard RLVR. The approach requires no external signal beyond the model's own generation probabilities.

## Key Contributions

- Confidence-aware reward: aggregates per-token log-probabilities into scalar confidence scores
- Awareness-based reward shaping: penalizes overconfident errors, reinforces correct+confident answers
- 2.3–4.0% average gain over GRPO baselines across model scales
- No external reward model or verifier required — entirely self-contained

## Relevance

Sits at the intersection of the GRPO training stability thread (EP-GRPO, M-GRPO) and reward model alternatives. Uses the model's own confidence as an implicit process signal — similar in spirit to EP-GRPO's entropy-gated modulation but through reward shaping rather than gradient modification. Connects also to the ECPO (June 8) approach of using internal statistical signals to improve credit assignment.

## My Thoughts

<!-- Add your own notes here -->
