# Adaptive task interview

Clarify only missing task details, acceptance criteria and operational constraints. Reuse answers in the conversation. Ask in the user's language, at most three questions at once; prefer a concrete example over a long questionnaire. The user describes work; the skill selects benchmarks.

Quality leaders, value leaders and the cheapest adequate option are all required outputs by default. Never turn them into an interview choice: do not ask what matters more among quality, balance, speed or minimum cost, which main-model objective to optimize, or what would justify paying extra. Concrete spending ceilings, deadlines and acceptable errors may still need clarification because they define feasibility, not which comparison to produce. If the task and constraints are already clear, proceed directly to all three comparisons.

## No task yet

“Для какой конкретной задачи выбираем модель? Опишите, что дадите на вход и какой результат хотите получить. Можно на одном примере.”

Wait for this answer before producing a task-specific ranking. You may research platforms independently, but do not invent the job.

## Core decisions

| Unresolved decision | Natural question | Effect on selection |
|---|---|---|
| Actual success | “Как выглядит отличный результат, а какой уже достаточно хорош для работы? Какие исправления допустимы?” | Separates ideal quality from the minimum floor for economical choices. |
| Budget | “Есть жёсткий предел расходов? Какой объём задач ожидается?” | Establishes a feasibility constraint and enables full-cost estimates for all three objectives. |
| Surface | “Где будете пользоваться моделью: в готовом приложении, через API или локально? Какие варианты уже доступны?” | Filters availability, settings, tools, billing. |
| Autonomy | “Вы будете проверять каждый шаг или агент должен сам выполнить работу? Это один ответ или длинная задача?” | Distinguishes response quality from completion, recovery, and oversight. |
| Errors | “Какие ошибки недопустимы? Когда лучше уточнить у вас или честно сказать, что данных недостаточно?” | Defines error/abstention thresholds and constraints. |

## Ask only on the relevant branch

| Branch | Follow-up | Evidence to seek |
|---|---|---|
| Research/facts | “Нужен поиск свежих данных или работа только с вашими материалами? Нужны проверяемые ссылки?” | Retrieval, grounded citations, coverage and error. |
| Business agent | “С какими приложениями он работает и какие действия запрещены даже ради результата?” | Domain/app slices, tools, completion with compliance. |
| Coding | “Что именно: небольшие правки, сложная ошибка, ревью или большой самостоятельный проект? Какая среда и чем проверяется результат?” | Matching repository/terminal tasks, tests, harness. |
| Writing/translation | “Для кого текст, на каком языке и что важно в стиле? Есть пример хорошего результата?” | Language-specific blind review, factual fidelity. |
| Documents/media | “Какие файлы и какого объёма? Нужен анализ, точное извлечение или создание нового материала?” | Input/output modalities, OCR/layout/media limits, task rubric. |
| Long context | “Нужно найти фрагмент или сопоставить сведения по всему документу? Какой обычный и максимальный объём?” | Retrieval versus integration at actual lengths. |
| Volume/latency | “Сколько задач в день и одновременно? Какое ожидание допустимо для первого полезного ответа и полного результата?” | Throughput, rate limits, queueing, elapsed time and cost. |
| Local/private | “Какие ограничения на передачу данных? Какое оборудование, память, длина контекста и число параллельных запросов?” | Exact weights/quantization, runtime, licensing, feasibility. |
| Existing setup | “Что сейчас используете? Есть пример задачи, с которой текущая модель не справилась?” | Establishes the baseline and concrete failure cases without selecting an objective. |
| Delegation | “Должен ли агент распределять работу и восстанавливаться после ошибок без вашего участия?” | Handoffs, recovery, state, end-to-end success. |

## Stop asking

Once task, constraints and acceptance floor suffice, research and produce all three comparisons. An absent priority order is not missing information and never blocks selection. Do not ask every question here. If the user cannot give numbers, use qualitative acceptance criteria and labeled ranges/unknowns. Keep “adequacy unknown” distinct from an assumed success threshold. Do not default to coding, maximum reasoning, unlimited spending, or autonomous actions.

These are an adapted interview, not verbatim video quotations. The video-origin reference identifies the author's actual questions and our operational additions.
