---
title: "HIPIF: Hierarchical Planning and Information Folding for Long-Horizon LLM Agent Learning"
authors: ["Juncheng Diao", "Zhicong Lu", "Peiguang Li", "Yongwei Zhou", "Changyuan Tian", "Qingbin Li", "Rongxiang Weng", "Jingang Wang", "Xunliang Cai"]
date: 2026-06-09
arxiv_id: "2606.10507v1"
url: "https://arxiv.org/abs/2606.10507"
score: 0.82
topics: [agentic RL, RL training, LLM agent, reinforcement learning]
status: unread
---

# HIPIF: Hierarchical Planning and Information Folding for Long-Horizon LLM Agent Learning

## Summary

HIPIF trains LLM agents for long-horizon tasks by decomposing execution around explicit subgoals and compressing completed subgoal histories (information folding) to eliminate the long-context interference that gradually degrades multi-turn agent reasoning. Subgoal-oriented process rewards and hierarchical reflection stabilize subgoal generation, transition, and execution end-to-end without auxiliary models or expert demonstrations. Experiments across three agentic benchmarks demonstrate consistent improvements over baselines including GRPO and hierarchical RL methods.

## Key Contributions

- Identifies long-context interference (growing histories weakening global task state tracking) as a distinct failure mode from sparse rewards in long-horizon agentic RL
- Information folding: completed subgoal histories are compressed into compact summaries, reducing context length without losing information
- Subgoal-oriented process rewards that guide subgoal generation, transition, and execution at each level
- End-to-end training without costly auxiliary models or task-specific expert demonstrations

## Relevance

Directly extends the hierarchical RL thread (ARISE Jun 12, HiPER Jun 14) with a new angle: long-context interference as the core challenge, not skill accumulation or variance reduction. Information folding complements HiPER's HAE theorem (variance reduction via hierarchical decomposition) with a memory management solution — HiPER ensures better gradients per subgoal, HIPIF ensures the agent doesn't confuse past subgoals with current ones as histories grow.

## My Thoughts

<!-- Add your own notes here -->
