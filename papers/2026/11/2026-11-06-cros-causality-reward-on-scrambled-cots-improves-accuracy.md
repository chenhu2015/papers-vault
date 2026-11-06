---
title: "CRoS: Causality Reward on Scrambled CoTs Improves Accuracy and Reasoning Faithfulness"
authors: ["Xiao Yu", "Justin Chih-Yao Chen", "Zaid Khan", "Hyunji Lee", "Mohit Bansal"]
date: 2026-10-30
arxiv_id: "2610.42054v1"
url: "http://arxiv.org/abs/2610.42054v1"
score: 0.84
topics: [RLVR, RL training, reward model, GRPO]
status: unread
---

# CRoS: Causality Reward on Scrambled CoTs Improves Accuracy and Reasoning Faithfulness

## Summary

CRoS introduces a causality reward for RLVR training that perturbs the order of reasoning steps (scrambling) rather than their content, cleanly measuring whether the final answer depends on CoT step sequencing rather than individual step information — avoiding the information-change confound in prior causality metrics that delete or inject errors into steps. On Reasoning Gym with Gemma-3-4B, CRoS achieves 46.8% OOD accuracy versus 43.8% for the strongest baseline and improves hint acknowledgment (CoT faithfulness) from 20.2% to 34.0%.

## Key Contributions

- Novel causality metric: scramble step order without altering content, isolating sequencing dependence
- Identifies why existing causality metrics fail: content-altering perturbations measure information sensitivity, not causal role
- CRoS reward induces more informative CoTs and better exploration/self-correction than content-perturbation baselines
- +3pp OOD accuracy, higher CoT-Pass@K across K=1–128, +13.8pp hint acknowledgment on Gemma-3-4B

## Relevance

Extends the GRPO training dynamics and reasoning faithfulness thread: existing RLVR outcome-only training fails to reinforce high-quality reasoning chains, and causality metrics applied during training can repair this but only if the metric isolates the right property. CRoS diagnoses why prior approaches introduced undesirable reasoning behaviors (less informative CoTs, reduced exploration) and fixes the core confound. Pairs with Chain of Faith (Nov 6 search, policy-internal CoT faithfulness rewards) and the broader reward hacking thread.

## My Thoughts

<!-- Add your own notes here -->
