---
title: "Toward Training Superintelligent Software Agents through Self-Play SWE-RL"
authors: ["Yuxiang Wei", "Zhiqing Sun", "Emily McMilin", "Jonas Gehring", "David Zhang", "Gabriel Synnaeve", "Daniel Fried", "Lingming Zhang", "Sida Wang"]
date: 2025-12-21
arxiv_id: "2512.18552v1"
url: "http://arxiv.org/abs/2512.18552v1"
score: 0.78
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# Toward Training Superintelligent Software Agents through Self-Play SWE-RL

## Summary

Self-Play SWE-RL (SSR) trains software agents via RL in a self-play setting where a single LLM alternately injects and repairs software bugs of increasing complexity on sandboxed real-world repositories, with each bug formally specified by a test patch rather than natural language—removing any need for human-labeled issues or curated tests. This grounds the self-play loop in actual production codebases with zero human data assumptions. SSR achieves +10.4 and +7.8 absolute points on SWE-bench Verified and SWE-bench Pro, consistently outperforming the human-data baseline across the entire training trajectory.

## Key Contributions

- Self-play framework requiring only sandboxed repos with source code—no human labels, curated issues, or pre-written tests
- Test-patch specification for bugs: formal, verifiable signal that avoids ambiguous natural language issue descriptions
- Bug complexity curriculum emerges naturally from the self-play interaction without explicit scheduling
- Outperforms human-data baseline on SWE-bench Verified (+10.4) and SWE-bench Pro (+7.8) across full training

## Relevance

A compelling instance of agentic RL applied to the software engineering domain, directly relevant to the LLM agent and tool use keywords in the interest profile. SSR extends the self-play paradigm seen in StePPO and ProceedRL (step-level credit assignment) to a real-world agentic task with automated, formally verifiable reward signals.

## My Thoughts

<!-- Add your own notes here -->
