---
title: "The Landscape of Agentic Reinforcement Learning for LLMs: A Survey"
authors: ["(survey — multiple authors)"]
date: 2025-09-02
arxiv_id: "2509.02547v5"
url: "https://arxiv.org/abs/2509.02547"
score: 0.82
topics: [agentic RL, LLM agent, reinforcement learning, RL training, tool use]
status: unread
---

# The Landscape of Agentic Reinforcement Learning for LLMs: A Survey

## Summary

A comprehensive survey that formalizes the distinction between LLM-RL (degenerate single-step MDPs) and Agentic RL (temporally extended POMDPs), proposing a twofold taxonomy covering both the agent's decision-making structure and the RL training methodology. It maps the landscape of exploration, credit assignment, curriculum, and scaffolding approaches for multi-turn LLM agents. Directly synthesizes many threads the vault has been accumulating — adaptive scaffolding, credit assignment, exploration in RLVR — making it a high-value reference for understanding the cluster structure.

## Key Contributions

- Formal distinction between LLM-RL (single-step MDPs) and Agentic RL (POMDPs with temporal extension), clarifying why standard RLVR methods need adaptation for agentic settings
- Twofold taxonomy spanning agent decision-making structures and RL training methodologies
- Comprehensive coverage of exploration, credit assignment, curriculum, and scaffolding for multi-turn LLM agents
- Survey of evaluation benchmarks and open challenges for agentic RL systems

## Relevance

This is a synthesis reference for the entire agentic RL and GRPO training dynamics vault threads. The adaptive scaffolding cluster (AutoScaffold, JoMoHa, Targeted Guidance, SkillScaffold, Agent-G², METIS, Scaf-GRPO), credit assignment papers (TriGRPO, SGR-OPSD, ProAS, CREDO, EG-GRPO), and exploration cluster (TGRL, EDEN, PSRA) all map to sub-chapters of this survey — it provides the conceptual scaffolding to understand why these clusters are related.

## My Thoughts

<!-- Add your own notes here -->
