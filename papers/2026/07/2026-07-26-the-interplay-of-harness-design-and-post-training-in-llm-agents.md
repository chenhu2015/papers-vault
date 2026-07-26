---
title: "The Interplay of Harness Design and Post-Training in LLM Agents"
authors: ["Kyungmin Kim", "Youngbin Choi", "Seoyeon Lee", "Suhyeon Jun", "Dongwoo Kim", "Sangdon Park"]
date: 2026-07-26
arxiv_id: "2606.25447"
url: "https://arxiv.org/abs/2606.25447"
score: 0.87
topics: [agentic RL, LLM agent, tool use, RL training]
status: unread
---

# The Interplay of Harness Design and Post-Training in LLM Agents

## Summary

First systematic empirical study of how agent harness design — which tools are exposed, how they are described, and what auxiliary information accompanies each observation — interacts with post-training both in-distribution and under OOD task/tool environment shifts. Extends ALFWorld to treat harness as a controllable dimension and supports evaluation under tool/task distribution shift. Shows that harness-aware post-training substantially improves OOD adaptation, while minimal-design harnesses cause drastic performance drops under stronger tool environment shifts.

## Key Contributions

- Extended ALFWorld benchmark treating harness as a first-class design variable (tool exposure, descriptions, auxiliary observation content)
- Empirical evidence that harness choice is not neutral: the same post-training algorithm produces very different OOD adaptation depending on harness design
- Harness-aware post-training not only improves in-distribution performance but also enables robust OOD adaptation — a finding absent from prior agentic RL work
- Minimal-effort harnesses compound under tool environment shift, showing the harness is a load-bearing component of the RL learning signal

## Relevance

This paper directly closes Gap #15 (harness choice and RL trainability), which OpenForgeRL (Jul 24) opened and PATS (Jul 25) partially addressed from the training-context angle. OpenForgeRL showed the harness affects trainability; PATS showed dynamic context adaptation compensates; this paper shows that harness design systematically mediates OOD robustness and provides the first controlled study of the mechanism. The trio (OpenForgeRL → PATS → Harness Interplay) now fully characterizes how scaffold design interacts with post-training dynamics.

## My Thoughts

<!-- Add your own notes here -->
