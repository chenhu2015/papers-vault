---
title: "SeekJudge: A Practical Reward Framework for Reinforcement Learning in Computer-Use Agents"
authors: ["Yang Wan", "Zhenhao Zhang", "Jierui Wang", "Linchao Zhu"]
date: 2026-07-25
arxiv_id: "2607.23263v1"
url: "https://arxiv.org/abs/2607.23263"
score: 0.76
topics: [agentic RL, LLM agent, reward model, tool use]
status: unread
---

# SeekJudge: A Practical Reward Framework for Reinforcement Learning in Computer-Use Agents

## Summary

SeekJudge uses four role-specialized agents (Condense, Ground, Seek, Analyze) in a Seek-Analyze loop to produce step-level trajectory verdicts for computer-use agent RL, with a seed-calibrated distillation pipeline training one shared 9B backbone to serve all four roles cheaply. It is the first model-based reward to match or surpass native rule-based supervision in online RL for long-horizon GUI tasks, providing step-level judgments at a small per-call context that scales to much longer trajectories than a closed-source model call. An additional reward server architecture improvement speeds up judging in RL, making model-based reward a practical drop-in for rule-based supervision in GUI agent training.

## Key Contributions

- Four-role agent decomposition (Condense → Ground → Seek-Analyze loop) for trajectory verdict, enabling parallel role-specialization within a single distilled model
- Seed-calibrated distillation: a shared 9B backbone trained for all four roles via calibrated seed examples, far cheaper per call than closed-source LLMs
- Step-level judgments: unlike trajectory-only verifiers, SeekJudge assigns step-level credit within GUI trajectories
- First model-based reward matching/surpassing rule-based supervision in online RL for computer-use agents

## Relevance

SeekJudge extends the vault's reward model thread (PAIR internal reward, CSO critical step DPO, RSPO reward-swap) to the computer-use / GUI domain, where verifiable rules are expensive to maintain and drift with app updates. The four-role decomposition is structurally analogous to VERDICT's disagreement-consensus (Aug 14) — both are training-free or lightly-trained inference-time judgment systems — but SeekJudge is trained specifically for RL reward rather than evaluation, and achieves parity with rule-based RL rewards for the first time.

## My Thoughts

<!-- Add your own notes here -->
