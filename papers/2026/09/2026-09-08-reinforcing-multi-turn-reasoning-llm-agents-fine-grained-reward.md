---
title: "Reinforcing Multi-Turn Reasoning in LLM Agents via Fine-Grained Reward Structure and Credit Assignment"
authors: ["Quan Wei", "Siliang Zeng", "Chenliang Li", "Zhongruo Wang", "William Brown", "Oana Frunza", "Wei Deng", "Anderson Schneider", "Yuriy Nevmyvaka", "Yang Katie Zhao", "Alfredo Garcia", "Mingyi Hong"]
date: 2026-09-08
arxiv_id: "2505.11821v3"
url: "http://arxiv.org/abs/2505.11821v3"
score: 0.80
topics: [agentic RL, RL training, GRPO, PPO, reward model, LLM agent]
status: unread
---

# Reinforcing Multi-Turn Reasoning in LLM Agents via Fine-Grained Reward Structure and Credit Assignment

## Summary

This paper categorizes multi-turn LLM agent reward structures into terminal, delayed, and per-turn granularities, derives GRPO and PPO algorithms tailored to each turn-level MDP formulation, and empirically shows that dense per-turn rewards consistently outperform sparse structures across training dynamics and task outcomes. PPO with per-turn rewards achieves the highest correctness on diverse multi-turn QA datasets, providing systematic ablation grounding for why methods like RTPO and TRIAL are effective.

## Key Contributions

- Formal taxonomy of multi-turn reward structures: terminal reward, delayed reward, and per-turn reward, each as a distinct turn-level MDP formulation
- Derivation of GRPO and PPO algorithm variants tailored to each of the three MDP formulations
- Empirical confirmation that per-turn reward structures consistently outperform sparser structures in training dynamics and numerical performance
- PPO + dense per-turn rewards achieves highest answer correctness on multi-turn search and game agent benchmarks

## Relevance

This paper provides the systematic ablation grounding for the multi-turn credit assignment thread — it confirms empirically what RTPO, SAPO, TRIAL, and T-STAR achieve architecturally: that credit at the turn/step level is strictly better than trajectory-level for multi-turn agents. The three-way taxonomy (terminal/delayed/per-turn) also provides a conceptual vocabulary for classifying all prior credit assignment methods in the thread.

## My Thoughts

<!-- Add your own notes here -->
