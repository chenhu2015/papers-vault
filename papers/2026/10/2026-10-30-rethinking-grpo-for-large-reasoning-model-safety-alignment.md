---
title: "Rethinking GRPO for Large Reasoning Model Safety Alignment"
authors: ["Jiawei Chen", "Yi Zhang", "Jiawei Du", "Zhonghou Lv", "Tairan Chen", "Junyuan Shang", "Jinchang Hou", "Xiao Yang", "Yu Tian", "Chenfu Bao", "Chao Yu", "Zhaoxia Yin"]
date: 2026-10-30
arxiv_id: "2610.23085v1"
url: "http://arxiv.org/abs/2610.23085v1"
score: 0.85
topics: [GRPO, RLHF, RLAIF, reward model, RL training, reinforcement learning]
status: unread
---

# Rethinking GRPO for Large Reasoning Model Safety Alignment

## Summary

This paper identifies two failure modes when using GRPO for safety alignment of large reasoning models: advantage collapse (homogeneous rollout groups yield vanishing advantages) and unsafe diversification (entropy regularization diversifies unsafe responses when the safety signal vanishes). The proposed Beacon framework introduces Safety Signal Recovery (SSR) combining advantage-guided trajectory filtering and safe reference supervision, plus Safety-Utility Decoupled Alignment (SUDA) with category-aware rewards and benign-only KL anchoring to prevent over-refusal. Across four Qwen3 and DeepSeek-R1-Distill variants on eight benchmarks, Beacon reduces safety error by up to 32.83 percentage points while preserving reasoning performance.

## Key Contributions

- Names and formalizes two GRPO failure modes for safety: advantage collapse and unsafe diversification
- SSR: advantage-guided trajectory filtering + safe reference supervision to recover safety learning signal
- SUDA: category-aware rewards + benign-only KL anchoring — decouples safety and utility optimization
- Validated on Qwen3-1.7B/7B/14B/32B and DeepSeek-R1-Distill-Qwen-7B/14B/32B; 8 benchmarks

## Relevance

Extends the multi-objective / constrained RL for LLMs thread (previously 2 entries: CoRL + Pareto-Dominant Clarification) with a new angle: GRPO-specific failure modes during safety alignment rather than explicit CMDP formulations. The advantage collapse finding is notable — it connects GRPO training dynamics to the RL training dynamics / scaling thread, offering a theoretical handle on why GRPO can fail silently in safety-relevant settings.

## My Thoughts

<!-- Add your own notes here -->
