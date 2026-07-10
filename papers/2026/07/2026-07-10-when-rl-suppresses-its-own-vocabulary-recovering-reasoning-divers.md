---
title: "When RL Suppresses Its Own Vocabulary: Recovering Reasoning Diversity in Puzzle-to-Math Transfer"
authors: ["Mayug Maniparambil", "Arjun Karuvally", "Terrence Sejnowski", "Fergal Reid"]
date: 2026-07-10
arxiv_id: "2605.29190v1"
url: "https://arxiv.org/abs/2605.29190"
score: 0.88
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# When RL Suppresses Its Own Vocabulary: Recovering Reasoning Diversity in Puzzle-to-Math Transfer

## Summary

Studies cross-domain transfer of reasoning skills in a 7B model trained exclusively on constraint-satisfaction puzzles (no math in SFT or RL stages), showing that puzzle-SFT builds a reasoning primitive vocabulary and GSPO then composes them into compute-verify chains—but suppresses exploratory primitives like hypothesize and backtrack. A novelty bonus using perplexity under the reference model rewards diverse correct rollouts, restoring exploratory primitives and lifting hard-math performance from 16% to 36% pass@32. The reasoning primitive-level framework (9-class span classifier + motif extraction) provides a new lens for tracking how RLVR reshapes chain-of-thought structure across training stages and domains.

## Key Contributions

- Puzzle-to-math cross-domain transfer recipe (SFT on puzzles → GSPO → novelty-bonus GSPO) raises hard-math ceiling from 16% to 36% pass@32 with zero math in post-training data
- 9-class reasoning primitive span classifier + motif extraction framework for mechanistically tracking CoT evolution across training stages
- Novelty bonus: perplexity under the reference model as a diversity signal; rewards diverse-but-correct rollouts; restores suppressed exploratory primitives (hypothesize, backtrack)
- Finding: vanilla GSPO composes primitives into compute-verify chains (+6pp) but simultaneously suppresses exploratory backtracking (+7pp recovered by novelty bonus)

## Relevance

Directly advances the diversity-in-RLVR thread: "When RL Suppresses Its Own Vocabulary" identifies a seventh RLVR failure mode — *exploratory primitive suppression* — where standard RL collapses the model's behavioral vocabulary to the compute-verify mode, structurally complementing Reaching Beyond the Mode's answer-distribution collapse (output side) and TA-GRPO's question-diversity collapse (input side). The novelty bonus (perplexity-based) is also the most practical implementation of the diversity reward concept from search 1 today, which returned empty at the title level — this paper is the state of the art on that thread.

## My Thoughts

<!-- Add your own notes here -->
