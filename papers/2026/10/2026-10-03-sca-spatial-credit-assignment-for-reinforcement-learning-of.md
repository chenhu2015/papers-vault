---
title: "SCA: Spatial Credit Assignment for Reinforcement Learning of GUI Agents"
authors: ["Shengtian Yang", "Ziyu Xiong", "Kaibing Yang", "Guangfeng Cai", "Yewen Li", "Peng Jiang", "Gai Kun", "Qingpeng Cai", "Lei Feng"]
date: 2026-09-29
arxiv_id: "2609.36939"
url: "https://arxiv.org/abs/2609.36939"
score: 0.85
topics: [agentic RL, LLM agent, tool use, GRPO]
status: unread
---

# SCA: Spatial Credit Assignment for Reinforcement Learning of GUI Agents

## Summary

SCA addresses a structural failure in binary reward evaluation for GUI agents: spatially different failed clicks are treated identically, and all-fail rollout groups yield no relative learning signal. When successes exist in a group, SCA predicts each response's reward from the others using screen-coordinate proximity to successful clicks; when all responses fail, it orders them by distance to the annotated target and derives relative credit from that ranking. The spatial references only influence the training update; the deployed policy is unchanged. Consistently improves GUI grounding and offline action prediction across professional domains.

## Key Contributions

- Diagnoses two failure modes of group-relative reward for GUI: identical treatment of spatially distinct failures, and zero-signal all-fail groups
- Mixed-group mode: predicts each response's reward from spatial proximity to same-group successes
- All-fail mode: orders failed clicks by distance to annotated target, constructing a relative advantage ranking
- Spatial oracle used only at training time; inference policy is unmodified

## Relevance

Directly answers the SeekJudge (scored 0.77, 2026-10-02) open thread on model-based reward for GUI agents, but from a complementary angle: instead of a learned judge model, SCA uses the geometric structure of screen space as the credit signal. This is also a concrete extension of the step-credit cluster to the GUI domain — the "step" is a click action, and credit is assigned via spatial proximity rather than temporal trajectory analysis.

## My Thoughts

<!-- Add your own notes here -->
