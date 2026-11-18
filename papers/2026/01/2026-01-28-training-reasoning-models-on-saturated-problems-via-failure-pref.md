---
title: "Training Reasoning Models on Saturated Problems via Failure-Prefix Conditioning"
authors: ["Minwu Kim", "Safal Shrestha", "Anubhav Shrestha", "Keith Ross"]
date: 2026-01-28
arxiv_id: "2601.20829v2"
url: "http://arxiv.org/abs/2601.20829v2"
score: 0.80
topics: [RL training, reinforcement learning, GRPO, agentic RL]
status: unread
---

# Training Reasoning Models on Saturated Problems via Failure-Prefix Conditioning

## Summary

Addresses the RLVR saturation bottleneck: as models improve, training problems become saturated (nearly all rollouts correct) leaving minimal reward gradient signal. Proposes failure-prefix conditioning, which shifts exploration toward failure-prone reasoning states by conditioning on prefixes of rare incorrect trajectories, achieving gains comparable to training on newly-collected medium-difficulty problems. An iterative variant that refreshes failure prefixes during training unlocks additional gains after performance plateaus.

## Key Contributions

- Formally characterizes RLVR saturation as a training bottleneck: saturated problems yield near-zero gradient signal as reward variance collapses
- Failure-prefix conditioning: condition the model on failure prefixes of its own rare incorrect trajectories to maintain exploration in failure-prone regions
- Achieves gains comparable to collecting newly-labeled medium-difficulty problems, without any external data collection
- Iterative variant that refreshes failure prefixes during training continues to improve after plateau

## Relevance

Directly relevant to the RLVR/GRPO training mechanics cluster. This paper solves the dual of the zero-advantage-on-hard-problems problem (PICO, Scaf-GRPO, HATCH): those papers address zero reward on problems too hard to solve; this paper addresses zero gradient on problems too easy (all correct). Together, these two clusters cover both ends of the difficulty spectrum for RLVR training signal collapse.

## My Thoughts

<!-- Add your own notes here -->
