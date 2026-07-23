---
title: "Masked Diffusion Language Models are Strong and Steerable Text-Based World Models for Agentic RL"
authors: ["Darshan Deshpande"]
date: 2026-05-07
arxiv_id: "2607.16204"
url: "https://arxiv.org/abs/2607.16204"
score: 0.75
topics: [agentic RL, RL training, LLM agent, GRPO, tool use]
status: unread
---

# Masked Diffusion Language Models are Strong and Steerable Text-Based World Models for Agentic RL

## Summary

This paper shows that masked diffusion language models (MDLMs) outperform autoregressive LLMs as text-based world models for agentic RL training, because bidirectional denoising enables conditioning on globally interdependent state anchors (tool schemas, prior turns, expected outcomes) that left-to-right generation cannot handle. Using 239,403 grounded state-action trajectories across 9 environments and 12 LLM families, MDLMs achieve better coherence and rollout diversity than LLMs 4x their size. A plug-and-play GRPO framework achieves up to 47% absolute gains on OOD environments without environment-specific fine-tuning.

## Key Contributions

- Formalizes text-based world modeling as a steerable transition-dynamics problem decomposed into initial state, task context, tool schemas, domain rules, and steering directives
- MDLMs outperform AR LLMs 4x their size in coherence, groundedness, and rollout diversity due to bidirectional anchor-aware denoising
- 239,403 grounded state-action trajectories spanning 9 open-source environments and 12 frontier LLM families (public dataset)
- Plug-and-play GRPO training framework with deterministic state checks; zero-shot transfer to OOD environments (ScienceWorld, ALFWorld, AppWorld)

## Relevance

Directly relevant to the agentic RL thread: the world model provides diverse synthetic rollouts for GRPO training without requiring live environment access per step. The diversity improvement over AR models addresses the mode collapse failure mode that BPO and GFlowRL (today) both target from different angles—BPO exploits prefix sharing in real sandboxes, GFlowRL uses distribution-matching objectives, and this paper uses bidirectional MDLMs to generate more diverse synthetic rollouts. Tool schema conditioning connects to the interest profile's tool use and LLM agent axes.

## My Thoughts

<!-- Add your own notes here -->
