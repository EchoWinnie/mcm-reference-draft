# Deliverables and language routing

## Language defaults

Resolve two settings independently: `paper_language` and `guide_language`.

1. Explicit instructions take precedence, including mixed-language requests.
2. Without a paper preference, use English for the MCM/ICM-style reference paper.
3. Without a guide preference, use the user's conversation language. Chinese conversation means Simplified Chinese unless the user uses or requests another variant. If there is no usable language signal, use Chinese as the primary-audience fallback.
4. The source problem's language does not override the user's reading language. An English PDF from a Chinese user still normally yields an English paper and Chinese guide. A Spanish request yields an English paper and Spanish guide unless otherwise specified.

Translate domain terms accurately; preserve equations, variable names, dataset fields, source titles and identifiers when required for traceability. Explain uncommon English technical terms in the guide's language. Keep the guide readable without depending on English fluency. If a language or scanned source cannot be read reliably, mark the limitation rather than claiming universal translation accuracy.

## English reference paper

Use roughly **2,000–3,500 English words as a soft budget for a normal multi-question problem**, excluding code and raw outputs. This is a product default, not a COMAP rule or a mandatory target. A small task should be shorter; extend the budget when needed to cover actual requirements. Do not pad prose, remove essential equations or omit questions to meet a count. Markdown has no reliable page count.

Typical structure, adapted to the problem:

1. **Title and draft status** — identify the topic and supplied problem; state once that this is a reference draft for team discussion.
2. **Summary** — usually about 200–350 words for a full draft, shorter for small problems. Present the objective, main models, supported results and important limitations. Draft this last.
3. **Problem and assumptions** — concise requirements, relevant data, defensible assumptions and units. Include only notation used later.
4. **Model development and answers** — organize by the actual questions or a clear dependency chain. For each need, include its mathematical formulation, solution procedure, result or analytic consequence, interpretation and evidence status.
5. **Validation and sensitivity** — report actual feasibility/error checks, baseline comparisons and meaningful perturbations. If some checks remain pending, distinguish them from completed ones.
6. **Strengths, limitations and conclusions** — discuss model-specific tradeoffs and the answer to the real-world question, not generic praise.
7. **Problem-specific communication** — include a memo, letter or other artifact only if requested. Match the intended audience and required language.
8. **References** — include only used, identifiable sources. If no external literature was needed, do not invent a bibliography.

Sections may be merged for brevity. Preserve content rather than enforcing these exact labels or a fixed number of questions. Keep internal script paths and working logs out of the academic narrative; the team guide holds reproduction details.

## Team guide

Default language for the primary audience is Chinese. For a normal task, aim for a compact guide rather than another full paper. Cover:

- **这份参考稿解决了什么**: requirements answered and the location of their results; identify partial answers.
- **建模思路与取舍**: why the main model fits, how questions connect, important assumptions and one worthwhile alternative if relevant.
- **结果可信到什么程度**: actual calculations/checks, data limitations, hypothetical examples and unresolved issues.
- **如何复现**: executable entry point, relative input/output paths, required existing dependencies, key parameters, seeds and the command actually used. Clearly label unexecuted code.
- **队伍下一步**: prioritize a few concrete improvements for modeling, programming and writing, each with a reason or acceptance condition. Avoid vague tasks such as “improve the model.”
- **使用记录**: concise, factual notes on AI help and external sources, useful for the team to prepare any required disclosure. Record unavailable metadata as unavailable.

Localize these headings for other guide languages. A tiny task can combine them into a few paragraphs. The guide explains decisions and limitations, not every line of code.

## Supporting artifacts

Example layout for a numerical task:

```text
output/
  reference-paper.md
  team-guide.md
  code/
    solve.py
  results/
    summary.json
  figures/
    comparison.png
```

Create only needed directories. There is no requirement for a separate planning report, a diagram, a PDF or a fixed chart count. Preserve original attachments and refer to them explicitly or copy authorized inputs into a self-contained package when useful.

For each important numerical result, keep enough machine-readable evidence to recover its input source, assumptions/parameters, method, actual value, units and validation status. A small JSON/CSV with a concise method note is sufficient; no large workflow engine is required. Illustrative and real-data results must remain distinguishable in file names or metadata and in the paper.

Graphs should have readable labels in the paper's language, units, a stated data source and a purpose in the argument. Use valid inline `$...$` and display `$$...$$` math for a Markdown deliverable; inspect generated file formats when exporting.

## Data gaps and partial drafts

When necessary data is missing, write the sections that can be supported: problem formulation, assumptions, symbolic model, identifiability/feasibility reasoning, solution method and precise input requirements. Explain where quantitative conclusions cannot yet be drawn. A missing CSV does not justify an invented “optimal” schedule or fabricated validation metric.

Do not leave generic placeholders such as “insert result here.” Write a substantive limitation, for example: “The route ranking cannot be identified without travel times; the formulation below is executable once those times are provided.” Delivering this as a partial reference is acceptable and must be labeled accordingly.
