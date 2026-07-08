---
title: "Self-Improvement Can Self-Regress: The Rise-and-Collapse Failure Mode of LLM Self-Training"
authors: ["Anonymous"]
date: 2026-07-08
arxiv_id: "2606.21090v1"
url: "https://arxiv.org/abs/2606.21090"
score: 0.88
topics: [agentic RL, RL training, GRPO, reward model, PPO]
status: unread
---

# Self-Improvement Can Self-Regress: The Rise-and-Collapse Failure Mode of LLM Self-Training

## Summary

Identifies a fifth RLVR failure mode — within-task rise-and-collapse — where REINFORCE post-training on competitive programming tasks quickly peaks (within tens of gradient steps) and then collapses to near-zero pass@1, due to policy over-optimization on a fixed distribution rather than cross-task catastrophic forgetting; KL and EWC constraints do not prevent it. Studies three remedy levels across a controlled 10-campaign multi-seed testbed: CARE (between-campaign capability posterior + transfer gate + regression-aware belief revision), ES (within-campaign early-stop that rolls forward the peak checkpoint), and GRPO (group-relative normalization); on Qwen-2.5-7B, ES achieves the largest gains (22.2%), GRPO closely follows (20.7%), and GRPO+ES gives mixed evidence. GRPO raises the training floor but does not eliminate the within-campaign collapse cliff, whose peak-to-end gap remains ~17 points under both REINFORCE and GRPO.

## Key Contributions

- Names and characterizes the rise-and-collapse failure mode: within-task over-optimization on fixed distribution, distinct from all four prior RLVR failure modes (SeL, diversity collapse, capability boundary collapse, view-dependent advantage collapse)
- Establishes a controlled multi-seed (10 campaigns × 5 seeds) testbed for studying LLM self-training dynamics across Qwen-2.5-3B, 7B, and Gemma-3-4B
- Shows GRPO raises the training floor but does not eliminate the collapse cliff; ES is the most effective within-campaign remedy for 7B models
- CARE v2 significantly outperforms naive REINFORCE on 3B models where the base RL is fragile, suggesting remedy efficacy is regime-dependent

## Relevance

The rise-and-collapse failure mode is the fifth named RLVR failure mode in the vault, and the first that operates across training campaigns (within-task temporal scale) rather than within a single training run — it is structurally distinct from SeL (information self-locking at the reward level), diversity/gradient collapse (TA-GRPO), capability boundary collapse (RL-PLUS), and view-dependent advantage collapse (ConsistRoll). The ES remedy (roll forward peak checkpoint, set next budget to peak_step+3) is the simplest operationally and suggests that peak detection — not regularization — is the right control signal for this failure mode, consistent with Nemotron-Cascade 2's strategy of distilling from intermediate checkpoints rather than training to convergence.

## My Thoughts

<!-- Add your own notes here -->
