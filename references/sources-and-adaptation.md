# Sources and adaptation decisions

Reviewed on 2026-11-05. These links document design influences; they are not installed dependencies. Instructions and examples in this package are newly written for a concise, multilingual reference-draft workflow. Upstream scripts, templates and applications were not installed or executed.

## Sources adopted at the workflow level

### XiaoMaColtAI/math-modeling-skill

- [SkillsMP listing](https://skillsmp.com/creators/xiaomacoltai/math-modeling-skill/skill)
- [Original SKILL.md](https://github.com/XiaoMaColtAI/math-modeling-skill/blob/main/SKILL.md)

The inspected entry separates modeling, implementation and writing and describes papers as reference material. This skill keeps that dependency order and result-to-paper consistency. It omits compulsory graph quotas, multiple heavyweight gates and dual-format publication, because those are unnecessary for a compact team reference.

### jihe520/MathModelAgent

- [Project](https://github.com/jihe520/MathModelAgent)
- [Analysis and modeling instructions](https://github.com/jihe520/MathModelAgent/blob/main/skills/2analysis-modeling/SKILL.md)

The inspected instructions connect problem requirements, assumptions, variables, constraints and implementation. This skill retains that handoff but produces a single shortened paper and team guide rather than the full stage-report suite. It maps unnumbered requirements as well as numbered tasks, important for varied MCM/ICM problem statements. The local installation was also inspected as a reference, not activated as the full workflow.

### woodfishhhh/EZ_math_model

- [Project skill](https://github.com/woodfishhhh/EZ_math_model/blob/main/skills/ez-math-model/SKILL.md)
- [Run-mode protocol](https://github.com/woodfishhhh/EZ_math_model/blob/main/skills/ez-math-model/references/run-mode-protocol.md)

The inspected protocol separates results from supplied data, authorized demonstrations and missing-input cases. This skill adapts that idea to result-level evidence labels so analytic or supported partial work can still be delivered. It does not require upstream setup state, external runtimes or synthetic fallback data.

## MCM/ICM source of authority

- [COMAP official instructions](https://www.contest.comap.com/undergraduate/contests/mcm/instructions.html)

The page inspected on 2026-11-05 describes the 2027 contest, including an English PDF, a Summary Sheet, a 25-page solution limit and AI-use reporting. Those are dated official-submission requirements, not the length or format of this Markdown reference product. For an actual contest task, retrieve the relevant year's official instructions and problem; do not apply the latest year's rules to an older task automatically.

The design borrows the emphasis on a result-focused summary, explicit assumptions, model explanation, validation and clear conclusions. This skill does not submit files or certify compliance. A team can use its factual AI-assistance record when preparing disclosures required by the applicable contest rules.

## Example of a source not adopted as authority

[A community MCM competition pack](https://github.com/handsomeZR-netizen/mathmodel-skill/blob/main/competitions/mcm/README.md) was also inspected. The fetched seed version contained claims about unlimited pages and mandatory letters that should not be treated as general rules. This package takes page/format rules from the applicable official source and communication requirements from the actual problem statement. Repository popularity, marketing promises and self-assigned quality scores are not evidence of contest performance.
