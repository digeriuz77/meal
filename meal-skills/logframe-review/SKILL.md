---
name: logframe-review
description: Independently review an Education logframe, logical framework (LFA), or results framework for vertical IF-THEN logic, horizontal measurement coherence, assumptions, and structural completeness. Use after results-chain-alignment or when evaluating a logframe before M&E planning.
---

# Logframe Review

## Purpose and Trigger
Conduct an independent scored review of an Education logframe or results framework across 6 scored sections plus design-flaw flags, enforcing critical-weighting rules, LFA/funder terminology fairness, and traceable recommendations.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- Standard table/matrix, narrative results summary, proposal/design extract, or two versions for comparison.
- **Partial logframes**: Note present vs. missing components, apply checks possible, and mark unassessable dimensions `"Not Assessed"` (label overall summary provisional).
- **Narrative description**: Reconstruct a parsed framework table first; flag unmentioned components as `"not confirmed present"`.
- **Non-text image/screenshot**: Request a readable text or Markdown table export; never infer unseen contents.
- **Non-MEAL input**: Return a brief suitability note and stop.

Always map funder hierarchy labels before scoring using [Funder Formats](../../meal-references/funder-formats.md#1-results-hierarchy-terminology-mapping). For **LFA format** frameworks, apply LFA rules fairly: Intervention Logic, OVIs (Objectively Verifiable Indicators, checked against QQQTT: Quantity, Quality, target group, Time, Place), Sources of Verification, Pre-conditions at activity level, one Specific Objective, and typically 3 to 6 Results. Do NOT penalize activity-level pre-conditions in LFA logframes.

## Scoring Thresholds
- **PASS**: All or nearly all checklist items satisfied; minor gaps only.
- **PARTIAL**: Majority satisfied, 1 to 2 significant gaps.
- **FAIL**: Fundamental requirements missing or major structural/logic breaks.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Structural Completeness** or **Vertical Logic** automatically triggers **Major Issues**.

## Six Scored Review Sections (Plus Common Design Flaws)

### 1. Structural Completeness (Critical Weight)
- Four standard columns present and populated: Narrative Summary / Intervention Logic, Indicators / OVIs (with baselines & targets), Means / Sources of Verification, and Assumptions.
- Complete top-to-bottom hierarchy: Goal/Impact -> Outcome(s)/Purpose -> Output(s) -> Activities (process milestones or completion criteria at activity level; pre-conditions for LFA).
- Every result level has at least one indicator and specified data source; assumptions appear at each level transition.

### 2. Vertical Logic (Critical Weight)
Test bottom-up `IF-THEN` plausibility:
- `IF` inputs AND pre-conditions/assumptions hold -> activities completed.
- `IF` activities completed AND assumptions hold -> outputs produced.
- `IF` outputs achieved AND assumptions hold -> Education outcomes occur (verify educator practice, enrollment/attendance, retention, and learning links across the Education causal chain).
- `IF` outcomes occur AND assumptions hold -> Goal contributed to realistically.
Check for orphan outputs/outcomes, missing intermediate steps, and outputs disguised as activities or outcomes disguised as outputs.

### 3. Horizontal Logic (Measurement)
- Indicators directly measure the attached result statement (not weak proxies).
- Specific named data sources (e.g., `"Termly EMIS school register"`, `"EGRA Grade 3 assessment"`, not generic `"project reports"`), consistent across time and feasible.
- Targets referenced to quantified baselines; Education equity disaggregation dimensions (sex, age/grade, disability, geography) specified.
- Focused indicator volume (typically `1-2` at Goal, `2-3` per Outcome/Output).

### 4. Assumptions Analysis
- External factors outside program control, written as positive conditions (`"Ministry maintains curriculum release schedule"`), not risks (`"No strikes"`) or internal management duties (`"Project hires coaches on time"`).
- Critical assumptions carry monitoring triggers/mitigation notes; minimal assumptions at activity level.

### 5. Indicator Quality Quick Check
Rapid SMART check (Specific, Measurable, Achievable, Relevant, Time-bound) or QQQTT check for OVIs. Flag any indicator failing `2+` criteria and recommend `indicator-quality-review` for deep per-indicator scoring.
- **Large logframes (>10 outputs or 30+ indicators)**: Assess a representative sample of 5 to 6 indicators across levels, document systemic patterns (e.g., `"all Outcome indicators count workshop attendance"`), and flag disproportionate size.

### 6. Strategic Considerations
- Alignment with Theory of Change pathways.
- Cross-cutting Education inclusion: gender differentiation, disability inclusion (WG/CFM), safe learning environment/safeguarding, and climate/school resilience where relevant.
- Post-project institutional sustainability and government/school ownership indicators.

### 7. Common Design Flaws (Fold Into Sections 1 to 6; No Separate Score)
Outputs stated as activities (`"Conduct teacher workshops"` vs. `"120 teachers trained in structured pedagogy"`); outcomes stated as outputs; excessive indicator counts; missing baselines; generic copied donor text; missing equity disaggregation; circular indicator restating result.

## Output Format
Produce clean editable Markdown with:
1. **Logframe Review Summary**: Intake Mode, Funder Format Identified, Overall Rating, and 6-row Score Summary table (`PASS / PARTIAL / FAIL / Not Assessed`).
2. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Always keep all three headings; write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
3. **Priority Recommendations** (max 5, specific level/indicator citations).
4. **Detailed Findings** across Sections 1 to 6 plus **Detailed Findings Table** (`Level | Result | Issue | Severity | Recommendation | Evidence ID`) and **Design Flaw Flags**.

## Output Rules and Resumption
- Distinguish `"approval status not supplied"` from confirmed approval; distinguish structural format differences (e.g., LFA) from substantive logic flaws.
- Keep facts, interpretations, assumptions, and proposed fixes separate. On resume, re-validate source versions and prior claims against original files.
