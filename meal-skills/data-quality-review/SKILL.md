---
name: data-quality-review
description: Independently review an Education Data Quality Assessment (DQA), VIPRT audit, verification report, or routine EMIS/LMS quality check for scope adequacy, source verification rigor, VIPRT coverage, systems assessment, and action plan quality. Use after data-quality-planning and DQA execution.
---

# Data Quality Assessment (DQA) Review

## Purpose and Trigger
Conduct an independent methodological review of a completed Education DQA report, data verification report, routine quality check, or prospective DQA plan across 8 scored dimensions. Desk review evaluates assessment rigor and documentation; physical back-checking and system audits occur in the field.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md) and [Education MEAL Standards](../../meal-references/education-meal-standards.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Full DQA report** -> full 8-dimension review.
- **DQA plan (prospective)** -> assess Sections 1, 3 (planned), 4, 6, 7, and 8; mark Verification Rigor (`Section 2`) and retrospective outcomes `"Not Assessed (prospective plan)"` and label rating provisional.
- **Data verification report** -> emphasize Section 2 verification rigor and ratios; flag absent VIPRT/systems coverage.
- **Routine periodic data quality check** -> calibrate expectations for lighter frequency while checking arithmetic and evidence.
- **Partial / Narrative description** -> review present sections; flag silent elements `"not confirmed present"`.
- **Non-MEAL input** -> return suitability note and stop.

State intake mode, document classification, and Evidence IDs (`filename#heading`, page, table, row).

## Scoring Thresholds
- **PASS**: Dimension satisfied with strong evidence and no major concerns.
- **PARTIAL**: Present with notable methodological or evidence gaps.
- **FAIL**: Missing, methodologically compromised, or invalidates confidence in data.

**Overall Rating:**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Improvement**: `1 FAIL`, or `3+ PARTIAL`.
- **Serious Concerns**: `2+ FAIL`.

**Verification Ratio Benchmarks (where verification ratios are reported):**
- Acceptable: reported value within `+/- 5%` of recounted source value.
- Minor discrepancy: `5% to 10%` difference.
- Major discrepancy: `> 10%` difference (requires root cause analysis and remediation).

## Eight Review Dimensions

### 1. Scope Adequacy
- High-risk and core Education reporting indicators included (or selection rationale justified), covering quantitative (EMIS/enrollment/attendance/assessment scores/LMS) and qualitative/partner sources across decentralized sites, not merely easy-to-access central offices.

### 2. Verification Rigor
- Physical source records (school attendance books, graded assessment scripts, signed training sheets, raw LMS logs) traced and recounted at multiple school/partner sites, not merely electronic report-to-spreadsheet comparisons.
- Recount methodology and verification ratios clearly shown.

### 3. VIPRT Coverage
All five VIPRT lenses evaluated with concrete evidence (document review, system tests, interviews, observations):
- **Validity**: Consistent application of Education indicator definitions (enrollment vs. attendance vs. retention; LMS completion vs. competency).
- **Integrity**: Controls against capitation/headcount inflation, duplicate learners, or unlogged edits; minor PII access restrictions.
- **Precision**: Clear denominators, grade/age bands, disability categories, and unit boundaries.
- **Reliability**: Standardized instruments, observer/scorer IRR consistency, stable EMIS/LMS extraction rules.
- **Timeliness**: Termly capture, entry, and submission schedules meeting decision needs.

### 4. Systems Assessment
- Full Education data pathway mapped (`classroom/LMS -> entry -> aggregation -> QA -> report`), evaluating staff capacity, digital validation rules (e.g., ODK/KoboToolbox skip/range checks), backups, and minor PII security.

### 5. Action Plan Quality (Heavily Weighted)
- Every finding paired with a concrete corrective action, responsible role (labeled `proposed` unless approved), timeline, and completion verification method.

### 6. Independence
- Assessor independent from primary data collector/reporter; potential conflicts of interest disclosed.

### 7. Follow-Up on Prior DQA
- References prior DQA findings and verifies whether previously claimed closures held up (or `"N/A"` if documented as first DQA).

### 8. Documentation and Bias Controls
- Methodology, checklists, site-visit records, and sampling/selection criteria appended; distinguishes sampling error from systematic bias (which larger samples cannot fix).

## Output Format
1. **Data Quality Assessment Review Summary**: Intake Mode, Document Type, Overall Rating, and 8-row Score Summary table (`PASS / PARTIAL / FAIL / N/A / Not Assessed`).
2. **VIPRT Summary Table** (if assessed): `Dimension | Key Evidence & Finding | Concern Level (None / Minor / Major)`.
3. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
4. **Priority Recommendations**, **Detailed Findings** (1 through 8), **Design Flaw Flags**, and **Unresolved Decisions (`MEAS-D*`)**.

## Output Rules and Resumption
- Distinguish prospective DQA plans from retrospective DQA reports clearly.
- Do not infer deliberate tampering merely from missing audit logs; classify missing logs as control gaps requiring investigation.
- Keep facts, verified ratios, assumptions, and proposed fixes separate. On resume, verify inherited closure claims against original source files.
