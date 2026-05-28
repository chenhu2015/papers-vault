---
title: "Evaluate-as-Action: Self-Evaluated Process Rewards for Retrieval-Augmented Agents"
authors: ["Jiangming Shu", "Yuxiang Zhang", "Ye Ma", "Xueyuan Lin", "Jitao Sang"]
date: 2026-03-10
arxiv_id: "2603.09203v2"
url: "https://arxiv.org/abs/2603.09203"
score: 0.83
topics: [agentic RL, tool use, GRPO, reward model, LLM agent]
status: unread
---

# Evaluate-as-Action: Self-Evaluated Process Rewards for Retrieval-Augmented Agents

## Summary

EvalAct converts implicit retrieval quality assessment into an explicit policy action via a Search-to-Evaluate protocol: each retrieval step is immediately followed by a structured self-evaluation score, yielding trajectory-aligned process signals. Process-Calibrated Advantage Rescaling (PCAR) then rescales GRPO advantages segment-by-segment based on evaluation confidence, emphasising reliable steps and updating uncertain ones conservatively. On 7 open-domain QA benchmarks, EvalAct achieves the best average accuracy with largest gains on multi-hop tasks.

## Key Contributions

- Search-to-Evaluate protocol: retrieval assessment made an explicit action, generating structured process signals from the trajectory itself
- Process-Calibrated Advantage Rescaling (PCAR): GRPO advantage rescaling weighted by per-segment evaluation confidence
- Self-evaluation avoids external reward model or intermediate label requirements
- Strongest gains on multi-hop reasoning tasks where intermediate retrieval quality matters most

## Relevance

Combines the "reward model as action" idea with the GRPO credit assignment thread — treating self-evaluation as a policy output rather than an external signal is a novel design point for agentic RL research, and PCAR is a natural extension of the advantage-rescaling ideas seen in DVAO and ConSPO.

## My Thoughts

<!-- Add your own notes here -->
