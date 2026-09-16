# Validate on real work

Public benchmarks narrow candidates. A workload trial checks whether the proxy transfers. This remains a proposed experiment unless execution and its data/cost boundaries are authorized.

For routine use, the trial can be the first few ordinary tasks with a short checklist. Do not require a dataset project, evaluation service, or implementation before the user can start. Use the fuller design below when the decision warrants it.

## Screening trial

Use 5–10 representative cases for a quick first screen, including ordinary work, a difficult case, incomplete information, and a relevant failure/constraint case. This is a practical starting heuristic, not statistical validation. Use more cases and repeated runs when outcomes vary, finalists are close, or errors matter greatly. Rare failures require targeted cases and suitable sample sizes.

Define success before seeing outputs. Match language, input size, tools, typical prompts, output format, and review burden. Split tuning examples from held-out comparison examples; do not tune on the cases used to announce a winner.

First hold prompts, harness, tools, data, and limits fixed to compare models/configurations. Separately allow comparable prompt tuning per candidate and report the whole-system comparison with each prompt version. Do not mix the two experiments.

## Grade the actual deliverable

- Coding: executable acceptance checks, regression behavior, requested scope, maintainability review as needed.
- Extraction/classification: schema, field/label accuracy, omissions and severe errors against labeled examples.
- Research/documents: source-supported claims, valid citations, coverage, calculations and fabricated facts.
- Writing/design: blinded review with a user-specific rubric, factual fidelity and editing effort; do not reward verbosity by default.
- Agents: final state plus process constraints, permissions, recovery, retries, abstentions, human intervention and forbidden side effects.

Calibrate an LLM judge against human judgments, blind/randomize candidate order, and inspect disagreements; one model's preference is not ground truth. Separate minor differences from critical errors.

## Record and decide

`case | model/version + provider + effort | harness/prompt | acceptance | severe errors | abstention | human edits | retries/tools | billed cost | first useful output | full elapsed time`

Keep cost and time for failed attempts. Divide total cost by accepted jobs; zero accepted jobs makes cost per success undefined, not zero. Report sample count and variability. A handful of runs cannot establish reliable p95 or a production SLA. Do not present planned tests as measurements.

For stacks, compare to a single-model baseline, including handoff overhead and propagated errors. Agreement between agents is not proof of correctness.

Reject configurations missing hard requirements. Use the same task rubric to compare three objectives: strongest quality, worthwhile quality for full cost, and lowest comparable cost among configurations that pass the user's acceptance floor. One model may win more than one category; different configurations need their own evidence. A cheaper untested model remains a candidate to test, not a demonstrated adequate option. Change effort when a measured benefit justifies it. State ties, sample limits and inconclusive evidence, and use an explicit provisional tie-breaker.

Recheck after changed snapshots, prices, platform/harness, tools, prompts, task distribution, or regressions. Do not schedule monitoring unless requested.

## Basis

[OpenAI evaluation guidance](https://developers.openai.com/api/docs/guides/evaluation-best-practices) recommends task-specific evaluation and human calibration: “Combine metrics with human judgment.” This workflow is platform-independent and does not require the OpenAI Evals service. Check current lifecycle docs before selecting a hosted evaluation service.
