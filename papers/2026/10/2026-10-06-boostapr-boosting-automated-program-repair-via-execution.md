---
title: "BoostAPR: Boosting Automated Program Repair via Execution-Grounded Reinforcement Learning with Dual Reward Models"
authors: ["Yuanhao Li", "Hongbo Wang", "Xiaotang Shang", "Xunzhu Tang", "Yiming Cao", "Xuhong Chen"]
date: 2026-10-06
arxiv_id: "2605.09134v4"
url: "https://arxiv.org/abs/2605.09134"
score: 0.87
topics: [agentic RL, RL training, reinforcement learning]
status: unread
---

# BoostAPR: Boosting Automated Program Repair via Execution-Grounded Reinforcement Learning with Dual Reward Models

## Summary

BoostAPR addresses sparse execution feedback in program repair RL by training dual reward models: a sequence-level correctness assessor and a line-level credit allocator derived from execution outcomes. PPO optimization uses the line-level model to redistribute rewards to critical edit regions at an intermediate granularity naturally suited to code changes. Evaluated on SWE-Gym and four benchmarks, achieving 40.7% on SWE-bench Verified (+22.9pp over base model) with strong cross-language generalization.

## Key Contributions

- Dual reward model architecture: sequence-level outcome assessor + line-level credit allocator, both trained from execution outcomes
- Line-level credit redistribution via PPO at an intermediate granularity between token and trajectory
- Three-stage training pipeline: SFT on execution-verified demonstrations → reward model training → PPO with line-level credit
- 40.7% SWE-bench Verified, 24.8% Defects4J (Python→Java transfer), 84.5% HumanEval-Java, 95.0% QuixBugs

## Relevance

BoostAPR extends the DepGPO execution-trace thread to automated program repair: where DepGPO uses command dependency graphs extracted from execution traces to assign backward credit, BoostAPR trains a separate line-level credit allocator from execution outcomes. The key difference is that BoostAPR's credit allocator is a learned model (trained from execution feedback), while DepGPO's dependency graph is automatically derived from program structure. Both operate at an intermediate granularity (line/terminal-command) between token and trajectory. BoostAPR's dual-model design is also related to ProVer's two-phase structure (judge proposes pivot, outcome verifies), but applied to code repair with a learned rather than judge-based first stage.

## My Thoughts

<!-- Add your own notes here -->
