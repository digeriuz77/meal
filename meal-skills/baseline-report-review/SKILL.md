---
name: baseline-report-review
description: Independently review an Education baseline report, study, assessment, or pre-intervention dataset for indicator coverage, school/household sampling rigor, equity disaggregation, measurement consistency across rounds, data quality, and target validation. Use after baseline-planning or when evaluating any baseline report.
---

# Baseline Report Review

## Purpose and Trigger
Conduct an independent quality review of an Education baseline study or pre-intervention report across 10 scored dimensions to verify whether it provides a valid, ethical, and comparable foundation for midline and endline measurement. Statistical power and complex multi-level modeling should be verified by a statistician where needed.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Full baseline report**: Complete study with methodology, findings, and annexes -> full 10-dimension review.
- **Baseline data summary / tables only**: Score Sections 1, 3, and 4 in full; mark methodology sections `"Not Assessed (tables only)"` and label summary provisional.
- **Methodology section only**: Assess Sections 2, 4, 5, and 9; mark results sections `"Not Assessed"`.
- **Rapid / accelerated education baseline or secondary EMIS compilation**: Calibrate expectations for speed/source limits; emphasize indicator coverage, source comparability, and comparability limits.
- **Partial / Draft**: Review present components; flag missing sections as `"needs development"`.
- **Narrative description**: Summarize understanding first; flag silent areas as `"not confirmed present"`.
- **Non-MEAL input**: Return suitability note and stop.

State intake mode, document classification, and exact source IDs (`filename#heading`, page, table, row).

## Scoring Thresholds
- **PASS**: Complete, methodologically sound, and valid for longitudinal comparison.
- **PARTIAL**: Present with methodological gaps or incomplete coverage.
- **FAIL**: Missing, methodologically flawed, or invalid for endline comparison.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Indicator Coverage** or **Sampling Methodology** automatically triggers **Major Issues**.

## Ten Review Dimensions

### 1. Indicator Coverage (Critical Weight)
- Baseline values quantified for all logframe outcome and goal indicators (plus relevant output indicators; an output starts at zero only if definitions and records confirm zero prior delivery).
- Operational definitions match the governing framework; no key indicators silently dropped.

### 2. Sampling Methodology (Critical Weight)
- Representative probability design (or justified design), documented frame (school-based EMIS/roster vs. household-based, noting out-of-school exclusions), precision/power calculation parameters, **cluster DEFF / ICC** for school/classroom multi-stage samples, and nonresponse/absenteeism adjustments.
- Convenience sampling or unadjusted clustered school samples fail statistical comparison standards.

### 3. Equity Disaggregation
- Sex, age/grade bands, geography/urban-rural, disability status (WG/CFM), institution type, and program/study track as applicable; sub-totals reconcile to totals and missing categories are reported separately.

### 4. Measurement Consistency Across Rounds
- Assessment tools (e.g., EGRA/EGMA, competency tests, classroom observation rubrics) and protocols appended or fully documented for exact replication at midline/endline.
- Academic calendar timing (start/middle/end of term), cohort vs. cross-sectional tracking, assessment language, and recall windows explicitly stated.
- Flag post-exposure surveys relying on retrospective recall labeled improperly as `"baseline"`.

### 5. Comparison Group (If Quasi-Experimental or Experimental)
- Mark `"N/A"` if descriptive baseline without counterfactual arms.
- Where present: allocation/matching documented, baseline balance/equivalence tested, spillover and school/learner attrition risks mitigated.

### 6. Data Quality
- School and learner response rates, assessment completion rates, missing-data patterns, floor/ceiling test effects, inter-rater reliability (for observations), data cleaning, and outlier handling documented.

### 7. Education Context Analysis
- Contextual factors (school calendar disruptions, teacher turnover, language of instruction, concurrent programs, policy shifts) linked directly to ToC assumptions and future round threats.

### 8. Target Validation
- Baseline empirical values explicitly compared against planned program targets; unrealistic targets flagged with specific, evidence-grounded suggested adjustments labeled `proposed`.

### 9. Ethical Compliance and Child Safeguarding
- Ministry/IRB ethics approval, parent/guardian informed consent, age-appropriate child/learner assent, minor PII data protection, and enumerator safeguarding/referral protocols documented.

### 10. Report Usability
- Findings organized by Education outcome/result area (not by tool), master baseline indicator summary table included, annexes complete (tools, frame, detailed tables), and recommendations specific and actionable.

## Output Format
Frame critical findings around whether the defect invalidates endline comparison, distinguishing methodological flaws from documentation gaps:
1. **Baseline Report Review Summary**: Intake Mode, Document Type, Overall Rating (note provisional if partial), and 10-row Score Summary table (`PASS / PARTIAL / FAIL / N/A / Not Assessed`).
2. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
3. **Priority Recommendations** (3 to 5 items; include specific suggested revised target values where baseline data show targets are miscalibrated).
4. **Detailed Findings** (1 through 10) and **Design Flaw Flags**.
5. **Evidence & Unresolved Decisions Register (`MEAS-D*`)**.

## Output Rules and Resumption
- Distinguish `"not confirmed present"` from `"missing"` and `"approval status not supplied"` from confirmed sign-off.
- On resume, re-check original source files and flag any updated baseline numbers or revised framework versions.
