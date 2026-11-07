---
title: "Does Chain-of-Thought Reliance Follow a Scaling Law? Larger Models Follow Their Steps More, Independent of Post-Training"
authors: ["Esther Xin"]
date: 2026-10-28
arxiv_id: "2610.38433v1"
url: "https://arxiv.org/abs/2610.38433"
score: 0.80
topics: [RLHF, reward model, reinforcement learning, LLM agent]
status: unread
---

# Does Chain-of-Thought Reliance Follow a Scaling Law? Larger Models Follow Their Steps More, Independent of Post-Training

## Summary

Using a synthetic box-swap task with exact ground truth, the authors measure how much model answers follow step-edits injected mid-chain, across 25 open-weight models. CoT reliance rises from 16–18% at 0.6B to 97–100% at 14B Qwen3 (logistic in log N, R²=0.89), with capability as the primary driver (r=0.99 correlation between reliance and step accuracy); post-training changes reliance by at most 0.03 at ≥4B. The finding that scale makes CoT more load-bearing directly informs the reward faithfulness thread: monitoring CoT causality is more reliable for larger models.

## Key Contributions

- Synthetic box-swap methodology: injects a wrong-but-valid state into the model's own CoT mid-chain, measures answer-follows-edit rate as exact CoT reliance metric
- Logistic scaling law for reliance in Qwen3 (R²=0.89), validated on Gemma 3 and Llama 3
- Capability is the primary driver (r=0.99 reliance vs step accuracy), not model family or post-training
- Post-training barely affects reliance (Δ≤0.03 at ≥4B) — a finding that constrains what RLVR can achieve for CoT faithfulness
- No model up to 14B solves the task internally (without written steps): CoT is load-bearing for capable models

## Relevance

This paper is the empirical companion to CRoS (scrambled CoT causality) and Chain of Faith (policy-internal reward for CoT faithfulness): where those papers propose methods to improve CoT faithfulness in RLVR, this paper establishes that reliance itself scales predictably with model capability — which means large models are good targets for CoT monitoring, but small models may not be meaningfully monitored at all.

## My Thoughts

<!-- Add your own notes here -->
