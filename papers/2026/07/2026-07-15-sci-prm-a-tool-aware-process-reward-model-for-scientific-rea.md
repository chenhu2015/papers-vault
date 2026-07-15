---
title: "SCI-PRM: A Tool Aware Process Reward Model for Scientific Reasoning Verification"
authors: ["Xiangyu Zhao", "Henry Hengyuan Zhao", "Yiheng Wang", "Wanghan Xu", "Yuhao Zhou", "Qinglong Cao", "Zhiwang Zhou", "Lei Bai", "Wenlong Zhang", "Xiao-Ming Wu"]
date: 2026-07-15
arxiv_id: "2606.04579"
url: "http://arxiv.org/abs/2606.04579v2"
score: 0.78
topics: [reward model, tool use, agentic RL, RL training, LLM agent]
status: unread
---

# SCI-PRM: A Tool Aware Process Reward Model for Scientific Reasoning Verification

## Summary

Constructs SCIPRM70K with chain-of-tool trajectories interleaving reasoning with scientific tool execution, then trains SCI-PRM to provide step-level reward on tool selection, execution accuracy, and result interpretation in a single inference pass. SCI-PRM enables best-of-N test-time scaling and serves as a dense RL reward signal that mitigates advantage disappearance in sparse-reward settings. Extends the tool-aware PRM thread (GroundedPRM, DART) from math to scientific reasoning domains (biology, chemistry, physics).

## Key Contributions

- SCIPRM70K: 70K chain-of-tool trajectories for biology, chemistry, physics with explicit interleaving of reasoning and tool execution
- SCI-PRM scores tool selection, execution accuracy, and result interpretation at each step in a single inference pass (no re-encoding overhead unlike text PRMs)
- Dense reward signal that mitigates advantage disappearance — the sparse-reward failure mode identified in the vault (DART, RSPO)
- Extends tool-aware PRM beyond math: first domain-specific PRM for scientific reasoning with heterogeneous tool types

## Relevance

Directly extends the vault's tool-use PRM thread: GroundedPRM uses MCTS + tool execution to verify math steps; DART discovers tool insertion points via tree rollouts; SCI-PRM provides step-level reward for tool-augmented scientific reasoning chains. Together they suggest a general pattern: tool execution as ground-truth verifier for PRM training, applicable across any domain with executable tools. The advantage disappearance mitigation also connects to RSPO's dense-for-sampling observation — process rewards help convergence without corrupting the outcome objective if applied carefully.

## My Thoughts

<!-- Add your own notes here -->
