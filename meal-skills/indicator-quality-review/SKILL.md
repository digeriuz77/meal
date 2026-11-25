---
name: indicator-quality-review
description: Independently review Education M&E indicators, KPIs, or Indicator Reference Sheets (IRS / PIRS) for SMART and CREAM quality, operational definition precision, equity disaggregation, data burden, and result-level accuracy. Use after indicator-reference-sheets or when evaluating any indicator set.
---

# Indicator Quality Review

## Purpose and Trigger
Conduct an independent quality assessment of Education indicators, KPIs, and Indicator Reference Sheets (IRS / PIRS) using anchored 1 to 5 SMART scoring, formulation rules, standard Education indicator protection, equity disaggregation checks, and set-level balance diagnostics.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Verify input contains actual indicators before scoring:
- List/table, CSV/spreadsheet columns, logframe extract, full IRS/PIRS, or user description.
- **Meta-documents (checklists/templates about indicators)**: Inform user and assess only embedded real indicators if present.
- **Evaluation questions**: Redirect to `evaluation-tor-review`.
- **Activity statements (`"Run 10 coaching sessions"`)**: Flag as activity, not indicator, and suggest output/outcome phrasing.
- **Non-MEAL input**: Return suitability note and stop.

State intake mode (`project-context/`, designated folder, or explicit files) and exact source IDs (`filename#heading`, page, table, row).

## SMART Scoring Anchors (1 to 5 Scale)
Score each supplied dimension; mark missing target or timeframe as `N/A` rather than penalizing an indicator statement for fields held in another document:
- **S (Specific, 1 to 5)**: `5` = quantity, quality standard, target learner/educator population, and geography explicit; `3` = states measure but misses population or location; `1` = undefined/unmeasurable concept.
- **M (Measurable, 1 to 5)**: `5` = named source, collection tool, and calculation/analysis plan; `3` = measurable construct with unclear/unverified source; `1` = no feasible consistent measurement.
- **A (Achievable, 1 to 5)**: `5` = target grounded in baseline/evidence/rationale; `3` = plausible without cited evidence; `1` = supplied target unrealistic against evidence; `N/A` if no target supplied.
- **R (Relevant, 1 to 5)**: `5` = directly measures attached result along the Education causal chain; `3` = acknowledged proxy; `1` = measures unrelated construct.
- **T (Time-bound, 1 to 5)**: `5` = specific dates/academic term milestones; `3` = general timeframe; `1` = no timeframe; `N/A` if no timeframe supplied.

**Composite SMART Score**: Average of scored dimensions ONLY (exclude `N/A`). If `< 5` dimensions scored, report provisionally (e.g., `"3.3/5.0 (3 dimensions scored)"`). Flag any indicator with composite `< 3.0` OR any single dimension equal to `1`.

## Overall Quality Rating Thresholds
- **Strong**: All indicators score `3.5+` composite AND zero critical formulation issues.
- **Mixed**: Some indicators above `3.0`, some below, or systemic single-dimension gap (e.g., all lack equity disaggregation).
- **Needs Work**: Any indicator `< 3.0` composite, OR `> 2` critical formulation issues, OR majority missing data sources or disaggregation.
*(Keep numerical SMART anchors diagnostic; do not conflate them with statistical estimates or document section PASS/FAIL ratings.)*

## Core Technical Checks per Indicator
1. **Result-Level Placement**: Distinguish Activity -> Output -> Intermediate Outcome -> Outcome -> Goal along the [Education Causal Chain Ladder](../../meal-references/education-meal-standards.md#1-education-causal-chain-ladder).
2. **Formulation Precision & Numerators/Denominators**:
   - Pattern: `[measure] + [target group] + [quantification] + [quality threshold] + [time & location]`.
   - Flag double-barreled indicators (`"teachers trained and students passing"`), process-as-outcome errors, undefined jargon (`"improved pedagogy"`), missing units, unclear denominators, missing direction of change, and conflated unique learners vs. attendance/contact events.
   - **Nonresponse / All-Eligible Denominators**: Preserve supplied denominators and separate missing-status counts. A confirmed-positive share over all eligible cases is a valid conservative bound without claiming unknown cases are negative; distinguish it from respondent-only rates and population prevalence.
3. **Education Standard Indicator Protection**: Check against recognized Education standard sets (SDG 4, UNESCO UIS, INEE Minimum Standards, EGRA/EGMA, funder standard Education indicators). **Do NOT recommend rewording fixed standard indicators**; verify correct result level, population, and disaggregation compliance instead.
4. **Education & Equity Disaggregation**: Check sex/gender, age/grade band, disability (WG/CFM), geography/urban-rural, institution type, field of study, and language/vulnerability; flag privacy/small-cell suppression where needed without recommending unsafe collection.
5. **Data Source Quality & Continuity**: Specifically named source (EMIS, LMS, observation rubric, test), accessible/authorized, matched to reporting frequency, consistent across rounds, with baseline value or plan.
6. **Set-Level Coverage (Sets of 5+ Indicators)**: Check result-level balance, activity-count dominance (`>50%` activity counts), outcome/learning gaps, and denominator availability.

## Output Format
Calibrate detail to set size (`1-4`: detailed card for every indicator + strengths for `4.0+`; `5-14`: summary scorecard for all + detailed assessment for `< 3.0` or critical issues; `15+`: full summary scorecard + top 5-6 highest-issue items):
1. **Indicator Quality Assessment Summary**: Intake Mode, Indicators Reviewed (`N`), Overall Quality Rating, Data Completeness, Summary Scorecard (`# | Indicator | SMART Score | Disagg | Data Source | Priority Issues | Evidence ID`).
2. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
3. **Cross-Cutting Findings**, **Detailed Assessment**, **Priority Recommendations**, and **Unresolved Decisions (`MEAS-D*`)**.
4. Keep facts, interpretations, assumptions, and proposed rewordings distinct. Refer users needing structural framework review to `logframe-review`.
