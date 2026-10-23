---
title: "Ring-Zero: Scaling Zero RL to a Trillion Parameters for Emergent Reasoning"
authors: ["Xinyu Tang", "Qianggang Cao", "Yurou Liu", "Yuliang Zhan", "Xiaochong Lan", "Yifan Li", "Yuchen Yan", "Han Peng", "Zican Dong", "Zhenduo Zhang", "Tianshu Wang", "Xinyu Kong", "Zujie Wen", "Wayne Xin Zhao", "Zhiqiang Zhang", "Jun Zhou"]
date: 2026-07-14
arxiv_id: "2607.12395v2"
url: "https://arxiv.org/abs/2607.12395"
score: 0.79
topics: [RL training, RLHF, RLAIF, GRPO, PPO]
status: unread
---

# Ring-Zero: Scaling Zero RL to a Trillion Parameters for Emergent Reasoning

## Summary

Scales zero-RL (RLVR without human-annotated data) to 1T parameters with a stable pipeline using clipped importance sampling, training-inference ratio correction, and mixed-precision control. Identifies sequential discovery→sharpening training phases and emergent cognitive behaviors (structured formatting, self-verification, parallel reasoning) that eliminate the need for hand-crafted heuristics. Proposes a structured CoT evaluation framework across comprehensibility, reproducibility, and efficiency dimensions.

## Key Contributions

- Stable 1T-parameter zero-RL training via clipped importance sampling + training-inference ratio correction + mixed-precision control
- Two-phase training dynamics: discovery phase (strategy exploration) followed by sharpening phase (strategy consolidation)
- Emergent behaviors at scale: structured formatting, self-verification, parallel reasoning — making hand-crafted prompts redundant
- Structured CoT evaluation framework: comprehensibility, reproducibility, efficiency — measuring CoT quality beyond final-answer accuracy

## Relevance

Connects directly to the test-time compute + RL scaling angle surfaced today, providing the largest-scale empirical validation of zero-RL to date. The two-phase dynamics and emergent behavior observations also bear on the "How RL Reshapes LLM Reasoning" paper's strategy-selection model surfaced in the same search.

## My Thoughts

<!-- Add your own notes here -->
