---
title: "Counterfactual Rollout Replay: Forkable Environments as Free Process Rewards for Software Engineering Agents"
authors: ["Yuanhao Li", "Hongbo Wang", "Xuhong Chen", "Yiming Cao", "Xunzhu Tang"]
date: 2026-09-29
arxiv_id: "2609.33875v1"
url: "https://arxiv.org/abs/2609.33875"
score: 0.88
topics: [agentic RL, RL training, LLM agent, agentic, GRPO]
status: unread
---

# Counterfactual Rollout Replay: Forkable Environments as Free Process Rewards for Software Engineering Agents

## Summary

Counterfactual Rollout Replay (CRR) exploits forkable executable environments (e.g., containerised SWE sandboxes) to generate step-level return contrasts without any learned process reward model: a small set of decision points are selected, the environment is forked and an alternative action sampled, and the branch rolled forward under the current policy to compute a counterfactual return. The realised trajectory advantage at selected steps is replaced by the contrast between actual and counterfactual terminal returns. On SWE-bench Verified, CRR yields 41.7% pass@1 versus 36.7% for extended outcome-only GRPO, a 5-point gain on identical wall-clock budget.

## Key Contributions

- Forkable-environment counterfactual: state restoration used to branch at selected decision points and sample an alternative action, rolling forward under the current policy
- "Free" process rewards: no human process labels and no learned PRM — supervision cost is near-zero; only replay compute (forking) is added
- Selective branching: only a small subset of decision points are counterfactually evaluated per trajectory to control cost
- Combines with existing process-reward and trajectory-search methods; standalone 5.0-point pass@1 gain on SWE-bench Verified

## Relevance

Like ASCT (same digest), CRR provides counterfactual-grounded step credit that avoids the fluency confound identified in "Credit Without Ground Truth." The mechanism is complementary to ASCT: while ASCT builds an attentive search tree over alternative actions at every visited state, CRR uses environment forking for a sparser, cheaper sample of branches — better suited to expensive real-world execution environments (code sandboxes) rather than text-based grids. Together ASCT + CRR define a counterfactual credit design space: attentive-dense (ASCT) vs. sparse-fork (CRR).

## My Thoughts

<!-- Add your own notes here -->
