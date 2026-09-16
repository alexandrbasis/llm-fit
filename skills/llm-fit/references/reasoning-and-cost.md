# Reasoning settings and full-task economics

The unit of recommendation is an exact model/version, access route, reasoning configuration and relevant harness. Treat supported controls, defaults, billing rules and output limits as live facts. Use the [source entrypoints](source-map.md), then the exact model and surface documentation; keep no permanent provider-to-setting mapping here.

## Select and verify a configuration

Start with a task hypothesis, not a fixed effort label:

| Work | Starting hypothesis | Evidence for changing it |
|---|---|---|
| Simple extraction, classification, short transformations | Least expensive supported configuration likely to meet the floor | Omissions, ambiguity, schema/tool errors or unacceptable corrections. |
| Routine analysis, drafting, coding or research | Documented default/balanced behavior; compare cheaper configurations for the value ranking | Acceptance, rework, elapsed time and billed cost on representative examples. |
| Difficult debugging, multi-source judgment, planning or long tool workflows | Compare supported configurations with different reasoning budgets/effort | Improvement in correctness or completion sufficient to justify added cost/time. |
| Especially hard asynchronous work | Consider the most capable supported setting when task difficulty warrants it | Improvement over cheaper settings within deadlines and spending limits. |

These are hypotheses to test, not promises that harder thinking always helps. Higher effort cannot supply absent sources, tools, input modalities or a clear goal. A longer answer does not demonstrate better reasoning.

For every recommended configuration, verify at run time:

- Exact snapshot/checkpoint and the requested product, API endpoint, host or runtime.
- Whether reasoning is configurable, automatic, disabled, or not exposed; native names, supported values, defaults and any compatibility restrictions.
- Whether a control means an effort preference, explicit compute/token budget, mode or something else; how it interacts with tools and output limits.
- How reasoning and visible output are billed/capped, including differences between usage reports and displayed text.
- Benchmark configuration versus proposed configuration, with any missing evidence for transferring quality claims.

Use plain language followed by the verified native setting. If unknown, say “setting not verified”; distinguish this from documented automatic behavior. Do not invent a setting or transplant syntax between providers, endpoints or products. Even identical setting names require outcome comparison, not an assumption of equal compute, cost or quality.

For hosted intermediaries, verify both the underlying model and the actual route. For local inference, read the exact publisher card and runtime docs for checkpoint, quantization, context configuration, hardware/memory, license and concurrency. Parameter count alone cannot establish fit or speed. No model-specific examples belong in this reference.

## Compare full cost and useful time

Fetch current official prices for the selected route. Check which charges apply: input/output/reasoning, cache reads/writes, context tiers, tool/search fees, requests, retries and minimum charges. Count each billed class once. Apply discounts only when the workload qualifies; record currency, pricing date and assumptions.

When measurements exist:

```text
model/tool cost per accepted task = cost of all attempted runs / accepted completed tasks
useful output per hour = accepted completed tasks / elapsed workload hours
```

Zero accepted tasks makes cost per success undefined. For heterogeneous work, report per task class or use explicit user-valued units. State workload mix and concurrency; human correction time and infrastructure are separate unless explicitly included in total cost.

Distinguish token throughput, first-token latency, first useful result, full-task elapsed time and throughput under load. Include tool waits, queueing, retries and validation in completion time. Benchmark costs describe that benchmark; they do not predict the user's bill without a workload match.

- **API:** estimate task cost only with stated volume, tokens, steps, success/retry and cache assumptions. If unknown, give unit prices and a scenario/range rather than a fabricated precise bill.
- **Subscription:** verify current plan, access, quotas and expected usage. Compare incremental versus total plan cost explicitly; an already-paid plan is not unlimited free capacity. Token prices do not directly translate into subscription quotas.
- **Local:** account for actual hardware/rental, memory, utilization, concurrency and material operating costs. State whether existing hardware cost is sunk or included. Free weights do not establish free completed work.

## Keep the three decisions distinct

For quality, compare the configurations with the strongest task evidence; cost only breaks ties within hard limits. For value, compare added quality with added full cost, including errors and human correction. An option dominated on both relevant quality and cost needs a specific additional advantage or uncertainty to remain a contender.

The cheapest adequate configuration is the lowest comparable full-cost option among those with supported adequacy in the checked pool. A low unit price does not prove this. If quality or cost ranges overlap, report the ambiguity or conditions that change the winner. If no evidence establishes adequacy, recommend a budget candidate to test without calling it adequate. Its success floor comes from the user's task, not from a generic benchmark cutoff.
