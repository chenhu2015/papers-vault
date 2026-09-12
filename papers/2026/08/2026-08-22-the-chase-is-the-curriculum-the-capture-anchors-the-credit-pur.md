---
title: "The Chase Is the Curriculum, the Capture Anchors the Credit: Pursuit-Evasion Self-Play for Zero-Data LLM Reasoning"
authors: ["Jing Yu", "Shengchao Chen", "Yiyun Tan"]
date: 2026-08-22
arxiv_id: "2608.21871v1"
url: "http://arxiv.org/abs/2608.21871v1"
score: 0.82
topics: [RL training, agentic RL, reward model, GRPO, RLAIF]
status: unread
---

# The Chase Is the Curriculum, the Capture Anchors the Credit: Pursuit-Evasion Self-Play for Zero-Data LLM Reasoning

## Summary

LURE frames zero-data curriculum generation as a pursuit-evasion game: an LLM evader positions tasks along each environment's difficulty axis to stay at the capture frontier (barely catchable), trained via a capture-frontier reward peaking at 50% solve rate; the pursuer earns capture-anchored dense process credit from monotone verifier progress group-normalized jointly with the terminal capture signal under a round-anchored KL for stable co-evolution. Across three verifiable reasoning environments and three backbone families, LURE outperforms advanced baselines under unified/specialist settings, achieving stronger aggregate OOD zero-shot accuracy across nine held-out benchmarks.

## Key Contributions

- Pursuit-evasion game formulation: curriculum task generation (evader) and RL policy improvement (pursuer) as a co-evolutionary game — unifies curriculum design with credit signal construction
- Capture-frontier reward: peaks at 50% solve rate, turning "barely catchable" into a learned positioning strategy rather than a hand-tuned rejection band — principled learnability signal
- Capture-anchored dense process credit: monotone verifier progress (step-level signal) group-normalized jointly with terminal capture (round-level signal) — avoids both sparse terminal-only and uncalibrated step-level rewards
- Round-anchored KL: stabilizes evader-pursuer co-evolution by constraining each round's policy shift relative to the round's starting point

## Relevance

LURE synthesizes two open threads from prior digests: (1) the learnability-calibrated curriculum thread (FrogNano from Sep 10, excluded by cap) — LURE provides the principled game-theoretic grounding for what FrogNano achieves heuristically; (2) the dense process credit thread (T1, TASPO, CRISP from Sep 11) — LURE's capture-anchored credit is the first dense credit signal whose calibration is itself a learned outcome of the training process rather than a design choice.

## My Thoughts

<!-- Add your own notes here -->
