---
title: "LLM-as-a-Tutor: Policy-Aware Prompt Adaptation for Non-Verifiable RL"
authors: ["Yujin Kim", "Namgyu Ho", "Sangmin Hwang", "Joonkee Kim", "Yongjin Yang", "Sangmin Bae", "Seungone Kim", "Jaehun Jung", "Se-Young Yun", "Hwanjun Song"]
date: 2026-07-09
arxiv_id: "2607.04412v1"
url: "http://arxiv.org/abs/2607.04412v1"
score: 0.75
topics: [RL training, RLHF, RLAIF, reinforcement learning]
status: unread
---

# LLM-as-a-Tutor: Policy-Aware Prompt Adaptation for Non-Verifiable RL

## Summary

LLM-as-a-Tutor introduces prompt adaptation as a new axis of policy-awareness in non-verifiable RL: a single LLM acts as both examiner (pairwise-comparing rollouts to identify non-challenging prompts) and generator (appending atomic constraints to those prompts in an append-only, monotonically difficulty-raising design). This self-calibrating curriculum consistently outperforms both static-prompt and rubric-adapting baselines on three complex instruction-following benchmarks.

## Key Contributions

- Identifies a critical misalignment in non-verifiable RL: static training prompts become non-challenging as the policy improves, collapsing the LLM judge's discriminative power
- Proposes prompt adaptation as the missing axis of policy-awareness (complementary to rubric adaptation and rollout diversity)
- Append-only atomic constraint design ensures monotonic difficulty increase — prevents difficulty regression unlike free-form rewriting
- Single-model examiner+generator eliminates the need for a separate difficulty oracle or human-curated difficulty schedule

## Relevance

LLM-as-a-Tutor connects the adaptive curriculum thread (AdaPrefix-GRPO, ADS) to the non-verifiable RLHF setting. Where verifiable RL can use task success rate as a natural difficulty signal, non-verifiable instruction-following has no oracle — this paper shows that pairwise rollout comparison by an LLM judge can substitute. The self-calibrating framing is structurally related to Active-GRPO's imitate-or-reinforce switch (both adapt to policy capability rather than following a static schedule), but applied to prompt difficulty rather than reference quality.

## My Thoughts

<!-- Add your own notes here -->
