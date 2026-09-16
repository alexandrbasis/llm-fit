# Understand a benchmark before using its ranking

The stable knowledge is how to identify relevant evidence. Benchmark identities, versions, definitions, task sets and winners come from live sources. Never treat a remembered benchmark name as a complete description of what its current version measures.

## Translate the task into evidence needs

Pick the requirements that can change the recommendation. This table maps tasks to capabilities, not to fixed benchmarks.

| Task | Look for measured capabilities | Transfer gap to check |
|---|---|---|
| Faithful editing, summarization | Preservation of facts, conditions, numbers and scope; instruction compliance; omissions | General writing preference may reward appealing additions that this task forbids. |
| Writing, translation, ideation | User-specific style, target-language fluency, meaning preservation, human preference | Style preference is not factuality or regional/language fit. |
| Research and factual analysis | Source retrieval, claim support, citation accuracy, coverage, calibrated abstention, calculations | Closed-book knowledge is not grounded research. Read the actual error denominator and answer rate. |
| Extraction and classification | Field/label accuracy, schema validity, omissions and severe errors | Schema compliance alone cannot establish correct values. |
| Coding and terminal work | Task completion, regression checks, constraints, repository/tool handling | Short patches, debugging and long autonomous work require different evidence. |
| Professional documents and analysis | Domain-matched tasks, complete deliverables, rubric compliance, calculations | A neighboring profession or partial rubric score may not establish task success. |
| Business, browser or desktop agents | Correct final state, permitted actions, tool/UI use, recovery and human intervention | API tools and GUI interaction are different environments; success may hide forbidden side effects. |
| Long inputs | Retrieval, cross-document integration, contradictions and synthesis at actual lengths | Advertised capacity and finding one fact are insufficient for full-document reasoning. |
| Image, audio or video work | Exact input/output modality and task: understanding, transcription, creation or editing | Understanding a modality does not establish generation quality or exact document extraction. |
| Delegated or multi-stage work | Handoff correctness, coordination, recovery, total task success and oversight | Single-agent results and agreement between agents do not prove system reliability. |

Treat language, domain, difficulty, input size, autonomy and tool environment as cross-cutting filters. One evaluation may cover several requirements; avoid counting correlated evidence twice.

## Build a compact live benchmark card

For each evaluation used to rank candidates, inspect the current methodology plus representative task examples and extract:

1. **Identity:** owner, exact name/version/split, source links, publication/evaluation date and access date; maintained successor if any.
2. **Construct:** what the test intends to measure; domain, language, modality, task examples, input sizes and task duration/complexity.
3. **Metric:** actual scoring rule, denominator, direction, aggregation, partial credit, error/abstention handling, constraint violations and distinction between repeated attempts and reliable single-run success.
4. **Environment:** model snapshots, provider, thinking settings, prompts, tools/harness, retrieval/access, budgets, time limits and safeguards.
5. **Evidence quality:** sample count, repeats, uncertainty, coverage of current candidates, saturation and disclosed contamination or tuning. Note evaluator/provider involvement without assuming bias from missing scores.
6. **Economics:** what cost and time include; measured wall time versus estimates or token counts; failures, tools, retries and concurrency.
7. **Task mapping:** exact user requirement supported, matching slice, important mismatch, and whether the result can discriminate finalists or only check a minimum.

A short card is enough; do not reproduce an entire paper. Unknown fields stay unknown. If a missing field affects a comparison, qualify or exclude that comparison. Quote a short relevant definition when a surprising metric or contested interpretation drives the decision, then explain its effect.

## Use or reject the evidence

Use close task matches for ranking, narrower tests for the requirement they actually measure, and distant proxies only as supporting context. Choose a small complementary set; more benchmarks do not automatically add information. A saturated test can still identify a failed requirement but may not distinguish the leaders.

Compare like with like: metric/version, model configuration, harness, tools and budgets. Changes in these can explain a score difference. Cross-benchmark percentages are not a common quality scale. Preserve unresolved contradictions rather than selecting a favorable number. Read current pages even when an old report is familiar; embedded older abstracts may describe different methods.

When no suitable public evaluation exists, state the gap. Use verified capability/constraint evidence to form a provisional shortlist and [a task-specific trial](validation.md) to test it. An official capability claim alone cannot prove the acceptance floor. Explain the mapping and its limits to the user without asking them to become a benchmark expert.
