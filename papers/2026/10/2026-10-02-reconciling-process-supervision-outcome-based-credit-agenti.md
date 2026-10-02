---
title: "Reconciling Process Supervision with Outcome-Based Credit in Agentic Policy Optimization"
authors: ["Jingxiao Yang", "Wangjie Gan", "Yingxuan Zhuang", "Wenqi Zhang", "Jintao Chen", "Xuhong Zhang"]
date: 2026-08-31
arxiv_id: "2608.31077v2"
url: "http://arxiv.org/abs/2608.31077v2"
score: 0.82
topics: [agentic RL, RL training, reward model, LLM agent]
status: unread
---

# Reconciling Process Supervision with Outcome-Based Credit in Agentic Policy Optimization

## Summary

TASPO converts privileged information available during training into outcome-grounded action credit by aggregating PI-induced likelihood shifts at the executable-action level and converting them into mean-preserving weights on trajectory advantage. This ensures the verified outcome still determines the update direction while PI only redistributes credit across actions, closing the supervision-credit gap that arises when fine-grained supervision does not directly imply fine-grained credit. TASPO improves over GRPO by 10.6% across three agentic benchmarks and generalizes better to unseen tasks.

## Key Contributions

- Formalizes the "supervision-credit gap": PI-induced likelihood changes describe policy preference shifts, not outcome-aligned credit — fine-grained supervision does not automatically yield fine-grained credit
- Decision-applicable PI constructed from verified successful experience; likelihood shifts aggregated at executable-action granularity (not token level)
- Mean-preserving weight conversion: outcome determines direction and average scale; PI only redistributes credit within the trajectory — preserving verifiability guarantees
- 10.6% gain over GRPO; ablations confirm that action-level assignment (vs. token-level) specifically stabilizes optimization

## Relevance

TASPO contributes a principled framing that applies to the entire step-credit cluster: every method that uses a "fine-grained signal" (HaPRL's process annotations, DARS's predicate graph, T2SPO's regression estimates) implicitly faces the supervision-credit gap. TASPO's mean-preserving weight design is a concrete solution that preserves the outcome-verification guarantee while using internal signals to sharpen credit. The paper's distinction between PI-for-supervision and PI-for-credit is directly relevant to the open question of whether CCS/cross-attention/TGPO PRM proxies select for the same high-quality trajectories.

## My Thoughts

<!-- Add your own notes here -->
