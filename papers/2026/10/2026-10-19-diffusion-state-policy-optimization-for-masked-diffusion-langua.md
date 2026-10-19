---
title: "Diffusion-State Policy Optimization for Masked Diffusion Language Models"
authors: ["DiSPO authors"]
date: 2026-10-19
arxiv_id: "2602.06462v4"
url: "http://arxiv.org/abs/2602.06462v4"
score: 0.87
topics: [RL training, reward model, GRPO, agentic RL, step credit]
status: unread
---

# Diffusion-State Policy Optimization for Masked Diffusion Language Models

## Summary

DiSPO introduces step-level credit assignment for masked diffusion LMs by branching at intermediate masked states: it resamples currently masked positions from rollout-cached logits, scores the resulting completions, and updates only the newly filled tokens — requiring no extra diffusion rollouts. A fixed-state objective and reuse-friendly policy-gradient estimator make it a drop-in plug-in that consistently improves diffu-GRPO and SPG on math and planning benchmarks under matched compute.

## Key Contributions

- Credit assignment at intermediate masked states, not just terminal completions
- Branching via rollout-cached logit resampling — no additional diffusion rollouts required
- Fixed-state objective with policy-gradient estimator compatible with standard trainers
- Plug-in design validated on LLaDA-8B-Instruct across math and planning benchmarks

## Relevance

Directly extends the diffusion LM RL thread (PACT + GDPO + CJ-GRPO) with a fourth paper now adding step-level credit assignment — filling the same gap PACT addresses but from a branching-state rather than trajectory-segment perspective. Also bridges the step-credit cluster to diffusion LMs specifically.

## My Thoughts

<!-- Add your own notes here -->
