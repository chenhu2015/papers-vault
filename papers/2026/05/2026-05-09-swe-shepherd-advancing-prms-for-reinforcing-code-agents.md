---
title: "SWE-Shepherd: Advancing PRMs for Reinforcing Code Agents"
authors: ["Mahir Labib Dihan", "Md Ashrafur Rahman Khan"]
date: 2026-05-09
arxiv_id: "2604.10493v1"
url: "http://arxiv.org/abs/2604.10493v1"
score: 0.84
topics: [reward model, agentic RL, LLM agent, agentic]
status: unread
---

# SWE-Shepherd: Advancing PRMs for Reinforcing Code Agents

## Summary

SWE-Shepherd introduces Process Reward Models (PRMs) that provide dense, step-level supervision for repository-level code agents on SWE-Bench. The framework constructs an action-level reward dataset from SWE-Bench trajectories and trains a lightweight PRM to evaluate intermediate code editing, file navigation, and test execution actions. Without full RL training, the PRM guides inference-time action selection, improving interaction efficiency and action quality on SWE-Bench Verified.

## Key Contributions

- Action-level reward dataset constructed from SWE-Bench trajectories labelling intermediate actions (code edits, file navigation, test execution)
- Lightweight PRM trained on top of a base LLM to estimate usefulness of intermediate actions at inference time
- Demonstrated improved interaction efficiency and action quality on SWE-Bench Verified without requiring full RL training
- Identifies challenges in aligning intermediate step rewards with final task success

## Relevance

This directly extends the reward model research thread (Rollout Pass-Rate, Power Distribution, TraceLift from May 7) into the agentic coding domain, bridging two persistent interests: PRMs for step-level credit assignment and agentic RL for tool-using code agents. The SWE-Bench framing also connects to the CodeScout and agentic RL papers found today.

## My Thoughts

<!-- Add your own notes here -->
