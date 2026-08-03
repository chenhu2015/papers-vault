---
title: "LoRA Scaffolded Policy Optimization (LSPO): A Sampling-Time Low-Rank Scaffold for Recovering Reinforcement-Learning Gradient on Zero-Reward Cliff Prompts"
authors: ["Ken Ding"]
date: 2026-08-03
arxiv_id: "2607.27787"
url: "http://arxiv.org/abs/2607.27787v1"
score: 0.83
topics: [GRPO, PPO, RL training, reinforcement learning, agentic RL]
status: unread
---

# LoRA Scaffolded Policy Optimization (LSPO)

## Summary

LSPO addresses the cliff-prompt (all-fail group) problem in GRPO: each RL step it detects cliff prompts, fits a LoRA adapter via brief supervised training on ground-truth solutions, re-rolls cliff prompts with base+adapter to produce successful completions, splices these back into the RL batch with importance-sampling correction, then takes a GRPO step on the base model alone—the adapter is discarded, yielding a base-only checkpoint. On DeepMath-103K with DeepSeek-R1-Distill-Qwen-1.5B, LSPO beats DAPO on all 16 benchmark/pass@k evaluation cells, with gains up to +10.7 points on AIME24/pass@4.

## Key Contributions

- Detects all-fail cliff prompts each RL step and bootstraps them with a transient LoRA adapter trained on ground-truth solutions
- Importance-sampling correction splices adapter-generated successful completions into the main GRPO batch without biasing the base policy gradient
- Adapter is discarded after each step; no architectural change to the trained model (base-only checkpoint)
- Beats DAPO on all 16 (benchmark, pass@k) cells on DeepMath-103K at 1000-step horizon

## Relevance

LSPO is the 10th distinct approach to Gap #16 (GRPO all-fail group handling) in the vault. Its mechanism introduces a fourth structural class beyond the three previously identified: (1) reward shaping within groups (CIGPO, RDPO, OC-GRPO), (2) proxy substitution (ProGPO), (3) within-group NL contrast (GRSD), (4) group filtering/routing (TAO-RL, TACO/OGAR). LSPO's class is *sampling-time scaffolding*: it does not change the reward, filter, or contrast — it temporarily augments the model's sampling capability with a LoRA adapter to produce positive examples, then discards the adapter. This is structurally closest to ProGPO (both manufacture a positive signal from cliff groups) but operates at the parameter level rather than the reward level. The IS-corrected splicing mechanism is also new: it integrates external completions into GRPO without requiring a separate off-policy algorithm.

## My Thoughts

<!-- Add your own notes here -->
