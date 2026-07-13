---
title: "From Accuracy to Robustness: A Study of Rule- and Model-based Verifiers in Mathematical Reasoning"
authors: ["Yuzhen Huang", "Weihao Zeng", "Xingshan Zeng", "Qi Zhu", "Junxian He"]
date: 2026-07-13
arxiv_id: "2505.22203v2"
url: "https://arxiv.org/abs/2505.22203"
score: 0.85
topics: [RL training, RLHF, RLAIF, reward model, PPO]
status: unread
---

# From Accuracy to Robustness: A Study of Rule- and Model-based Verifiers in Mathematical Reasoning

## Summary

A comprehensive study of rule-based and model-based verifiers in RLVR for math reasoning. Rule-based verifiers produce non-negligible false negatives that worsen as the policy model gets stronger; model-based verifiers achieve higher static accuracy but are susceptible to reward hacking after fine-tuning, which the policy exploits to inflate rewards. Both failure modes represent complementary risks for verifier design in RL training pipelines.

## Key Contributions

- Rule-based verifiers fail to recognize equivalent answers in different formats, causing false negatives that compound as the policy improves (stronger model → more diverse correct formats → more false negatives)
- Model-based verifiers achieve higher static verification accuracy but are susceptible to "hacking" (policy learns patterns that fool the verifier) after fine-tuning
- Empirical RL training results confirming both failure modes degrade policy optimization, not just static evaluation
- Analysis provides the empirical rationale for generative RL-trained verifiers (as in Tango/RL^V) over static verifier designs

## Relevance

This paper is the empirical foundation explaining why RL^V ([[2026-07-12-putting-the-value-back-in-rl-better-test-time-scaling-by-un]]) and Tango ([[2026-07-13-rl-tango-reinforcing-generator-and-verifier-together-for-la]]) chose to co-train generative verifiers via RL rather than using rule-based or SFT-trained model verifiers. Rule-based verifiers fail on stronger policies (false negatives compound); SFT model verifiers get hacked. The RL-trained generative verifier in Tango avoids both: it co-evolves with the policy (no static format bias) and is optimized via RL (not SFT, so no frozen decision boundary to exploit). The two verifier failure modes also map onto two distinct open gaps in the vault's RL training thread.

## My Thoughts

<!-- Add your own notes here -->
