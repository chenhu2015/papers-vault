---
title: "Rewarding Better Thinking for LLM Preference Alignment"
authors: ["Xubo Liu", "Wenya Guo", "Ruxue Yan", "Xinying Qian", "Ying Zhang"]
date: 2026-08-31
arxiv_id: "2607.19824"
url: "https://arxiv.org/abs/2607.19824"
score: 0.74
topics: [reinforcement learning, RL training, RLHF, reward model, RLAIF]
status: unread
---

# Rewarding Better Thinking for LLM Preference Alignment

## Summary

TCR (Thinking Checklist Reward) is a process-oriented reward for RL-based preference alignment that converts preference pairs into sample-specific thinking checklists and evaluates whether the model's reasoning trace addresses the preference-implied considerations. To avoid redundancy with outcome-level supervision, TCR applies an exponential moving average (EMA) residual formulation to isolate a complementary thinking surplus — the portion of reasoning quality not predictable from the outcome reward alone. Across five models and three model families, TCR consistently improves alignment performance.

## Key Contributions

- Thinking Checklist Reward: preference pairs are converted into checklists of considerations the winning response addressed, evaluated against the generated reasoning trace
- EMA residual formulation: the thinking reward uses the EMA of outcome rewards as a baseline, reporting only the residual thinking quality beyond what outcome-level feedback already captures — prevents double-counting
- Sample-specific supervision: each checklist is derived from the specific preference pair, not a global rubric, aligning the process signal with the instance-level preference
- Consistent gains across five models from three families on diverse alignment benchmarks; ablations confirm both the checklist supervision and EMA residual are individually necessary

## Relevance

TCR is the first vault paper to explicitly decompose process reward into "thinking surplus" over outcome reward using an EMA residual — a technique complementary to DataPRM/ToolPRM's environment-aware approach (Aug 26) and EFCA's return reweighting (Aug 30). The EMA residual framing also connects to the OPD/RL integration thread: both OPDVR (Aug 30) and TCR use reward-level decomposition to combine two supervision signals without double-counting; they apply the idea at different granularities (trajectory-level vs. token/trace-level).

## My Thoughts

<!-- Add your own notes here -->
