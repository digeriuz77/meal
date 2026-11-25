---
name: sampling-plan-review
description: Independently review an Education sampling plan, sample size calculation, school/classroom cluster strategy, or qualitative sampling design for method appropriateness, sample size verification, frame quality, selection rigor, domain precision, and feasibility. Use after sampling-plan-draft or when reviewing any sampling methodology.
---

# Sampling Plan Review

## Purpose and Trigger
Conduct an independent methodological review of an Education sampling plan across 7 scored dimensions, including **independent recomputation** of any supplied sample size calculation. Complex multi-stage, optimal-allocation, or multi-level power designs should additionally undergo formal statistical consultation.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md) and [Education MEAL Standards](../../meal-references/education-meal-standards.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Standalone sampling plan** -> full 7-dimension review.
- **Embedded in baseline, survey, or evaluation methodology** -> extract sampling content and review standalone.
- **Sample size calculation only** -> verify parameters and recompute formula in Section 2; mark remaining sections `"Not Assessed"` (provisional summary).
- **Qualitative sampling strategy** -> evaluate selection criteria, institutional/learner diversity, and saturation review rules instead of survey sample size formulas.
- **Brief / Narrative description** -> summarize understanding first; flag silent areas as `"not confirmed present"`.
- **Non-MEAL input** -> return suitability note and stop.

State intake mode, document classification, sampling method identified, and Evidence IDs (`filename#heading`, page, table, row).

## Scoring Thresholds
- **PASS**: Methodologically sound, independently verified, and well-documented.
- **PARTIAL**: Present with documentation gaps or methodological concerns.
- **FAIL**: Missing, mathematically wrong, unrepresentative, or infeasible.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Method Appropriateness** or **Sample Size Justification** automatically triggers **Major Issues**.

## Seven Review Dimensions

### 1. Method Appropriateness (Critical Weight)
- Chosen design (SRS, systematic, stratified, school/classroom multi-stage cluster, PPS, LQAS, or purposive qualitative) matches the estimand or evaluation question.
- Randomization vs. convenience: convenience sampling cannot establish prevalence or valid LQAS error bounds.
- Alternatives considered; school-based vs. household-based frame choice justified for out-of-school vs. enrolled populations.

### 2. Sample Size Justification and Verification (Critical Weight)
Verify whether all required parameters are stated and justified: confidence level (e.g., 95%, `z = 1.96`), margin of error, expected proportion/variance, **design effect (`DEFF`) / `ICC`** for school/classroom clustering, power & MDE (for comparisons), finite population correction (when sample > 5% of `N`), and nonresponse/absenteeism/attrition uplift.
- **Independent Verification Procedure**: Identify formula, verify every parameter, recompute arithmetic step by step, compare claimed vs. recalculated `n` (flag discrepancies >= 5%, noting smaller rounding differences), and check nonresponse/invitation buffer. Mark `"Unchecked / Unresolved"` if parameters are missing; never rubber-stamp an unverified total.
- **Education Cluster Flag**: Clustered school/classroom designs WITHOUT `DEFF` or `ICC` justification are always a **Critical Issue**. Also check cluster count sufficiency (too few schools cannot be rescued by testing more students per school).
- **Minimum Cell Size Rule**: Flag any planned reporting subgroup `< 30` observations and warn against statistical generalization.

### 3. Sampling Frame Quality
- Frame source (EMIS school list, enrollment roster, LMS registry, household listing), date/currency, unique IDs, completeness, duplicates, and omissions (unregistered non-formal schools, absent learners, out-of-school youth) assessed without exposing minor PII.

### 4. Selection Procedure
- Replicable step-by-step instructions (random seed/software, systematic interval + periodicity check, PPS probability steps at each stage, random exclusion rules if clusters exceed design size in LQAS, and non-biased reserve/replacement rules forbidding ad-hoc convenience substitution of absent students).

### 5. Equity Disaggregation Feasibility
- Sample size and stratification/oversampling support required Education subgroups (sex, age/grade band, disability status, geography/urban-rural, institution type, study track) with design weights documented for disproportionate strata.

### 6. Practical Feasibility
- Realistic relative to fieldwork days, academic term/exam schedules, school travel dispersion (e.g., visiting 60 dispersed rural schools in 2 weeks), budget, and enumerator capacity, with contingencies for school closures or inaccessible sites.

### 7. Limitations Transparency and Longitudinal Alignment
- Coverage bias, absenteeism/attrition effects, qualitative non-generalizability, and consistency with prior baseline methodology (for midline/endline designs) honestly disclosed.

## Output Format
1. **Sampling Plan Review Summary**: Intake Mode, Document Type, Sampling Method Identified, Overall Rating, and 7-row Score Summary table (`PASS / PARTIAL / FAIL / Not Assessed`).
2. **Sample Size Verification Table** (if calculations provided): `Parameter | Stated | Recalculated / Assessment`.
3. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
4. **Priority Recommendations**, **Detailed Findings** (1 through 7), **Design Flaw Flags**, and **Unresolved Decisions (`MEAS-D*` / `EVAL-D*`)**.

## Output Rules and Resumption
- Distinguish purposive qualitative sampling from statistical prevalence designs; never apply numeric survey sizing formulas to qualitative guides.
- Keep supplied facts, recalculated arithmetic, assumptions, and proposed fixes separate. On resume, recalculate affected outputs whenever parameters or frames change.
