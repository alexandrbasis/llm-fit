---
name: model-selector
description: Select AI models for a specific task using current sources. Recommend top three for quality, top three for value, and the cheapest adequate option, with verified reasoning settings. Use for model recommendations and workload-to-model matching across apps, APIs, and local deployment.
---

# Model Selector

Recommend **model + supported reasoning configuration + delivery surface** in the user's language. Reasoning means both the actual thinking setting and a concise explanation of the choice, never hidden chain of thought. Cover general work: writing, research, coding, analysis, documents, multimodal tasks and agents.

## Knowledge boundaries

Keep three layers separate:

1. **Stable method:** task interview, evidence selection, comparison rules and validation, stored in this skill.
2. **Live knowledge:** available models, benchmarks and their methods, results, reasoning controls, prices and platform limits, fetched from current sources each run.
3. **Run-specific decision:** task profile, dated evidence ledger, rankings and uncertainty, kept in the current response or requested report.

The package contains source entrypoints, not model names, model examples, benchmark inventories, fixed scoring formulas from a benchmark, prices or supported-setting lists. Do not write discovered facts back into the skill as defaults. Links are starting points: follow maintained successors and discover other primary sources when needed. Historical video provenance is optional context in [video-origin.md](references/video-origin.md), not a recommendation database.

## 1. Establish the task and acceptance floor

Extract the job as input → work → deliverable → observable success. Identify domain, language, modalities, volume, tools, autonomy, review burden, and existing baseline. Separate hard constraints (surface, deployment/privacy, context, deadlines, spending ceilings) from preferences.

Define both **best possible quality** for this task and **minimum acceptable quality**: required content/behavior, unacceptable errors, tolerable corrections, and when clarification or abstention is acceptable. The cheapest adequate choice depends on this floor; never invent a universal passing percentage. Distinguish a spending ceiling from a preferred target cost.

If no task exists, ask for one concrete example and expected result before ranking. Otherwise use [interview.md](references/interview.md) only for unanswered questions that could change feasibility, ranking or effort; batch at most three short questions. Let users describe work, not name benchmarks. Reuse context and state low-impact assumptions. If a missing constraint could invalidate the result, resolve it or keep the affected recommendation conditional. A user declining more questions gets a provisional answer with assumptions.

**Done when:** the task, hard constraints, ideal quality, and acceptance floor are clear enough to compare, or the unresolved points are explicitly conditional.

## 2. Discover and understand current evidence

Read [source-map.md](references/source-map.md) for entrypoints and [benchmark-selection.md](references/benchmark-selection.md) for matching current benchmarks to this task. Choose a small set of important capabilities, usually two to four. Discover current evaluations for these capabilities, then read each selected evaluation's current methodology and task examples before trusting its leaderboard. Explain the mapping: task requirement → measured capability → benchmark/slice → transfer limitation.

Research current model catalogs and prices alongside evaluations. Include plausible quality leaders, efficient candidates and specialists within the user's deployment boundaries; do not require provider diversity. Start with a manageable pool, usually five to eight models across both objectives, and expand if evidence or budget options are weak. Do not restrict discovery to the models ranked in the video or covered by one leaderboard. Stop when each objective has credible contenders, meaningful lower-cost alternatives have been considered, and remaining gaps are explicit.

Verify exact names/snapshots, availability, capabilities, settings and commercial terms against official documentation. Benchmark owners are authoritative about their own measurements; label provider self-reports. Read sources before citing them, and record access date separately from publication/evaluation date.

Keep a compact working ledger:

`model/version | provider/surface | reasoning/configuration | constraint fit | benchmark card + task evidence/URL | quality | cost/time basis | dates | gaps`

Prefer direct workload measurements, then close independent proxies, then distant benchmarks and labeled claims. Missing scores mean unknown. A new model needs its own evidence; a predecessor's score does not transfer automatically. Without live access, say the current market cannot be verified and use any dated evidence only provisionally.

