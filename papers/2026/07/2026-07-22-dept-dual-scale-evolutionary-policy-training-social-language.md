---
title: "Breaking the Impasse: Dual-Scale Evolutionary Policy Training for Social Language Agents"
authors: ["Minzheng Wang", "Run Luo", "Yanbo Wang", "Zichen Liu", "Yuqiao Tan", "Tao Tan", "Xu Nan", "Yinhe Zheng", "Wenji Mao"]
date: 2026-05-09
arxiv_id: "2605.08721"
url: "https://arxiv.org/abs/2605.08721"
score: 0.77
topics: [agentic RL, RLHF, RLAIF, LLM agent, reinforcement learning]
status: unread
---

# Breaking the Impasse: Dual-Scale Evolutionary Policy Training for Social Language Agents

## Summary

DEPT identifies the evolution impasse failure mode in self-play RLVR for open-ended social language games: agents converge to homogenized behaviors, match outcomes become deterministic, and gradient signals collapse, halting further policy improvement. It detects impasse by monitoring dual-scale value baseline divergence (short-horizon vs. long-horizon value estimates) alongside match entropy, then activates asymmetric advantage reshaping to restore gradient signals and enforce strategic exploration. Experiments across multiple social language games show DEPT sustains policy evolution and outperforms strong baselines that suffer from impasse-induced degeneration.

## Key Contributions

- Characterization of the evolution impasse failure mode: homogenized self-play strategies → deterministic match outcomes → gradient collapse in RLVR
- Dual-scale value baseline divergence as a real-time diagnostic signal: divergence between short-horizon and long-horizon value estimates detects when policy dynamics have stagnated
- Match entropy as a complementary impasse signal: low entropy confirms deterministic outcome distribution
- Asymmetric advantage reshaping: dynamically modulates the optimization landscape upon impasse detection to restore diverse gradient signals and strategic diversity

## Relevance

Directly addresses the confirmed open gap on self-play/adversarial training for reasoning LLMs (carried forward since Jul 13). DEPT is the first paper in the vault to characterize the evolution impasse failure mode in RLVR self-play and propose a detection + intervention mechanism. The asymmetric advantage reshaping connects to DISPO's asymmetric IS clipping — both papers intervene differently on gradient signals depending on observed outcome quality, though at different granularities (self-play policy divergence vs. response-level correctness). The dual-scale value baseline divergence as a diagnostic is structurally analogous to CoBA-RL's Capability-Oriented Value function tracking training gain: both monitor the *rate of change* of policy value rather than just its magnitude.

## My Thoughts

<!-- Add your own notes here -->
