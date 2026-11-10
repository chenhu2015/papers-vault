---
title: "Addressing Over-Refusal in LLMs with Competing Rewards"
authors: ["Taeyoun Kim", "Aviral Kumar"]
date: 2026-06-30
arxiv_id: "2606.31748v1"
url: "https://arxiv.org/abs/2606.31748"
score: 0.80
topics: [reinforcement learning, RL training, reward model, GRPO, agentic RL]
status: unread
---

# Addressing Over-Refusal in LLMs with Competing Rewards

## Summary

SEAR addresses the safety-refusal trade-off as an adversarial optimization problem: a reasoning player explores unsafe strategies while an answer player ensures the final output is safe, both trained as one model within one chain-of-thought using dense process rewards. The model deliberately engages in harmful reasoning as exploration while reliably flipping to a safe answer, mitigating over-refusal without sacrificing safety and resisting direct reasoning-manipulation attacks — with process rewards found crucial for stable competing-objective optimization.

## Key Contributions

- Adversarial competing-reward framework: reasoning player explores unsafe paths; answer player enforces safe output — cast as competing objectives in one CoT
- Process rewards essential: dense process rewards required for stable optimization of competing objectives; outcome rewards alone fail
- Over-refusal mitigation: resolves ambiguity via unsafe reasoning exploration, allowing appropriate compliance on harmless prompts
- Attack resistance: model that knows unsafe reasoning is resistant to attacks that directly manipulate the reasoning chain toward harmful outputs

## Relevance

SEAR is adjacent to the MLLM refusal/calibration mini-cluster (RC-GRPO, Aerial-R1) but addresses the LLM safety domain rather than visual grounding. The competing-reward adversarial framework is a new mechanism for explicit refusal control via reward design — complementing the consistency-enforcement (Aerial-R1) and over-refusal penalty (RC-GRPO) approaches. The finding that process rewards are crucial for stable competing-objective optimization is relevant to the GRPO training dynamics thread.

## My Thoughts

<!-- Add your own notes here -->
