---
name: me-plan-draft
description: Draft an operational Education M&E, MEL, or MEAL plan from supplied program and indicator materials, or run a structured coherence check on an existing plan against its framework. Use when constructing or updating a full 11-component MEAL plan before independent me-plan-review.
---

# M&E / MEL / MEAL Plan Draft

## Purpose and Trigger
Construct a practical, operational Education M&E / MEL / MEAL plan connecting program results, indicators, collection tools, EMIS/LMS data flows, data quality assurance, roles, safeguarding, learning routines, and decision use; OR run a cross-document coherence check on an existing plan. The output is a proposed draft for program-team review, not an approved commitment. Follow with `me-plan-review` independently.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Program summary, proposal, ToC, or results framework/logframe.
- Indicator list or stated monitoring/learning purpose.
- Known funder reporting obligations, data sources, academic calendar, or resource constraints.

State intake mode (`project-context/`, designated folder, or explicit files) and confirm ambiguous files.

## Procedure
1. **Confirm Scope**: Identify intake mode, audience, education sub-sector(s), funder format, implementation stage, academic calendar horizon, and whether drafting new, revising, or checking coherence.
2. **Extract Framework Facts**: Extract results logic, indicator wording, populations, baselines, targets, reporting cycles, data sources (EMIS, LMS, school records, assessments), staffing, budget, and data-use needs with Evidence IDs (`filename#heading`, page, table, row).
3. **Preserve Authority and Epistemic Boundaries**:
   - Never silently alter approved indicator wording, baselines, targets, or funder obligations; flag gaps instead.
   - For every status claim (`approved`, `authorized`, `rejected`), cite an explicit status-bearing source statement; otherwise write `"approval/status not supplied"`.
   - Record conflicting versions with both Evidence IDs. If a signed/approved source conflicts with an unsigned later draft, use the signed source as working baseline (`proposed`) and flag the governance decision (`MEAS-D*`).
4. **Draft the Eleven Plan Components**: Link every indicator across components (source -> method/tool -> collection vs. reporting frequency -> responsible role -> QA/IRR -> analysis -> learning/use) using explicit placeholders where inputs are missing.
5. **Check Coherence & Operational Alignment**: Verify alignment across results logic, indicators, academic calendar, disaggregation, data quality, safeguarding, roles, learning questions, and budget/staffing.
6. **Evaluate Workload Strictly From Evidence**: Calculate collection burden only when volumes and unit times are supplied; never invent budgets, staff FTE/LOE, sample sizes, or targets.
7. **Return Output and Decision Queue**: Deliver the 11-component plan, editable indicator & collection matrix, evidence register, assumptions/proposals, and prioritized `MEAS-D*` decisions. Recommend independent review via `me-plan-review`.

## Eleven Plan Components
1. **Program Context, Education Results Logic, and Intended Use** (funder format, sub-sector, academic calendar)
2. **Monitoring, Evaluation, and Learning Agenda** (learning questions linked to scheduled reflection routines and real decisions)
3. **Indicator Matrix and Definitions** (referencing IRS/PIRS; one row per indicator preserving exact IDs and wording)
4. **Data Sources, Collection Methods, and Tools** (EMIS, LMS, classroom observations, learning assessments, surveys/FGDs, with tool readiness status)
5. **Collection, Academic-Term, and Reporting Schedule** (distinguishing collection, analysis, and reporting frequencies; aligned to school terms/exams)
6. **Disaggregation and Equity Considerations** (sex, age/grade, disability via WG/CFM, geography, institution type, language/vulnerability; small-cell suppression)
7. **Data Management, Quality Assurance (VIPRT), Safeguarding, and Data Protection** (data flow from collection through storage, access, child/guardian consent, minor PII protection, retention, and disposal; action taken when DQA fails)
8. **Analysis, Interpretation, and Methodological Limitations** (distinguishing contribution/observed change from causal attribution; cohort vs. cross-sectional rules; blank vs. zero)
9. **Reporting, Learning (CLA), and Decision-Use Routines** (explicit feedback loops showing how findings inform decisions; a meeting without a decision purpose is not adaptive management)
10. **Roles and Responsibilities** (named functional roles separated across collection, QA/IRR, analysis, reporting; proposed roles marked `proposed`)
11. **Resources, Risks, External Assumption Monitoring, and Implementation Decisions** (monitoring external Education assumptions and risks; explicit `MEAS-D*` queue)

## Coherence Check Output Requirement
When running a coherence check on an existing plan, include these exact standalone headings without numbering or abbreviations:
```markdown
## Critical Issues
## Important Issues
## Minor Improvements
```
Write `"None identified from supplied files."` or `"Not assessable from supplied files."` under any empty heading.

## Missing, Conflicting, or Unsuitable Inputs
- **No indicator list**: Draft the 11-component structural shell and list required `MEAS-D*` decisions before the indicator matrix can be populated.
- **No staffing or budget data**: Mark resource feasibility as `"Not assessable from supplied files"` rather than substituting generic percentage benchmarks as project facts.
- **Insufficient source details**: Produce a bounded draft with explicit `[Pending: ...]` placeholders.
- **Non-MEAL request**: State scope boundary and stop.

## Completion Checklist
- All 11 components are included or explicitly flagged as unresolved.
- Calendar units (sessions, active school weeks, terms, collection events) are never conflated.
- Indicators, methods, academic windows, equity disaggregation, safeguarding/QA, roles, and learning uses trace coherently.
- Facts, assumptions, proposals, and `MEAS-D*` decisions are clearly separated.
- Next step points to independent `me-plan-review`.
