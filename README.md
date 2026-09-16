# Model Selector

An agent skill for choosing AI models for a specific task using current evidence.

It returns:

- Up to three models for the strongest task quality.
- Up to three models for the best value, considering completed work, cost and human corrections.
- The cheapest option with evidence that it meets the task's acceptance criteria, or a clearly labeled candidate to test when evidence is missing.

Each recommendation includes the access platform, a verified reasoning setting, the reason for choosing it, sources and uncertainty. The same model may appear in several categories.

## How it works

The skill asks for the task when none is supplied, then asks only questions that can change the choice. It identifies relevant capabilities, discovers current benchmarks, reads their methods and task examples, and checks current model catalogs, settings and prices.

The package stores the selection method and links to source services. Model names, benchmark versions, rankings, pricing and supported-setting lists are researched during each run. Results from a previous selection do not become defaults.

Public benchmarks are evidence to assess, not guarantees about a different workload. The skill explains transfer gaps and proposes a small check on representative tasks. Browsing is needed for a current recommendation. Without it, conclusions remain provisional.

## Install in Codex

Ask Codex:

```text
Use $skill-installer to install the skill from
https://github.com/alexandrbasis/model-selector/tree/main/skills/model-selector
```

The skill directory is `skills/model-selector`. Installation includes its `references` and `agents` directories. For an existing installation, ask Codex to update it from this repository while preserving any local changes.

For another agent that supports skills, install the complete directory in that agent's skill location. The instructions do not require a particular model provider or paid evaluation platform. `agents/openai.yaml` contains Codex interface metadata.

## Use

```text
Use $model-selector to choose models for checking Russian product requirements.
Find omissions and contradictions while preserving every condition and exception.
I will use an API and review the final output.
Compare quality leaders, best-value choices, and the cheapest adequate option.
Explain the reasoning settings and what I should validate on my documents.
```

The skill responds in the user's language. It supports writing, research, coding, documents, extraction, multimodal work and agent workflows. Task-specific evidence determines the selection.

It provides advice and read-only research. Paid experiments, private-data uploads and configuration changes need authorization for those actions.

## Files and origin

Start with [SKILL.md](skills/model-selector/SKILL.md). Supporting references cover the [interview](skills/model-selector/references/interview.md), [source entrypoints](skills/model-selector/references/source-map.md), [benchmark selection](skills/model-selector/references/benchmark-selection.md), [reasoning and cost](skills/model-selector/references/reasoning-and-cost.md), and [validation](skills/model-selector/references/validation.md).

The workflow was inspired by [IndyDevDan's video about selecting agent benchmarks](https://www.youtube.com/watch?v=9weiIHy9T_0). Its [origin note](skills/model-selector/references/video-origin.md) distinguishes the video's ideas from this skill's additions. No ranking from the video is inherited, and this project is not affiliated with the author or the linked evaluation services.
