# Choosing and checking a compact modeling solution

Read the parts relevant to the problem. This is a decision guide, not a mandatory catalog of methods.

## Requirement mapping and assumptions

Collect every explicit requested output, including unnumbered tasks and appended letters. Keep its input, mathematical object, constraints, downstream use and expected evidence visible. A letter is a communication deliverable, not necessarily a new mathematical subproblem.

For each important assumption, state its reason, its consequence and one way to test or relax it. Distinguish a fact supplied by the problem from a modeling convenience. If an interpretation makes a later task vacuous, revisit the interpretation before optimizing.

Use a simple baseline to establish what extra complexity earns. Choose model families by the mechanism, available data, decision and constraints, not by contest letter, popularity or a fixed small-sample threshold. Do not force AHP/TOPSIS, grey prediction, neural networks or evolutionary optimization onto every problem.

## Optimization, allocation, routing and scheduling

- Define min/max objective, variable domains, bounds and all resource, capacity, compatibility, timing and dependency constraints.
- Check for a feasible solution before claiming an optimum. If the feasible set is empty, explain the conflicting requirements and analyze an explicitly stated relaxation rather than hiding the infeasibility.
- Use exact enumeration for genuinely small discrete problems, an appropriate solver for larger ones, or a justified heuristic with bounds/comparisons where available.
- Recompute the objective and all constraints from the returned solution, including integer and binary conditions. Rounding a relaxed solution is not a valid feasibility proof.
- Compare the same outcome under changed budgets or constraints. Enlarging a feasible set cannot worsen the exact optimum for an otherwise unchanged optimization objective; investigate violations rather than inventing a causal story.
- For multi-objective decisions, discuss units, normalization and weight origin. Prefer transparent tradeoffs over a single unexplained composite score.

## Prediction, statistics and data analysis

- Define the prediction target, horizon and information available at decision time. Prevent future-data leakage, test-set tuning and transformations fitted on the full dataset before splitting.
- Use a relevant naive baseline, an appropriate time/group split and task-relevant error measures. A fitted curve alone is not out-of-sample validation.
- Distinguish description, prediction and causation. Report uncertainty and extrapolation boundaries appropriate to the actual evidence.
- Missing observations, imputed values and assumptions about measurement errors should remain identifiable. A small sample does not automatically justify a specific named algorithm.

## Mechanistic, dynamic and simulation models

- Specify state variables, units, governing relations, initial/boundary conditions and parameter origins. Check dimensional consistency, signs and limiting cases.
- Separate calibrated parameters from assumptions; examine identifiability when multiple parameter sets fit similarly.
- Use conservation laws, analytic cases, step-size or grid refinement as appropriate. A smooth simulated curve is not validation by itself.
- For stochastic simulation, distinguish numerical sampling uncertainty from uncertain real-world inputs. Save the seed and check stability when material.

## Evaluation, ranking and networks

- For rankings, justify criteria, direction, scaling and weights. Check double-counting of correlated criteria and whether plausible weight changes reverse the recommendation.
- Data-derived weighting does not by itself establish a criterion's real-world importance. State value judgments and stakeholder tradeoffs explicitly.
- For networks, verify direction, connectivity, capacities, conservation, timing and path feasibility as relevant. A shortest path under the wrong edge interpretation does not answer the problem.

## Small, meaningful validation set

Select tests that could actually overturn the proposed answer: a hand-checkable case, an independent objective/constraint calculation, a relevant baseline, a consequential parameter range or a different plausible interpretation.

For sensitivity analysis state what varied, why that range is reasonable, what stayed fixed and what changed in the decision or outcome. Do not call arbitrary variation “robustness” or insert a standard ±10% without context. Robustness requires checking the uncertainty of interest; a nominal optimum alone is not robust.

Record checks and outcomes in the results. A numeric calculation, solver success, executable script and scientifically validated model are distinct claims. Use the strongest claim actually supported, and reflect its limits in the reference paper.
