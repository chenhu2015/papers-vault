---
title: "OPID: On-Policy Skill Distillation for Agentic Reinforcement Learning"
authors: ["Shuo Yang", "Jinyang Wu", "Zhengxi Lu", "Yuhao Shen", "Fan Zhang", "Lang Feng", "Shuai Zhang", "Haoran Luo", "Zheng Lian", "Zhengqi Wen", "Jianhua Tao"]
date: 2026-07-04
arxiv_id: "2606.26790"
url: "https://arxiv.org/abs/2606.26790"
score: 0.88
topics: [agentic RL, RL training, LLM agent, GRPO, tool use]
status: unread
---

# OPID: On-Policy Skill Distillation for Agentic Reinforcement Learning

## Summary

OPID extracts hierarchical skill supervision directly from completed on-policy trajectories — episode-level workflow/failure-avoidance rules and step-level decision knowledge at critical timesteps — without requiring external skill memory. A critical-first routing mechanism selects which skill granularity to inject into the interaction history, then the old policy re-scores the same response under both original and skill-augmented contexts; the log-probability shift forms a token-level self-distillation advantage combined with the outcome reward for GRPO optimization. Evaluated on ALFWorld, WebShop, and Search-QA, OPID outperforms outcome-only RL and existing skill-distillation baselines in performance, sample efficiency, and robustness.

## Key Contributions

- Hierarchical on-policy skill extraction from completed rollouts: episode-level global workflow/failure rules + step-level critical-timestep decision knowledge, with no external memory required
- Critical-first routing: use step-level skills when critical decisions are identified, fallback to episode-level skills as default; routing is policy-driven without a separate classifier
- Token-level self-distillation advantage from log-probability shift when re-scoring the same response under skill-augmented vs. original context with the old policy
- Combined outcome advantage + skill-distillation advantage for GRPO, preserving RL as the primary training objective while adding distribution-matched hindsight supervision

## Relevance

OPID directly advances the context-view credit thread opened by UCOB (Jul 3): where UCOB used return-to-go comparison across skill-conditioned vs. no-skill contexts as its credit signal, OPID uses log-probability shift under skill vs. no-skill re-scoring — a tighter, per-token signal that avoids the trajectory-level aggregation of return-to-go. The on-policy extraction requirement distinguishes OPID from UCOB (which assumed pre-built external skill memory), closing the practical gap for settings where skill memory is unavailable or mismatched with the current policy's state distribution.

## My Thoughts

<!-- Add your own notes here -->
