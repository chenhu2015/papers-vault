---
title: "MADA-RL: Multi-Agent Debate-Aware Reinforcement Learning for Parameter-Efficient Reasoning in Compact Models"
authors: ["Martino M. L. Pulici", "Cuong Xuan Chu", "Evgeny Kharlamov", "Zifeng Ding", "Volker Tresp", "Yunpu Ma"]
date: 2026-07-20
arxiv_id: "2607.18006"
url: "https://arxiv.org/abs/2607.18006"
score: 0.77
topics: [agentic RL, RL training, LLM agent, RLHF]
status: unread
---

# MADA-RL: Multi-Agent Debate-Aware Reinforcement Learning for Parameter-Efficient Reasoning in Compact Models

## Summary

MADA-RL specializes compact LLMs (≤4B) into generator and critic roles trained with a debate-aware learning signal, fine-tuning only LoRA adapters (16x fewer trainable params than full fine-tuning). The central contribution is a counterfactual critic advantage that defines the critic's advantage as its reward minus the generator ensemble's per-instance accuracy, forcing critics to correct generator errors rather than imitate them. On five math reasoning benchmarks, MADA-RL raises DeepSeek-R1-Distill-Qwen-1.5B from 39.9% to 41.9% (+2.0pp) using 16x fewer trainable parameters.

## Key Contributions

- Counterfactual critic advantage: redefines critic advantage as critic reward minus generator ensemble per-instance accuracy, creating a dynamic role-conditioned baseline
- Generator + critic role specialization via LoRA adapters; 16x parameter efficiency vs. full fine-tuning
- Multi-round deployment protocol composing specialized agents at inference time
- Highest critic improvement rate of any baseline evaluated, confirming critics learn to correct (not imitate) generator errors

## Relevance

MADA-RL is a form of adversarial self-play RL for reasoning, using multi-agent debate as the training signal. The counterfactual advantage connects to the credit assignment thread (counterfactual credit was explored in CRAFT, Jul 2; here applied at the inter-agent level rather than token level). The paper partially addresses the open gap on self-play adversarial training for reasoning LLMs (confirmed sparse through DEPT), though with modest gains and math-only evaluation—the gap for agentic/code domains remains open.

## My Thoughts

<!-- Add your own notes here -->
