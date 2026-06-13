---
title: "Reasoning Arena: Trace Tournaments When Verifiable Rewards Fall Short"
authors: ["Han Zhou", "Adam X. Yang", "Laurence Aitchison", "Anna Korhonen", "Albert Q. Jiang"]
date: 2026-06-13
arxiv_id: "2606.09380"
url: "https://arxiv.org/abs/2606.09380"
score: 0.82
topics: [reward model, GRPO, agentic RL, LLM agent]
status: unread
---

# Reasoning Arena: Trace Tournaments When Verifiable Rewards Fall Short

## Summary

RLVR training silently wastes compute when all sampled traces for a prompt receive identical rewards, collapsing advantage estimates to zero. Reasoning Arena addresses this by running pairwise LLM-as-judge trace tournaments when scalar verifiable rewards are uniform, converting zero-signal groups into a usable preference gradient without modifying the primary reward function.

## Key Contributions

- Characterizes zero-variance group problem: all-correct and all-wrong prompts both produce zero GRPO advantage, silently wasting rollout compute on uninformative prompts
- Trace tournament: pairwise LLM-as-judge comparisons over reasoning traces when scalar verifiable reward is uniform within a group
- Preference gradient derived from tournament outcomes is injected as a fallback signal, compatible with any RLVR setup
- Consistent improvement on math reasoning over standard RLVR baselines

## Relevance

This addresses the same zero-variance group failure mode as Query Recycling (Jun 11) but from the reward side rather than the sampling side: where Query Recycling dynamically resamples zero-variance groups from a pool, Reasoning Arena replaces the collapsed scalar reward with a preference signal for those groups. The two approaches are complementary and could be stacked.

## My Thoughts

<!-- Add your own notes here -->
