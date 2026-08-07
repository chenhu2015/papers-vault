---
title: "DPEPO: Diverse Parallel Exploration Policy Optimization for LLM-based Agents"
authors: ["Junshuo Zhang", "Chengrui Huang", "Feng Guo", "Zihan Li", "Ke Shi", "Menghua Jiang", "Jiguo Yu", "Shuo Shang", "Shen Gao"]
date: 2026-04-27
arxiv_id: "2604.24320v1"
url: "https://arxiv.org/abs/2604.24320"
score: 0.80
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# DPEPO: Diverse Parallel Exploration Policy Optimization for LLM-based Agents

## Summary

DPEPO introduces a parallel multi-environment agent paradigm where an LLM agent interacts with multiple environments simultaneously and shares cross-trajectory experiences within each step. The hierarchical reward scheme combines a trajectory-level success reward with two step-level diversity rewards — Diverse Action Reward and Diverse State Transition Reward — that actively penalize behavioral redundancy and promote broad exploration. On ALFWorld and ScienceWorld, DPEPO achieves SOTA success rates while maintaining efficiency comparable to sequential baselines.

## Key Contributions

- Novel multi-environment parallel interaction paradigm: agent acts in N environments simultaneously and shares cross-trajectory experiences at each step
- Hierarchical reward: trajectory-level success reward + step-level Diverse Action Reward (action space coverage) + Diverse State Transition Reward (state space coverage)
- SFT warm-up stage to impart basic parallel reasoning before RL
- SOTA on ALFWorld and ScienceWorld with comparable efficiency to strong sequential baselines

## Relevance

DPEPO directly addresses the exploration gap in agentic RL that AXPO (Aug 3) diagnosed through the Thinking-Acting Gap lens: AXPO addressed the credit side (resampling all-wrong subgroups), while DPEPO addresses the exploration side (explicit diversity rewards for action and state space coverage). In the vault's agentic RL exploration taxonomy, DPEPO joins AXPO (prefix-fixing resampling) and RAPO (retrieval-augmented step-level exploration) as a third structural class: explicit diversity reward shaping via parallel multi-environment interaction.

## My Thoughts

<!-- Add your own notes here -->
