---
title: "DISA: Offline Importance Sampling for Distribution-Matching LLM-RL"
authors: ["Shaobo Wang", "Yujie Chen", "Yafeng Sun", "Wenjie Qiu", "Zhihui Xie", "Sihang Li", "Yucheng Li", "Huiqiang Jiang", "Xingzhang Ren", "Xuming Hu", "Dayiheng Liu", "Linfeng Zhang"]
date: 2026-05-17
arxiv_id: "2605.17295"
url: "https://arxiv.org/abs/2605.17295"
score: 0.78
topics: [RL training, GRPO, reward model, reinforcement learning, RLAIF]
status: unread
---

# DISA: Offline Importance Sampling for Distribution-Matching LLM-RL

## Summary

DISA decouples partition function estimation from policy optimization in distribution-matching RL: unlike methods that learn the partition function online alongside the policy, DISA estimates it via importance sampling from offline proposal trajectories and freezes it before RL begins, preventing calibration errors from distorting policy gradients. On 6 math and 3 code benchmarks DISA matches FlowRL and outperforms GRPO/GSPO while retaining substantially more solution strategy diversity as confirmed by LLM-as-judge evaluation.

## Key Contributions

- Decoupled importance-sampled partition function: estimated offline from proposal trajectories, frozen before policy optimization begins
- Formal separation of partition function estimation from policy learning in data, gradients, loss, and diagnostics — enables independent quality diagnosis
- Retains strategy-level diversity better than GRPO/GSPO at matched accuracy levels
- +13.8 Mean@8 over LoRASFT on the same offline proposal trajectories

## Relevance

DISA addresses the solution diversity gap the vault has tracked since T1 (Jul 12): standard GRPO collapses to single solution modes, losing the diversity that T1 showed enables test-time scaling. DISA provides a theoretically grounded mechanism to preserve it: by matching the full distribution of rewarded solutions (not maximizing one), it retains the solution-space breadth that enables parallel sampling TTS. The offline decoupling is complementary to RL^V's generative verifier (Jul 12): RL^V uses the verifier to select among diverse solutions at test time; DISA ensures those diverse solutions exist in the first place via training-time distribution matching.

## My Thoughts

<!-- Add your own notes here -->
