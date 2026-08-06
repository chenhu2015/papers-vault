---
title: "Switch-Reasoner: Learn When to Think in Multitask Mixtures via Reinforcement Learning"
authors: ["Yiyang Fang", "Pei Fu", "Jinjie Li", "Jian Liang", "Wenke Huang", "Ruijie Luo", "Shaojie Zhang", "Jian Luan", "Yi R. Fung", "Mang Ye"]
date: 2026-08-06
arxiv_id: "2607.08572"
url: "https://arxiv.org/abs/2607.08572"
score: 0.80
topics: [multimodal models, vision language models, agentic RL, GRPO, VLM]
status: unread
---

# Switch-Reasoner: Learn When to Think in Multitask Mixtures via Reinforcement Learning

## Summary

Switch-Reasoner is a GRPO-based framework for multimodal LLMs that learns to adaptively select between explicit reasoning (Think-then-Answer) and direct answering, treating thinking as a virtual tool invocation within the RL policy. A dual-level regulation mechanism balances overall Thinking vs. Direct mode use while providing sample-level supervision based on the relative benefit of each choice, addressing the instability of always-thinking or always-direct collapse during post-training. Evaluated on 11 multimodal tasks, Switch-Reasoner reduces unnecessary reasoning while maintaining strong performance and achieving a better accuracy-efficiency trade-off than fixed-paradigm baselines.

## Key Contributions

- Frames adaptive reasoning mode selection as a RL problem: thinking is a virtual tool invocation the policy can invoke or skip
- Dual-level regulation: global balance of Thinking/Direct mode frequencies + sample-level supervision from relative benefit
- Addresses always-thinking or always-direct collapse as a stability failure mode in multitask GRPO post-training
- Evaluated on 11 multimodal tasks with demonstrated accuracy-efficiency trade-off improvements

## Relevance

Switch-Reasoner connects to the AXPO/SPyCE VLM agentic RL thread (Aug 3) by addressing reasoning-mode allocation in multimodal GRPO, and extends the Aug 5 SFT Conflicts/RL Coexists near-orthogonal gradient insight to the multitask heterogeneous-task regime. The dual-level regulation mechanism is structurally related to PROGRESS's teacher-guided coverage reward — both use a dual-granularity supervision signal (global balance + sample-level) to stabilize agentic RL training decisions.

## My Thoughts

<!-- Add your own notes here -->
