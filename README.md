# LLM Fit

An agent skill for choosing AI models for a specific task using current evidence.

It returns four compact blocks:

1. Top three models for task quality, each with a reasoning setting and a concrete reason.
2. Benchmarks that fit the task, with an explanation of their relevance.
3. A matrix of the models' benchmark results, measured settings and what the differences mean.
4. Cost efficiency, including the value top three and the cheapest adequate option, or a clearly labeled candidate to test when evidence is missing.

Each recommendation includes the access platform, verified settings, sources and relevant uncertainty. The same model may appear in several categories. The [output contract](skills/llm-fit/references/output-contract.md) keeps the recommendation short and puts evidence next to the claims it supports.

## How it works

The skill asks for the task when none is supplied, then clarifies only missing task details, acceptance criteria and operational constraints. It compares all three objectives without asking the user to choose between quality, balance and minimum cost. It identifies relevant capabilities, discovers current benchmarks, reads their methods and task examples, and checks current model catalogs, settings and prices.

The package stores the selection method and links to source services. Model names, benchmark versions, rankings, pricing and supported-setting lists are researched during each run. Results from a previous selection do not become defaults.

Public benchmarks are evidence to assess, not guarantees about a different workload. The skill explains transfer gaps briefly and names a concrete check when evidence is missing. Detailed test plans are optional. Browsing is needed for a current recommendation. Without it, conclusions remain provisional.

## Install in Codex

Ask Codex:

```text
Use $skill-installer to install the skill from
https://github.com/alexandrbasis/llm-fit/tree/main/skills/llm-fit
```

The skill directory is `skills/llm-fit`. Installation includes its `references` and `agents` directories. For an existing installation, ask Codex to update it from this repository while preserving any local changes.

For another agent that supports skills, install the complete directory in that agent's skill location. The instructions do not require a particular model provider or paid evaluation platform. `agents/openai.yaml` contains Codex interface metadata.

## Use

```text
Use $llm-fit to choose models for checking Russian product requirements.
Find omissions and contradictions while preserving every condition and exception.
I will use an API and review the final output.
Compare quality leaders, best-value choices, and the cheapest adequate option.
Explain the reasoning settings and what I should validate on my documents.
```

The skill responds in the user's language. It supports writing, research, coding, documents, extraction, multimodal work and agent workflows. Task-specific evidence determines the selection.

It provides advice and read-only research. Paid experiments, private-data uploads and configuration changes need authorization for those actions.

## Files and origin

Start with [SKILL.md](skills/llm-fit/SKILL.md). Supporting references cover the [interview](skills/llm-fit/references/interview.md), [source entrypoints](skills/llm-fit/references/source-map.md), [benchmark selection](skills/llm-fit/references/benchmark-selection.md), [reasoning and cost](skills/llm-fit/references/reasoning-and-cost.md), and [validation](skills/llm-fit/references/validation.md).

The workflow was inspired by [IndyDevDan's video about selecting agent benchmarks](https://www.youtube.com/watch?v=9weiIHy9T_0). Its [origin note](skills/llm-fit/references/video-origin.md) distinguishes the video's ideas from this skill's additions. No ranking from the video is inherited, and this project is not affiliated with the author or the linked evaluation services.
