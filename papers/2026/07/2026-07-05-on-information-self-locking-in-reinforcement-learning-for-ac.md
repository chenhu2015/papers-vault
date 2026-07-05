---
title: "On Information Self-Locking in Reinforcement Learning for Active Reasoning of LLM agents"
authors: ["Deyu Zou", "Yongqiang Chen", "Fan Feng", "Mufei Li", "Pan Li", "Yu Gong", "James Cheng"]
date: 2026-07-05
arxiv_id: "2603.12109"
url: "https://arxiv.org/abs/2603.12109"
score: 0.78
topics: [agentic RL, LLM agent, RL training, GRPO]
status: unread
---

# On Information Self-Locking in Reinforcement Learning for Active Reasoning of LLM agents

## Summary

Identifies Information Self-Locking (SeL), a bidirectional failure mode in outcome-based RL for LLM agents where weak action selection deprives belief tracking of useful evidence while weak belief tracking obscures the credit of informative actions, creating a self-reinforcing collapse into non-exploratory behavior. AREW (Advantage Reweighting) addresses SeL by using directional critiques to reallocate credit within trajectories, yielding up to 60-point performance gains across 9 agentic tasks of varying complexity.

## Key Contributions

- Formal decomposition of agentic RL into Action Selection (AS) and Belief Tracking (BT) as coupled capabilities
- Information Self-Locking (SeL): names the bidirectional bottleneck where weak AS and weak BT mutually starve each other of learning signal
- AREW (Advantage Reweighting): directional critiques used to reallocate credit within trajectories without changing the policy gradient algorithm
- Validated across 9 agentic tasks spanning varying complexity levels, up to 60-point gains

## Relevance

SeL diagnoses a failure mode at the intersection of the credit assignment thread and the agentic RL exploration thread. Where the Jul 2–4 papers (TRIAGE, CRAFT, UCOB, OPID) all diagnosed credit misassignment for known-good trajectories, SeL explains why agents fail to generate informative trajectories in the first place — the credit assignment problem and the exploration problem are coupled. AREW's directional critique reweighting connects to the same advantage-reshaping principle used in TRIAGE's role-conditioned credit and CRAFT's counterfactual token importance.

## My Thoughts

<!-- Add your own notes here -->
