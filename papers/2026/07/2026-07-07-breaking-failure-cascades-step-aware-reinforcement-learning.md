---
title: "Breaking Failure Cascades: Step-Aware Reinforcement Learning for Medical Multimodal Reasoning"
authors: ["Junha Jung", "Minbyul Jeong", "Suhyeon Lim", "Sungwook Jung", "Jaehoon Yun", "Taeyun Roh", "Mujeen Sung", "Jaewoo Kang"]
date: 2026-07-07
arxiv_id: "2606.31825v1"
url: "http://arxiv.org/abs/2606.31825v1"
score: 0.72
topics: [GRPO, multimodal, vision-language, VLM, RL training, agentic RL]
status: unread
---

# Breaking Failure Cascades: Step-Aware Reinforcement Learning for Medical Multimodal Reasoning

## Summary

MRPO (Medical Reasoning-aware Policy Optimization) diagnoses cascading errors from early reasoning step failures as the leading cause of incorrect predictions in medical visual question answering, noting that outcome-centric training (GRPO) assigns uniform signal regardless of where in the chain the reasoning went wrong. MRPO assigns exponentially larger penalties to tokens in earlier invalid reasoning steps when the final answer is incorrect, breaking the failure cascade without penalizing correct reasoning paths. Applied over Qwen3-VL-8B, MRPO reduces early-stage reasoning failures from 64.0% to 13.0% and outperforms HuatuoGPT-Vision-34B by 2.79 points.

## Key Contributions

- Failure cascade diagnosis: outcome-centric RL fails to distinguish where in the chain reasoning broke down
- Step-position-weighted exponential penalty: heavier signal assigned to earlier invalid steps when final answer is wrong
- Selective penalization: correct reasoning paths are untouched regardless of step position
- 64% → 13% early-stage failure reduction on medical VQA with 4× smaller model

## Relevance

Extends the RLVR credit assignment thread into the step-position dimension. The credit assignment hierarchy in the vault covers response-level (RLHF), role-typed segment (TRIAGE), sentence-level (Jul 6), token-level (AT-RL, TAPO), and process reward (CF-GRPO, MRPO for medical VLM); MRPO adds position-weighted exponential credit decay within a reasoning chain, which is a temporal-position analog of the geometric discount in RL value functions applied to reasoning steps rather than time steps.

## My Thoughts

<!-- Add your own notes here -->
