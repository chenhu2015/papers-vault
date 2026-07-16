---
title: "Benchmark Test-Time Scaling of General LLM Agents"
authors: ["Xiaochuan Li", "Ryan Ming", "Pranav Setlur", "Abhijay Paladugu", "Andy Tang", "Hao Kang", "Shuai Shao", "Rong Jin", "Chenyan Xiong"]
date: 2026-02-22
arxiv_id: "2602.18998"
url: "https://arxiv.org/abs/2602.18998"
score: 0.75
topics: [LLM agent, agentic RL, tool use, multimodal models]
status: unread
---

# Benchmark Test-Time Scaling of General LLM Agents

## Summary

General AgentBench evaluates TTS strategies for general LLM agents across search, coding, reasoning, and tool-use in a unified environment. The key finding is that neither sequential scaling (iterative interaction) nor parallel scaling (multiple trajectory sampling) yields effective improvements for general agents — due to context ceiling in sequential scaling and verification gap in parallel scaling. This diagnostic complements TTI and the Scaling TTS paper by identifying the failure modes that make agent TTS fundamentally harder than single-turn reasoning TTS.

## Key Contributions

- General AgentBench: unified multi-skill benchmark spanning search, coding, reasoning, and tool-use domains for general LLM agents
- Context ceiling in sequential scaling: agents exhaust usable context before solving long-horizon tasks, truncating their effective reasoning window
- Verification gap in parallel scaling: without a reliable verifier to select among parallel trajectories, sampling diversity is wasted
- Substantial performance gap between domain-specific and general-agent evaluation — domain-specialist agents don't transfer

## Relevance

Provides the diagnostic complement to TTI's positive result: TTI shows interaction horizon scaling *can* work for web agents when training is designed for it; General AgentBench shows why naive TTS fails for general agents — context ceiling and verification gap. The verification gap finding connects directly to the LLMs-as-a-Jury result (Jul 15): the jury's shared-error floor is precisely the verification gap in the parallel scaling case, and is what makes PRM-style verifiers still valuable despite consensus.

## My Thoughts

<!-- Add your own notes here -->
