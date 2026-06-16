---
title: "ExpRL: Exploratory RL for LLM Mid-Training"
authors: ["Violet Xiang", "Amrith Setlur", "Chase Blagden", "Nick Haber", "Aviral Kumar"]
date: 2026-06-16
arxiv_id: "2606.17024v1"
url: "http://arxiv.org/abs/2606.17024v1"
score: 0.85
topics: [RLHF, reward model, LLM agent, agentic RL, RL training]
status: unread
---

# ExpRL: Exploratory RL for LLM Mid-Training

## Summary

ExpRL proposes RL-based mid-training using large human-written QA corpora, where reference solutions are hidden from the policy and used only to construct problem-specific grading rubrics for an LLM judge. The judge compares on-policy reasoning traces against the reference and assigns outcome- or process-level dense rewards, reinforcing partial progress and useful intermediate reductions that sparse final-answer rewards miss. ExpRL outperforms SFT, sparse-reward GRPO, and self-distillation as a priming stage before subsequent sparse-reward RL on challenging math tasks.

## Key Contributions

- Uses LLM judge as dense reward signal from hidden reference solutions (references as reward scaffolds, not imitation targets)
- Process-level rewards credit partial progress, intermediate reductions, and productive reasoning that sparse outcome rewards discard
- Establishes RL mid-training as superior to SFT and self-distillation for priming sparse-reward RL
- Mixed-domain experiments extend results beyond math, suggesting generality of the reference-as-scaffold paradigm

## Relevance

This paper directly addresses the LLM-as-judge angle for reward signal generation — a fresh thread that connects the RLHF interest-profile keyword with the reward model quality work (PRISM, Distributional PRMs from Jun 13–14). Where PRISM fixed training-time step bias in PRMs and Distributional PRMs calibrated inference-time scores, ExpRL replaces the PRM altogether with a rubric-generating LLM judge, sidestepping the data imbalance problem at the cost of judge inference overhead.

## My Thoughts

<!-- Add your own notes here -->
