# Recommendation output contract

Use these four blocks in order, in the user's language. The first table is the answer; the following blocks substantiate it. Default to a compact answer, roughly 300–500 words including table cells. This is a brevity guide, not a reason to omit material evidence or requested scope. No narrative preamble, standalone user-profile recap, repeated final recommendation or unsolicited evaluation plan.

## 1. Top three models

Rank the three strongest feasible models for the task's quality requirements. Always include the recommended reasoning configuration and one concrete reason for each model. Use this table:

`Rank | Model / platform | Reasoning | Why this model for this task`

Keep each reason to one sentence linking a task requirement to evidence or an explicit inference. Avoid generic praise. Link exact configuration support through the model/setting cell. Give one starting setting, not a menu of effort levels; add an escalation condition only if it changes the practical recommendation.

If the control is documented as automatic or absent, say so. If the setting is unknown, mark it unverified instead of inventing one. When fewer than three models qualify, provide those and one short reason for the shortfall. Unknown task superiority means a provisional order, not a fabricated quality claim.

Directly below the table, include one short line with the check date and evidence status, for example whether this is a public-evidence comparison or includes real task measurements. Mention only assumptions that could change the selection. Do not repeat the user's job description.

## 2. Benchmarks that fit this task

Usually choose two to four current benchmarks or relevant slices. For each, give a linked name and version, the capability measured and why it matters for the stated task, in one short line. Identify a material domain, language or environment mismatch there. A relevant single test is better than padding with unrelated ones.

Read methods using [benchmark-selection.md](benchmark-selection.md), but keep the full benchmark cards in the working ledger. If no suitable public test exists, say so here; preserve the remaining blocks with explicit unknowns.

## 3. Results for these models

Use one comparison matrix. Rows are the selected benchmarks; the first three model columns correspond to the models in block 1, in the same order:

`Benchmark / metric / direction | First model | Second model | Third model | What the difference means for this task`

Populate the cells with verified results, units and the measured reasoning setting. A shared setting may be in a header or a compact note; when it differs from the recommendation, show it in the affected cell. Never present a score at another setting as a measurement of the recommended configuration. Cite the result through the benchmark row label or the cell when it has a different source.

Use “not published” or “not verified” for missing scores, never zero. Show dates/versions or environment differences where needed to avoid a false comparison. If rows are incomparable, state that in the interpretation column instead of numerically ranking them. Explain the metric's meaning and direction briefly: a rating, success rate and partial rubric score are different quantities. Do not average different rows into an invented total.

Interpret each row in one short sentence: who has the stronger relevant evidence, whether the gap is meaningful, and what it supports in the task. State a tie or unknown when uncertainty prevents a winner. If evidence does not explain the order in block 1, mark that order provisional and identify the tie-breaker. Do not repeat the whole table in paragraphs.

## 4. Cost efficiency

Use one compact table to compare cost for the models in block 1 and show the top three by value. Add economical alternatives only when they enter the value top three; preserve three distinct models within that ranking. A model shared by both rankings appears once in this table. Use these columns:

`Value rank | Model + reasoning | Comparable cost | What you gain or give up`

Mark ranks 1–3 for value, and a dash for a quality finalist outside the value top three. If the order is unverified, label it provisional once. Each value recommendation has a supported setting and a one-line task-specific reason. An additional model's quality evidence needs a nearby link; it does not inherit the benchmark scores of the quality finalists.

Prefer observed cost per accepted task. Otherwise show a clearly labeled estimate or current unit prices with units and source. State the cost basis once above the table: API, subscription or local deployment, currency, and any material workload assumption. Do not mix these cost bases or use token prices to claim subscription efficiency. If incompatible routes are compared, separate them within this block and leave unsupported ordering unresolved.

End this block with one line naming the cheapest adequate model and reasoning, the evidence that it meets the task floor, and its quality concession. If adequacy or full task cost is missing, label it the cheapest candidate to test and name the specific missing check. Cheapest means among the checked eligible candidates. Do not quietly replace the user's whole task with a simpler subtask to make a cheap model qualify; any partial-task candidate must be labeled as such.

This final line completes the answer. A detailed validation plan, routing design, API example or extended methodology belongs only in an explicitly requested expansion, or in the relevant block when indispensable to act.

## Final check

- Four blocks in order; no repeated opening or closing winner.
- Every recommended model has an exact supported setting, documented automatic behavior or an explicit verification gap, plus a concrete reason.
- Benchmark choice follows the task; numbers are sourced and correctly tied to measured configurations.
- Cost uses comparable units; provisional rankings and missing adequacy are visible where they matter.
- Tables use valid Markdown: separate header cells, one separator row and consistent column counts. Keep cells short and put blank lines around tables.
