---
title: "Taming Masked Diffusion Language Models via Consistency Trajectory Reinforcement Learning with Fewer Decoding Step"
authors: ["Jingyi Yang", "Guanxu Chen", "Xuhao Hu", "Jing Shao"]
date: 2025-09-28
arxiv_id: "2509.23924v1"
url: "http://arxiv.org/abs/2509.23924v1"
score: 0.80
topics: [diffusion language models, GRPO, RL training, reinforcement learning, agentic RL]
status: unread
---

# Taming Masked Diffusion Language Models via Consistency Trajectory Reinforcement Learning with Fewer Decoding Step

## Summary

CJ-GRPO identifies and addresses a fundamental training-inference inconsistency when applying GRPO to masked diffusion language models (MDLMs): MDLM decoding is non-causal and parallel, so rollout trajectories differ structurally from the optimization trajectories used in standard AR-derived GRPO, causing optimization errors from skip-step mismatches. Two decoding innovations (EOS Early Rejection and Ascending Step-Size scheduler) enable competitive full diffusion-style decoding with fewer steps, while CJ-GRPO enforces consistency between rollout and optimization trajectories to correct skip-step errors. Validated on LLaDA-8B-Instruct across math and planning benchmarks, extending the PACT+GDPO diffusion LM RL thread.

## Key Contributions

- Diagnosis of training-inference inconsistency in AR-derived GRPO applied to non-causal parallel MDLMs
- EOS Early Rejection (EOSER): suppresses premature EOS tokens to unlock full diffusion-style decoding
- Ascending Step-Size (ASS) scheduler: progressive step sizing for competitive fewer-step MDLM inference
- CJ-GRPO: rollout–optimization consistency constraint that corrects skip-step optimization errors in MDLM RL

## Relevance

Third entry in the diffusion LM RL thread (alongside PACT and GDPO). Where PACT introduced potential-anchored step credit for diffusion LMs and GDPO derived an ELBO-based GRPO objective, CJ-GRPO addresses the orthogonal problem of trajectory consistency—the rollout/optimization mismatch specific to masked (non-autoregressive) diffusion models. Together these three papers cover step credit, objective derivation, and trajectory consistency for diffusion LM RL.

## My Thoughts

<!-- Add your own notes here -->
