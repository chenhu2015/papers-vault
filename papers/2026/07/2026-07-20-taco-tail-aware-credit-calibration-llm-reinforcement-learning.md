---
title: "When Implausible Tokens Get Reinforced: Tail-Aware Credit Calibration for LLM Reinforcement Learning"
authors: ["Xiuyi Lou", "Zicheng Xu", "Yu-Neng Chuang", "Hoang Anh Duy Le", "Zhaozhuo Xu", "Guanchu Wang", "Vladimir Braverman"]
date: 2026-07-08
arxiv_id: "2607.07976"
url: "http://arxiv.org/abs/2607.07976v1"
score: 0.86
topics: [GRPO, reward model, RL training, reinforcement learning]
status: unread
---

# When Implausible Tokens Get Reinforced: Tail-Aware Credit Calibration for LLM Reinforcement Learning

## Summary

TACO identifies Positive-Credit Contamination: in GRPO-style training, low-probability tail tokens that are contextually erroneous receive the same positive credit as plausible tokens when the trajectory is correct, indiscriminately reinforcing flawed reasoning. It computes a per-token tail-risk score using local generation context—distinguishing unexpected rarity from useful uncertainty-driven exploration—and uses this score to calibrate (reduce but not zero) positive credit for risky tokens, so recurring useful rare patterns still accumulate reinforcement while noise is suppressed. Tested on 3 LLMs and 8 benchmarks, TACO improves training stability and supports sustained performance in long-horizon RL over GRPO baselines.

## Key Contributions

- Identifies Positive-Credit Contamination as a distinct failure mode: correct-trajectory positive credit is uniformly broadcast to all tokens, including low-probability tail tokens that are contextually wrong
- Per-token tail-risk score using local generation context that distinguishes erroneous rarity from uncertainty-driven exploration (useful rare patterns vs. noise)
- Calibrated credit assignment: suppresses positive updates for high-risk tokens without zeroing gradients, allowing useful rare patterns to accumulate reinforcement over time
- 3 LLMs × 8 benchmarks evaluation showing improved training stability and sustained long-horizon performance gains

## Relevance

TACO extends the token-level credit assignment thread (EGRSD, Prune-OPD) with a new axis: not just *which* tokens to weight by entropy or truncation, but how to calibrate *positive credit* for tokens that are low-probability but contextually erroneous. While EGRSD gates uncertain tokens downward in OPD and RL-ZVP gates uncertain tokens upward for zero-variance prompts, TACO gates tail-risky tokens downward in positive-credit trajectories — a complementary mechanism that addresses contamination rather than coverage.

## My Thoughts

<!-- Add your own notes here -->
