---
title: "Single-Rollout Asynchronous Optimization for Agentic Reinforcement Learning"
authors: ["Zhenyu Hou", "Yujiang Li", "Jie Tang", "Yuxiao Dong"]
date: 2026-09-08
arxiv_id: "2607.07508v1"
url: "http://arxiv.org/abs/2607.07508v1"
score: 0.80
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Single-Rollout Asynchronous Optimization for Agentic Reinforcement Learning

## Summary

SAO replaces GRPO's group-wise sampling with single-rollout per prompt plus strict double-side token-level clipping to stabilize asynchronous agentic RL over 1000+ training steps, eliminating off-policy degradation while maintaining competitive throughput. Deployed in GLM-5.2 (750B-A40B) training, SAO consistently outperforms GRPO variants on SWE-Bench Verified, BeyondAIME, and IMOAnswerBench, and shows particular effectiveness in online learning settings with evolving environments.

## Key Contributions

- Single-rollout per prompt replacing group-wise sampling to reduce off-policy effects and improve generalization in async RL
- Practical value-model training designs for off-policy robustness alongside the single-rollout strategy
- Strict double-side token-level clipping for optimization stability over 1000+ gradient steps
- Production-scale deployment in GLM-5.2 (750B-A40B); outperforms GRPO on SWE-Bench Verified, BeyondAIME, IMOAnswerBench

## Relevance

SAO adds a fifth agentic RL efficiency axis (asynchronous training stability) orthogonal to SAPO's shared-backbone critic elimination, EvoHarness-RL's harness-annealing, HARTS's prefix sharing, and SINKFLEX-RL's attention kernel. The production deployment context at 750B scale is uniquely important: it confirms that single-rollout RL is viable at the largest scales, where group-wise sampling in GRPO is most memory-prohibitive. The convergence of SAPO and SAO on "eliminate group sampling" suggests this is a robust direction for large-scale agentic RL.

## My Thoughts

<!-- Add your own notes here -->
