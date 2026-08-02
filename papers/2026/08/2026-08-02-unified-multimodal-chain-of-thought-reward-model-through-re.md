---
title: "Unified Multimodal Chain-of-Thought Reward Model through Reinforcement Fine-Tuning"
authors: ["Yibin Wang", "Zhimin Li", "Yuhang Zang", "Chunyu Wang", "Qinglin Lu", "Cheng Jin", "Jiaqi Wang"]
date: 2025-05-06
arxiv_id: "2505.03318"
url: "https://arxiv.org/abs/2505.03318"
score: 0.85
topics: [multimodal models, vision-language, VLM, RLHF, reward model, GRPO]
status: unread
---

# Unified Multimodal Chain-of-Thought Reward Model through Reinforcement Fine-Tuning

## Summary

UnifiedReward-Think trains the first unified multimodal reward model that reasons in explicit long chains-of-thought (CoT) before issuing reward signals, covering both visual understanding and generation reward tasks. Training uses a three-stage pipeline: GPT-4o CoT distillation cold start, large-scale rejection sampling on unified multimodal preference data, then GRPO fine-tuning on incorrect samples to explore diverse reasoning paths. The result is a reward model whose reliability scales with reasoning depth, closing the gap between shallow pairwise scoring and auditable step-level judgement.

## Key Contributions

- **First unified multimodal CoT reward model**: one model covers visual understanding reward (image QA, hallucination detection) and visual generation reward (text-to-image alignment) via multi-dimensional step-by-step reasoning
- **Three-stage exploration-driven training**: cold-start distillation → rejection sampling on large-scale unified preference data → GRPO on incorrect samples to learn diverse correct reasoning paths
- **CoT reasoning improves reward reliability**: explicit long-chain reasoning reduces reward hallucination and improves robustness; implicit reasoning from CoT training also improves direct-response accuracy
- **Demonstrated across diverse vision reward tasks**: extensive experiments show superiority over both shallow RM and CoT-prompt baselines

## Relevance

This directly closes Gap #4 (dedicated VLM reward model training): prior vault papers used reward models as black-box scalars; UnifiedReward-Think is the first paper in the vault to train a reward model whose internal process is explicit, step-by-step, and multimodal. The GRPO training on incorrect samples is an instance of exploration-driven GRPO that connects to the same framework used in Gap #16 papers (all-fail groups), but applied to reward model training rather than policy training. Found via Search 3 (meta-reasoning + verifiable rewards), making it a retroactive answer to a gap opened much earlier.

## My Thoughts

<!-- Add your own notes here -->
