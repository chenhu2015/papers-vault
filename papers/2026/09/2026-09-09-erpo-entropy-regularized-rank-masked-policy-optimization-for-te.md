---
title: "Entropy-Regularized Rank-Masked Policy Optimization for Test-Time Reinforcement Learning in Code Generation"
authors: ["Jiacheng Xu", "Feng Chen", "Xiuneng Xu", "Bo An"]
date: 2026-09-09
arxiv_id: "2609.09135v1"
url: "http://arxiv.org/abs/2609.09135v1"
score: 0.78
topics: [RL training, reward model, agentic RL, GRPO]
status: unread
---

# Entropy-Regularized Rank-Masked Policy Optimization for Test-Time Reinforcement Learning in Code Generation

## Summary

ERPO introduces probe-driven TTRL for code generation, constructing output-free probe inputs from problem statements and defining a Probe Consensus Reward (PCR) from behavioral agreement across candidate programs' executions — bypassing the need for canonical answers. To prevent reward hacking through spurious consensus, ERPO adds rank masking (converting low-PCR samples into conservative negative updates) and an entropy ceiling to control policy drift. The method substantially improves pass@1 and pass@k in both in-domain adaptation and zero-shot transfer.

## Key Contributions

- Probe-driven reward: constructs probe inputs from problem statement, executes candidates on probes, measures behavioral agreement as a training signal (no canonical answers needed)
- Rank masking: converts low-Probe Consensus Reward samples into conservative negative updates, blocking reward hacking through spurious consensus
- Entropy ceiling: prevents policy drift during test-time adaptation
- Substantially improves pass@1 and pass@k in in-domain adaptation and zero-shot transfer on coding benchmarks

## Relevance

Directly relevant to the reward model and RL training threads — ERPO addresses the open problem of constructing a reward signal for code generation without ground-truth outputs, a key gap for deploying GRPO/TTRL in production code agents. The Probe Consensus Reward is an execution-artifact credit source (behavioral agreement from probe execution), connecting to the "structured credit from execution artifacts" open gap identified in Sep 08; ERPO operationalizes this for test-time without the full verifier infrastructure required by VICT.

## My Thoughts

<!-- Add your own notes here -->
