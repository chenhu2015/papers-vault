---
title: "Does RL Expand the Capability Boundary of LLM Agents? A PASS@(k,T) Analysis"
authors: ["Zhiyuan Zhai", "Wenjing Yan", "Xiaodan Shao", "Xin Wang"]
date: 2026-04-16
arxiv_id: "2604.14877v1"
url: "https://arxiv.org/abs/2604.14877"
score: 0.76
topics: [agentic RL, LLM agent, tool use, reinforcement learning]
status: unread
---

# Does RL Expand the Capability Boundary of LLM Agents? A PASS@(k,T) Analysis

## Summary

PASS@(k,T) is a two-dimensional metric that jointly varies sampling budget k and interaction depth T to separate whether RL for LLM agents expands capability (new strategies accessible) vs. improves reliability (existing strategies more consistent). For compositional sequential tool-use, RL genuinely expands the capability boundary — the RL agent's pass@k curve stays above the base model's and the gap widens at large k, contradicting the static-reasoning result where base and RL curves converge. Mechanism analysis shows RL reweights the base strategy distribution toward the subset whose downstream reasoning integrates retrieved information correctly, with SFT regressing the boundary on the same compositional tasks.

## Key Contributions

- PASS@(k,T) metric: 2D generalization of pass@k adding interaction depth T, separating capability expansion from efficiency improvement
- Task-type finding: RL expands capability on compositional sequential tool-use (widening gap at large k) but not on simpler tasks (prior static-reasoning result holds)
- SFT isolation: under matched training data, SFT regresses the capability boundary on compositional tasks — isolating self-directed exploration as causal factor
- Mechanism: RL reweights base strategy distribution toward downstream-reasoning-effective subset, not just making all strategies more reliable

## Relevance

Directly addresses the vault's central question of what RL training achieves for agentic settings: the CA survey (Aug 13) catalogued mechanism papers; PASS@(k,T) provides the evaluation lens to measure whether those mechanisms produce genuine capability expansion. The task-type conditioning (compositional tool-use vs. simple tasks) maps precisely onto the vault's tool-use thread and suggests the process reward / credit assignment papers are most impactful for compositional multi-step tool-use tasks.

## My Thoughts

<!-- Add your own notes here -->
