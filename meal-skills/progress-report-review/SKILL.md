---
name: progress-report-review
description: Independently review an Education progress, quarterly, semi-annual, annual, final, or donor report for indicator coverage, arithmetic and denominator verification, single-period no-trend compliance, equity disaggregation, narrative-data alignment, and internal consistency. Use after progress-report-draft.
---

# Progress Report Review

## Purpose and Trigger
Conduct an independent 10-dimension quality review and evidence reconciliation audit of an Education progress or donor report. Verify that reported performance numbers reconcile mathematically, comparisons respect period/cohort/denominator boundaries, narrative explains both progress and shortfalls honestly, and recommendations are feasible.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Quarterly report** -> calibrate to output indicators, activity progress, financial alignment (outcome indicators optional unless scheduled).
- **Semi-annual report** -> output + scheduled outcome indicators, mid-year reflection.
- **Annual / Final report** -> all indicators (cumulative + period), full narrative, learning/sustainability.
- **Funder-specific format** -> check funder format requirements from [Funder Formats](../../meal-references/funder-formats.md#2-funder-me-and-reporting-format-expectations) alongside quality standards.
- **Indicator table only** -> score Sections 1 to 4 in full; mark narrative sections `"Not Assessed"` (provisional rating).
- **Narrative only** -> score Sections 5 to 9; flag inability to verify Data Plausibility without indicator table.
- **Partial / Draft** -> review present sections without treating intentional omissions as full-report failures.
- **Non-MEAL input** -> return suitability note and stop.

State intake mode, document classification, reporting period, and source Evidence IDs (`filename#heading`, page, table, row).

## Scoring Thresholds
- **PASS**: Complete, arithmetically verified, and well-explained.
- **PARTIAL**: Present with significant gaps, missing explanations, or reconciliation defects.
- **FAIL**: Missing, contains implausible/contradictory numbers, or violates comparison integrity.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, exactly `2 PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Data Plausibility** automatically triggers **Major Issues**.

## Indicator Achievement and Reconciliation Standards
- Compute percentage of target ONLY when ratio direction is meaningful and actual/target share exact definitions and reporting basis. Show actual, target, arithmetic, and gap.
- Percentage of target is NOT an `"on-track"` judgment (which requires supplied time-phased expectations and context). Never invent universal percentage rating bands (`>=100%`, `80-99%`, etc.) to judge severity. For lower-is-better or zero-target indicators, interpret gap directly.
- **Single-Period vs. Multi-Period Rule**: Single-period reports permit period-vs.-target checks ONLY. A baseline or end-of-project target is NOT a prior reporting period; forbid trend claims on single-period inputs. For two+ periods, verify identical definitions, learner cohorts, denominators, reporting windows, and cumulative-vs.-period basis; never sum cumulative totals across periods; distinguish percentage-point change from relative percent change.
- **Counts, Rates, and Missing Data**: Never equate blank/missing with zero or `"not reported"` with `"not collected"`. Distinguish unique learners from attendance events, workshops, or LMS logins. Flag red flags: achievement `> 150%`, exact `100%` clustering across multiple indicators, unexplained cohort jumps, silent definition changes, or population exceedance.

## Ten Review Dimensions

### 1. Indicator Coverage
All expected indicators for the report type reported; new, deferred, or modified indicators explained; consistent definitions across periods.

### 2. Data Completeness
Baseline, target, actual, source citation, unit, numerator/denominator, and period vs. cumulative label clear for every reported indicator.

### 3. Data Plausibility and Arithmetic (Critical Weight)
Percentages match numerator/denominator; disaggregated totals reconcile; cohort attrition (`n_pre`, `n_post`, `n_matched`) and LMS completion vs. competency match records; numbers realistic given academic calendar, school count, and budget.

### 4. Equity Disaggregation
Sex, age/grade band, disability status (WG/CFM), geography/urban-rural, institution type, and study track disaggregated where required; unclassified/missing counts shown separately without distorting sub-totals.

### 5. Narrative-Data Alignment
Discusses both successes and shortfalls; claims backed by cited table numbers; challenges linked to affected indicators; anecdotes/success stories labeled illustrative rather than prevalence proof; zero unsupported causal impact claims from routine monitoring.

### 6. Variance Explanation
Below-target indicators explained with root causes and specific, time-bound corrective proposals (`proposed` until approved); large target exceedances checked for DQA/capitation bias.

### 7. Activity Progress
Activities carry clear status (`Completed / On Track / Delayed / Cancelled`) aligned to academic term timing, with evidence and revised timeline proposals for delays.

### 8. Financial Alignment
Burn rate and budget vs. actual expenditure (if supplied) align proportionately with activity/output delivery; mark `"Not Assessed"` if financial figures were excluded by scope.

### 9. Lessons and Adaptation
Evidence-grounded, non-generic lessons linked directly to program decisions or proposed adaptations rather than repeated verbatim from prior reports.

### 10. Internal Consistency
Cross-check indicator table <-> narrative <-> activity table <-> financial summary <-> prior periods <-> multi-partner aggregation (flagging double-counting across partner schools).

## Output Format
1. **Progress Report Review Summary**: Intake Mode, Report Type, Reporting Period, Overall Rating, and 10-row Score Summary table.
2. **Comparison Eligibility & Arithmetic Audit Table** (where multi-period or percentage checks apply).
3. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
4. **Priority Recommendations** (citing exact numbers and Evidence IDs; distinguish wrong data from missing disclosures; avoid repeating identical fixes across sections).
5. **Detailed Findings** (Sections 1 to 10) and **Design Flaw Flags**.
6. **Unresolved Decisions (`REP-D*`)**.
