---
title: "RLVR Training of LLMs Does Not Improve Thinking Ability for General QA: Evaluation Method and a Simple Solution"
authors: ["Kaiyuan Li", "Jing-Cheng Pang", "Yang Yu"]
date: 2026-06-06
arxiv_id: "2603.20799v1"
url: "http://arxiv.org/abs/2603.20799v1"
score: 0.82
topics: [RL training, RLHF, reinforcement learning, GRPO, reward model]
status: unread
---

# RLVR Training of LLMs Does Not Improve Thinking Ability for General QA: Evaluation Method and a Simple Solution

## Summary

This paper shows empirically that RLVR gains on verifiable tasks (math, code) do not transfer to general QA (GQA) — the trained thinking processes are far less effective on GQA than on verifiable tasks, apparently because GQA rewards admit shortcuts that bypass high-quality reasoning. The proposed fix, START (Separated Thinking And Response Training), first trains only the thinking process with rewards on the final answer before joint training, which improves both reasoning quality and final accuracy across GQA benchmarks and RL algorithms. The Cross-Generation evaluation framework introduced here enables quality measurement of intermediate reasoning steps independently of final-answer accuracy.

## Key Contributions

- Cross-Generation evaluation: feeds generated thinking context into LLMs of varying capability to assess thinking quality independent of final answer
- Key finding: RLVR on verifiable tasks does not automatically improve thinking on general QA; GQA shortcut rewards bypass quality reasoning
- START method: separate the thinking-process training phase (reward on final answer only), then combine — avoids reward shortcuts
- Validates START across multiple GQA benchmarks and RL algorithms, showing improvements in both reasoning quality and final accuracy

## Relevance

This directly addresses the OOD generalization question from the June 4 planned (but blocked) search. The finding that RLVR gains don't transfer is a critical counterpoint to the assumption underlying much of the current RL-for-LLM work in this digest. START's approach of separating reasoning training from answer training connects to the Separated Thinking thread and has implications for how GRPO and PPO should be applied beyond math/code domains.

## My Thoughts

<!-- Add your own notes here -->
