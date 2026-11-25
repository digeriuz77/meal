---
name: me-plan-review
description: Independently review an Education M&E, MEL, or MEAL plan, PMP, or indicator framework across eight operational dimensions for coherence, practical collection, roles, quality assurance, safeguarding, and reporting routines. Use after me-plan-draft or when reviewing any operational monitoring plan.
---

# M&E / MEL / MEAL Plan Review

## Purpose and Trigger
Conduct an independent operational review of an Education M&E / MEL / MEAL plan across 8 scored dimensions to verify that the plan is complete, internally coherent, aligned to the academic calendar, and realistic to implement rather than aspirational boilerplate.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Full M&E / MEAL / MEL Plan**: All operational sections present -> apply full 8-dimension review. (Note: a full plan whose sections are vague or aspirational scores `PARTIAL` or `FAIL`, NOT `"Partial / Draft"`.)
- **Performance Management Plan (PMP)**: Full review; note intentionally lighter process sections.
- **Indicator Framework / Reference Sheets**: Assess Sections 2 and 3 in full; mark Sections 4 to 7 `"Not Assessed (out of scope)"`.
- **High-Level M&E Framework**: Strategic check; note operational details may sit in a companion manual.
- **Data Management Plan**: Focus on Sections 3, 5, and 6; mark evaluation-only scope `"Not Assessed"`.
- **Partial / Draft**: Structural sections absent by design -> review present sections, flag omissions as `"needs development"`, and label overall summary provisional.
- **Non-MEAL input**: Return suitability note and stop.

State intake mode, document classification, funder format (if named), and source Evidence IDs (`filename#heading`, page, table, row).

## Scoring Thresholds
- **PASS**: Complete, coherent, and operationally credible.
- **PARTIAL**: Present with significant gaps or inconsistencies.
- **FAIL**: Missing, fundamentally flawed, or blocks M&E implementation.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, exactly `2 PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Structural Completeness** or **Indicator Framework Quality** automatically triggers **Major Issues**.

## Eight Review Dimensions

### 1. Structural Completeness (Critical Weight)
Check presence and substance of: results framework link, indicator definitions/IRS, data collection plan, roles/responsibilities, reporting schedule, quality assurance/safeguarding, evaluation calendar, and resource/budget section across the full M&E cycle (not merely a copied logframe).

### 2. Indicator Framework Quality (Critical Weight)
- Indicators match scope and reporting obligations without demanding impossible goal-level attribution; balanced beyond activity counts.
- Each indicator has definition, named source, baseline, target, frequency, and Education equity disaggregation; SDG 4 / UNESCO UIS / funder standard indicators preserved intact; proportionate set size (flag `>30`).
- Refer once to `indicator-quality-review` if deep per-indicator SMART scoring is needed.

### 3. Data Collection Plan
- Methods, specific tools (assessment rubrics, observation guides, EMIS/LMS queries, surveys), collection frequencies, sampling logic, baseline protocol, and collection owners specified per indicator.
- Flag unverified secondary EMIS/LMS access, software names without tool readiness (`"KoboToolbox"` without validation/translation details), and unaligned school-calendar timing.

### 4. Roles, Responsibilities, and Capacity
- Distributed across M&E staff, program/pedagogical staff, teachers/school heads, and partners (never dumping all work on a single M&E Coordinator).
- Supervisory/IRR roles, enumerator/observer training plans, partner capacity, and safeguarding clearance addressed.

### 5. Reporting Framework and Learning (CLA)
- Distinct collection, analysis, and reporting frequencies per audience (funder, Ministry/schools, communities/parents, internal team).
- Concrete learning routines and feedback loops linking evidence review meetings to program adaptation decisions.

### 6. Quality Assurance, Safeguarding, and Data Protection
- Ongoing VIPRT DQA protocols (not one-time checks), spot-checks/re-abstraction, observation IRR calibration, error/outlier handling, and tool version control.
- Child assent, guardian consent, IRB/Ministry approvals, and minor PII security rules explicit.

### 7. Evaluation Planning
- Evaluation types (baseline, midline, endline, process, impact), decision links, preliminary questions, independence provisions, and dedicated evaluation budget (mark `"Not Assessed"` if out of scope for document type).

### 8. Internal Consistency
Cross-check indicators <-> collection methods <-> roles/capacity <-> reporting vs. collection frequency <-> evaluation use of routine monitoring. Flag operational blockers (e.g., monthly reporting tied to termly/annual collection) as Critical Issues.

## Common Design Flaws (Fold Into Sections 1 to 8)
Logframe copied without operational detail; donor-only compliance boilerplate; single M&E staff overload; missing baseline plan; upward-only reporting with zero school/community feedback; static plan with no adaptation loop; evaluation listed without budget or independence.

## Output Format
1. **M&E Plan Review Summary**: Intake Mode, Document Type, Overall Rating (note provisional if partial), and 8-row Score Summary table.
2. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
3. **Priority Recommendations** (3 to 5 concrete items).
4. **Detailed Findings** (Sections 1 to 8) and **Design Flaw Flags**.
5. **Evidence & Unresolved Decisions Register (`MEAS-D*`)**.

## Output Rules and Resumption
- Distinguish `"existing"` from `"approved"` (`"approval status not supplied"` when silent); never treat missing QA or consent records in text as proof the real-world safeguard never occurred.
- Keep facts, calculations, assumptions, and proposed revisions strictly separate. On resume, verify inherited claims against original files.
