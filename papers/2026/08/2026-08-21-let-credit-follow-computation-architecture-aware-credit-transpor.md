---
title: "Let Credit Follow Computation: Architecture-Aware Credit Transport for Large Language Model Reinforcement Learning"
authors: ["Qifan Shi", "Zhaolu Kang", "Chenghua Zhu"]
date: 2026-08-21
arxiv_id: "2608.21501v1"
url: "http://arxiv.org/abs/2608.21501v1"
score: 0.88
topics: [agentic RL, RL training, GRPO, reward model]
status: unread
---

# Let Credit Follow Computation: Architecture-Aware Credit Transport for Large Language Model Reinforcement Learning

## Summary

CompPO introduces computation-conditioned credit transport (CCT), mapping the Transformer policy's own attention concentration to a per-token retention gate that parameterizes the causal credit kernel in GAE, replacing the architecture-agnostic stationary geometric kernel of fixed-discount GAE. A transport-aligned critic (TAC) reuses the actor's hidden states and routing information without a second same-scale Transformer. Across five Qwen3-4B seeds, CompPO reaches 61.4% held-out accuracy versus 53.8% for tuned GRPO, with the Comp-GAE+TAC interaction contributing +2.4pp beyond either component alone.

## Key Contributions

- CCT framework: decomposes LLM RL credit into evidence, transport operator, and update geometry — identifies the transport operator as the underexplored component
- Comp-GAE: attention concentration → bounded per-token retention gate → path-dependent generalized-advantage trace with trajectory-specific causal kernel
- TAC (transport-aligned critic): reuses actor hidden states and routing info; recovers fixed-coefficient GAE with constant gate; avoids second full-scale Transformer
- Stability gains: 10/12 PPO-grid runs stable vs 3/12 for GRPO; +4.3 and +3.9 greedy pass@1 macro points on Qwen3-4B and Llama-3.1-8B

## Relevance

CompPO directly addresses the architecture-agnostic limitation of both fixed-discount GAE and GRPO's group-relative broadcast — the specific gap in the hindsight-informed credit redistribution convergence pattern (TRIAL+T-STAR+TASPO+CRISP) identified in prior digests. Where TASPO and CRISP use hindsight from completed trajectories, CompPO uses the policy's internal computation (attention) as the transport medium — a complementary angle that does not require completed trajectories.

## My Thoughts

<!-- Add your own notes here -->
