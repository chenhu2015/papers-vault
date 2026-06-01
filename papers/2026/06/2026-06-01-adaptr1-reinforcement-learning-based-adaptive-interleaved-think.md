---
title: "AdaptR1: Reinforcement Learning Based Adaptive Interleaved Thinking in Multi-hop Question Answering"
authors: ["Yuxin Wang", "Jiahao Lu", "Qifeng Wu", "Shicheng Fang", "Chuanyuan Tan", "Yining Zheng", "Xuanjing Huang", "Xipeng Qiu"]
date: 2026-06-01
arxiv_id: "2605.31062"
url: "https://arxiv.org/abs/2605.31062"
score: 0.79
topics: [GRPO, LLM agent, agentic]
status: unread
---

# AdaptR1: Reinforcement Learning Based Adaptive Interleaved Thinking in Multi-hop Question Answering

## Summary

AdaptR1 uses a fully RL-based strategy with a quality-gated efficiency reward to dynamically allocate reasoning budgets at each reasoning step of multi-hop QA — no SFT cold-start required. Under Graph-R1 setting, AdaptR1 reduces average thinking tokens by 69.71% (90.35% on HotpotQA) while maintaining comparable or better accuracy. Analysis reveals that overthinking in multi-hop reasoning is concentrated in initial planning stages, motivating step-wise adaptive allocation.

## Key Contributions

- Step-wise reasoning budget allocation via RL — unlike prior work that makes a single query-level thinking/no-thinking decision
- Quality-gated efficiency reward balances accuracy and token economy without SFT initialization
- 69.71% average token reduction and 90.35% on HotpotQA under Graph-R1 with maintained performance
- Empirical finding: overthinking in multi-hop tasks clusters at initial planning steps, not uniformly distributed

## Relevance

The step-wise adaptive thinking angle is distinct from reasoning budget papers covered in May 24 (which targeted overall budget), and the multi-hop QA setting with graph-based search connects to the search-augmented RL thread from May 28. The finding about overthinking concentration at planning stages is actionable for agentic GRPO design.

## My Thoughts

<!-- Add your own notes here -->
