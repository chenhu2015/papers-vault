---
title: "UCOB: Learning to Utilize and Evolve Agentic Skills via Credit-Aware On-Policy Bidirectional Self-Distillation"
authors: ["Songjun Tu", "Chengdong Xu", "Qichao Zhang", "Yiwen Ma", "Yaocheng Zhang", "Linjing Li", "Dong Li", "Xiangyuan Lan", "Dongbin Zhao"]
date: 2026-06-28
arxiv_id: "2606.29502"
url: "https://arxiv.org/abs/2606.29502"
score: 0.79
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# UCOB: Learning to Utilize and Evolve Agentic Skills via Credit-Aware On-Policy Bidirectional Self-Distillation

## Summary

UCOB treats skill-conditioned and no-skill prompts as two on-policy context views of the same model, comparing their return-to-go within the same task and anchor state to determine which view provides better credit. The higher-return view acts as the local teacher, enabling bidirectional distillation: useful skill behaviors are internalized from the skill-conditioned view, while misleading skill usage is corrected. UCOB also guides skill memory updates, retrieval, and reflection self-training — achieving 23.5 and 18.0 point gains over SOTA on ALFWorld and WebShop.

## Key Contributions

- **Return-to-go credit comparison**: skill-conditioned vs. no-skill rollout at same task/anchor state; the higher-return view becomes the local teacher — avoids the "privileged teacher" assumption that fails when retrieved skills mislead
- **Bidirectional distillation**: internalize useful skill-conditioned behaviors AND correct misleading ones; direction is credit-determined, not fixed
- **Integrated skill lifecycle**: UCOB's credit signal drives skill memory updates, utility-aware retrieval, and reflection self-training — a unified mechanism unlike Bayesian-Agent/SkillRise which separate lifecycle from credit
- **Strong benchmarks**: 23.5pt gain on ALFWorld, 18.0pt gain on WebShop vs. SOTA skill-memory baselines

## Relevance

UCOB directly extends the skill lifecycle synthesis from the vault (SkillRise Jul 31 + Bayesian-Agent + ReSkill). Where SkillRise uses cross-task discounted downstream outcomes for cross-episode credit, UCOB uses return-to-go comparison at anchor states for within-task skill credit. The bidirectional distillation design resolves the "misleading skill" failure mode that Bayesian-Agent's lifecycle model diagnosed but did not solve. UCOB's 23.5pt ALFWorld gain also provides a direct comparison point for RLVMR (Aug 1, 83.6% on ALFWorld hardest split) — both use ALFWorld but with different approaches, enabling future cross-paper analysis.

## My Thoughts

<!-- Add your own notes here -->
