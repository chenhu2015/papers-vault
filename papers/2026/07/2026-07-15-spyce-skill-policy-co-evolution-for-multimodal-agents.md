---
title: "SPyCE: Skill-Policy Co-evolution for Multimodal Agents"
authors: ["Ru Zhang", "Weijie Qiu"]
date: 2026-07-15
arxiv_id: "2607.13854v2"
url: "http://arxiv.org/abs/2607.13854v2"
score: 0.85
topics: [agentic RL, multimodal models, tool use, LLM agent]
status: unread
---

# SPyCE: Skill-Policy Co-evolution for Multimodal Agents

## Summary

SPyCE addresses the gap between memory-based (static retrieval) and reward-based (scalar signal) approaches to reusable skill learning in multimodal agentic RL by distilling trajectories into a hierarchical skill library (execution skills for local visual operations; workflow skills for high-level tool-use priors) that co-evolves with the policy during training. The closed loop means improved policies yield better distilled skills and evolving skills provide stronger rollout priors for policy training. Evaluated across 8 benchmarks, SPyCE consistently outperforms both RL-based and memory-based baselines, with ablations confirming both hierarchy levels and the co-evolution mechanism are necessary.

## Key Contributions

- Hierarchical skill library with two levels: execution skills (local visual operations, e.g. click, scroll, extract) and workflow skills (high-level tool-use orchestration priors)
- Co-evolution training loop: policy rollouts distilled into skills → skills condition policy rollouts → improved rollouts refine skills; no static skill store
- Demonstrates that RL-based methods (scalar reward, no skill reuse) and memory-based methods (static retrieval, no policy update) are both insufficient; joint skill-policy optimization needed
- SOTA across 8 multimodal agent benchmarks; both hierarchy levels and co-evolution mechanism ablate as individually critical

## Relevance

Directly extends the vault's agentic tool-use RL thread (SkillGate Aug 20, SSPO Aug 22) to multimodal agents: where SkillGate addressed selector credit starvation with disjoint credit channels, SPyCE addresses skill reuse by co-evolving the skill library with the policy rather than treating skills as static retrievals or frozen tool APIs. The workflow-skill level is structurally similar to MileGPO's milestone inference, but operates at the planning-prior level rather than the credit-signal level.

## My Thoughts

<!-- Add your own notes here -->
