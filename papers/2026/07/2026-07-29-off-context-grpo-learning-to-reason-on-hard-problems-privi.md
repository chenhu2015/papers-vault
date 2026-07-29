---
title: "Off-Context GRPO: Learning to Reason on Hard Problems using Privileged Information"
authors: ["Priyank Agrawal", "Ankur Samanta", "Shervin Ghasemlou", "Jalaj Bhandari", "Kavosh Asadi", "Daniel Jiang", "Aditya Modi"]
date: 2026-07-21
arxiv_id: "2607.19313"
url: "https://arxiv.org/abs/2607.19313"
score: 0.80
topics: [RL training, GRPO, agentic RL, RLAIF]
status: unread
---

# Off-Context GRPO: Learning to Reason on Hard Problems using Privileged Information

## Summary

Off-Context GRPO (OC-GRPO) solves the zero-learning-signal cliff in RLVR where models cannot generate any correct solutions on hard problems, receiving no gradient signal. Guided rollouts are generated from prompts containing privileged information (e.g., solution prefixes), then an importance-corrected objective steers the update back toward the unguided target objective, preventing the distribution mismatch that makes uncorrected guided training unstable. On standard mathematical reasoning benchmarks, OC-GRPO achieves +3.9% absolute improvement (13.8% relative) over vanilla GRPO with negligible additional cost.

## Key Contributions

- **Off-context rollout definition**: rollouts generated from prompts with privileged guidance, but target objective defined by original unguided prompt — separating generation context from learning context
- **Importance-corrected objective**: IS correction to bridge guided → unguided distribution mismatch; without IS, guided training destabilizes (distribution mismatch between rollout policy and optimization target)
- **Hard-problem zero-cliff solution**: specifically targets cases where vanilla GRPO gets zero learning signal across all rollouts, which is the extreme case of Gap #16's all-fail group pathology
- **+13.8% relative improvement** over vanilla GRPO on math reasoning with negligible overhead

## Relevance

Addresses the zero-reward cliff that is the degenerate extreme of Gap #16 (GRPO all-fail group amplification): when no correct solutions can be generated, all groups have zero reward and zero gradient, but Dark Room's variance-profile criterion doesn't apply because there is no gradient at all. OC-GRPO provides a principled escape hatch via privileged-guided rollouts + IS correction, complementing CIGPO (today, per-turn variance injection) and ARMOR (Jul 28, off-policy anchor samples) as distinct mechanisms for handling the zero-signal failure regime.

## My Thoughts

<!-- Add your own notes here -->
