---
title: "When Self-Belief Misleads: Active Label Acquisition for Reinforcement Learning with Verifiable Rewards"
authors: ["Li Wang", "Xiaodong Lu", "Xiaohan Wang", "Yikun Ban", "Jiajun Chai", "Wei Lin", "Tianhao Peng", "Guojun Yin"]
date: 2026-05-26
arxiv_id: "2605.25864v1"
url: "http://arxiv.org/abs/2605.25864v1"
score: 0.80
topics: [RLVR, RL training, reward model, RLAIF]
status: unread
---

# When Self-Belief Misleads: Active Label Acquisition for Reinforcement Learning with Verifiable Rewards

## Summary

RLAVR proposes active learning to identify which RLVR training samples most benefit from ground-truth labels, using the Corrective Advantage Gap (CAG) metric that measures divergence between pseudo- and oracle-reward advantages at the sample level. CARE translates the oracle CAG criterion into a practical pre-query acquisition policy, stabilizing training by mixing a small fraction of GT labels with pseudo-labels and avoiding training collapse. The approach generalizes across domains, model families, and scales, directly addressing RLVR's expensive dependency on labeled data.

## Key Contributions

- Identifies that RLVR training collapse under pseudo-labels stems from unequal annotation value across samples — some samples benefit far more from GT labels than others
- Corrective Advantage Gap (CAG): measures sample-level supervision value as the divergence between pseudo- and oracle-reward advantage signals
- CARE: practical pre-query acquisition policy translating oracle CAG into a deployable active learning criterion
- Demonstrates effectiveness across diverse domains, model families, and model scales with limited annotation budget

## Relevance

Bridges RLVR and RLAIF paradigms: rather than choosing between expensive GT labels (RLVR) or noisy pseudo-labels (RLAIF), actively selects the most valuable subset to annotate. Directly connected to the RLAIF thread the search targeted today.

## My Thoughts

<!-- Add your own notes here -->
