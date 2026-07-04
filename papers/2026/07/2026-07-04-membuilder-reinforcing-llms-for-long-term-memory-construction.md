---
title: "MemBuilder: Reinforcing LLMs for Long-Term Memory Construction via Attributed Dense Rewards"
authors: ["Zhiyu Shen", "Ziming Wu", "Fuming Lai", "Shaobing Lian", "Yanghui Rao"]
date: 2026-07-04
arxiv_id: "2601.05488"
url: "https://arxiv.org/abs/2601.05488"
score: 0.75
topics: [reinforcement learning, RL training, LLM agent, reward model, GRPO]
status: unread
---

# MemBuilder: Reinforcing LLMs for Long-Term Memory Construction via Attributed Dense Rewards

## Summary

MemBuilder trains LLMs via RL to orchestrate multi-dimensional long-term memory construction with attributed dense rewards, addressing sparse trajectory-level rewards via synthetic session-level question generation for dense intermediate supervision, and the memory attribution problem via contribution-aware gradient weighting that scales policy updates by each memory component's downstream impact. A 4B model trained with MemBuilder outperforms closed-source baselines on long-term dialogue benchmarks, demonstrating RL-based memory construction with fine-grained attribution at small scale.

## Key Contributions

- Attributed dense reward framework for multi-dimensional memory construction: each memory component receives credit proportional to its measured downstream conversational impact
- Synthetic session-level question generation as a proxy dense reward for sparse trajectory-level supervision in long-horizon dialogue RL
- Contribution-aware gradient weighting: policy updates are scaled by each memory component's attribution score, not uniform across the memory
- Demonstrates competitive closed-source performance with a 4B parameter model via fine-grained RL attribution — credit quality substitutes for model scale

## Relevance

MemBuilder extends the credit assignment/dense reward thread (PASS, DuCA, ReasonRAG) to the memory construction domain: instead of crediting which action in a navigation trajectory was decisive, it asks which memory write was decisive for future conversational consistency. The contribution-aware gradient weighting is the memory-domain equivalent of TRIAGE's role-typed credit (Jul 2) — it is a form of role-typed gradient attribution where the "role" is the memory dimension (episodic fact, preference, temporal state, etc.) rather than the agentic action type.

## My Thoughts

<!-- Add your own notes here -->
