---
title: "Maestro: Reinforcement Learning to Orchestrate Hierarchical Model-Skill Ensembles"
authors: ["Jinyang Wu", "Guocheng Zhai", "Ruihan Jin", "Yuhao Shen", "Zhengxi Lu", "Fan Zhang", "Haoran Luo", "Zheng Lian", "Zhengqi Wen", "Jianhua Tao"]
date: 2026-05-22
arxiv_id: "2605.22177"
url: "https://arxiv.org/abs/2605.22177"
score: 0.85
topics: [agentic RL, multimodal models, vision language models, reward model]
status: unread
---

# Maestro: Reinforcement Learning to Orchestrate Hierarchical Model-Skill Ensembles

## Summary

Maestro reframes heterogeneous multimodal tasks as sequential decision-making over a hierarchical model-skill registry, training a lightweight 4B policy via outcome-based RL (no step-level supervision) to dynamically compose ensembles of frozen expert models and a two-tier skill library. The RL orchestrator decides at each step whether to invoke an external expert, which model-skill pair to select, and when to terminate — achieving 70.1% average accuracy across 10 multimodal benchmarks, surpassing GPT-5 (69.3%) and Gemini-2.5-Pro (68.7%). The policy generalizes to unseen models and skills without retraining, with out-of-domain experts yielding 59.5% average on four challenging benchmarks.

## Key Contributions

- RL-trained lightweight orchestrator (4B) outperforms GPT-5 and Gemini-2.5-Pro on 10 multimodal benchmarks via dynamic expert/skill composition
- Outcome-based RL optimization with no step-level supervision: the orchestrator learns to terminate optimally without annotated trajectories
- Two-tier hierarchical skill library: model-level (which expert to call) and skill-level (which capability to invoke)
- Zero-shot generalization to unseen models and skills: augmenting with out-of-domain experts improves over closed-source baselines without retraining

## Relevance

Distinct from prior multi-agent RL digests (ICRL, MARCH) — Maestro targets heterogeneous expert orchestration rather than multi-agent cooperation, and does so via RL rather than SFT. The practical result (4B model beating GPT-5 on multimodal tasks via orchestration RL) connects to the user's interest in agentic RL and multimodal VLM efficiency.

## My Thoughts

<!-- Add your own notes here -->
