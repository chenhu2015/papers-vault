---
title: "Expected Reasoning-Step Return Unifies On-Policy Learning from Rewards and Teachers"
authors: ["Qiangqiang He", "Jin Li"]
date: 2026-09-26
arxiv_id: "2609.32674"
url: "https://arxiv.org/abs/2609.32674"
score: 0.85
topics: [agentic RL, RL training, reward model, RLAIF]
status: unread
---

# Expected Reasoning-Step Return Unifies On-Policy Learning from Rewards and Teachers

## Summary

ERSR (Expected Reasoning-Step Return) treats semantic reasoning steps as macro-actions and uses Monte Carlo student-policy rollouts to place both RL rewards and teacher distillation signals in a common return space for step-level comparison. This reveals an outcome-dependent asymmetry: student actions are more beneficial than teacher replacements on successful trajectories, while teacher replacements are more beneficial on failed ones. R²OPL operationalises this by reinforcing student reasoning on successes and distilling teacher guidance on failures, using group success rate for difficulty scaling and student-probe gains for per-step modulation.

## Key Contributions

- ERSR metric: MC rollouts from the student policy estimate expected final task reward for student vs. teacher actions at each reasoning step, placing both in a common return space
- Asymmetry finding: student beats teacher on success trajectories; teacher beats student on failure trajectories — provides a principled switch criterion
- R²OPL algorithm: reinforces student reasoning on successful trajectories, distills teacher signals on failed ones; group success rate for difficulty scaling
- Student-probe gains: a step-level signal that tracks whether a step's answer shifts toward the correct answer, used for per-step modulation weight

## Relevance

Directly extends the step-credit thread — provides a principled, jointly-estimated framework for deciding when to apply RL vs. distillation credit at each reasoning step. This generalises the granularity-mixing problem explored by GACA (which mixes episode vs. step credit based on NLL criticality) to the orthogonal axis of reward vs. teacher credit. The ERSR framework could compose with BoT-GRPO (which integrates token-level process rewards into GRPO) by using ERSR-guided switching to decide which trajectory segments benefit from token-level vs. outcome-level credit.

## My Thoughts

<!-- Add your own notes here -->
