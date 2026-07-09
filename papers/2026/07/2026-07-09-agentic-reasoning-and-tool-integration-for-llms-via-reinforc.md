---
title: "Agentic Reasoning and Tool Integration for LLMs via Reinforcement Learning"
authors: ["Joykirat Singh", "Raghav Magazine", "Yash Pandya", "Akshay Nambi"]
date: 2026-07-09
arxiv_id: "2505.01441v1"
url: "http://arxiv.org/abs/2505.01441v1"
score: 0.75
topics: [agentic RL, LLM agent, tool use, reinforcement learning, agentic]
status: unread
---

# Agentic Reasoning and Tool Integration for LLMs via Reinforcement Learning

## Summary

ARTIST (Agentic Reasoning and Tool Integration in Self-improving Transformers) is a unified framework that enables LLMs to autonomously decide when, how, and which tools to invoke within multi-turn reasoning chains using outcome-based RL — without requiring step-level supervision. Experiments on mathematical reasoning and multi-turn function calling benchmarks show up to 22% absolute improvement over base models, with analyses showing RL training drives deeper reasoning and more selective tool invocation.

## Key Contributions

- Unified framework coupling agentic reasoning, RL training, and multi-turn tool integration without step-level supervision labels
- Outcome-based RL reward formulation: learns robust tool-use strategies from final answer correctness alone, sidestepping the dense labeling bottleneck of supervised tool-use methods
- 22% absolute improvement over base models on math reasoning + function calling benchmarks
- Analysis shows trained models invoke tools more selectively and generate higher-quality intermediate reasoning steps — RL improves the quality of tool-use decisions, not just frequency

## Relevance

ARTIST complements AutoTool (Jul 07) in the vault's agentic tool-use thread: where AutoTool focuses on the invocation decision (when to use a tool vs. text-only reasoning) with dual-mode rewards, ARTIST addresses the full multi-turn tool integration pipeline — when, how, and which tool — using a single outcome-based reward. Together they bracket the tool-use design space: AutoTool is mode-selective and efficiency-oriented; ARTIST is pipeline-complete and learns from outcome signals alone. DynaWeb (Jul 09) adds a third complementary angle: learning tool-use environments via world models rather than direct interaction.

## My Thoughts

<!-- Add your own notes here -->
