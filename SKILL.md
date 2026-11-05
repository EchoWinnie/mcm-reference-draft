---
name: mcm-reference-draft
description: Produce a concise MCM/ICM mathematical-modeling reference paper from a problem statement and attachments, with models, verified calculations where possible, and a team explanation. 用于美赛数模参考解、精简论文初稿和队伍讨论稿；默认英文论文＋中文思路说明，支持其他输入与说明语言。Use for an end-to-end reference draft, not official submission, standalone translation, or a full contest-production pipeline.
metadata:
  version: "1.0.0"
---

# MCM/ICM Reference Draft

## Outcome and scope

Turn a supplied modeling problem into a coherent, concise reference solution that a team can study, critique, reproduce and develop. The deliverable should resemble a shortened modeling paper, with actual reasoning and supported conclusions, rather than a model-name list, proposal or empty outline.

The default audience is a Chinese modeling team, but the workflow is language-independent. Accept problem statements in any language the host can read. Default to an **English reference paper plus a Chinese team guide** for Chinese-language conversations. For other conversation languages, keep the paper in English and write the team guide in the user's language. Explicit language preferences override both defaults. Do not infer language from a username, storage path or location.

Label the paper once near its start: **Reference draft for team discussion — not a submission-ready report.** This label limits the scope of the deliverable, not the accuracy of the work. Do not deliberately introduce errors, omit required questions or weaken analysis to make it “not submittable.” Reduce exposition and optional sophistication while preserving mathematical validity and evidence.

Use this workflow for requests such as “给这道美赛题一个精简参考解” or “produce a concise MCM reference paper.” If the user requests only model selection, code or a particular section, honor that narrower scope. Actual contest submission, repository publication and other external actions are separate requests.

## Start without a setup questionnaire

1. Read the problem and inspect available attachments. If no problem has been supplied, ask for it; do not invent a contest problem. Identify the year and problem letter only when supported by the material.
2. Map every explicit requirement to an intended output: numbered questions, unnumbered requests, required comparisons, scenarios, and any memo, letter or other communication artifact. Preserve the original task structure; do not assume three questions or infer a fixed model from a problem letter.
3. Record available and missing inputs, units, field meanings and meaningful ambiguity. Use a reasonable stated assumption when it allows progress. Ask only if a missing choice or fact would materially change the problem, while completing independent work.
4. Select paper and guide languages from the rule above. Use Markdown by default. State any consequential assumption in a short progress update, then continue through modeling, computation and writing without approval after every stage.

For full drafts read [deliverables and languages](references/deliverables-and-languages.md). When selecting or checking models, use the relevant parts of [modeling and validation](references/modeling-and-validation.md). [Source notes](references/sources-and-adaptation.md) document design provenance; they are for maintenance, not mandatory live dependencies.

## Work from the question to a defensible answer

### 1. Understand the data and build a tractable modeling route

- Inspect the actual attachments before asserting their columns, periods, size or quality. Check missing values, duplicates, units, time order and obvious physical limits; preserve the original files.
- Select one economical, interpretable main route for each distinct modeling need. Reuse a common model across questions when appropriate. Add a baseline or alternative only when it tests a material choice; do not stack algorithms to appear sophisticated.
- State the problem-specific reason for each modeling choice and its applicability. Separate supplied facts, externally sourced facts, assumptions and decisions.
- Define symbols, units, parameter sources, decision-variable domains and the objective or governing relationships. Include the constraints, initial/boundary conditions or observation model needed for implementation. Explain how outputs answer each requirement and feed later questions.
- For important ambiguity, compare plausible interpretations and show what changes. Do not remove an essential mechanism or constraint merely to make the model easy to solve.

### 2. Solve enough to support the reference paper

