---
title: "Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates"
authors: ["Yibo Li", "Zijie Lin", "Ailin Deng", "Xuan Zhang", "Yufei He", "Shuo Ji", "Tri Cao", "Bryan Hooi"]
date: 2026-07-31
arxiv_id: "2601.18510"
url: "https://arxiv.org/abs/2601.18510"
score: 0.75
topics: [agentic RL, LLM agent, RL training, reward model]
status: unread
---

# Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates

## Summary

JitRL enables test-time policy optimization for LLM agents without any gradient updates by maintaining a dynamic non-parametric memory of past experiences and retrieving relevant trajectories to estimate action advantages on-the-fly. The additive logit modulation rule — where retrieved advantage estimates directly adjust output logits — is proven to be the exact closed-form solution to the KL-constrained policy optimization objective, grounding the training-free approach in standard RL theory. Outperforms fine-tuning methods including WebRL on WebArena and Jericho while reducing monetary costs by over 30×, establishing a new SOTA among training-free continual learning methods.

## Key Contributions

- Training-free RL: non-parametric memory of experiences + on-the-fly advantage estimation via trajectory retrieval
- Closed-form proof: additive logit update is the exact solution to the KL-constrained policy optimization objective
- Avoids catastrophic forgetting by design (no weight updates), enabling continual adaptation across tasks
- 30× cost reduction over fine-tuning methods (WebRL) while achieving superior performance on WebArena and Jericho

## Relevance

JitRL is the complement to the training-loop approaches that dominate the vault: rather than improving the RL training process (GRPO variants, credit assignment, CIGPO, etc.), it achieves policy optimization at test time via memory retrieval. Its KL-constrained proof connects it to the IG-based credit family — the KL log π_RL/π_ref term that appears in Progress Advantage and CIGPO also appears here as the optimization objective, but JitRL's additive logit solution makes it tractable without gradients. This establishes a bridge between the IG-based training-loop papers and the inference-time memory systems (MemAgent, CompactionRL).

## My Thoughts

<!-- Add your own notes here -->
