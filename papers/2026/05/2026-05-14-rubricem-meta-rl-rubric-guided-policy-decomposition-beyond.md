---
title: "RubricEM: Meta-RL with Rubric-guided Policy Decomposition beyond Verifiable Rewards"
authors: ["Gaotang Li", "Bhavana Dalvi Mishra", "Zifeng Wang"]
date: 2026-05-14
arxiv_id: "2605.10899"
url: "https://arxiv.org/abs/2605.10899"
score: 0.89
topics: [agentic RL, LLM agent, tool use, reward model, RLHF]
status: unread
---

# RubricEM: Meta-RL with Rubric-guided Policy Decomposition beyond Verifiable Rewards

## Summary

RubricEM trains deep research agents — systems that plan, search, evaluate evidence, and synthesise long-form reports — where verifiable rewards are unavailable. It uses rubrics as a shared interface across hierarchical policy decomposition, LLM judge feedback, and agent memory, enabling staged policy execution and reuse of past-attempt experience. This approach extends RLVR to open-ended long-horizon tasks where outputs lack ground-truth answers and trajectories span many tool-augmented decisions.

## Key Contributions

- Reframes rubrics as a structural backbone for policy decomposition, judge feedback, and episodic memory — not just final-answer evaluators
- Stagewise policy decomposition breaks long-horizon agent trajectories into sub-policies aligned with rubric criteria
- Enables experience reuse: past attempts are integrated into agent memory via the shared rubric interface
- Addresses the core gap where RLVR fails: tasks with no ground-truth verifier (open-ended research synthesis)

## Relevance

This paper directly extends the agentic RL interest beyond the standard verifiable-reward setting. It complements the long-horizon agent work (BEACON, HCAPO, MiRA from May 10) by solving the harder case where no oracle exists — highly relevant to the LLM agent and tool use threads that have been building across the digest.

## My Thoughts

<!-- Add your own notes here -->
