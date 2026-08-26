---
title: "Walk the Talk: Bridging the Reasoning-Action Gap for Thinking with Images via Multimodal Agentic Policy Optimization"
authors: ["Wenhao Yang", "Yu Xia", "Jinlong Huang", "Shiyin Lu", "Qing-Guo Chen", "Zhao Xu", "Weihua Luo", "Kaifu Zhang", "Yuchen Zhou", "Xiaobo Xia", "Yuanyu Wan", "Lijun Zhang", "Tat-Seng Chua"]
date: 2026-04-08
arxiv_id: "2604.06777v1"
url: "http://arxiv.org/abs/2604.06777v1"
score: 0.86
topics: [multimodal models, vision language models, agentic RL, VLM, tool use]
status: unread
---

# Walk the Talk: Bridging the Reasoning-Action Gap for Thinking with Images via Multimodal Agentic Policy Optimization

## Summary

MAPO addresses the reasoning-action discrepancy in multimodal RL: outcome rewards treat correct textual reasoning as success even when the model invokes visual tools imprecisely, accumulating noise over multi-turn trajectories. The fix: require the model to generate explicit descriptions of visual tool outputs, then couple semantic alignment between description and actual observation with the task reward. This advantage estimation reduces gradient variance theoretically, and MAPO outperforms prior methods on multiple visual reasoning benchmarks.

## Key Contributions

- Identifies and formalises the reasoning-action discrepancy: textual plausibility masks executive failure (imprecise visual tool invocation) under standard outcome-based RL
- MAPO mandates explicit textual descriptions for visual content obtained via tool usage during Multimodal Chain-of-Thought reasoning
- Novel advantage estimation coupling semantic alignment between model description and actual observation with task reward
- Theoretical result: the coupled advantage estimator inherently reduces gradient variance
- Empirical improvements across multiple visual reasoning benchmarks

## Relevance

Provides the missing link between the vault's multimodal RL thread (SPyCE Aug 23, GEAR Aug 23, EvolveVLA Aug 20) and the credit assignment thread (Credit Without Ground Truth Aug 21). MAPO's "reasoning-action discrepancy" is a specific manifestation of the Credit Without Ground Truth problem in multimodal settings: outcome reward treats the text reasoning trajectory as the locus of credit, ignoring whether the visual actions were causally responsible for success. MAPO's description-alignment reward is structurally analogous to GEAR's evidence-grounding reward but operates at the visual tool invocation level rather than long-context evidence overlap.

## My Thoughts

<!-- Add your own notes here -->
