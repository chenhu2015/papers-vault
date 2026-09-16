---
title: "CodeGrep: An RL-Trained Retrieval Agent for LLM Coding Agents"
authors: ["Wuya Chen", "Yihao yang", "Yang Cao", "Yue Lin"]
date: 2026-08-06
arxiv_id: "2608.05886v1"
url: "http://arxiv.org/abs/2608.05886v1"
score: 0.78
topics: [agentic RL, tool use, GRPO, LLM agent]
status: unread
---

# CodeGrep: An RL-Trained Retrieval Agent for LLM Coding Agents

## Summary

CodeGrep trains a 14B retrieval agent end-to-end with GRPO to issue multi-turn grep, glob, and read tool calls that return candidate files to a frozen downstream coding agent, improving SWE-Bench Verified resolve rate from 25.8% to 27.0% while using 15% fewer rounds and 19% fewer tokens on resolved instances. Key finding: applying the efficiency signal at the advantage layer (rather than reward layer) reduces KL drift and translates cleanly to downstream efficiency, and a precision threshold of ~0.45 separates retrieval helpers from retrieval degraders. Supervision is mined from 67K open-source agent trajectories via CATM in a Git-worktree multi-turn RL environment.

## Key Contributions

- GRPO-trained multi-turn retrieval agent (grep/glob/read) as a frozen upstream module for coding agents
- Efficiency signal at advantage layer (vs. reward layer) reduces KL drift — concrete advantage-shaping finding
- Precision threshold empiric: BM25 (0.375) degrades, Jina (0.445) neutral, CodeGrep (0.677) crosses the help threshold
- CATM supervision mining from 67K open-source trajectories; Git-worktree multi-turn RL environment

## Relevance

CodeGrep instantiates the tool-use GRPO thread (cf. A²Agent, ARISE-RL) in the retrieval-as-tool domain, and adds a new insight about advantage-layer efficiency signaling that applies broadly to any GRPO-based agent where efficiency is a training objective. The frozen-upstream-module architecture is the inverse of Harness-RL (which trains the model given a fixed harness) — CodeGrep trains a tool-using sub-agent given a fixed downstream agent.

## My Thoughts

<!-- Add your own notes here -->
