---
title: "Retrieval, Reward, and Training Protocols: What Matters in Training Search Agents?"
authors: ["Yibo Zhao", "Zichen Ding", "Jiawei Wu", "Zun Wang", "Xiang Li"]
date: 2026-05-31
arxiv_id: "2605.27881"
url: "https://arxiv.org/abs/2605.27881"
score: 0.82
topics: [agentic RL, reward model, LLM agent, tool use, RLHF]
status: unread
---

# Retrieval, Reward, and Training Protocols: What Matters in Training Search Agents?

## Summary

A controlled empirical study isolates three underexplored dimensions of search agent RL training: corpus quality (fixing Wikipedia 2018 coverage yields larger gains than switching algorithms), reward type (outcome-based rewards match or beat process-level credit assignment in most settings), and training data diversity with off-policy utilization. Key finding: data quality dominates algorithm choice, and outcome rewards outperform process rewards for search agent training in most conditions.

## Key Contributions

- Identifies critical data-coverage issue in widely-used Wikipedia 2018 corpus; fixing it yields larger gains than algorithm changes
- Systematic comparison of outcome-based vs. process-based rewards across three base models: simplest outcome reward is competitive or superior in most settings
- Process-level credit assignment shown to over-correct agent behavior in some conditions
- Practical guidelines on training data diversity, off-policy data utilization, and search budget scaling

## Relevance

Directly relevant to the search-augmented agentic RL thread (IG-Search, TIPS, EvalAct, SLATE — May 28 digest). The finding that outcome rewards beat process rewards for search agents counterbalances the DeepTool and PRO-CUA results that advocate for process rewards in other agentic domains, adding an important nuance to the reward design thread.

## My Thoughts

<!-- Add your own notes here -->
