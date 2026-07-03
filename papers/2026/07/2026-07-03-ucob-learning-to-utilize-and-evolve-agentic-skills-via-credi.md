---
title: "UCOB: Learning to Utilize and Evolve Agentic Skills via Credit-Aware On-Policy Bidirectional Self-Distillation"
authors: ["Songjun Tu", "Chengdong Xu", "Qichao Zhang", "Yiwen Ma", "Yaocheng Zhang", "Linjing Li", "Dong Li", "Xiangyuan Lan", "Dongbin Zhao"]
date: 2026-06-28
arxiv_id: "2606.29502v1"
url: "http://arxiv.org/abs/2606.29502v1"
score: 0.82
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# UCOB: Learning to Utilize and Evolve Agentic Skills via Credit-Aware On-Policy Bidirectional Self-Distillation

## Summary

UCOB challenges the privileged-teacher assumption in skill-memory agentic RL: retrieved skills may help in some states and mislead in others, so the skill-conditioned view should not unconditionally be the teacher. UCOB compares return-to-go between skill-conditioned and no-skill views at the same anchor state, using the higher-return view as the local credit signal to simultaneously internalize useful skills, correct misleading ones, and update skill memory and retrieval. Achieves +23.5pp on ALFWorld and +18.0pp on WebShop over SOTA baselines.

## Key Contributions

- Formal diagnosis of the privileged-teacher fragility in skill-conditioned agentic RL: the same skill prompt may help at one state and mislead at another, making fixed teacher assignment invalid
- Credit-aware bidirectional self-distillation: compares return-to-go of skill-conditioned vs no-skill views at identical anchor states; higher-return view teaches, lower-return view learns
- Joint optimization: the same credit signal drives skill memory updates, utility-aware retrieval weighting, and reflection self-training — three components updated from a single on-policy comparison
- Consistent gains across model scales on ALFWorld (+23.5pp), WebShop (+18.0pp), and Search-QA over skill-free RL and skill-memory baselines

## Relevance

UCOB operationalizes a credit assignment problem that none of the prior vault papers address: when should the policy trust its retrieved experience vs. its own reasoning? The return-to-go comparison at anchor states is structurally related to DuCA's (Jul 2) dual-horizon advantage normalization — both recognize that the credit signal from one context (turn-level vs. session-level for DuCA; skill-conditioned vs. no-skill for UCOB) can contaminate the other, and both solve it by separating and locally normalizing the two signals before merging.

## My Thoughts

<!-- Add your own notes here -->
