---
title: "STAPO: Selective Trajectory-Aware Policy Optimization for LLM Agent Training"
authors: ["Qiuyi Qi", "Tian Liang", "Mutian Bao", "Jinjian Zhang", "Dongnan Liu", "Wei Zhou", "Linjian Mo", "Ming Kong", "Jie Liu", "Feng Zhang", "Qiang Zhu"]
date: 2026-07-26
arxiv_id: "2607.04963"
url: "https://arxiv.org/abs/2607.04963"
score: 0.82
topics: [agentic RL, LLM agent, GRPO, RL training]
status: unread
---

# STAPO: Selective Trajectory-Aware Policy Optimization for LLM Agent Training

## Summary

Diagnoses 'trajectory neglect' in long-horizon agentic RL — intermediate steps where agents lose focus on task goal and interaction history — and shows that Shannon entropy conflates inherent state complexity with agent confidence, producing unreliable step-level uncertainty estimates. Proposes normalized entropy (deviation from the agent's average behavior under a given state) to precisely locate neglect-prone steps, then applies a joint trajectory-aware reward plus trajectory-independent penalty in a hierarchical group-based RL framework. Achieves state-of-the-art performance on ALFWorld, WebShop, and Search-Augmented QA while substantially reducing trajectory neglect.

## Key Contributions

- Trajectory neglect diagnosis: identifies the failure mode where agents lose task/history focus at intermediate steps of long-horizon tasks
- Normalized entropy: measures confidence deviation relative to the agent's own average behavior under a state, decoupling state complexity from agent uncertainty
- Hierarchical group-based RL (STAPO): uses normalized entropy to locate outlier steps, then applies trajectory-aware reward (signal) + trajectory-independent penalty (regularizer) jointly
- State-of-the-art on three agentic benchmarks; evaluated on Qwen2.5 family

## Relevance

STAPO addresses the intermediate-step focus problem from a different angle than prior work: TRACE (Jul 25) assigns dense credit across turns; PATR (Jul 25) focuses rollout budget on high-quality states via PRM; STAPO focuses gradient budget on high-uncertainty steps via normalized entropy. The normalized entropy metric is the closest vault paper to BPO's entropy-weighted branching (Gap #12: entropy as structural signal), applying it to gradient allocation rather than rollout allocation. This partially closes Gap #12 from the training update perspective.

## My Thoughts

<!-- Add your own notes here -->
