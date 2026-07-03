---
title: "TAPO: Tool-Aware Policy Optimization via Credit Transfer for Multimodal Search Agents"
authors: ["Chengqi Dong", "Chuhuai Yue", "Hang He", "yandong liu", "Fenghe Tang", "S Kevin Zhou", "Xiaohan Wang", "Jiajun Chai", "Guojun Yin"]
date: 2026-06-04
arxiv_id: "2606.05784v1"
url: "http://arxiv.org/abs/2606.05784v1"
score: 0.88
topics: [agentic RL, tool use, multimodal, GRPO, VLM]
status: unread
---

# TAPO: Tool-Aware Policy Optimization via Credit Transfer for Multimodal Search Agents

## Summary

TAPO formally characterizes credit misassignment in GRPO for tool-augmented multimodal search agents: over 50% of failing trajectories have valuable tool-use steps wrongly penalized by uniform advantage broadcast. It exploits the parameter-determinism of information-acquisition tools to construct intra-batch counterfactual witnesses, then applies confidence-gated conservative advantage correction with no extra annotation, models, or sampling. Provides consistent plug-and-play improvements over GRPO, GSPO, and SAPO on multimodal search benchmarks.

## Key Contributions

- Empirical quantification of tool-use credit misassignment: >50% of failing trajectories and failing tool-use actions have structurally correctable credit errors under GRPO's uniform broadcast
- Parameter-determinism principle: similar tool call parameters define equivalent information-acquisition actions and should share comparable credit — formalizes when intra-batch counterfactual witnesses are valid
- Confidence-gated conservative advantage correction that compensates misassigned negative credit for tool-use steps in failing trajectories without extra sampling or models
- Plug-and-play compatibility with GRPO, GSPO, and SAPO; evaluated across multiple multimodal search benchmarks

## Relevance

TAPO fills the VLM credit assignment gap that searches 1 and 4 failed to find directly: it is specifically about credit for tool-use steps in multimodal (image+text) search agents, the intersection of the credit assignment thread and the VLM/multimodal topic axis. The parameter-determinism counterfactual (same tool parameters → same information acquisition → comparable credit) is CRAFT's (Jul 2) counterfactual token importance applied at the tool-call level rather than the token level — making TAPO the tool-use analogue of CRAFT within the same sibling/counterfactual credit family.

## My Thoughts

<!-- Add your own notes here -->
