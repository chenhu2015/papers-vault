---
title: "PAIR: Prefix-Aware Internal Reward Model for Multi-Turn Agent Optimization"
authors: ["Wonjoong Kim", "Yeonjun In", "Sangwu Park", "Dongha Lee", "Chanyoung Park"]
date: 2026-08-15
arxiv_id: "2605.17877"
url: "http://arxiv.org/abs/2605.17877v2"
score: 0.78
topics: [agentic RL, reward model, LLM agent, GRPO, RL training, RLAIF]
status: unread
---

# PAIR: Prefix-Aware Internal Reward Model for Multi-Turn Agent Optimization

## Summary

PAIR uses the LLM's own hidden states as a lightweight dense step-level reward signal for GRPO training in multi-turn agent tasks, replacing costly external reward models. The key finding is that standard hidden-state probes degrade under prefix contamination in multi-step settings—biased toward coherence with a possibly corrupted prefix rather than grounded correctness—while attention-based features remain robust but underperform on clean inputs. PAIR's two-stage architecture (frozen hidden-state probe + corrective attention head) achieves the highest AUROC on contaminated trajectories at negligible inference cost.

## Key Contributions

- Identifies prefix contamination as a failure mode for hidden-state probes in multi-turn agent settings: probes track coherence with the (corrupted) prefix rather than grounded correctness
- Proposes two-stage PAIR: frozen hidden-state probe (belief-consistency) + lightweight attention head (grounded correctness correction)
- Provides dense step-level reward signals for GRPO training without external model calls, ground-truth dependencies, or full-trajectory rollouts
- Achieves highest AUROC on contaminated trajectories at negligible inference overhead

## Relevance

Prefix contamination in multi-step settings is a direct analog of SOD's cascading divergence amplification: both show that errors at step T propagate and corrupt supervision quality at step T+n. PAIR addresses this from the reward-signal side (corrupted signals → unreliable step credit), while SOD addresses it from the distillation side (corrupted trajectory states → unreliable teacher divergence). Together they define a two-sided contamination problem in multi-turn agentic RL. PAIR's internal-probe mechanism opens a new dimension in the vault's process reward model thread (VPS, VPRM, VERDICT): all prior methods use external verifiers or output-level signals; PAIR uses sub-model internal activations.

## My Thoughts

<!-- Add your own notes here -->
