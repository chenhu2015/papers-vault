---
title: "Reframe: Observation-Aligned Multi-Teacher On-Policy Distillation for Agentic Visual Reasoning"
authors: ["Haozhi Yuan", "Handong Li", "Yifan Zhang"]
date: 2026-11-09
arxiv_id: "2611.12886"
url: "https://arxiv.org/abs/2611.12886"
score: 0.80
topics: [agentic RL, tool use, multimodal models, VLM, GRPO, vision-language]
status: unread
---

# Reframe: Observation-Aligned Multi-Teacher On-Policy Distillation for Agentic Visual Reasoning

## Summary

Reframe addresses two failure modes in agentic visual RL: models ignoring tool-returned observations, and poorly-grounded actions limiting subsequent distillation signal. Ground-Drop-GRPO (GD-GRPO) trains spatial/temporal specialist teachers with evidence-aware rewards and stochastic removal of the original visual input, forcing reliance on tool-returned observations. Observation-Gated-MOPD (OG-MOPD) detects deficient tool actions mid-rollout and replaces them with canonical alternatives before resuming distillation from the repaired observation state. The two stages are mutually reinforcing, and neither requires a task-specific SFT cold start; Reframe outperforms both Mix-RL and vanilla MOPD across 14 image/video benchmarks.

## Key Contributions

- GD-GRPO: evidence-aware rewards + stochastic original-input removal → forces grounded tool-observation use
- OG-MOPD: mid-rollout canonical action replacement → repairs distillation signal from bad tool actions
- Mutual reinforcement: better observation grounding improves OG-MOPD signal quality
- No task-specific SFT cold start required
- Outperforms Mix-RL and vanilla MOPD across 14 image/video benchmarks; GD-GRPO increases observation dependence vs. outcome-based GRPO in ablations

## Relevance

Extends both the adaptive scaffolding cluster (JoMoHa's joint model+harness RL; SkillScaffold's selective injection) and the VLM/multimodal thread into the agentic visual domain. Specifically addresses the tool-use grounding problem for visual agents — an open gap in the vault where VLM + agentic RL intersect. The observation-alignment framing is a novel angle not covered by existing cluster entries.

## My Thoughts

<!-- Add your own notes here -->