**Done when:** selected benchmarks have understood methods and task fit, and plausible candidates for both quality and economy have dated evidence or explicit gaps.

## 3. Compare configurations under three objectives

Read [reasoning-and-cost.md](references/reasoning-and-cost.md). Verify every recommended setting on the actual surface. Keep benchmark settings distinct from recommended settings; results at one effort do not establish results at another. If no control is exposed, use documented automatic behavior, or mark it unverified.

Apply hard constraints first. Produce these three outputs unless the user explicitly narrows the request:

| Output | Decision rule |
|---|---|
| **Top 3 by quality** | Rank feasible configurations by task quality, correctness and reliability. Price does not lower rank; declared hard spending/deadline limits still apply. Use lower cost/time only to break a quality tie. |
| **Top 3 by value** | Compare useful accepted work against full cost and human rework, at acceptable quality. Explain whether each price increase buys a meaningful task benefit. Use the quality/cost frontier; exclude a clearly inferior, costlier option unless a material constraint or uncertainty explains its inclusion. |
| **Cheapest adequate option** | Select the least expensive eligible configuration with enough evidence that it meets the stated floor. Scope “cheapest” to the checked candidates, surface, workload and pricing assumptions. If adequacy or comparative task cost is unknown, name a cheapest candidate to test and explicitly leave this conclusion unverified. |

Use three distinct models within each top-three list when evidence supports three. The same model may appear in both lists and be the cheapest adequate choice, possibly at different supported settings. Seven unique models are not required. A model at several effort levels is still one model. If fewer qualify, list fewer and explain; when no floor is evidenced, keep value candidates explicitly provisional rather than declaring them adequate.

Use the user's priorities to choose one overall starting recommendation from these comparisons. “Value” is not an arbitrary benchmark-score/price ratio: use such a ratio only if the metric has a meaningful cardinal interpretation for this task and costs are comparable. Avoid averaging unrelated percentages or inventing weights. Explain ties, conflicts and uncertainty; call an unsupported ordering an order to test, not a proven ranking. If unknown candidates could change a winner, state that coverage limit.

For multi-stage work, consider routing only when gains justify handoffs, verification and failure complexity; retain a single-model baseline. Advice does not change the user's active model or settings.

**Done when:** the three objectives are answered or explicitly unresolved, every proposed configuration is supported, and adequacy is separated from mere plausibility.

## 4. Deliver a usable recommendation

Lead with the overall starting choice, verified setting, main reason, date checked and confidence. Briefly state the task, acceptance floor and assumptions. Then present:

1. **Top 3 — quality.** `Rank | Model + surface | Reasoning and why | Task-quality evidence | Cost/time | Limitation`
2. **Top 3 — value.** `Rank | Model + surface | Reasoning | Why this tradeoff | Full-cost basis | Quality concession / evidence gap`
3. **Cheapest adequate.** Model/configuration, evidence of adequacy, cost assumptions, what is sacrificed and when to escalate. If unverified, label it “cheapest candidate to test,” with the missing check.

Reuse shared facts when models overlap. Explain the decisive benchmark choices and direct-versus-proxy evidence with links near the claims. State why another option could win. For a stack, add stage → model/setting → escalation condition without replacing the three outputs.

Finish with a small validation recipe from [validation.md](references/validation.md), using real representative tasks. Say whether tests were run. Separate measured, estimated and unknown cost/speed; API prices, subscription quotas and local infrastructure are different cost bases. Detailed calculations or API snippets are optional when needed to act.

This skill authorizes advice and read-only research. Paid experiments, private-data uploads, deployment and configuration changes require existing task authorization. Missing evidence calls for a concrete proportionate trial, not an unrequested evaluation project.

**Complete when:** the user sees quality leaders, best-value choices and the cheapest evidenced adequate option (or the exact gap), with usable settings, fresh sources and a practical next step.
