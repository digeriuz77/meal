---
name: progress-report-draft
description: Reconcile Education monitoring evidence, verify indicator coverage and arithmetic, and draft an editable Quarterly, Semi-Annual, Annual, Final, or Donor Progress Report grounded in project-context/ and verified sources. Use when constructing a progress report or running pre-review evidence reconciliation before independent progress-report-review.
---

# Progress Report Draft and Evidence Reconciliation

## Purpose and Trigger
Operate as a two-stage Construct skill for Education monitoring and reporting:
1. **Stage 1 (Evidence Reconciliation)**: Reconcile indicator coverage, arithmetic, numerators/denominators, period vs. cumulative basis, single-period no-trend limits, cohort comparability, and equity disaggregations from supplied raw trackers, EMIS/LMS extracts, or `project-context/indicator-ledger.md`.
2. **Stage 2 (Report Construction)**: Draft a structured, traceable Quarterly, Semi-Annual, Annual, Final, or Funder-formatted Education Progress Report using [Progress Report Template](./template.md).

This skill does not verify source records in the field or establish causal attribution. Follow every report draft with independent `progress-report-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Monitoring data extract, indicator tracker, activity status log, or `project-context/indicator-ledger.md`.
- Governing framework (Logframe, Results Framework, M&E Plan) or prior comparable period report (when available).
- Report type (`Quarterly`, `Semi-Annual`, `Annual`, `Final`, or named funder format) and reporting window/academic term.

State the active intake mode (`project-context/`, designated folder, or explicit files) and exact files/versions used.

## Procedure

### Stage 1: Reconcile Monitoring Evidence and Arithmetic
1. **Confirm Scope and Reporting Basis**: Identify report type, academic term/period, governing framework, funder format, and whether the task is evidence reconciliation only or full report drafting.
2. **Extract Every Indicator Value with Provenance**: Capture period, academic window, unit, numerator/denominator, eligible learner/educator cohort, cumulative vs. period basis, target, actual, source, and equity disaggregations. Cite `filename#heading`, page, table, or row.
3. **Check Coverage Against Framework**: Compare expected indicators (calibrated to report type; e.g., quarterly focuses on outputs/activities, annual/final covers all outcome/goal indicators) against supplied data. Distinguish `"Not reported in supplied material"` from `"Not collected"`; never turn blank fields into `0`.
4. **Verify Arithmetic and Disaggregation Totals**:
   - Recompute percentages ONLY when numerator, denominator, unit, and population universe are explicit.
   - Check that disaggregated sub-totals (sex, age/grade, disability, geography, institution type) reconcile to totals; report unclassified/missing counts separately.
   - Distinguish **unique learners** from **attendance sessions, coaching contacts, or LMS logins**, and distinguish **enrolled** vs. **active** vs. **completed** vs. **competency-verified**.
   - Show target variance (`actual - target`) alongside percentage of target ONLY when ratio direction is meaningful and definitions/periods match. Do not treat percentage of target alone as an `"on-track"` judgment without supplied time-phased expectations and context, and never invent rating bands or universal target-attainment thresholds.
5. **Assess Period Comparison Eligibility**:
   - Compare across periods ONLY when definitions, units, cohorts/grades, denominators, reporting windows, and cumulative-vs-period basis match. Decline non-comparable comparisons and explain why.
   - Distinguish **percentage-point change** (subtracting two percentages) from **relative percent change** (`(new - old) / old`); state explicitly which is used.
   - **Single-Period Boundary**: If only one period is supplied, perform single-period checks only and state clearly that no trend can be inferred.
   - **Pre/Post Learning Gains**: Keep matched cohorts (`n_pre`, `n_post`, `n_matched`, attrition rate) distinct from unmatched cross-sectional scores, and do not equate simple pre/post gains with causal impact.

### Stage 2: Construct the Education Progress Report
6. **Assemble Standard Sections**: Draft the 10 standard components in [Progress Report Template](./template.md) calibrated to report type:
   - Executive Summary
   - Program & Academic Context Overview
   - Longitudinal Indicator Achievement Table (using the standardized Education ledger columns)
   - Results Narrative by Result Level (covering both achievements and shortfalls; linking qualitative stories only as illustrative examples, never prevalence proof)
   - Activity Progress & Academic Calendar Alignment (`Completed / On Track / Delayed / Cancelled` with evidence and revised timeline proposals)
   - Equity Disaggregation & Learning/Transition Analysis
   - Challenges, Risks & External Assumptions Monitoring
   - Lessons Learned & Proposed Adaptations (tagged `proposed` unless already adopted)
   - Financial Summary & Burn-Rate Alignment (only from supplied financial figures; mark `"Financial data not supplied"` otherwise)
   - Data Quality Limitations, Safeguarding Notes, Unresolved Decisions (`REP-D*`), and Evidence Register
7. **Reconcile Internally Before Delivery**: Verify every figure in narrative matches the indicator table, activity progress aligns with indicator outputs, and financial progress aligns with programmatic claims (if supplied).

## Standalone Check Output Requirement
When running in **Evidence Reconciliation Check Mode** (without full report drafting), include these exact standalone Markdown headings without numbering or abbreviations:
```markdown
## Critical Issues
## Important Issues
## Minor Improvements
```
Write `"None identified from supplied files."` or `"Not assessable from supplied files."` under any empty heading.

## Missing, Conflicting, or Unsuitable Inputs
- **Single period only**: Draft the report covering period performance and explicitly exclude trend claims.
- **Missing definitions or denominators**: Do not compute rates or compare affected values; log `REP-D*` data gaps.
- **Conflicting actuals across trackers**: Present both numbers with Evidence IDs and flag reconciliation as a critical unresolved decision.
- **Missing framework**: Report supplied indicators only without claiming full logframe coverage.
- **Non-MEAL request**: State scope boundary and stop.

## Completion Checklist
- Periods, denominators, cohorts, units, and cumulative vs. period basis are explicit throughout.
- Blank/missing values are never treated as zero or proof of non-collection.
- Single-period inputs carry zero trend claims; pre/post changes carry zero causal attribution claims.
- Narrative covers both successes and off-track/delayed areas accurately matched to table arithmetic.
- Facts, assumptions, proposed adaptations/corrective actions, and unresolved `REP-D*` decisions are clearly separated.
- Next step queues independent `progress-report-review`.
