# Contributing

Thanks for helping keep this list aligned with the survey  
**Scaling Large Reasoning Models beyond Human Supervision: A Path toward Superintelligence**.

## Place papers by ladder level (Figure 1)

| Level | Put here if … |
|-------|----------------|
| **L0** | Per-instance human labels / preferences (reference baselines) |
| **L1** | Reusable LLM judge or reward model; tasks/envs still human |
| **L2** | Human-free reward (entropy / consensus / reference likelihood / env outcome); tasks & envs still human |
| **L3** | Experience stream (tasks and/or environments) is model-authored from seeds |
| **L4** | Reward, tasks, and environments **co-evolve** in a closed loop |

Prefer **one primary level** per paper. Prefer covering works cited in the survey.

## Badge format

```markdown
- Paper Title (ShortName)
  <a href="https://arxiv.org/pdf/XXXX.XXXXX?"><img src="https://img.shields.io/badge/arxiv-XXXX.XXXXX-silver" alt="Paper"></a>
  <a href="https://github.com/org/repo"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/org/repo"><img src="https://img.shields.io/github/stars/org/repo" alt="stars"></a>
```
