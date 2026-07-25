---
title: "Process Reward Informed Tree Rollout for Effective Multi-Turn RL"
authors: ["Xintong Li", "Sha Li", "Yuwei Zhang", "Changlong Yu", "Rongmei Lin", "Hongye Jin", "Shuyi Guan", "Xin Liu", "Linwei Li", "Qingyu Yin", "Jingbo Shang"]
date: 2026-07-17
arxiv_id: "2607.15610v1"
url: "http://arxiv.org/abs/2607.15610v1"
score: 0.85
topics: [agentic RL, RL training, reward model, LLM agent, tool use]
status: unread
---

# Process Reward Informed Tree Rollout for Effective Multi-Turn RL

## Summary

PATR organizes multi-turn agentic RL rollouts as trees where each turn is a branching decision point, using a process scorer to evaluate partial trajectories and selectively branch from promising states while reusing shared prefixes and early-stopping degenerate paths. The resulting rollout groups remain compatible with standard policy optimization (GRPO/RLOO) while providing more efficient exploration under the same training budget. PATR improves over strong baselines by +5.0 points on SWE-Bench and +9.3 points on FrozenLake.

## Key Contributions

- Reframes agentic RL exploration as "where to branch": each turn is a decision point, tree structure replaces independent trajectory sampling
- Process scorer evaluates partial trajectories to identify promising branching states (quality-aware, not entropy-based)
- Prefix reuse reduces redundant computation; conservative early-stopping eliminates degenerate path budget waste
- Compatible with standard GRPO/RLOO policy optimization — no algorithm change required; applicable to SWE-Bench (largely unexplored by prior tree-rollout methods)

## Relevance

PATR is the PRM-guided counterpart to BPO (Jul 22, entropy-based prefix branching in sandboxes). BPO identifies branching points via policy entropy (oracle-free); PATR uses a process scorer (requires a trained or prompted PRM). Together they establish the design space for tree-structured agentic RL: oracle-free structural signal (entropy) vs. learned process signal (PRM). PATR's SWE-Bench evaluation is important — BPO was tested on code agents but not specifically on SWE-Bench's repository-level complexity. The ToolVerse Turn-Aware Relative Advantage (Jul 24) is a fourth approach to the same "where does credit go" question in multi-turn rollouts, now alongside BPO (entropy branching), TRACE (TD log-ratio), and PATR (PRM branching).

## My Thoughts

<!-- Add your own notes here -->
