---
title: "ProAS: A Progress-Aware Advantage Shaping Framework for Multi-Turn Agentic Reinforcement Learning"
authors: ["Bowen Ding", "Mingda Wan", "Yuhan Chen", "Jiyao Yuan", "Qi Zhu", "Futing Wang", "Heyuan Deng", "Fei Mi", "Lifeng Shang", "Tao Lin"]
date: 2026-10-13
arxiv_id: "2610.18683v2"
url: "http://arxiv.org/abs/2610.18683v2"
score: 0.84
topics: [agentic RL, GRPO, RL training, LLM agent]
status: unread
---

# ProAS: A Progress-Aware Advantage Shaping Framework for Multi-Turn Agentic Reinforcement Learning

## Summary

ProAS addresses GRPO's uniform credit assignment by constructing an Agentic Reference Graph (ARG) that tracks action dependencies across a trajectory, then applies two operations: Masking Unreasonable Incentives (MUI) suppresses positive advantage on structurally unwarranted actions, and Asymmetric Penalty Redistribution (APR) downweights deviating actions in failed trajectories. The plug-and-play framework achieves 91.9%/94.3% success on ALFWorld and 66.7%/70.8% on WebShop at 1.5B/7B scale with 2.44x convergence speedup, robustly generalizing across imperfect ARGs.

## Key Contributions

- Agentic Reference Graph (ARG) encodes action dependency structure for trajectory-level credit routing
- MUI: masks positive advantage on actions that are structurally unreasonable given trajectory context
- APR: asymmetrically redistributes penalties to actions that deviate most from reference trajectories
- 2.44x convergence speedup; robust to distilled/imperfect ARGs; plug-and-play into existing GRPO variants

## Relevance

Contributes to the step-credit cluster from the graph/structure angle, complementing AttnSR (attention-based), AdaStep (variance-based), C3 (confidence-based), and PEARL (pattern-memory-based). The ARG construction is the unique mechanism here — it goes beyond step-local credit to reason about cross-step dependency structure, which explains the convergence speedup.

## My Thoughts

<!-- Add your own notes here -->
