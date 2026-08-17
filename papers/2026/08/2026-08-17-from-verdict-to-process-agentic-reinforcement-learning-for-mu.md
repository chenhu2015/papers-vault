---
title: "From Verdict to Process: Agentic Reinforcement Learning for Multi-Stage Fact Verification"
authors: ["Rongxin Yang", "Shenghong He", "Siyuan Zhu", "Chao Yu"]
date: 2026-08-17
arxiv_id: "2606.13262v1"
url: "http://arxiv.org/abs/2606.13262v1"
score: 0.74
topics: [agentic RL, RL training, reward model, LLM agent]
status: unread
---

# From Verdict to Process: Agentic Reinforcement Learning for Multi-Stage Fact Verification

## Summary

ProFact trains a unified policy to coordinate four stages of fact verification (claim decomposition, evidence seeking, answer generation, verdict prediction) end-to-end using process-aware rewards that provide stage-level learning signals to bridge sparse, delayed veracity labels. End-to-end trajectory optimization outperforms both isolated-stage optimization and fixed-heuristic coordination in verification accuracy and inference efficiency. The design is structurally analogous to CSO (critical step selection) and RSPO (process-reward for sampling diversity) but applied to a structured multi-stage verification pipeline, adding a new domain to the process-aware agentic RL taxonomy.

## Key Contributions

- ProFact: unified agentic RL policy for four-stage fact verification pipeline, trained end-to-end
- Process-aware rewards: stage-level signals replacing sparse final veracity labels
- End-to-end optimization outperforms both isolated-stage training and fixed-heuristic coordination
- Demonstrates process reward generalization beyond code/math tasks to fact verification

## Relevance

The vault's process reward taxonomy now covers: PAIR (internal LLM hidden-state probe), CSO (critical step selection), RSPO (reward-swap process+outcome), SeeNav-Agent/SRGPO (step grouping), SeekJudge (4-role Seek-Analyze), and REVERSE (search process rewards). ProFact adds a fifth architectural pattern: a single unified policy with stage-indexed process rewards rather than specialized sub-agents or an external verifier. This extends the process reward applicability domain from tool-use/navigation to structured reasoning pipelines (NLP fact verification).

## My Thoughts

<!-- Add your own notes here -->
