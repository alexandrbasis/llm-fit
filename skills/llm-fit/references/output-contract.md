# Recommendation output contract

Use these four blocks in order, in the user's language. The first table is the answer; the following blocks substantiate it. Default to a compact answer, roughly 300–500 words including table cells. This is a brevity guide, not a reason to omit material evidence or requested scope. No narrative preamble, standalone user-profile recap, repeated final recommendation or unsolicited evaluation plan.

## 1. Top three models

Present the three strongest feasible candidates established by [ranking-evidence.md](ranking-evidence.md). Assign places only where their relative quality is supported; otherwise mark the affected rows “unresolved” and identify an unordered shortlist once. Always include the recommended reasoning configuration and one concrete reason for each model. Render a real Markdown table using this structure, replacing the placeholders:

```markdown
| Rank / status | Model / platform | Reasoning | Why this model for this task |
| --- | --- | --- | --- |
| Supported place or unresolved | Exact candidate / surface | Verified setting | One task-specific reason |
```

Keep each reason to one sentence linking a task requirement to evidence or an explicit inference. Avoid generic praise. Link exact configuration support through the model/setting cell. Give one starting setting, not a menu of effort levels; add an escalation condition only if it changes the practical recommendation.

If the control is documented as automatic or absent, say so. If the setting is unknown, mark it unverified instead of inventing one. When fewer than three models qualify, provide those and one short reason for the shortfall. Label a proposed setting without adequate outcome evidence as a configuration to test. “Preliminary” qualifies a supported conditional ranking; it cannot substitute for its basis.

Directly below the table, include one short line with the check date and evidence status, for example whether this is a public-evidence comparison or includes real task measurements. Include a material market-scope restriction or discovery gap here; avoid implying a market-wide comparison when only one ecosystem was checked. Mention only assumptions that could change the selection. Do not repeat the user's job description.

## 2. Benchmarks that fit this task

Usually choose two to four current benchmarks or relevant slices. For each, give a linked name and version, the capability measured and why it matters for the stated task, in one short line. Identify a material domain, language or environment mismatch there. A relevant single test is better than padding with unrelated ones.

Read methods using [benchmark-selection.md](benchmark-selection.md), but keep the full benchmark cards in the working ledger. If no suitable public test exists, say so here; preserve the remaining blocks with explicit unknowns.

## 3. Results for these models

Use one comparison matrix. Rows are the selected benchmarks; the first three model columns correspond to the models in block 1, in the same order:

```markdown
| Benchmark / metric / direction | First candidate | Second candidate | Third candidate | What the difference means for this task |
| --- | --- | --- | --- | --- |
| Linked test and metric | Score + tested setting | Score + tested setting | Score + tested setting | Supported interpretation |
```

Populate the cells with verified results, units and the measured reasoning setting. A shared setting may be in a header or a compact note. If only another effort was measured, put “not measured at the recommended setting” first; an optional labeled alternate-setting result is supporting context only. A multi-model completion result belongs to that system, not to a standalone candidate's score cell. Cite the result through the benchmark row label or the cell when it has a different source.

Use “not published” or “not verified” for missing scores, never zero. Show dates/versions or environment differences where needed to avoid a false comparison. If rows are incomparable, state that in the interpretation column instead of numerically ranking them. Explain the metric's meaning and direction briefly: a rating, success rate and partial rubric score are different quantities. Do not average different rows into an invented total.

Interpret each row in one short sentence: who has the stronger relevant evidence, whether the gap is meaningful, and what it supports in the task. Distinguish a supported tie from unknown relative performance. If evidence does not explain the order in block 1, repair the ordering or leave it unresolved. Put any material task-emphasis assumption next to the affected selection. Do not repeat the whole table in paragraphs.

Account briefly for user-named candidates absent from the tables: why they were excluded or what remains unverified. Put quality/identity reasons here and cost/availability reasons in block 4; each requested item needs only one disposition. Do not add a separate market survey or full discovery log.

## 4. Cost efficiency

Use one compact table to compare cost for the models in block 1 and show the top three by value. Add economical alternatives only when they enter the value top three; preserve three distinct models within that ranking. A model shared by both rankings appears once in this table. Use these columns:

```markdown
| Value rank / status | Model + reasoning | Comparable cost | What you gain or give up |
| --- | --- | --- | --- |
| Supported place or unresolved | Exact candidate + setting | Amount, units and basis | Retained quality and useful tradeoff |
```

Mark supported ranks 1–3 for value, “unresolved” where the evidence does not establish relative value, and a dash for a quality finalist outside the value shortlist. Each value recommendation has a supported setting and a one-line explanation of the retained task quality and useful gain or saving. An additional model's quality evidence needs a nearby link; it does not inherit the benchmark scores of the quality finalists. Apply the shared-pool check before excluding it from the quality shortlist.

Prefer observed cost per accepted task. Otherwise show a clearly labeled estimate or current unit prices with units and source. State the cost basis once above the table: API, subscription or local deployment, currency, and any material workload assumption. Do not mix these cost bases or use token prices to claim subscription efficiency. If incompatible routes are compared, separate them within this block and leave unsupported ordering unresolved.

End this block with one line naming the cheapest adequate model and reasoning, the evidence that it meets the task floor, and its quality concession. If adequacy or full task cost is missing, label it the cheapest candidate to test and name the specific missing check. Cheapest means among the checked eligible candidates. Do not quietly replace the user's whole task with a simpler subtask to make a cheap model qualify; any partial-task candidate must be labeled as such.

This final line completes the answer. A detailed validation plan, routing design, API example or extended methodology belongs only in an explicitly requested expansion, or in the relevant block when indispensable to act.

## Final check

- Four blocks in order; no repeated opening or closing winner.
- Every recommended model has an exact supported setting, documented automatic behavior or an explicit verification gap, plus a concrete reason.
- Each numbered place and consequential exclusion is supported; unresolved ordering stays unresolved even when a general caveat is present.
- Discovery covers the permitted market scope; each user-named candidate is accounted for, and any material coverage limit is visible without implying inferiority from missing scores.
- Benchmark choice follows the task; numbers are sourced and tied to the exact tested configuration and system. Task emphasis follows the request or is explicitly conditional.
- Cost uses comparable units; each value position has a quality/cost basis, and missing adequacy is visible where it matters.
- Tables render as Markdown, not code blocks. Each column has its own nonempty header cell, followed immediately by one separator row with the same cell count. Every data row matches that count; escape literal pipes inside cells. Keep cells short, put blank lines around tables, and inspect the rendered table when a preview is available.
