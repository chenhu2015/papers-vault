---
title: "CoHARL: Co-Evolving Agent Policies and Executable Harnesses with Reinforcement Learning"
authors: ["Jianwen Chen", "Peng Xia", "Kaide Zeng", "Siwei Han", "Zhen-Yu Zhang", "Charles Fleming", "Xinyu Ye", "Huaxiu Yao"]
date: 2026-11-02
arxiv_id: "2610.36469v1"
url: "http://arxiv.org/abs/2610.36469v1"
score: 0.80
topics: [agentic RL, RL training, reinforcement learning, LLM agent, tool use]
status: unread
---

# CoHARL: Co-Evolving Agent Policies and Executable Harnesses with Reinforcement Learning

## Summary

CoHARL jointly evolves the LLM agent policy and the executable harness (tool interface) during RL training, addressing the mismatch between optimizing a harness for a fixed policy and training a policy under a fixed harness. A population of harnesses is maintained; the policy learns from rollouts across the population while a proposer revises harness code using execution traces. CoHARL achieves 27.6% resolved rate on SWE-rebench (+6.4pp over harness-only search) and shows gains on SWE-bench Verified and Terminal-Bench 2.0.

## Key Contributions

- Population-based harness co-evolution: policy trains across a harness population; proposer rewrites harness code from execution traces during training
- Frames tool interface adaptation as part of the RL loop, not a separate pre-training step
- 27.6% on SWE-rebench vs. 21.2% harness-only search; gains on SWE-bench Verified and Terminal-Bench 2.0
- Outperforms both one-shot harness search before RL and alternating single-harness revision approaches

## Relevance

CoHARL opens a new angle in the long-horizon agentic RL thread: instead of optimizing agent behavior under a fixed environment interface, it co-evolves the interface itself. This is qualitatively distinct from CORD's gradient conflict management or QwenGyre's elastic infrastructure — it targets the harness-policy coupling that is specific to tool-use agents. Directly extends the agentic RL + tool use thread.

## My Thoughts

<!-- Add your own notes here -->
