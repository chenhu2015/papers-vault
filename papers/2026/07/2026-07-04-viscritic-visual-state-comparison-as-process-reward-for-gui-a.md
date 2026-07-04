---
title: "VisCritic: Visual State Comparison as Process Reward for GUI Agents"
authors: ["Jiachen Qian"]
date: 2026-07-04
arxiv_id: "2606.24525"
url: "https://arxiv.org/abs/2606.24525"
score: 0.73
topics: [vision-language models, VLM, agentic, multimodal models, LLM agent]
status: unread
---

# VisCritic: Visual State Comparison as Process Reward for GUI Agents

## Summary

VisCritic replaces text-only process reward models for GUI agents with a visual process reward that verifies actions by comparing pre-action and post-action screenshots in visual feature space using a Siamese vision transformer, capturing GUI state changes that text-only PRMs systematically miss. An Action-Aware Critic Head jointly evaluates action success, task progress, and error type from visual change representations, with weakly supervised training data automatically constructed from existing trajectories. VisCritic serves as a plug-and-play process reward enhancement across five GUI agent benchmarks without re-training the agent policy.

## Key Contributions

- Siamese vision transformer for visual state comparison: pre-action vs. post-action screenshot in visual feature space, generating change-aware representations
- Action-Aware Critic Head jointly scoring action success, task progress, and error type from visual change features — three distinct credit signals from a single visual comparison
- Automatic critic-training data pipeline from existing trajectories with weak supervision, avoiding expensive human labeling of GUI state changes
- Plug-and-play design: enhances diverse GUI agent policies without modifying agent training — usable as a post-hoc process reward signal

## Relevance

VisCritic fills the VLM-specific gap in the process reward thread: all prior vault entries on process supervision (PASS, SWE-Shepherd, ReasonRAG, DRE) used text-only reward signals, while VisCritic argues that GUI agents require visual state change as the primary verification signal — the GUI domain's equivalent of TAPO's (Jul 3) finding that tool-use credit requires parameter-determinism witnesses rather than uniform text broadcast. The Siamese comparison architecture is a natural complement to SPARC (also today): where SPARC decouples perception from reasoning in the agent's forward pass, VisCritic decouples action verification from textual reasoning in the critic's scoring.

## My Thoughts

<!-- Add your own notes here -->
