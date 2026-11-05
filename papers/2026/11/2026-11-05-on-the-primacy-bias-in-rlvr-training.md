---
title: "On the Primacy Bias in RLVR Training"
authors: ["Phuc Minh Nguyen", "Ngoc-Hieu Nguyen", "Parshin Shojaee", "Chinh Duc La", "Duy Minh Ho Nguyen", "Rui Zhang", "Khoa D. Doan", "Ting Hua", "Nitesh V. Chawl"]
date: 2026-11-02
arxiv_id: "2611.04061v1"
url: "http://arxiv.org/abs/2611.04061v1"
score: 0.83
topics: [GRPO, RL training, RLHF, reinforcement learning]
status: unread
---

# On the Primacy Bias in RLVR Training

## Summary

RLVR training exhibits primacy bias: mixed-data training disproportionately sharpens performance on easy problems while yielding marginal gains on hard ones, though hard problems are precisely what expands the model's reasoning frontier. Training too long on hard problems causes forgetting on easy ones, explaining prior conflicting observations — in OOD domains where the base model is weak, hard-problem RL genuinely expands reasoning; on well-trained domains, forgetting masks genuine gains.

## Key Contributions

- Identifies primacy bias mechanism in RLVR: easy problems crowd out hard ones during mixed training, biasing representation updates
- Demonstrates that hard problems genuinely expand model representations and push capability boundaries
- Shows a forgetting-expansion tradeoff: prolonged hard-problem training improves OOD capability but degrades easy-problem performance
- Reconciles conflicting prior observations about RLVR effectiveness across different domain conditions

## Relevance

Core paper for the GRPO training dynamics thread; directly explains the OOD generalization failure finding from "Not All Reasoning Generalizes" (Nov 4) and provides a unifying mechanism for why RLVR gives inconsistent gains across domains. The easy/hard curriculum design question is now a central open problem in the thread.

## My Thoughts

<!-- Add your own notes here -->
