---
name: measurement-feasibility
description: Assess whether proposed Education indicators, assessments, and data collection plans are feasible given stated staff, teacher/enumerator time, school calendar windows, access permissions, and budget. Use when designing or streamlining a measurement plan before independent review.
---

# Measurement Feasibility and Burden

## Purpose and Trigger
Evaluate Education measurement demands, operational bottlenecks, calendar conflicts, safeguarding constraints, and burden-reduction options while preserving required accountability and learning evidence. This is a structured assessment, not a verified budget costing, statistical power calculation, or authorization to drop indicators. Pair outputs with `indicator-quality-review` and `me-plan-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md) and [Education MEAL Standards](../../meal-references/education-meal-standards.md).

## Minimum Inputs
- Indicator list, IRS set, or draft measurement plan.
- Planned data sources, assessments, or tools, if known.
- At least one stated constraint (staff/teacher/enumerator hours, school calendar window, permissions/access, connectivity, or budget). If no constraints are supplied, state explicitly what cannot be calculated.

State intake mode (`project-context/`, designated folder, or explicit files) and files reviewed.

## Procedure
1. **Confirm Scope and Constraints**: Identify intake mode, decision to support, indicator list, and known constraints; separate evidenced constraints from unknowns.
2. **Extract Measurement Specifications**: Extract definitions, target populations, school/site counts, disaggregation requirements, tools, collection frequency, reporting frequency, roles, QA steps, and resources with Evidence IDs (`filename#heading`, page, table, row).
3. **Build Demand Inventory**: Separate routine administrative/EMIS/LMS data already collected from new primary collection (assessments, classroom observations, surveys, KIIs/FGDs), cleaning, IRR/QA checks, analysis, and reporting.
4. **Assess Feasibility Across Eight Dimensions**:
   - **Data Availability & Permissions**: Confirm whether Ministry/school/LMS access and ethical/IRB approvals are evidenced or unconfirmed.
   - **Measurement Validity**: Flag weak proxies (e.g., enrollment registers used to claim attendance or learning).
   - **Operational Capacity**: Inventory events, schools, classes, assessors, and review steps; mark missing volumes.
   - **Academic Calendar & Time**: Check collection against term dates, exam blackouts, school holidays, and recall windows.
   - **Equity & Accessibility**: Assess local-language tool translation, disability accommodation (WG/CFM, accessible formats), offline/low-connectivity LMS/EMIS constraints, and out-of-school learner reach.
   - **Data Quality**: Account for verification, supervisor back-checks, observation IRR calibration, and EMIS reconciliation time.
   - **Child Safeguarding & Ethics**: Include time and protocols for guardian consent, learner assent, privacy anonymization, and safeguarding training.
   - **Resource Dependence**: Keep documented costs/staff separate from missing cost inputs; never claim a plan is "within budget" without supplied quantities and unit costs.
5. **Calculate Workload Strictly From Supplied Inputs**: Apply transparent arithmetic (`units * time_per_unit * frequency`) only when both volumes and unit times are supplied. Follow the strict burden rules below.
6. **Propose Burden-Reduction Options**: Identify practical options (sampling schools/classrooms instead of census testing, aligning collection to existing term exams/supervisory visits, harmonizing EMIS extracts, streamlining low-value indicators). For every option, document: requirement affected, evidence preserved vs. lost, validity/equity risk, and approval required.
7. **Return Output**: Deliver an editable measurement-demand matrix, supported workload totals (if calculable), proposed options with tradeoffs, and `MEAS-D*` decisions required.

## Burden Calculation Rules
- **Count Each Task Once**: Never double-count sub-roles inside an activity total (e.g., if an enumerator's assessment hours are inside total field team hours, do not add them a second time). Use mutually exclusive role totals or activity totals with explicit role allocation.
- **Never Conflate Calendar Units**: Do not equate workshop/coaching sessions with active school weeks, or assume every term/quarter equals 12 working weeks or every month equals 4 weeks. When exact collection counts or school calendars are absent, report the supplied per-event/weekly rate plus an explicit formula (`N_events * hours_per_event`). Optional hypothetical scenarios must be labeled `hypothetical scenario` and never treated as confirmed capacity totals.
- **Consistent Units Only**: Show exact period (per assessment round, term, month, or year) and include setup, consent, travel, data entry, cleaning, QA, and reporting only when their unit times are supplied.

## Missing, Conflicting, or Unsuitable Inputs
- **Missing volumes or unit times**: Analyze burden drivers qualitatively and state clearly that workload hours cannot be computed.
- **Unconfirmed EMIS/school access**: Classify access as unconfirmed and specify verification needed before relying on it.
- **Conflicting frequencies or school counts**: Display both figures with Evidence IDs and show the resulting calculation impact.
- **Non-MEAL request**: State scope and stop.

## Completion Checklist
- Every supplied indicator and collection task is represented in the demand matrix.
- Arithmetic uses supplied inputs only, avoids double-counting, and separates calendar assumptions from confirmed facts.
- Academic calendar constraints, safeguarding requirements, and disability/language equity effects are evaluated.
- Every proposed simplification states information lost, validity/equity risk, and required approval (`MEAS-D*`).
- No budgets, targets, sample sizes, or staff commitments were invented.
