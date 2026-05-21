---
title: "Mitigating LLM Hallucination via Behaviorally Calibrated Reinforcement Learning"
authors: ["Jiayun Wu", "Jiashuo Liu", "Zhiyuan Zeng", "Tianyang Zhan", "Tianle Cai", "Wenhao Huang"]
date: 2025-12-22
arxiv_id: "2512.19920v3"
url: "http://arxiv.org/abs/2512.19920v3"
score: 0.79
topics: [RLHF, RLAIF, reward model, RL training, reinforcement learning]
status: unread
---

# Mitigating LLM Hallucination via Behaviorally Calibrated Reinforcement Learning

## Summary

This work reframes RLVR to train models to output calibrated probabilities of correctness—either abstaining or flagging uncertain claims—rather than just maximizing answer correctness. Using strictly proper scoring rules as reward signals, a Qwen3-4B model trained on math tasks achieves uncertainty quantification surpassing GPT-5's hallucination ratio in-domain and matches frontier models (Grok-4, Gemini-2.5-Pro) on cross-domain factual QA calibration error. The result shows behavioral calibration as a transferable meta-skill decoupled from raw accuracy.

## Key Contributions

- Reframes RLVR objective: reward calibrated confidence output rather than binary correctness
- Strictly proper scoring rules (Brier, log-loss) as RL reward signals for uncertainty quantification
- Behavioral calibration shown as a transferable meta-skill: trained on math, generalizes to factual QA
- 4B model surpasses GPT-5 on log-scale Accuracy-to-Hallucination Ratio (0.806 vs 0.207) in-domain

## Relevance

Introduces a fundamentally different reward design philosophy from the accuracy-maximizing RLVR dominant in recent digests: rewarding calibration rather than correctness. Connects to the RLHF/reward model core interest while opening a new angle on what "correct" RL reward should optimize.

## My Thoughts

<!-- Add your own notes here -->
