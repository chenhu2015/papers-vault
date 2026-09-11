---
title: "CRISP: Critical Step Perception for Training Efficient Deep Search Agents"
authors: ["Haosi Mo", "Zihao Yan", "Ruiqing Zhang", "Zhongli Li", "Hexuan Deng", "Xuebo Liu", "Min Zhang"]
date: 2026-08-03
arxiv_id: "2608.01867v2"
url: "https://arxiv.org/abs/2608.01867"
score: 0.80
topics: [agentic RL, RL training, tool use, LLM agent, reward model]
status: unread
---

# CRISP: Critical Step Perception for Training Efficient Deep Search Agents

## Summary

CRISP trains efficient deep search agents by distinguishing evidence-gathering tool interactions from redundant ones via Backward Evidence Induction — a strong model traverses completed trajectories backward from the final answer, labeling each tool-call step as evidence-critical or redundant. A distilled critical-step recognizer performs full-trajectory analysis in a single pass, enabling an efficiency-aware reward applied only on successful rollouts. CRISP reduces interaction turns by 15.1% (BrowseComp) and 33.2% (HLE-Verified) while maintaining competitive accuracy.

## Key Contributions

- Backward Evidence Induction: strong model traverses completed trajectory backward from final answer, labels each tool-call step as evidence-providing/preserving or redundant — step-level supervision without requiring per-step ground truth
- Critical-step recognizer distillation: full-trajectory analysis in a single forward pass, enabling scalable inference-time and reward-time step classification
- Efficiency-aware reward applied only to successful rollouts: preserves evidence-critical steps while pruning redundancy; avoids suppressing steps that gather necessary evidence (failure mode of uniform tool-use penalty)
- 15.1% and 33.2% turn reduction on BrowseComp/HLE-Verified with maintained accuracy

## Relevance

CRISP is structurally complementary to SVRL (Sep 10's search-aware penalty) but operates at the training signal level rather than the reward component level. SVRL adds tool-efficiency as a reward component; CRISP identifies which tool calls are evidence-critical via backward tracing and shapes the training reward accordingly. Together they define two axes of efficiency in agentic RL: reward-level efficiency penalty (SVRL) vs. step-level credit discrimination (CRISP). The Backward Evidence Induction mechanism is also the search-agent analog of TASPO's privileged information — both use hindsight information from completed trajectories to assign more accurate per-step credit.

## My Thoughts

<!-- Add your own notes here -->
