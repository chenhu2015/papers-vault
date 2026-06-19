---
title: "Reward as An Agent for Embodied World Models"
authors: ["Pu Li", "Zhigang Lin", "Qiang Wu", "Yongxuan Lv", "Fei Wang", "Shan You"]
date: 2026-06-19
arxiv_id: "2606.19990v1"
url: "http://arxiv.org/abs/2606.19990v1"
score: 0.77
topics: [GRPO, agentic RL, reward model, reward hacking, LLM agent]
status: unread
---

# Reward as An Agent for Embodied World Models

## Summary

Broader exploration in world-model RL is susceptible to reward hacking when the reward signal is imperfect, so existing methods stay conservatively near the training distribution. This paper introduces 'Reward as an Agent' — an agentic verifier that actively evaluates generated behaviors to provide robust reward signals under distribution shift — paired with DynDiff-GRPO, which diversifies action-space exploration via diffusion-based trajectory sampling beyond conservative rollout regimes. Together they enable substantially broader RL exploration grounded in robust verification, yielding accuracy gains across multiple open-source embodied world models.

## Key Contributions

- Diagnoses the core problem: lack of reliable verification (not exploration per se) is what makes broader exploration susceptible to reward hacking
- 'Reward as an Agent': the reward itself becomes an active agent that evaluates generated behaviors rather than a static scoring function, improving robustness under distribution shift
- DynDiff-GRPO: diffusion-based action-space diversification expands trajectory coverage without relying on the base policy's existing distribution
- Demonstrated across multiple open-source embodied world models with significant accuracy gains

## Relevance

Introduces a novel reward-as-agent framing that connects the reward hacking thread (HARVE Jun 8, PRIME Jun 17, Preference Instability Jun 18) with the exploration-exploitation problem in GRPO training. The claim that the bottleneck is *verification* rather than *exploration* itself is a clean inversion of the standard view. EnvRL (Jun 18) added environment dynamics as auxiliary objectives to improve the action policy's world model; this paper instead makes the *verifier* more robust, allowing the policy to explore more freely — two complementary solutions to the same conservative-rollout problem.

## My Thoughts

<!-- Add your own notes here -->
