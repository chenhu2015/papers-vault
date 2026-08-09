---
title: "State2State: Environment-Derived Mid-Training for LLM Agents"
authors: ["Xuanyu Lei", "Yiqi Zhu", "Chenliang Li", "Kaiming Liu", "Peng Li", "Ming Yan", "Jieping Ye", "Ya-Qin Zhang", "Yang Liu"]
date: 2026-08-09
arxiv_id: "2608.04934"
url: "https://arxiv.org/abs/2608.04934"
score: 0.79
topics: [agentic RL, RL training, LLM agent, tool use, agentic]
status: unread
---

# State2State: Environment-Derived Mid-Training for LLM Agents

## Summary

State2State eliminates all external supervision: agents explore environments autonomously and generate training objectives by challenging themselves to reach discovered target states, verified via rule-based state matching without any expert trajectories or manual task design. Used as a mid-training stage before downstream RL on ALFWorld and ScienceWorld, it improves final performance and learning efficiency with evidence of cross-environment generalization.

## Key Contributions

- Environment-derived task synthesis: converts explored states into state-reaching objectives, eliminating both expert trajectory supervision and manual task specification
- Rule-based state-matching verifier: enables verifiable success signals without handcrafted reward functions
- Mid-training paradigm: positioned between pretraining and downstream RL as an environment-learning stage that builds interaction and manipulation capabilities
- Cross-environment generalization: mid-training in one environment improves performance in others, suggesting transferable environmental priors

## Relevance

State2State introduces a **fifth structural class** in the vault's agentic RL training paradigm taxonomy. The existing four (EnvACE: policy-as-environment via world rehearsal; EnvFactory: automated real-world API environment synthesis; DPEPO: explicit diversity rewards across simultaneous environments; AXPO: prefix-fixing resampling of all-wrong subgroups) all presuppose some external specification — either real APIs, human-designed tasks, or outcome verifiers. State2State's key distinction is eliminating ALL external specification: the environment itself becomes both the curriculum generator and the verifier. This directly extends the Aug 8 thread on environment bottleneck solutions while introducing a new dimension (self-directed task emergence) not covered by any prior class.

## My Thoughts

<!-- Add your own notes here -->
