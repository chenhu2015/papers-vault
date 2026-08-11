---
title: "SHAPE: Stage-aware Hierarchical Advantage via Potential Estimation for LLM Reasoning"
authors: ["Zhengyang Ai", "Zikang Shan", "Xiaodong Ai", "Jingxian Tang", "Hangkai Hu", "Pinyan Lu"]
date: 2026-04-08
arxiv_id: "2604.06636"
url: "https://arxiv.org/abs/2604.06636"
score: 0.83
topics: [RL training, GRPO, reward model, agentic RL]
status: unread
---

# SHAPE: Stage-aware Hierarchical Advantage via Potential Estimation for LLM Reasoning

## Summary

SHAPE formalizes LLM reasoning as a trajectory through empirical solvability states, assigning segment-level credit via a potential-function-based advantage that prioritizes breakthroughs in low-potential states, and token-level credit via entropy-driven redistribution. The hierarchical mechanism directly synthesizes the TD/potential approach (segment level) with entropy gating (token level), achieving 3% average accuracy gain with 30% reduced token consumption across three base models and five benchmarks.

## Key Contributions

- Solvability state space formalism: each reasoning position maps to an empirical solvability potential, converting sparse outcome rewards into dense potential differences
- Segment-level stage-aware advantage function: prioritizes credit for efficient breakthroughs in low-potential (hard) states, penalizing verbosity that increases tokens without potential gain
- Token-level entropy-driven redistribution: within each segment, entropy at each position redistributes credit to sharpen execution signals on decisive tokens
- 3% average accuracy gain with 30% token reduction — the dual improvement confirms that verbosity and uncertainty are directly coupled via the entropy signal

## Relevance

SHAPE is the most direct instantiation of Gap #6 (TD credit + entropy gating synthesis) found in the vault to date: the segment-level potential function acts as a state-value estimate (analogous to Gated-BEPO's empirical Bellman backup but via solvability rather than rollout graph), and the token-level entropy redistribution is exactly the entropy gating signal from DASH and CSCR applied hierarchically. Unlike Gated-BEPO (which applies TD backup at the step level) or DASH (which applies entropy gating at the token level independently), SHAPE explicitly combines both signals in a hierarchical structure — potential estimation determines segment-level priority, entropy redistribution determines token-level allocation within segments.

## My Thoughts

<!-- Add your own notes here -->
