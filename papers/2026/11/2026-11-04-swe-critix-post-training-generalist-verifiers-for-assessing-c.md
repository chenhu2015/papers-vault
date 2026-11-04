---
title: "SWE-Critix: Post-Training Generalist Verifiers for Assessing Coding-Agent Trajectories"
authors: ["Jiajun Hu", "Chun Yong Chong"]
date: 2026-10-09
arxiv_id: "2610.13356v2"
url: "http://arxiv.org/abs/2610.13356v2"
score: 0.75
topics: [agentic RL, RL training, reward model, LLM agent, agentic]
status: unread
---

# SWE-Critix: Post-Training Generalist Verifiers for Assessing Coding-Agent Trajectories

## Summary

SWE-Critix trains 30B generalist verifiers for coding-agent trajectories using SFT then RL on CodeForge-Preview trajectories; the verifier predicts completion labels and generates natural-language explanations. Classification accuracy improves from 57% (base Qwen3-30B-A3B) to 66% after SFT and 78% after RL, demonstrating that RL training substantially improves trajectory verification quality over SFT alone. This addresses the core oracle-evaluator gap in deployed coding agents operating on long-horizon software engineering tasks without readily available ground-truth success criteria.

## Key Contributions

- Generalist verifier design: predicts completion label + generates natural-language explanation from task + trajectory
- Trains on CodeForge-Preview trajectories with SFT+RL pipeline; RL phase contributes substantial accuracy gain (+12pp over SFT alone, +21pp over base)
- Addresses the oracle-evaluator gap: coding agents in production lack a readily available oracle, so a learned verifier replaces it
- Releases models, datasets, and training code

## Relevance

Extends the reward model keyword from the interest profile into the coding-agent domain: SWE-Critix is a reward model for coding-agent trajectories, trained with RL, in a setting where verifiable rewards don't naturally exist. Connects to the long-horizon agentic RL thread's credit assignment debate — here the signal comes from a learned generalist verifier rather than a task oracle.

## My Thoughts

<!-- Add your own notes here -->
