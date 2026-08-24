# Awesome-Scaling-LRM-Beyond-Human-Supervision

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths?style=social)](https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths)
[![GitHub](https://img.shields.io/badge/-github-teal?logo=github)](https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths)
[![arXiv](https://img.shields.io/badge/Survey-Coming_Soon-b31b1b.svg)](#-citation)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths/pulls)

> Companion repository for the survey  
> **Scaling Large Reasoning Models beyond Human Supervision: A Path toward Superintelligence**

A curated list of papers, code, and benchmarks from the survey, organized by the **receding-supervision ladder (L0 → L4)**.

---

## 📢 News

- **2026-08** Expanded coverage to survey papers across **L0–L4**, and added **Figure 1** (receding-supervision ladder).
- Contributions welcome — place each work under its **primary** ladder level.

---

## 📖 Figure 1 · Receding-Supervision Ladder

<p align="center">
  <img src="assets/fig1_ladder.png" width="100%" alt="Figure 1: The receding-supervision ladder from L0 to L4"/>
</p>

<p align="center"><em>Figure 1 from the survey: as human supervision recedes, autonomy of the learning loop increases (L0 → L4).</em></p>

| Level | Reward | Experience | Humans still govern |
|:-----:|--------|------------|---------------------|
| **L0** | human (per instance) | human | judgment of every instance |
| **L1** | reusable verifier | human | standard of judgment |
| **L2** | **human-free** | human | supply of experience only |
| **L3** | human-free | **human-free** | only initial seeds |
| **L4** | human-free | human-free | **nothing** — closed co-evolution |

<p align="center">
  <img src="assets/fig_landscape.png" width="100%" alt="Evolutionary landscape of milestones along L0–L4"/>
</p>

<p align="center"><em>Survey landscape figure: representative milestones along the five-level progression.</em></p>

---

## 📑 Table of Contents

- [L0 · Per-instance Supervision](#l0--per-instance-supervision-reference)
- [L1 · Verifier-based Supervision](#l1--verifier-based-supervision)
- [L2 · Human-free Reward](#l2--human-free-reward)
- [L3 · Human-free Experience](#l3--human-free-experience)
- [L4 · Autonomous Co-evolution](#l4--autonomous-co-evolution)
- [Evaluation](#evaluation-datasets-and-benchmarks)
- [Future Directions](#challenges-and-future-directions)
- [Contributing](#-contributing)
- [Citation](#-citation)

---

## L0 · Per-instance Supervision (Reference)

> Humans judge **every** training instance (answers or preferences). Starting point of the ladder.

- DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models
  <a href="https://arxiv.org/pdf/2402.03300?"><img src="https://img.shields.io/badge/arxiv-2402.03300-silver" alt="Paper"></a>
  <a href="https://github.com/deepseek-ai/DeepSeek-Math"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/deepseek-ai/DeepSeek-Math"><img src="https://img.shields.io/github/stars/deepseek-ai/DeepSeek-Math" alt="stars"></a>
- DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning
  <a href="https://arxiv.org/pdf/2501.12948?"><img src="https://img.shields.io/badge/arxiv-2501.12948-silver" alt="Paper"></a>
  <a href="https://github.com/deepseek-ai/DeepSeek-R1"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/deepseek-ai/DeepSeek-R1"><img src="https://img.shields.io/github/stars/deepseek-ai/DeepSeek-R1" alt="stars"></a>
- Training Language Models to Follow Instructions with Human Feedback (InstructGPT / RLHF)
  <a href="https://arxiv.org/pdf/2203.02155?"><img src="https://img.shields.io/badge/arxiv-2203.02155-silver" alt="Paper"></a>
- Let's Verify Step by Step (MATH / process supervision)
  <a href="https://arxiv.org/pdf/2305.20050?"><img src="https://img.shields.io/badge/arxiv-2305.20050-silver" alt="Paper"></a>
  <a href="https://github.com/openai/prm800k"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/openai/prm800k"><img src="https://img.shields.io/github/stars/openai/prm800k" alt="stars"></a>
- Welcome to the Era of Experience *(Silver & Sutton; experience-era thesis)*

---

## L1 · Verifier-based Supervision

> Humans no longer label every rollout; they provide a **reusable verifier** (LLM judge / reward model). Tasks & environments remain human-supplied.

### LLM as a Verifier

- Crossing the Reward Bridge: Expanding RL with Verifiable Rewards Across Diverse Domains
  <a href="https://arxiv.org/pdf/2503.23829?"><img src="https://img.shields.io/badge/arxiv-2503.23829-silver" alt="Paper"></a>
  <a href="https://huggingface.co/collections/virtuoussy/rlvr-67ea349b086e3511f86d1c1f"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Continuous Self-Improvement of LLMs by Test-time Training with Verifier-Driven Sample Selection (VDS-TTT)
  <a href="https://arxiv.org/pdf/2505.19475?"><img src="https://img.shields.io/badge/arxiv-2505.19475-silver" alt="Paper"></a>
- SSR-Zero: Simple Self-Rewarding Reinforcement Learning for Machine Translation
  <a href="https://arxiv.org/pdf/2505.16637?"><img src="https://img.shields.io/badge/arxiv-2505.16637-silver" alt="Paper"></a>
  <a href="https://github.com/Kelaxon/SSR-Zero"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Kelaxon/SSR-Zero"><img src="https://img.shields.io/github/stars/Kelaxon/SSR-Zero" alt="stars"></a>
  <a href="https://huggingface.co/collections/wjyccs/ssr-zero-6830189a8d2fd6fc7ce6fba6"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Omni-Thinker: Scaling Cross-Domain Generalization via Multi-Task RL with Hybrid Rewards
  <a href="https://arxiv.org/pdf/2507.14783?"><img src="https://img.shields.io/badge/arxiv-2507.14783-silver" alt="Paper"></a>
- Learning to Reason for Factuality
  <a href="https://arxiv.org/pdf/2508.05618?"><img src="https://img.shields.io/badge/arxiv-2508.05618-silver" alt="Paper"></a>
- Checklists Are Better Than Reward Models for Aligning Language Models (RLCF)
  <a href="https://arxiv.org/pdf/2507.18624?"><img src="https://img.shields.io/badge/arxiv-2507.18624-silver" alt="Paper"></a>
  <a href="https://github.com/viswavi/RLCF"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/viswavi/RLCF"><img src="https://img.shields.io/github/stars/viswavi/RLCF" alt="stars"></a>
- Rubrics as Rewards: Reinforcement Learning Beyond Verifiable Domains (RaR)
  <a href="https://arxiv.org/pdf/2507.17746?"><img src="https://img.shields.io/badge/arxiv-2507.17746-silver" alt="Paper"></a>
- Reinforcement Learning with Rubric Anchors (Rubicon)
  <a href="https://arxiv.org/pdf/2508.12790?"><img src="https://img.shields.io/badge/arxiv-2508.12790-silver" alt="Paper"></a>
- Breaking the Exploration Bottleneck: Rubric-Scaffolded RL (RuscaRL)
  <a href="https://arxiv.org/pdf/2508.16949?"><img src="https://img.shields.io/badge/arxiv-2508.16949-silver" alt="Paper"></a>
  <a href="https://github.com/IANNXANG/RuscaRL"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/IANNXANG/RuscaRL"><img src="https://img.shields.io/github/stars/IANNXANG/RuscaRL" alt="stars"></a>
- Kimi K2: Open Agentic Intelligence
  <a href="https://arxiv.org/pdf/2507.20534?"><img src="https://img.shields.io/badge/arxiv-2507.20534-silver" alt="Paper"></a>
  <a href="https://github.com/MoonshotAI/Kimi-K2"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/MoonshotAI/Kimi-K2"><img src="https://img.shields.io/github/stars/MoonshotAI/Kimi-K2" alt="stars"></a>
- Baichuan-M2: Scaling Medical Capability with Large Verifier System
  <a href="https://arxiv.org/pdf/2509.02208?"><img src="https://img.shields.io/badge/arxiv-2509.02208-silver" alt="Paper"></a>
  <a href="https://github.com/baichuan-inc/Baichuan-M2-32B"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/baichuan-inc/Baichuan-M2-32B"><img src="https://img.shields.io/github/stars/baichuan-inc/Baichuan-M2-32B" alt="stars"></a>
- Self-Rewarding Language Models
  <a href="https://arxiv.org/pdf/2401.10020?"><img src="https://img.shields.io/badge/arxiv-2401.10020-silver" alt="Paper"></a>
- Meta-Rewarding Language Models: Self-Improving Alignment with LLM-as-a-Meta-Judge
  <a href="https://arxiv.org/pdf/2407.19594?"><img src="https://img.shields.io/badge/arxiv-2407.19594-silver" alt="Paper"></a>
- Self-Taught Evaluators
  <a href="https://arxiv.org/pdf/2408.02666?"><img src="https://img.shields.io/badge/arxiv-2408.02666-silver" alt="Paper"></a>
- Process-based Self-Rewarding Language Models
  <a href="https://arxiv.org/pdf/2503.03746?"><img src="https://img.shields.io/badge/arxiv-2503.03746-silver" alt="Paper"></a>

### Reward Model as a Verifier

- Seed1.5-Thinking: Advancing Superb Reasoning Models with Reinforcement Learning
  <a href="https://arxiv.org/pdf/2504.13914?"><img src="https://img.shields.io/badge/arxiv-2504.13914-silver" alt="Paper"></a>
- General-Reasoner: Advancing LLM Reasoning Across All Domains
  <a href="https://arxiv.org/pdf/2505.14652?"><img src="https://img.shields.io/badge/arxiv-2505.14652-silver" alt="Paper"></a>
  <a href="https://github.com/TIGER-AI-Lab/General-Reasoner"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/TIGER-AI-Lab/General-Reasoner"><img src="https://img.shields.io/github/stars/TIGER-AI-Lab/General-Reasoner" alt="stars"></a>
  <a href="https://huggingface.co/collections/TIGER-Lab/general-reasoner-67fe9386e43e046489eac013"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- StructVRM: Aligning Multimodal Reasoning with Structured and Verifiable Reward Models
  <a href="https://arxiv.org/pdf/2508.05383?"><img src="https://img.shields.io/badge/arxiv-2508.05383-silver" alt="Paper"></a>
- Inference-Time Scaling for Generalist Reward Modeling (SPCT)
  <a href="https://arxiv.org/pdf/2504.02495?"><img src="https://img.shields.io/badge/arxiv-2504.02495-silver" alt="Paper"></a>
- Writing-Zero: Bridge the Gap Between Non-verifiable Problems and Verifiable Rewards
  <a href="https://arxiv.org/pdf/2506.00103?"><img src="https://img.shields.io/badge/arxiv-2506.00103-silver" alt="Paper"></a>
- Pre-Trained Policy Discriminators are General Reward Models (POLAR)
  <a href="https://arxiv.org/pdf/2507.05197?"><img src="https://img.shields.io/badge/arxiv-2507.05197-silver" alt="Paper"></a>
  <a href="https://github.com/InternLM/POLAR"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/InternLM/POLAR"><img src="https://img.shields.io/github/stars/InternLM/POLAR" alt="stars"></a>
  <a href="https://huggingface.co/collections/internlm/polar-68693f829d2e83ac5e6e124a"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Beyond the Trade-off: Self-Supervised RL for Reasoning Models' Instruction Following
  <a href="https://arxiv.org/pdf/2508.02150?"><img src="https://img.shields.io/badge/arxiv-2508.02150-silver" alt="Paper"></a>
  <a href="https://github.com/Rainier-rq/verl-if"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Rainier-rq/verl-if"><img src="https://img.shields.io/github/stars/Rainier-rq/verl-if" alt="stars"></a>
- EvolvR: Self-Evolving Pairwise Reasoning for Story Evaluation
  <a href="https://arxiv.org/pdf/2508.06046?"><img src="https://img.shields.io/badge/arxiv-2508.06046-silver" alt="Paper"></a>
  <a href="https://github.com/xindaaW/EvolvR"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/xindaaW/EvolvR"><img src="https://img.shields.io/github/stars/xindaaW/EvolvR" alt="stars"></a>
- Posterior-GRPO: Rewarding Reasoning Processes in Code Generation
  <a href="https://arxiv.org/pdf/2508.05170?"><img src="https://img.shields.io/badge/arxiv-2508.05170-silver" alt="Paper"></a>
- ReasonFlux-PRM: Trajectory-Aware PRMs for Long CoT Reasoning
  <a href="https://arxiv.org/pdf/2506.18896?"><img src="https://img.shields.io/badge/arxiv-2506.18896-silver" alt="Paper"></a>
  <a href="https://github.com/Gen-Verse/ReasonFlux"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Gen-Verse/ReasonFlux"><img src="https://img.shields.io/github/stars/Gen-Verse/ReasonFlux" alt="stars"></a>
  <a href="https://huggingface.co/collections/Gen-Verse/reasonflux-coder-6833109ed9300c62deb32c6b"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Math-Shepherd: Verify and Reinforce LLMs Step-by-step without Human Annotations
  <a href="https://arxiv.org/pdf/2312.08935?"><img src="https://img.shields.io/badge/arxiv-2312.08935-silver" alt="Paper"></a>
- Process Reinforcement through Implicit Rewards (PRIME)
  <a href="https://arxiv.org/pdf/2502.01456?"><img src="https://img.shields.io/badge/arxiv-2502.01456-silver" alt="Paper"></a>
  <a href="https://github.com/PRIME-RL/PRIME"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/PRIME-RL/PRIME"><img src="https://img.shields.io/github/stars/PRIME-RL/PRIME" alt="stars"></a>

---

## L2 · Human-free Reward

> No online human judgment / preference verifier. Reward from **intrinsic signals**, **consensus**, **reference likelihood**, or **environment outcomes**. Humans still supply tasks & environments.

### Intrinsic Certainty

- The Unreasonable Effectiveness of Entropy Minimization in LLM Reasoning (EM-RL)
  <a href="https://arxiv.org/pdf/2505.15134?"><img src="https://img.shields.io/badge/arxiv-2505.15134-silver" alt="Paper"></a>
  <a href="https://github.com/shivamag125/EM_PT"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/shivamag125/EM_PT"><img src="https://img.shields.io/github/stars/shivamag125/EM_PT" alt="stars"></a>
- Right Question is Already Half the Answer: Fully Unsupervised LLM Reasoning Incentivization (EMPO)
  <a href="https://arxiv.org/pdf/2504.05812?"><img src="https://img.shields.io/badge/arxiv-2504.05812-silver" alt="Paper"></a>
  <a href="https://github.com/QingyangZhang/EMPO"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/QingyangZhang/EMPO"><img src="https://img.shields.io/github/stars/QingyangZhang/EMPO" alt="stars"></a>
  <a href="https://huggingface.co/collections/qingyangzhang/empo-67f9f7ad7817ebff4b664010"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Maximizing Confidence Alone Improves Reasoning (RENT)
  <a href="https://arxiv.org/pdf/2505.22660?"><img src="https://img.shields.io/badge/arxiv-2505.22660-silver" alt="Paper"></a>
  <a href="https://github.com/satrams/rent-rl"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/satrams/rent-rl"><img src="https://img.shields.io/github/stars/satrams/rent-rl" alt="stars"></a>
- Confidence Is All You Need: Few-Shot RL Fine-Tuning of Language Models (RLSC)
  <a href="https://arxiv.org/pdf/2506.06395?"><img src="https://img.shields.io/badge/arxiv-2506.06395-silver" alt="Paper"></a>
- Learning to Reason without External Rewards (Intuitor)
  <a href="https://arxiv.org/pdf/2505.19590?"><img src="https://img.shields.io/badge/arxiv-2505.19590-silver" alt="Paper"></a>
  <a href="https://github.com/sunblaze-ucb/Intuitor"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/sunblaze-ucb/Intuitor"><img src="https://img.shields.io/github/stars/sunblaze-ucb/Intuitor" alt="stars"></a>
  <a href="https://huggingface.co/collections/sunblaze-ucb/intuitor-684f895c78ed2d3ef3a678b3"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- No Free Lunch: Rethinking Internal Feedback for LLM Reasoning
  <a href="https://arxiv.org/pdf/2506.17219?"><img src="https://img.shields.io/badge/arxiv-2506.17219-silver" alt="Paper"></a>
- Shop-R1: Rewarding LLMs to Simulate Human Behavior in Online Shopping via RL
  <a href="https://arxiv.org/pdf/2507.17842?"><img src="https://img.shields.io/badge/arxiv-2507.17842-silver" alt="Paper"></a>

### Consensus

- Co-Rewarding: Stable Self-supervised RL for Eliciting Reasoning in LLMs
  <a href="https://arxiv.org/pdf/2508.00410?"><img src="https://img.shields.io/badge/arxiv-2508.00410-silver" alt="Paper"></a>
  <a href="https://github.com/tmlr-group/Co-rewarding"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/tmlr-group/Co-rewarding"><img src="https://img.shields.io/github/stars/tmlr-group/Co-rewarding" alt="stars"></a>
- TTRL: Test-Time Reinforcement Learning
  <a href="https://arxiv.org/pdf/2504.16084?"><img src="https://img.shields.io/badge/arxiv-2504.16084-silver" alt="Paper"></a>
  <a href="https://github.com/PRIME-RL/TTRL"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/PRIME-RL/TTRL"><img src="https://img.shields.io/github/stars/PRIME-RL/TTRL" alt="stars"></a>
- Unsupervised Post-Training for Multi-Modal LLM Reasoning via GRPO (MM-UPT)
  <a href="https://arxiv.org/pdf/2505.22453?"><img src="https://img.shields.io/badge/arxiv-2505.22453-silver" alt="Paper"></a>
  <a href="https://github.com/waltonfuture/MM-UPT"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/waltonfuture/MM-UPT"><img src="https://img.shields.io/github/stars/waltonfuture/MM-UPT" alt="stars"></a>
- Consistent Paths Lead to Truth: Self-Rewarding RL for LLM Reasoning (CoVo)
  <a href="https://arxiv.org/pdf/2506.08745?"><img src="https://img.shields.io/badge/arxiv-2506.08745-silver" alt="Paper"></a>
  <a href="https://github.com/sastpg/CoVo"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/sastpg/CoVo"><img src="https://img.shields.io/github/stars/sastpg/CoVo" alt="stars"></a>
- ETTRL: Balancing Exploration and Exploitation in LLM Test-Time RL via Entropy
  <a href="https://arxiv.org/pdf/2508.11356?"><img src="https://img.shields.io/badge/arxiv-2508.11356-silver" alt="Paper"></a>
- Can Large Reasoning Models Self-Train?
  <a href="https://arxiv.org/pdf/2505.21444?"><img src="https://img.shields.io/badge/arxiv-2505.21444-silver" alt="Paper"></a>

### Reference-Implicit Signals

- Reinforcing General Reasoning without Verifiers (VeriFree)
  <a href="https://arxiv.org/pdf/2505.21493?"><img src="https://img.shields.io/badge/arxiv-2505.21493-silver" alt="Paper"></a>
  <a href="https://github.com/sail-sg/VeriFree"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/sail-sg/VeriFree"><img src="https://img.shields.io/github/stars/sail-sg/VeriFree" alt="stars"></a>
  <a href="https://huggingface.co/collections/zhouxiangxin/verifree-685a1e9509d0db2ed9731c62"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Beyond Verifiable Rewards: Scaling RL for Language Models to Unverifiable Data (JEPO)
  <a href="https://arxiv.org/pdf/2503.19618?"><img src="https://img.shields.io/badge/arxiv-2503.19618-silver" alt="Paper"></a>
- Language Models Are Hidden Reasoners (LaTRO)
  <a href="https://arxiv.org/pdf/2411.04282?"><img src="https://img.shields.io/badge/arxiv-2411.04282-silver" alt="Paper"></a>
  <a href="https://github.com/SalesforceAIResearch/LaTRO"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/SalesforceAIResearch/LaTRO"><img src="https://img.shields.io/github/stars/SalesforceAIResearch/LaTRO" alt="stars"></a>
- Direct Reasoning Optimization (DRO)
  <a href="https://arxiv.org/pdf/2506.13351?"><img src="https://img.shields.io/badge/arxiv-2506.13351-silver" alt="Paper"></a>
- RLPR: Extrapolating RLVR to General Domains without Verifiers
  <a href="https://arxiv.org/pdf/2506.18254?"><img src="https://img.shields.io/badge/arxiv-2506.18254-silver" alt="Paper"></a>
  <a href="https://github.com/OpenBMB/RLPR"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/OpenBMB/RLPR"><img src="https://img.shields.io/github/stars/OpenBMB/RLPR" alt="stars"></a>
- NOVER: Incentive Training via Verifier-Free Reinforcement Learning
  <a href="https://arxiv.org/pdf/2505.16022?"><img src="https://img.shields.io/badge/arxiv-2505.16022-silver" alt="Paper"></a>
  <a href="https://github.com/thinkwee/NOVER"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/thinkwee/NOVER"><img src="https://img.shields.io/github/stars/thinkwee/NOVER" alt="stars"></a>
  <a href="https://huggingface.co/collections/thinkwee/novereason-68937ca75331dfaddaf24016"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- Learning to Reason for Long-Form Story Generation (VR-CLI)
  <a href="https://arxiv.org/pdf/2503.22828?"><img src="https://img.shields.io/badge/arxiv-2503.22828-silver" alt="Paper"></a>
  <a href="https://github.com/Alex-Gurung/ReasoningNCP"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Alex-Gurung/ReasoningNCP"><img src="https://img.shields.io/github/stars/Alex-Gurung/ReasoningNCP" alt="stars"></a>

### Grounded Outcome Signals

Environment-adjudicated rewards (code tests, search, games) without online human labels — still L2 when tasks/envs are fixed.

- RLEF: Grounding Code LLMs in Execution Feedback with Reinforcement Learning
  <a href="https://arxiv.org/pdf/2410.02089?"><img src="https://img.shields.io/badge/arxiv-2410.02089-silver" alt="Paper"></a>
- Search-R1: Training LLMs to Reason and Leverage Search Engines with RL
  <a href="https://arxiv.org/pdf/2503.09516?"><img src="https://img.shields.io/badge/arxiv-2503.09516-silver" alt="Paper"></a>
  <a href="https://github.com/PeterGriffinJin/Search-R1"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/PeterGriffinJin/Search-R1"><img src="https://img.shields.io/github/stars/PeterGriffinJin/Search-R1" alt="stars"></a>
- R1-Searcher: Incentivizing the Search Capability in LLMs via RL
  <a href="https://arxiv.org/pdf/2503.05592?"><img src="https://img.shields.io/badge/arxiv-2503.05592-silver" alt="Paper"></a>
  <a href="https://github.com/RUCAIBox/R1-Searcher"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/RUCAIBox/R1-Searcher"><img src="https://img.shields.io/github/stars/RUCAIBox/R1-Searcher" alt="stars"></a>

---

## L3 · Human-free Experience

> The **experience stream** (tasks and/or environments) is no longer human-designed. Humans provide at most seeds.  
> Includes L2→L3 transitions (task-side or environment-side withdrawal).

### Task Generation (Fixed Environment)

- STaR: Bootstrapping Reasoning with Reasoning
  <a href="https://arxiv.org/pdf/2203.14465?"><img src="https://img.shields.io/badge/arxiv-2203.14465-silver" alt="Paper"></a>
  <a href="https://github.com/ezelikman/STaR"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/ezelikman/STaR"><img src="https://img.shields.io/github/stars/ezelikman/STaR" alt="stars"></a>
- Self-Instruct: Aligning Language Models with Self-Generated Instructions
  <a href="https://arxiv.org/pdf/2212.10560?"><img src="https://img.shields.io/badge/arxiv-2212.10560-silver" alt="Paper"></a>
  <a href="https://github.com/yizhongw/self-instruct"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/yizhongw/self-instruct"><img src="https://img.shields.io/github/stars/yizhongw/self-instruct" alt="stars"></a>
- WizardLM / Evol-Instruct: Empowering LLMs to Follow Complex Instructions
  <a href="https://arxiv.org/pdf/2304.12244?"><img src="https://img.shields.io/badge/arxiv-2304.12244-silver" alt="Paper"></a>
  <a href="https://github.com/nlpxucan/WizardLM"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/nlpxucan/WizardLM"><img src="https://img.shields.io/github/stars/nlpxucan/WizardLM" alt="stars"></a>
- SeRL: Self-Play Reinforcement Learning for LLMs with Limited Data
  <a href="https://arxiv.org/pdf/2505.20347?"><img src="https://img.shields.io/badge/arxiv-2505.20347-silver" alt="Paper"></a>
  <a href="https://github.com/wantbook-book/SeRL"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/wantbook-book/SeRL"><img src="https://img.shields.io/github/stars/wantbook-book/SeRL" alt="stars"></a>
- CoT-Self-Instruct: Building High-Quality Synthetic Prompts
  <a href="https://arxiv.org/pdf/2507.23751?"><img src="https://img.shields.io/badge/arxiv-2507.23751-silver" alt="Paper"></a>
- Beyond the Trade-off: Self-Supervised RL for Instruction Following
  <a href="https://arxiv.org/pdf/2508.02150?"><img src="https://img.shields.io/badge/arxiv-2508.02150-silver" alt="Paper"></a>
  <a href="https://github.com/Rainier-rq/verl-if"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Rainier-rq/verl-if"><img src="https://img.shields.io/github/stars/Rainier-rq/verl-if" alt="stars"></a>
- Self-Questioning Language Models (SQLM)
  <a href="https://arxiv.org/pdf/2508.03682?"><img src="https://img.shields.io/badge/arxiv-2508.03682-silver" alt="Paper"></a>
  <a href="https://github.com/lili-chen/self-questioning-lm"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/lili-chen/self-questioning-lm"><img src="https://img.shields.io/github/stars/lili-chen/self-questioning-lm" alt="stars"></a>
- Multi-Agent Evolve: LLM Self-Improve through Co-evolution (MAE)
  <a href="https://arxiv.org/pdf/2510.23595?"><img src="https://img.shields.io/badge/arxiv-2510.23595-silver" alt="Paper"></a>
- Socratic-Zero: Bootstrapping Reasoning via Data-Free Agent Co-evolution
  <a href="https://arxiv.org/pdf/2509.24726?"><img src="https://img.shields.io/badge/arxiv-2509.24726-silver" alt="Paper"></a>
- G-Zero: Self-Play for Open-Ended Generation from Zero Data
  <a href="https://arxiv.org/pdf/2605.09959?"><img src="https://img.shields.io/badge/arxiv-2605.09959-silver" alt="Paper"></a>
- SPICE: Self-Play In Corpus Environments Improves Reasoning
  <a href="https://arxiv.org/pdf/2510.24684?"><img src="https://img.shields.io/badge/arxiv-2510.24684-silver" alt="Paper"></a>
- OpenSIR: Open-Ended Self-Improving Reasoner
  <a href="https://arxiv.org/pdf/2511.00602?"><img src="https://img.shields.io/badge/arxiv-2511.00602-silver" alt="Paper"></a>
- AgentSynth: Scalable Task Generation for Generalist Computer-Use Agents
  <a href="https://arxiv.org/pdf/2506.14205?"><img src="https://img.shields.io/badge/arxiv-2506.14205-silver" alt="Paper"></a>
  <a href="https://github.com/sunblaze-ucb/AgentSynth"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/sunblaze-ucb/AgentSynth"><img src="https://img.shields.io/github/stars/sunblaze-ucb/AgentSynth" alt="stars"></a>

### Environment Construction & Agentic Experience

- ZeroGUI: Automating Online GUI Learning at Zero Human Cost
  <a href="https://arxiv.org/pdf/2505.23762?"><img src="https://img.shields.io/badge/arxiv-2505.23762-silver" alt="Paper"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/github/stars/OpenGVLab/ZeroGUI" alt="stars"></a>
  <a href="https://huggingface.co/collections/OpenGVLab/zerogui-68388cb7dbf608133c4b5fb2"><img src="https://img.shields.io/badge/huggingface-yellow"></a>
- SEAgent: Self-Evolving Computer Use Agent with Autonomous Learning from Experience
  <a href="https://arxiv.org/pdf/2508.04700?"><img src="https://img.shields.io/badge/arxiv-2508.04700-silver" alt="Paper"></a>
  <a href="https://github.com/SunzeY/SEAgent"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/SunzeY/SEAgent"><img src="https://img.shields.io/github/stars/SunzeY/SEAgent" alt="stars"></a>
- MemAgent: Reshaping Long-Context LLM with Multi-Conv RL-based Memory Agent
  <a href="https://arxiv.org/pdf/2507.02259?"><img src="https://img.shields.io/badge/arxiv-2507.02259-silver" alt="Paper"></a>
  <a href="https://github.com/BytedTsinghua-SIA/MemAgent"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/BytedTsinghua-SIA/MemAgent"><img src="https://img.shields.io/github/stars/BytedTsinghua-SIA/MemAgent" alt="stars"></a>
- Voyager: An Open-Ended Embodied Agent with Large Language Models
  <a href="https://arxiv.org/pdf/2305.16291?"><img src="https://img.shields.io/badge/arxiv-2305.16291-silver" alt="Paper"></a>
  <a href="https://github.com/MineDojo/Voyager"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/MineDojo/Voyager"><img src="https://img.shields.io/github/stars/MineDojo/Voyager" alt="stars"></a>
- Eureka: Human-Level Reward Design via Coding Large Language Models
  <a href="https://arxiv.org/pdf/2310.12931?"><img src="https://img.shields.io/badge/arxiv-2310.12931-silver" alt="Paper"></a>
  <a href="https://github.com/eureka-research/Eureka"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/eureka-research/Eureka"><img src="https://img.shields.io/github/stars/eureka-research/Eureka" alt="stars"></a>
- Genie: Generative Interactive Environments
  <a href="https://arxiv.org/pdf/2402.15391?"><img src="https://img.shields.io/badge/arxiv-2402.15391-silver" alt="Paper"></a>
- PAIRED: Emergent Complexity and Zero-shot Transfer via Unsupervised Environment Design
  <a href="https://arxiv.org/pdf/2012.02096?"><img src="https://img.shields.io/badge/arxiv-2012.02096-silver" alt="Paper"></a>
- Agent World Model: Infinity Synthetic Environments for Agentic RL
  <a href="https://arxiv.org/pdf/2602.10090?"><img src="https://img.shields.io/badge/arxiv-2602.10090-silver" alt="Paper"></a>
  <a href="https://github.com/Snowflake-Labs/agent-world-model"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Snowflake-Labs/agent-world-model"><img src="https://img.shields.io/github/stars/Snowflake-Labs/agent-world-model" alt="stars"></a>
- ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Tool-Use Agents
  <a href="https://arxiv.org/pdf/2602.06820?"><img src="https://img.shields.io/badge/arxiv-2602.06820-silver" alt="Paper"></a>
- CuES: Curiosity-driven and Environment-grounded Synthesis for Agentic RL
  <a href="https://arxiv.org/pdf/2512.01311?"><img src="https://img.shields.io/badge/arxiv-2512.01311-silver" alt="Paper"></a>
  <a href="https://github.com/modelscope/AgentEvolver"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/modelscope/AgentEvolver"><img src="https://img.shields.io/github/stars/modelscope/AgentEvolver" alt="stars"></a>
- EvoEnv: Self-Evolving Reasoning RL via Verifiable Environment Synthesis
  <a href="https://arxiv.org/pdf/2605.14392?"><img src="https://img.shields.io/badge/arxiv-2605.14392-silver" alt="Paper"></a>
- Don't Just Fine-tune the Agent, Tune the Environment
  <a href="https://arxiv.org/pdf/2510.10197?"><img src="https://img.shields.io/badge/arxiv-2510.10197-silver" alt="Paper"></a>
  <a href="https://github.com/inclusionAI/AWorld-RL"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/inclusionAI/AWorld-RL"><img src="https://img.shields.io/github/stars/inclusionAI/AWorld-RL" alt="stars"></a>

---

## L4 · Autonomous Co-evolution

> Reward, tasks, and environments **co-evolve** in a closed loop. Includes L3→L4 precursors highlighted in the survey.

- Absolute Zero: Reinforced Self-Play Reasoning with Zero Data (AZR)
  <a href="https://arxiv.org/pdf/2505.03335?"><img src="https://img.shields.io/badge/arxiv-2505.03335-silver" alt="Paper"></a>
  <a href="https://github.com/LeapLabTHU/Absolute-Zero-Reasoner"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/LeapLabTHU/Absolute-Zero-Reasoner"><img src="https://img.shields.io/github/stars/LeapLabTHU/Absolute-Zero-Reasoner" alt="stars"></a>
- R-Zero: Self-Evolving Reasoning LLM from Zero Data
  <a href="https://arxiv.org/pdf/2508.05004?"><img src="https://img.shields.io/badge/arxiv-2508.05004-silver" alt="Paper"></a>
  <a href="https://github.com/Chengsong-Huang/R-Zero"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Chengsong-Huang/R-Zero"><img src="https://img.shields.io/github/stars/Chengsong-Huang/R-Zero" alt="stars"></a>
- Language Self-Play For Data-Free Training (LSP)
  <a href="https://arxiv.org/pdf/2412.16720?"><img src="https://img.shields.io/badge/arxiv-2412.16720-silver" alt="Paper"></a>
- Co-Evolving LLM Coder and Unit Tester via Reinforcement Learning (CURE)
  <a href="https://arxiv.org/pdf/2506.03136?"><img src="https://img.shields.io/badge/arxiv-2506.03136-silver" alt="Paper"></a>
  <a href="https://github.com/Gen-Verse/CURE"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Gen-Verse/CURE"><img src="https://img.shields.io/github/stars/Gen-Verse/CURE" alt="stars"></a>
- Self-Challenging Language Model Agents
  <a href="https://arxiv.org/pdf/2506.01716?"><img src="https://img.shields.io/badge/arxiv-2506.01716-silver" alt="Paper"></a>
- SPIRAL: Self-Play on Zero-Sum Games Incentivizes Reasoning via Multi-Agent Multi-Turn RL
  <a href="https://arxiv.org/pdf/2506.24119?"><img src="https://img.shields.io/badge/arxiv-2506.24119-silver" alt="Paper"></a>
  <a href="https://github.com/spiral-rl/spiral"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/spiral-rl/spiral"><img src="https://img.shields.io/github/stars/spiral-rl/spiral" alt="stars"></a>
- POET: Paired Open-Ended Trailblazer
  <a href="https://arxiv.org/pdf/1901.01753?"><img src="https://img.shields.io/badge/arxiv-1901.01753-silver" alt="Paper"></a>
  <a href="https://github.com/uber-research/poet"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/uber-research/poet"><img src="https://img.shields.io/github/stars/uber-research/poet" alt="stars"></a>
- OMNI-EPIC: Open-endedness via Models of Human Notions of Interestingness with Environments Programmed in Code
  <a href="https://arxiv.org/pdf/2405.15568?"><img src="https://img.shields.io/badge/arxiv-2405.15568-silver" alt="Paper"></a>
  <a href="https://github.com/MaxenceFaldor/Omni-EPIC"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/MaxenceFaldor/Omni-EPIC"><img src="https://img.shields.io/github/stars/MaxenceFaldor/Omni-EPIC" alt="stars"></a>
- GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators
  <a href="https://arxiv.org/pdf/2512.19682?"><img src="https://img.shields.io/badge/arxiv-2512.19682-silver" alt="Paper"></a>
  <a href="https://github.com/Gen-Verse/GenEnv"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Gen-Verse/GenEnv"><img src="https://img.shields.io/github/stars/Gen-Verse/GenEnv" alt="stars"></a>
- Agent-World: Scaling Real-World Environment Synthesis for Evolving General Agent Intelligence
  <a href="https://arxiv.org/pdf/2604.18292?"><img src="https://img.shields.io/badge/arxiv-2604.18292-silver" alt="Paper"></a>
- Darwin Gödel Machine: Open-Ended Evolution of Self-Improving Agents
  <a href="https://arxiv.org/pdf/2505.22954?"><img src="https://img.shields.io/badge/arxiv-2505.22954-silver" alt="Paper"></a>
  <a href="https://github.com/jennyzzt/dgm"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/jennyzzt/dgm"><img src="https://img.shields.io/github/stars/jennyzzt/dgm" alt="stars"></a>

---

## Evaluation, Datasets and Benchmarks

### Capability — Hard-verifiable

**Math:** GSM8K ([2110.14168](https://arxiv.org/pdf/2110.14168?)) · MATH/MATH500 ([2305.20050](https://arxiv.org/pdf/2305.20050?)) · LiveMathBench ([2412.13147](https://arxiv.org/pdf/2412.13147?)) · NuminaMath/AMC ([2410.01271](https://arxiv.org/pdf/2410.01271?)) · [AIME 2024](https://artofproblemsolving.com/wiki/index.php/2024_AIME_I) · [AIME 2025](https://artofproblemsolving.com/wiki/index.php/2025_AIME_I) · RandomCalculation ([2507.10532](https://arxiv.org/pdf/2507.10532?))

**Code:** MBPP ([2108.07732](https://arxiv.org/pdf/2108.07732?)) · LiveCodeBench ([2403.07974](https://arxiv.org/pdf/2403.07974?)) · CRUXEval ([2401.03065](https://arxiv.org/pdf/2401.03065?)) · HumanEval ([2107.03374](https://arxiv.org/pdf/2107.03374?)) · CodeContests ([2203.07814](https://arxiv.org/pdf/2203.07814?)) · MHPP ([2405.11430](https://arxiv.org/pdf/2405.11430?)) · CodeElo ([2501.01257](https://arxiv.org/pdf/2501.01257?))

**Logic / Multi-choice:** ZebraLogic ([2502.01100](https://arxiv.org/pdf/2502.01100?)) · AutoLogi ([2502.16906](https://arxiv.org/pdf/2502.16906?)) · Sudoku-Bench ([2505.16135](https://arxiv.org/pdf/2505.16135?)) · AQuA ([1705.04146](https://arxiv.org/pdf/1705.04146?)) · CodeMMLU ([2410.01999](https://arxiv.org/pdf/2410.01999?)) · LogiQA ([2007.08124](https://arxiv.org/pdf/2007.08124?))

### Capability — Semi-verifiable / Expert / Open-ended

GPQA ([2311.12022](https://arxiv.org/pdf/2311.12022?)) · HLE ([2501.14249](https://arxiv.org/pdf/2501.14249?)) · MMLU ([2009.03300](https://arxiv.org/pdf/2009.03300?)) · MMLU-Pro ([2406.01574](https://arxiv.org/pdf/2406.01574?)) · CommonsenseQA ([1811.00937](https://arxiv.org/pdf/1811.00937?)) · CHARM ([2403.14112](https://arxiv.org/pdf/2403.14112?)) · MedQA ([2009.13081](https://arxiv.org/pdf/2009.13081?)) · MedBullets ([2402.18060](https://arxiv.org/pdf/2402.18060?)) · MedXpertQA ([2501.18362](https://arxiv.org/pdf/2501.18362?)) · FinanceQA ([2501.18062](https://arxiv.org/pdf/2501.18062?)) · FinTextQA ([2405.09980](https://arxiv.org/pdf/2405.09980?)) · FinBen ([2402.12659](https://arxiv.org/pdf/2402.12659?)) · FinanceBench ([2311.11944](https://arxiv.org/pdf/2311.11944?)) · LawBench ([2309.16289](https://arxiv.org/pdf/2309.16289?)) · LexEval ([2409.20288](https://arxiv.org/pdf/2409.20288?)) · LegalBench ([2308.11462](https://arxiv.org/pdf/2308.11462?)) · LEXam ([2505.12864](https://arxiv.org/pdf/2505.12864?)) · LitBench ([2507.00769](https://arxiv.org/pdf/2507.00769?)) · CS4 ([2410.04197](https://arxiv.org/pdf/2410.04197?)) · SS-GEN ([2406.15695](https://arxiv.org/pdf/2406.15695?)) · AlpacaEval ([2404.04475](https://arxiv.org/pdf/2404.04475?)) · IFEval ([2311.07911](https://arxiv.org/pdf/2311.07911?)) · MT-Bench ([2306.05685](https://arxiv.org/pdf/2306.05685?)) · EQ-Bench ([2312.06281](https://arxiv.org/pdf/2312.06281?)) · ToMBench ([2402.15052](https://arxiv.org/pdf/2402.15052?)) · EgoSocialArena ([2410.06195](https://arxiv.org/pdf/2410.06195?)) · SocialEval ([2506.00900](https://arxiv.org/pdf/2506.00900?))

### Reward-Axis Benchmarks

- MLLM-as-a-Judge
  <a href="https://arxiv.org/pdf/2402.04788?"><img src="https://img.shields.io/badge/arxiv-2402.04788-silver" alt="Paper"></a>
  <a href="https://github.com/Dongping-Chen/MLLM-Judge"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Dongping-Chen/MLLM-Judge"><img src="https://img.shields.io/github/stars/Dongping-Chen/MLLM-Judge" alt="stars"></a>
- Judging the Judges: Position Bias in LLM-as-a-Judge
  <a href="https://arxiv.org/pdf/2406.07791?"><img src="https://img.shields.io/badge/arxiv-2406.07791-silver" alt="Paper"></a>
- JudgeBench
  <a href="https://arxiv.org/pdf/2410.12784?"><img src="https://img.shields.io/badge/arxiv-2410.12784-silver" alt="Paper"></a>
  <a href="https://github.com/ScalerLab/JudgeBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/ScalerLab/JudgeBench"><img src="https://img.shields.io/github/stars/ScalerLab/JudgeBench" alt="stars"></a>
- JETTS
  <a href="https://arxiv.org/pdf/2504.15253?"><img src="https://img.shields.io/badge/arxiv-2504.15253-silver" alt="Paper"></a>
  <a href="https://github.com/SalesforceAIResearch/jetts-benchmark"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/SalesforceAIResearch/jetts-benchmark"><img src="https://img.shields.io/github/stars/SalesforceAIResearch/jetts-benchmark" alt="stars"></a>
- CodeJudgeBench
  <a href="https://arxiv.org/pdf/2507.10535?"><img src="https://img.shields.io/badge/arxiv-2507.10535-silver" alt="Paper"></a>
  <a href="https://github.com/hongcha0/CodeJudgeBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/hongcha0/CodeJudgeBench"><img src="https://img.shields.io/github/stars/hongcha0/CodeJudgeBench" alt="stars"></a>
- RewardBench
  <a href="https://arxiv.org/pdf/2403.13787?"><img src="https://img.shields.io/badge/arxiv-2403.13787-silver" alt="Paper"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/github/stars/allenai/reward-bench" alt="stars"></a>
- RM-Bench
  <a href="https://arxiv.org/pdf/2410.16184?"><img src="https://img.shields.io/badge/arxiv-2410.16184-silver" alt="Paper"></a>
  <a href="https://github.com/THU-KEG/RM-Bench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/THU-KEG/RM-Bench"><img src="https://img.shields.io/github/stars/THU-KEG/RM-Bench" alt="stars"></a>
- ViLBench
  <a href="https://arxiv.org/pdf/2503.20271?"><img src="https://img.shields.io/badge/arxiv-2503.20271-silver" alt="Paper"></a>
  <a href="https://github.com/UCSC-VLAA/ViLBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/UCSC-VLAA/ViLBench"><img src="https://img.shields.io/github/stars/UCSC-VLAA/ViLBench" alt="stars"></a>
- Socratic-PRMBench
  <a href="https://arxiv.org/pdf/2505.23474?"><img src="https://img.shields.io/badge/arxiv-2505.23474-silver" alt="Paper"></a>
  <a href="https://github.com/Xiang-Li-oss/Socratic-PRMBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Xiang-Li-oss/Socratic-PRMBench"><img src="https://img.shields.io/github/stars/Xiang-Li-oss/Socratic-PRMBench" alt="stars"></a>
- RewardBench 2
  <a href="https://arxiv.org/pdf/2506.01937?"><img src="https://img.shields.io/badge/arxiv-2506.01937-silver" alt="Paper"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/github/stars/allenai/reward-bench" alt="stars"></a>
- RewardAnything
  <a href="https://arxiv.org/pdf/2506.03637?"><img src="https://img.shields.io/badge/arxiv-2506.03637-silver" alt="Paper"></a>
  <a href="https://github.com/WisdomShell/RewardAnything"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/WisdomShell/RewardAnything"><img src="https://img.shields.io/github/stars/WisdomShell/RewardAnything" alt="stars"></a>

---

## Challenges and Future Directions

- **L1–L2:** judge bias, reward hacking, consensus traps, reference under-specification  
- **L3–L4:** difficulty miscalibration, co-adaptive hacking, distributional narrowing, non-stationarity  
- Open: efficient experience sampling; folding verifier-free signals into next-generation pre-training  

---

## 🤝 Contributing

1. Assign a **primary level (L0–L4)**.
2. Prefer the badge format used above (`arxiv` / `github` / `stars`).
3. PR note: one sentence on why that ladder level.

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📜 Citation

```bibtex
@article{yang2026scaling,
  title   = {Scaling Large Reasoning Models beyond Human Supervision: A Path toward Superintelligence},
  author  = {Yang, Zhiqin and Fu, Jingwen and Liu, Yuhan and Liu, Hengyu and Zhang, Yonggang and Cao, Kainan and Zhang, Zizhuo and Li, Chenxin and Yuan, Ruibin and Pan, Jiahao and Sun, Jiankai and Lin, Yunlong and Zhang, Zhenyuan and Xiong, Jing and Li, Yibo and Lin, Sida and Xue, Wei and Han, Bo and Guo, Yike},
  year    = {2026},
  note    = {Survey; companion repository: https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths}
}
```

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths&type=Date)](https://star-history.com/#visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths&Date)
