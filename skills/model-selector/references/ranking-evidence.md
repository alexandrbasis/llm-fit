# Establish the comparison before assigning places

Use this sequence internally before drafting the four output blocks. A recommendation may be an inference from public task proxies, but the stated evidence must support that inference. A caveat cannot repair an unsupported ranking.

## 1. Identify what was actually evaluated

For each result record the exact model/version, reasoning configuration, provider/route, harness, tools, budget and participating models. Distinguish the model doing the task from a grader that only evaluates its output.

Treat a fallback, routing chain, ensemble or helper model as part of the evaluated system whenever it contributes to completion. Attribute the result to that system. It can support a recommendation of the same feasible system, not a standalone-model score. For a standalone candidate, mark such a score as unavailable and mention the system result only as separately labeled context. Grading by another model alone does not make the contestant a multi-model system; assess judge limitations instead.

A benchmark harness may be a useful proxy for the user's environment. Record the transfer gap. A different reasoning setting, snapshot or contributing model is a different tested configuration, not merely an environment caveat.

## 2. Build one candidate comparison

Apply hard constraints, then compare the shared pool across the task's important capabilities. Quality contenders include inexpensive candidates and specialists. Price labels, provider reputation and placement in the value list do not determine eligibility for the quality list.

When a candidate outside the quality shortlist has a stronger relevant result, resolve why before finalizing: include it, identify a material constraint or task-evidence disadvantage, or leave the comparison unresolved. A result at a different effort is a reason to investigate, not an automatic promotion or dismissal. Show a short exclusion reason only when it changes the user's understanding; keep the full pool in the working ledger.

For quality, consider each model's strongest supported, feasible configuration with relevant evidence. For value, separately consider configurations that may reduce full cost. Neither maximum effort nor a default daily-use setting is automatically best. State the evidence or task-based hypothesis behind the recommended effort; keep unsupported configurations as candidates to test rather than transferring measured scores to them.

## 3. Resolve the task comparison

Use requirements, failure consequences and workload proportions supplied by the user to interpret conflicting results. A mixed task remains mixed unless the request establishes a dominant capability. If an assumed task emphasis changes the winner, state that condition next to the selection or leave the overall order unresolved. Clarify the work itself only when needed; the interview still never asks the user to choose among quality, value and low cost.

For each proposed place, check:

- Which comparable evidence favors this configuration over the next plausible alternative for this task?
- Does the advantage concern the recommended configuration and the evaluated system being recommended?
- Does a conflicting result, uncertainty range or excluded contender change that conclusion?

Public evidence can support a conditional ranking without a paid trial. State the actual condition. Where relative superiority remains unknown, present three eligible candidates without numbered places, or use a partial order with the unresolved positions marked. Use a tie only when the evidence supports a tie; missing evidence is not equality. A presentation order or proposed test order is not a quality rank. Cost/time may break an established quality tie within the user's constraints.

## 4. Establish value separately

Use the full-cost basis in [reasoning-and-cost.md](reasoning-and-cost.md). Each value place must explain the retained task quality and the useful gain or saving relative to the adjacent plausible alternative. Measured task cost is strongest; a supported workload estimate or clearly stated scenario can also support a conditional order.

Unit prices alone establish a tariff comparison. When task quality, configuration-specific cost or acceptance is unresolved, keep the candidates and prices but leave the value order unresolved. A cheap candidate may still belong in the shortlist; an unsupported numbered position does not become valid by calling it preliminary. Preserve the distinction between cheapest adequate and cheapest candidate to test.

## 5. Check the recommendation against the matrix

Finish the comparison before writing the model table. Read the two together once drafted: each superiority claim must follow from the displayed evidence or a nearby explicit inference, and every system/configuration mismatch must affect the claim it limits. Repair a contradiction by changing the claim, the selected configuration or the ordering, rather than appending a general disclaimer. Keep the required four-block output concise using [output-contract.md](output-contract.md).