- When data and execution tools are available, implement and run a minimal reproducible solution. Save the meaningful code and results used by the report. Merely describing future computations is insufficient when those computations can reasonably be completed now.
- Analytical solutions are valid evidence when the derivation and conditions are shown. A numerical solver is not obligatory for a problem that can be solved directly.
- Choose a bounded scope: establish the baseline, run the main model, check feasibility or errors, and test the most consequential assumption/parameter. Avoid an open-ended hyperparameter search or publication-scale experimentation unless requested.
- Check actual runtime capabilities. Reuse appropriate available tools; a missing optional optimizer may be replaced by a documented equivalent method, small-instance enumeration or a simpler baseline. Do not change operating-system protections or silently alter the mathematical problem.
- For randomness, save the seed and use a small set of repeats when stochastic variability could change conclusions. Report the variability actually measured.
- Check outputs against the original constraints, units and requirements rather than trusting only the solver's success flag. Match the selected checks to the model; see the validation reference.
- Build only figures or tables that support a conclusion. Prefer compact evidence tables when they suffice. Generate data charts from actual data/results; do not use generated images as empirical evidence or enforce a minimum number of charts.

### 3. Keep evidence status visible

Track the status of each important result, not only the report as a whole:

| Status | Meaning | How to report it |
|---|---|---|
| Computed | Actually run using supplied data or verified external data | Give inputs, metric, result and supporting output |
| Analytic | Derived under stated assumptions | Show the relevant derivation, conditions and conclusion |
| Illustrative | Computed or derived from explicitly hypothetical teaching inputs | Mark it as an illustration wherever its results appear; never treat it as an answer from the real data |
| Pending | Required data, computation or validation is unavailable | Explain the specific gap and its consequence; do not manufacture a value |

Missing required data must not silently become synthetic data. Produce the model, symbolic conclusions, input contract and supported portions that are still possible. If the user requests or authorizes a demonstration, a separate hypothetical example can illustrate the method. Otherwise, ask for missing data while continuing the supported work. A reference paper may be explicitly partial; it must still contain substantive material, not blank “TODO” sections.

All quoted performance improvements, rankings, optimal allocations and sensitivity findings must be supported by actual results or derivations. “We will validate” is a plan, not evidence that validation passed. Heuristics do not establish global optimality without an appropriate certificate, exhaustive comparison or proof.

### 4. Write the shortened paper and team guide

- Write the paper in its selected language (English by default) as connected academic prose: problem, model, solution, evidence, answer and limits. Use the report contract rather than a rigid contest template. Keep it concise but complete for the agreed scope.
- Write the summary after the results. It should identify the approach and the strongest supported answers, including partial-result boundaries where necessary; do not reuse the introduction as a summary or put unverified numbers in it.
- In the team guide, explain why the model was chosen, how the questions connect, which assumptions matter, how to reproduce results, and what the team should improve next. This is an actionable handoff, not a line-by-line translation of the paper.
- Include a brief memo or other requested communication artifact if the problem asks for it. Do not invent one merely because a problem is labeled ICM.
- Use references actually inspected, and distinguish source facts from assumptions. Do not invent articles, DOIs, data provenance or award claims.
- Cite the problem's year-specific official instructions if discussing formal requirements. Default reference drafts do not require a control number, official cover sheet, PDF compilation or a submission portal. Record actual AI assistance for the team's later disclosure; do not fabricate model versions or claim formal compliance without checking the applicable rules.

## Deliver and verify

By default save `reference-paper.md` and `team-guide.md` in a task output directory. When numerical work is performed, include `code/`, machine-readable `results/`, and only the figures used by the paper. Use the user's storage preferences; keep task outputs separate from this installed skill. Small scope requests may be answered inline when that is more useful.

Before delivery:

- Check that every requested item has an answer or an explicit, localized evidence gap.
- Check model/code agreement, constraints or applicable numerical diagnostics, and report-to-result consistency, including rounding and uncertainty.
- Confirm the paper is substantive prose with defined equations, interpreted results and model-specific limitations, not an outline or a list of model suggestions.
- Check language choices, local links, rendered math conventions and any supplied memo. State which checks were actually performed.
- End with a short status and links, distinguishing completed reference work from work still needed for a robust contest solution. Do not promise an award, full correctness or submission readiness.

If a defect changes a conclusion, fix the model or calculation and update the paper before finalizing. If progress is blocked, deliver the supported partial draft and identify the smallest missing input or tool needed to continue.
