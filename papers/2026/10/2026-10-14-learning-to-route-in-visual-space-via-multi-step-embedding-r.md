---
title: "Learning to Route in Visual Space via Multi-Step Embedding Retrieval"
authors: ["Tianyu Chen", "Mingyuan Zhou", "Jiaxing Wu"]
date: 2026-10-14
arxiv_id: "2609.38743v2"
url: "http://arxiv.org/abs/2609.38743v2"
score: 0.78
topics: [agentic RL, LLM agent, tool use, multimodal models, vision-language, RL training]
status: unread
---

# Learning to Route in Visual Space via Multi-Step Embedding Retrieval

## Summary

Introduces VHOP-Router, an end-to-end training pipeline (SFT + online imitation learning + RL) that converts a standard embedding model into an autoregressive multi-step visual retriever, enabling agentic visual search without requiring the agent to formulate intermediate text queries. On VHOP benchmark, it boosts retrieval from under 5% to 76.3% and improves agentic task success by 52.7% while reducing context token length by 61%. VHOP-Router operates entirely in visual latent space and generalizes to unseen difficulty levels, leaving native LLM capabilities intact.

## Key Contributions

- VHOP benchmark: five difficulty levels testing visual matching and multi-step search planning
- VHOP-Router training pipeline: SFT → online imitation learning → RL for autoregressive multi-step embedding navigation
- Offloads multi-step visual navigation to the retrieval tool, bypassing the LLM agent's text-query bottleneck
- 52.7% task success improvement and 23× reduction in in-context images vs. top-50-per-step baseline; generalizes across difficulty levels

## Relevance

Sits squarely at the intersection of agentic RL and tool use — the SOAR thread explored source-aware credit for search agents, while VHOP-Router explores RL-trained retrieval tools that relieve the agent of intermediate query formulation. The composability question is direct: can VHOP-Router's latent-space navigation compose with SOAR's attribution-structured trajectories to close the loop on multi-step visual agentic search?

## My Thoughts

<!-- Add your own notes here -->
