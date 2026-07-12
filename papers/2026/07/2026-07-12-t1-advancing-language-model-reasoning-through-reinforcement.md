---
title: "T1: Advancing Language Model Reasoning through Reinforcement Learning and Inference Scaling"
authors: ["Zhenyu Hou", "Xin Lv", "Rui Lu", "Jiajie Zhang", "Yujiang Li", "Zijun Yao", "Juanzi Li", "Jie Tang", "Yuxiao Dong"]
date: 2026-01-20
arxiv_id: "2501.11651"
url: "https://arxiv.org/abs/2501.11651"
score: 0.83
topics: [RL training, agentic RL, reinforcement learning, RLHF]
status: unread
---

# T1: Advancing Language Model Reasoning through Reinforcement Learning and Inference Scaling

## Summary

T1 scales RL training by combining synthesized chain-of-thought data (trial-and-error + self-verification) for initialization with oversampling diversity during RL to promote exploration. The resulting model exhibits clear inference scaling behavior: increased inference budgets directly improve T1's performance without additional verification, a property that standard RL-trained models often lack. This establishes a training-inference design connection between rollout diversity and test-time compute scaling that complements RL^V's verifier co-training approach.

## Key Contributions

- Synthesized CoT initialization integrating trial-and-error and self-verification for RL bootstrapping
- Oversampling during RL training promotes diversity and richer exploration of the solution space
- T1 exhibits robust inference scaling behavior: more inference compute → better performance, without extra verification mechanism
- Simple strategy for examining inference scaling: directly increasing inference budget improves T1's performance

## Relevance

T1 is the structural complement to RL^V from the same search thread: RL^V addresses inference scaling by co-training a verifier (how to use test-time compute), while T1 addresses it by training with exploration diversity (why the model can scale at inference). Together they answer two sides of the same question. T1's oversampling diversity mechanism also extends the rollout diversity framework (TA-GRPO input-level, Reaching Beyond the Mode output-level) with a new angle: sampling diversity during RL training as the mechanism that unlocks inference-time scaling behavior.

## My Thoughts

<!-- Add your own notes here -->
