---
title: "Diagnosing Training Inference Mismatch in LLM Reinforcement Learning via a Zero-Mismatch Reference"
authors: ["Tianle Zhong", "Neiwen Ling", "Yifan Pi", "Zijun Wei", "Tianshu Yu", "Geoffrey Fox", "Peng Wu", "Xiao Yu"]
date: 2026-05-14
arxiv_id: "2605.14220v2"
url: "https://arxiv.org/abs/2605.14220"
score: 0.85
topics: [RL training, GRPO, RLHF, agentic RL]
status: unread
---

# Diagnosing Training Inference Mismatch in LLM Reinforcement Learning via a Zero-Mismatch Reference

## Summary

VeXact introduces a zero-mismatch diagnostic setting to isolate Training-Inference Mismatch (TIM) — token-level probability disagreements from implementation differences between rollout and optimization stages — from off-policy drift and common stabilization mechanisms. The key finding is that small numerical disagreements alone, independent of off-policy drift, can cause training collapse by changing the effective optimization problem, establishing TIM as a first-order systems-level factor rather than benign numerical noise. A set of remedies is identified, complementing the DLC decomposition (Nov 7) of numerical discrepancy vs. policy lag.

## Key Contributions

- VeXact diagnostic setting: zero-mismatch reference that isolates TIM from off-policy drift and stabilization mechanisms, enabling clean attribution of instability to implementation-level differences
- Demonstrates TIM causes collapse independently: small token-level numerical disagreements can independently cause training collapse without any off-policy component
- TIM changes the effective optimization problem: not just noise but a systematic perturbation to the loss landscape
- Identifies a set of remedies, positioning TIM as a first-order concern in LLM RL systems alongside staleness and policy lag

## Relevance

This is the companion/predecessor to the DLC decomposition paper (On the Origin and Evolution of Training-Inference Mismatch, Nov 7 digest) which decomposed TIM into numerical discrepancy and policy lag components. VeXact isolates the numerical discrepancy component in a controlled setting and proves it is non-benign — directly grounding the Nov 7 paper's decomposition with experimental evidence. Together they form a coherent theory of training-inference mismatch in RLVR systems.

## My Thoughts

<!-- Add your own notes here -->
