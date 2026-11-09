---
title: "DE-Venus: A Data-Efficient RLVR Framework for Large Language Models"
authors: ["Shenzhi Yang", "Guangcheng Zhu", "Kai Tang", "Zhengqing Zang", "Xing Zheng", "Haobo Wang", "Yingfan Ma", "Bowen Song", "Bo Han", "Bo An", "Lei Feng", "Weiqiang Wang", "Junbo Zhao", "Gang Chen"]
date: 2026-09-03
arxiv_id: "2609.03324"
url: "https://arxiv.org/abs/2609.03324"
score: 0.85
topics: [RLAIF, GRPO, reward model, agentic RL, RL training]
status: unread
---

# DE-Venus: A Data-Efficient RLVR Framework for Large Language Models

## Summary

DE-Venus is a unified framework for data-efficient RLVR that treats supervision as evolving state across three modules: Active Data Selection (allocates training and annotation budgets), Weak Supervision Construction (derives learning signals from unlabeled examples), and Training-Time Supervision Refinement (filters or corrects unreliable targets). It unifies seven representative methods under a common interface expressed as offline dataset transitions or online transformations of targets, rewards, batches, and advantages. Achieves comparable or better model quality using only 10% of labels or 13% of relevant data, reducing observed convergence steps by 63–75% in business scenarios.

## Key Contributions

- Three-module lifecycle decomposition: Active Data Selection → Weak Supervision Construction → Training-Time Supervision Refinement
- Unified interface that supports seven representative data-efficient RLVR methods without modifying distributed training (verl) execution contracts
- 10% labels or 13% relevant data suffices to match or improve full-data baselines; 63–75% convergence step reduction in business settings
- Demonstrates data selection, noisy-label handling, and weak supervision as complementary, composable strategies rather than independent fixes

## Relevance

This paper directly addresses the RLVR data selection thread opened by InSight (Nov 8), extending beyond InSight's Bayesian MI framing to cover the full supervision lifecycle. DE-Venus is the most comprehensive treatment of data efficiency in RLVR to appear in this digest and complements InSight (difficulty + evidence decomposition) and FADE (difficulty-adaptive scheduling) by offering a unified framework that subsumes multiple selection strategies.

## My Thoughts

<!-- Add your own notes here -->
