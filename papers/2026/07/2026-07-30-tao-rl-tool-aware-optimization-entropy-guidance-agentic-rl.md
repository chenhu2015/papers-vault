---
title: "Tool-Aware Optimization with Entropy Guidance for Efficient Agentic Reinforcement Learning"
authors: ["Hongye Cao", "Nuo Yan", "Haoyuan Deng", "Ziwei Wang", "Tianpei Yang", "Jing Huo", "Yuyao Zhang", "Yang Gao"]
date: 2026-07-30
arxiv_id: "2606.03762v1"
url: "http://arxiv.org/abs/2606.03762v1"
score: 0.83
topics: [agentic RL, RL training, GRPO, tool use, LLM agent]
status: unread
---

# Tool-Aware Optimization with Entropy Guidance for Efficient Agentic Reinforcement Learning

## Summary

TAO-RL couples tool-aware trajectory filtering with entropy-guided exploration: at the data level it discards rollouts where all tool invocations fail and removes groups where all rollouts are either all-correct or all-incorrect (both degenerate advantage cases), then at the algorithmic level applies a tool-aware entropy bonus at post-tool-call tokens to encourage diverse reasoning at critical decision points. The filtering component directly addresses the GRPO all-fail/all-correct group pathology (Gap #16) from the tool-use angle, while the entropy bonus is complementary to STAPO's entropy gating (Jul 26). Evaluated on 7 challenging reasoning benchmarks across 3 model scales, demonstrating superiority over existing methods.

## Key Contributions

- Trajectory filtering criterion: discard groups where all tool calls fail AND groups where all rollouts are all-correct or all-incorrect — a group-filtering fix for Gap #16 applied to agentic tool-use settings
- Tool-aware entropy bonus that reshapes advantage at post-tool-call tokens, encouraging diverse reasoning paths at critical tool-interaction junctures
- Mutual reinforcement: filtering establishes clean training distribution; entropy bonus drives stronger exploration within that distribution
- Validated across 7 benchmarks and 3 model scales

## Relevance

TAO-RL's trajectory filtering condition (remove all-correct or all-incorrect groups) is a direct implementation of the group-filtering fix for Gap #16 (GRPO all-fail group amplification) that the Jul 29 digest noted as "still absent." It applies this fix specifically in the agentic tool-use setting, joining Dark Room (variance-profile), RDPO (quantile normalization), CIGPO (IG variance injection), and OC-GRPO (IS-corrected guided rollouts) as the fifth approach addressing different failure regimes of Gap #16. The entropy bonus at post-tool-call tokens is a new instantiation of entropy as a structural signal, complementary to STAPO's entropy gating and BPO's prefix branching.

## My Thoughts

<!-- Add your own notes here -->
