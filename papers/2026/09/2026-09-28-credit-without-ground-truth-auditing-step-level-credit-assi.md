---
title: "Credit Without Ground Truth: Auditing Step-Level Credit Assignment in LLM Agents Against Executed Replay"
authors: ["Haiyue Zhang"]
date: 2026-09-28
arxiv_id: "2608.19760v2"
url: "https://arxiv.org/abs/2608.19760"
score: 0.82
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# Credit Without Ground Truth: Auditing Step-Level Credit Assignment in LLM Agents Against Executed Replay

## Summary

This paper audits standard step-level credit signals — LLM-judge scores, outcome-conditioned logprob ratios, and policy confidence — against executed replay (counterfactual rollouts at each decision point in ALFWorld) and finds none show reliable incremental fidelity beyond shuffled controls. Implicit credit echoes policy fluency rather than causal contribution (median rank correlation +0.75), while outcome conditioning adds zero causal information. A 7-arm pre-registered training experiment confirms no credit signal reliably outperforms the untrained baseline, with effective training dose (sparser credit → fewer optimizer steps) as the dominant confound.

## Key Contributions

- Distinguishes step *correctness* (prior work's criterion) from step *contribution* (causal counterfactual via executed replay) — they come apart empirically
- Executed replay ground truth: 30.5% of ALFWorld decision points show nonzero replay contrast; measurability is model-dependent (13.1% vs. 26.8% counterfactual-free points across two similar-scale policies)
- Fluency confound: implicit credit (logprob ratio) correlates with policy fluency, not causal impact; replicates across two model families
- Dose confound in training: sparser credit retains fewer training examples — an order-of-magnitude spread in optimizer steps means experiments without sample-size matching measure dose, not credit content

## Relevance

This is the most important critical paper for the step-level credit cluster (GRAFT, SALT, ProCredit, TIGPO, MileGPO). If existing credit signals are confounded by policy fluency and effective training dose rather than causal contribution, the entire five-paper cluster may be measuring something other than step credit quality. The executed replay methodology also provides a concrete framework for validating future credit methods — papers claiming step-credit improvements should now match effective sample size and test against executed replay ground truth.

## My Thoughts

<!-- Add your own notes here -->
