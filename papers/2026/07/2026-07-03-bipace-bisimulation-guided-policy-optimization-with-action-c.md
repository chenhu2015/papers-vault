---
title: "BiPACE: Bisimulation-Guided Policy Optimization with Action Counterfactual Estimation for LLM Agents"
authors: ["Hanyang Wang", "Weijieying Ren", "Yuxiang Zhang", "Ding Cao", "Zhizhao Zeng", "Ke Zeng", "Tianxiang Zhao"]
date: 2026-06-24
arxiv_id: "2606.25556v1"
url: "http://arxiv.org/abs/2606.25556v1"
score: 0.90
topics: [agentic RL, GRPO, LLM agent, reward model]
status: unread
---

# BiPACE: Bisimulation-Guided Policy Optimization with Action Counterfactual Estimation for LLM Agents

## Summary

BiPACE diagnoses a state-action credit mismatch in GRPO-style agentic training: observation-hash partitioning creates singleton groups with zero signal, while within-group means conflate state-value and action-credit. It fixes both with bisimulation clustering (cosine distance in actor hidden-state geometry for behavioral equivalence) and action-conditioned peer baselines that nonparametrically estimate Q(s,a)-V(s). On ALFWorld/Qwen2.5-7B, BiPACE achieves 97.1% vs GiGPO's 90.8%, crossing the 95% threshold on every seed.

## Key Contributions

- Formal diagnosis of two GRPO credit pathologies: singleton group problem (zero signal from over-fine state partitioning) and action-credit conflation (within-group mean mixes state-value with action-specific advantage)
- BiGPO: bisimulation clustering via cosine distance in actor hidden-state space as a policy-induced proxy for bisimulation equivalence — substantially lowers singleton rate vs observation hashing
- PACE: action-conditioned peer baselines within behavioral clusters; Q-style estimate nonparametrically computes Q(s,a)-V(s) from return-to-go of peers taking different actions in equivalent states
- Only 11.3% wall-clock overhead per training step; no extra rollouts, critic, or auxiliary loss

## Relevance

BiPACE is the most principled response to CRAFT's (Jul 2) counterfactual token credit work: where CRAFT estimated counterfactual change in group advantage by reweighting sibling rollouts, BiPACE estimates local Q(s,a)-V(s) by clustering behaviorally equivalent states and comparing different actions within those clusters. The bisimulation proxy is conceptually adjacent to TRIAGE's (Jul 2) role-conditioned credit — both partition the step space by behavioral type rather than surface observation identity — but BiPACE uses the actor's own geometry rather than hand-defined role taxonomy.

## My Thoughts

<!-- Add your own notes here -->
