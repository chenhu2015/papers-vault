---
title: "RL Tango: Reinforcing Generator and Verifier Together for Language Reasoning"
authors: ["Kaiwen Zha", "Zhengqi Gao", "Maohao Shen", "Zhang-Wei Hong", "Duane S. Boning", "Dina Katabi"]
date: 2026-07-13
arxiv_id: "2505.15034v2"
url: "https://arxiv.org/abs/2505.15034"
score: 0.90
topics: [agentic RL, RL training, GRPO, reward model, RLHF]
status: unread
---

# RL Tango: Reinforcing Generator and Verifier Together for Language Reasoning

## Summary

Tango uses RL to concurrently train an LLM generator and a generative process-level verifier in an interleaved manner, with the verifier co-evolving alongside the generator. Unlike SFT-trained or frozen verifiers, the RL-trained generative verifier receives only outcome-level correctness rewards (no process annotations) and exhibits improved OOD robustness and generalization. Both components reach SOTA among 7B/8B models: the generator on five competition-level math benchmarks, the verifier on ProcessBench.

## Key Contributions

- Interleaved RL co-training of generator (policy) and generative process-level verifier without requiring explicit process-level annotations
- Generative verifier is trained via RL on outcome-level correctness rewards, not SFT — avoids the reward hacking failure mode of SFT-trained verifiers
- Co-evolved verifier exhibits improved OOD robustness over deterministic/SFT-trained verifiers, especially on the hardest problems
- SOTA on five competition-level math benchmarks (generator) and ProcessBench (verifier) at 7B/8B scale

## Relevance

Directly answers the RL^V verifier generalization question opened in the Jul 12 digest: the generative verifier generalizes OOD not through explicit calibration but by co-evolving via RL alongside the generator, avoiding the SFT reward-hacking failure documented in [[2026-07-13-from-accuracy-to-robustness-a-study-of-rule--and-model-based]]. Tango extends [[2026-07-12-putting-the-value-back-in-rl-better-test-time-scaling-by-un]] (RL^V) by co-training both components simultaneously rather than RL^V's asymmetric design where the generator updates are primary and the verifier co-trains on the same data. Together, Tango + RL^V + [[2026-07-13-when-to-solve-when-to-verify-compute-optimal-problem-solving]] characterize the full picture: what to co-train (Tango), why co-training produces a robust verifier (Accuracy-to-Robustness), and when the verifier is worth using at inference time (When to Solve/Verify).

## My Thoughts

<!-- Add your own notes here -->
