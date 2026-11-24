---
title: "When Credit Turns Against Tools: Transition-Aware Credit Assignment in Agentic Reinforcement Learning"
authors: ["Xiangyu Lu", "Zhanke Zhou", "Jiazhe Ning", "Chentao Cao", "Jiangchao Yao", "Bo Han"]
date: 2026-11-24
arxiv_id: "2611.11330v1"
url: "http://arxiv.org/abs/2611.11330v1"
score: 0.82
topics: [agentic RL, RL training, tool use]
status: unread
---

# When Credit Turns Against Tools: Transition-Aware Credit Assignment in Agentic Reinforcement Learning

## Summary

Identifies three coupled failure mechanisms in agentic RL training with tool use — tool-token imbalance (incorrect trajectories contain more tool tokens, generating negative credit), aggregation amplification (token-mean aggregation strengthens the negative signal), and failure-driven retries (tool errors extend trajectories, spreading negative credit to recovery attempts). Proposes TACA (Transition-Aware Credit Assignment), which applies Advantage Projection to enforce non-negative mean advantage on tool-call tokens, Decision Contrast to guide tool-use decisions by comparing rewards for tool-assisted vs. direct answers, and Supervised Replay to reinforce correct tool-call generation from prior trajectories.

## Key Contributions

- Mechanistic analysis of three failure modes causing tool-call degradation during agentic GRPO training
- Advantage Projection: minimal uniform shift to enforce non-negative tool-call advantage within each prompt group
- Decision Contrast: compares tool-assisted vs. direct-answer rewards to guide call initiation decisions
- Supervised Replay: reinforces correct tool calls from historically sampled correct trajectories
- MT-GRPO baseline +4.61pp (Qwen2.5-1.5B) and +3.61pp (Qwen2.5-3B) across six reasoning benchmarks

## Relevance

Directly addresses the RLVR training stability thread — specifically the agentic RL variant where tool token credit misattribution causes training collapse. This paper is TACA to DOT's length-shift problem: both diagnose a specific agentic GRPO failure mechanism and propose a targeted credit/token-level fix.

## My Thoughts

<!-- Add your own notes here -->
