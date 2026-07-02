---
title: "CRAFT: Counterfactual Credit Assignment from Free Sibling Rollouts for Self-Distilled Agentic Reinforcement Learning"
authors: ["Zibin Meng", "Kani Chen"]
date: 2026-07-02
arxiv_id: "2606.29476v1"
url: "https://arxiv.org/abs/2606.29476"
score: 0.88
topics: [agentic RL, GRPO, credit assignment, tool use, LLM agent, RLHF]
status: unread
---

# CRAFT: Counterfactual Credit Assignment from Free Sibling Rollouts for Self-Distilled Agentic Reinforcement Learning

## Summary

CRAFT proposes counterfactual token importance by reusing the G-1 sibling rollouts GRPO already samples, importance-weighting them by log-probability gap to form a signed per-token counterfactual credit estimate at near-zero extra compute. Two additional pillars — an asymmetric KL/distillation controller and a per-token polarized KL penalty switching between mode-seeking and mode-covering by credit sign — complete a three-pillar self-distilled agentic RL scheme. The estimator is proven consistent with a variance bound; evaluated across three agentic environments, four model scales, and five end-to-end methods.

## Key Contributions

- Pillar 1: Counterfactual Token Importance — reuses G-1 GRPO sibling rollouts, importance-weighting by log-probability gap to form a signed per-token credit estimate of counterfactual advantage change
- Pillar 2: Asymmetric KL/distillation controller — raises distillation weight as it lowers KL weight along EMA of gate activity, and conversely
- Pillar 3: Polarized KL penalty — per-token mode-seeking vs. mode-covering update switched by credit sign
- Proof of estimator consistency and variance bound; bit-exact reproducibility guarantees isolate algorithmic contribution from implementation drift

## Relevance

CRAFT's Pillar 1 is the counterfactual analog of SCPO's sibling-step credit (Jun 30): where SCPO borrows credit from semantically similar successful siblings to recover failed-step value, CRAFT estimates the counterfactual change in group advantage if teacher-preferred tokens were upweighted — using the same G-1 sibling rollouts GRPO already computes. The three-pillar design also connects to PASS (Jul 1): Pillars 2 and 3 address the channel contamination and resolution mismatch failure modes at the optimization layer rather than the signal layer. The agentic evaluation scope directly follows the FlowTracer thread queued for today.

## My Thoughts

<!-- Add your own notes here -->
