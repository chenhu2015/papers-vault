---
title: "Calibrated Decision Rewards: Training Language Models with a Judge That Knows How Sure It Is"
authors: ["Rudransh Agnihotri", "Manasvi Kapoor"]
date: 2026-11-18
arxiv_id: "2611.25135v1"
url: "http://arxiv.org/abs/2611.25135v1"
score: 0.88
topics: [reward model, RLHF, GRPO, RL training]
status: unread
---

# Calibrated Decision Rewards: Training Language Models with a Judge That Knows How Sure It Is

## Summary

RLCDR converts an LLM into a calibrated decision model that answers typed quality questions ("is the final answer correct?", "which step is the first error?") with probability distributions read in one forward pass, debiased over option orders and calibrated with ~100 labels. Using this as a GRPO reward raises MATH500 from 72.2% to 76.8% (+4.65 pts) without any reference answer, matching answer-key training, while the same model doubles as a PRM outperforming a dedicated 7B process reward model (ProcessBench F1 0.772 vs 0.722) with no step-level training.

## Key Contributions

- Decision-model formulation turns any LLM into a calibrated binary/multi-class reward with one forward pass and ~100 calibration labels
- Reference-free reward matches answer-key GRPO performance; expected calibration error is half that of a softmax judge on the same backbone
- Emergent PRM capability: without step training, the calibrated model finds the first wrong step better than a dedicated 7B PRM
- Six pre-registered hypotheses each tested with a falsifying control, mapping where the approach breaks down (overconfidence on out-of-distribution hard problems)

## Relevance

Directly bridges the PRM vocabulary gap noted in the recent digests: RLCDR achieves PRM-quality step evaluation without step supervision and no process labels, using only a calibrated decision head. The calibrated probability formulation is orthogonal to the GRPO objective variants cluster (LGPO, EPIC, APMPO) — it operates on the reward signal rather than the policy update rule.

## My Thoughts

<!-- Add your own notes here -->
