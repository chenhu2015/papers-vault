---
title: "Measure Twice, Click Once: Co-evolving Proposer and Visual Critic via Reinforcement Learning for GUI Grounding"
authors: ["Wenkai Wang", "Xiyun Li", "Hongcan Guo", "Wenhao Yu", "Tianqing Fang", "Haitao Mi", "Dong Yu", "Shengyu Zhang"]
date: 2026-04-23
arxiv_id: "2604.21268v1"
url: "http://arxiv.org/abs/2604.21268v1"
score: 0.82
topics: [agentic RL, VLM, vision-language, multimodal models, LLM agent, tool use]
status: unread
---

# Measure Twice, Click Once: Co-evolving Proposer and Visual Critic via Reinforcement Learning for GUI Grounding

## Summary

Measure Twice Click Once replaces static self-consistency strategies for GUI grounding with a co-evolutionary RL framework: a visual critic is trained alongside the proposer to select the best coordinate prediction by evaluating rendered screenshots, while a maturity-aware adaptive schedule dynamically rebalances training objectives for both modules. The proposer's spatial diversity strengthens the critic's robustness, and the maturing critic in turn unlocks deeper spatial exploration in the proposer — yielding significant grounding accuracy improvements across 6 benchmarks.

## Key Contributions

- Frames GUI grounding as a Propose-then-Critique problem where the critic evaluates proposals rendered on actual screenshots (not abstract logits)
- Co-evolutionary RL training: proposer and critic are jointly optimized with mutual reinforcement
- Maturity-aware adaptive schedule dynamically rebalances training objectives based on each module's current capability
- Formal analysis: proposer diversity → critic robustness; critic maturity → proposer spatial exploration
- Evaluated across 6 GUI grounding benchmarks with significant accuracy and reliability improvements

## Relevance

Directly extends the GUI/embodied VLM RL thread (covered via ERA, LMEE in earlier digests) into a novel co-evolution angle not previously seen. The proposer-critic architecture mirrors the actor-critic paradigm central to agentic RL and the VLM/tool-use interest profile keywords.

## My Thoughts

<!-- Add your own notes here -->
