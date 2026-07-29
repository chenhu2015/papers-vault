---
title: "CIGPO: Contextual Information-Gain Policy Optimization for Multi-Turn Evidence-Reading LLM Agents"
authors: ["Hao Dou"]
date: 2026-06-26
arxiv_id: "2607.16244"
url: "https://arxiv.org/abs/2607.16244"
score: 0.87
topics: [agentic RL, GRPO, reward model, LLM agent, RL training]
status: unread
---

# CIGPO: Contextual Information-Gain Policy Optimization for Multi-Turn Evidence-Reading LLM Agents

## Summary

CIGPO addresses GRPO reward variance collapse in multi-turn evidence-reading agents by injecting per-turn information-gain rewards, using the marginal increase in a frozen reference model's log-likelihood of the ground-truth answer as a dense per-turn signal. The variance-injection strategy prevents zero-advantage lock-in—where all sampled trajectories receive identical minimum penalties and group-relative advantages vanish—by preserving within-group reward variation throughout training. On HotpotQA with Qwen2.5-3B-Instruct, CIGPO reaches F1 0.518 from a 0.252 base (+105%), versus 0.430 for the best GRPO checkpoint and 0.000 for the final collapsed GRPO checkpoint.

## Key Contributions

- **Zero-advantage lock-in mechanism diagnosed**: all sampled trajectories receive minimum format penalty → group-relative advantage collapses to zero → policy gradient loss becomes zero → optimization deadlock
- **Per-turn IG signal**: marginal increase in frozen reference log-likelihood of ground truth as per-turn reward; equivalent to measuring how much each turn's retrieved evidence shifts the reference model toward the correct answer
- **Separate normalization**: IG and F1 rewards normalized independently to prevent scale mismatch; IG-weight curriculum applied during training
- **+105% F1 gain on HotpotQA** (0.252→0.518) preventing GRPO variance collapse that reduces vanilla GRPO from 0.430 to 0.000 by end of training

## Relevance

Directly addresses Gap #16 (GRPO all-fail group amplification) from Dark Room (Jul 25): the zero-advantage lock-in described here is the multi-turn format-penalty instantiation of Dark Room's all-fail group pathology, where std normalization under uniform group outcomes collapses the advantage to zero regardless of reward scale. The IG signal is a per-turn variant of Progress Advantage's log π_RL/π_ref (Jul 26): it measures the reference model's log-probability increase per turn rather than the final log-ratio, providing a finer-grained version of the same optimal advantage signal applied inside GRPO's normalization rather than after it.

## My Thoughts

<!-- Add your own notes here -->
