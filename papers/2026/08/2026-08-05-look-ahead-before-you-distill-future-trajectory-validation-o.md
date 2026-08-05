---
title: "Look Ahead Before You Distill: Future Trajectory Validation of Teacher Guidance for Agentic On-Policy Distillation"
authors: ["Chishui Chen", "Yaoyou Fan", "Te Sun", "Yi Yang", "Chenghao Sun", "Delin Mao", "Hongbo Qiao", "Zuowei Zhang", "Junxi Wang", "Chenxing Sun", "Yangen Hu", "Lu Pan", "Xuyang Liu", "Linfeng Zhang"]
date: 2026-08-05
arxiv_id: "2608.01953"
url: "https://arxiv.org/abs/2608.01953"
score: 0.76
topics: [agentic RL, LLM agent, RL training, reinforcement learning]
status: unread
---

# Look Ahead Before You Distill: Future Trajectory Validation of Teacher Guidance for Agentic On-Policy Distillation

## Summary

FutureBridge-OPD (FTB) addresses the accumulating-deviation problem in agentic on-policy distillation: as student trajectories diverge from teacher distribution in multi-turn tasks, high-disagreement states are promising supervision targets but teacher guidance at those states may be counter-productive. FTB executes a short teacher bridge at each high-disagreement state and measures whether the resulting student continuation increases the density of positive distillation signals, validating guidance before applying it. On ALFWorld, WebShop, and ScienceWorld (Qwen3-32B teacher → Qwen3-1.7B student), FTB outperforms vanilla OPD by 16.6 points and TCOD by 7.6 points on average.

## Key Contributions

- Diagnosis: quantitative analysis showing that high teacher-student disagreement states offer promising supervision opportunities, but their benefit depends on downstream trajectory effects
- FutureBridge: a short teacher bridge at high-disagreement states, followed by student continuation to measure whether the bridge increases positive distillation signal density
- Practical gate: apply teacher guidance only when the bridge improves downstream signal; skip or reduce supervision otherwise
- 16.6pt improvement over vanilla OPD and 7.6pt over TCOD across ALFWorld+WebShop+ScienceWorld

## Relevance

FutureBridge-OPD closes a specific gap in the agentic OPD literature that Guided-OPD (Aug 1) partially addressed: while Guided-OPD decays teacher intervention as training progresses, it does not validate *which* states benefit from teacher guidance. FTB's validation mechanism is complementary to PCSD's persistence weights and ADRS's TVA gate — all three are methods for determining *when* teacher supervision is beneficial in agentic RL, but at different granularities: PCSD at the token level (temporal persistence), ADRS at the group level (confidence-return correlation), and FTB at the trajectory level (downstream continuation density).

## My Thoughts

<!-- Add your own notes here -->
