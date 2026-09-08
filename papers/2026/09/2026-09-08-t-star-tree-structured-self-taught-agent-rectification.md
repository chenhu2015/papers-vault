---
title: "Reason in Chains, Learn in Trees: Self-Rectification and Grafting for Multi-turn Agent Policy Optimization"
authors: ["Yu Li", "Sizhe Tang", "Tian Lan"]
date: 2026-09-08
arxiv_id: "2604.07165v2"
url: "http://arxiv.org/abs/2604.07165v2"
score: 0.82
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# Reason in Chains, Learn in Trees: Self-Rectification and Grafting for Multi-turn Agent Policy Optimization

## Summary

T-STAR constructs a Cognitive Tree by merging functionally similar steps across independent trajectory samples, then back-propagates trajectory-level rewards through it via Introspective Valuation to produce variance-reduced step-level advantages. In-Context Thought Grafting synthesizes corrective reasoning from successful/failed branch contrasts at critical divergence points, and a Surgical Policy Optimization concentrates a Bradley-Terry preference loss at these critical steps, yielding consistent gains across embodied, interactive, reasoning, and planning benchmarks.

## Key Contributions

- Cognitive Tree: unified data structure merging functionally similar steps/nodes across independent trajectory samples to expose latent reward correlation structure
- Introspective Valuation: back-propagates trajectory-level rewards through the Cognitive Tree to obtain variance-reduced relative advantages at step level
- In-Context Thought Grafting: synthesizes corrective reasoning by contrasting successful and failed branches at critical divergence points in the Cognitive Tree
- Surgical Policy Optimization: Bradley-Terry type preference loss concentrated at critical steps, capitalizing on high-information policy gradient points

## Relevance

T-STAR extends the credit assignment thread via cross-trajectory structure: the Cognitive Tree exploits latent correlation between trajectories sampled by GRPO, recovering a richer advantage signal than GRPO's standard across-group comparison. The Introspective Valuation back-propagation is structurally analogous to RTPO's reverse-tree formulation but operates on the latent semantic tree across trajectories (not the causal sequential tree within a trajectory), making T-STAR composable with RTPO rather than redundant to it.

## My Thoughts

<!-- Add your own notes here -->
