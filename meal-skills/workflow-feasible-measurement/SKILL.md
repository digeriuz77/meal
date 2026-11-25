---
name: workflow-feasible-measurement
description: Run the end-to-end Education feasible-measurement pipeline chaining indicator quality review, workload feasibility, indicator reference sheets, M&E plan drafting, independent coherence review, and cross-artifact synchronization in project-context/. Use when operationalizing indicators into a burden-checked MEAL plan.
---

# Feasible Measurement Workflow

## Purpose and Trigger
Chain independent quality review, feasibility analysis, operational documentation, and plan drafting into a synchronized set of Education measurement artifacts, preserving `MEAS-D*` decisions and updating `project-context/` via `meal-context-manager`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Education results framework, logframe, or indicator set plus available collection/staffing/academic-calendar context (or active `project-context/`).
- Treat separate case folders independently; never combine unrelated project datasets into one run.

State the active intake mode (`project-context/`, designated folder, or explicit files) and exact source files/versions at the start.

## Chained Execution Sequence
Execute these stages in order, inspecting each saved Markdown artifact on disk:
1. **Baseline Quality Check (`indicator-quality-review`)**: Assess supplied indicators and write `indicator-review.md`.
2. **Workload & Burden Analysis (`measurement-feasibility`)**: Assess operational feasibility against school calendars, safeguarding, and staff time; write `burden.md`.
   - Sum time by role and actual collection month, separating one-time setup from recurring term/period tasks.
   - Never assume unstated capacity or equate coaching/workshop sessions with active calendar weeks. When exact calendar counts are absent, report supplied per-event/weekly rates plus an explicit formula (`N_events * unit_time`); keep optional hypothetical scenarios separate from source-supported totals.
   - Preserve all-eligible confirmed-positive shares separately from missing statuses and respondent-only rates (never classify unknown learners as negative).
3. **Operational Indicator Sheets (`indicator-reference-sheets`)**: Draft editable IRS records preserving required accountability evidence and reporting obligations when proposing burden tradeoffs; write `reference-sheets.md`.
4. **Operational Plan Draft (`me-plan-draft`)**: Draft the 11-component Education M&E plan aligned to academic windows and safeguarding; write `me-plan.md`.
5. **Independent Plan & Cross-Artifact Coherence Review (`me-plan-review`)**: Review `me-plan.md`, then compare EVERY indicator ID, exact wording/definition, numerator/denominator, source, collection vs. reporting frequency, role, and intended use across `indicator-review.md`, `burden.md`, `reference-sheets.md`, and `me-plan.md`. Log every discrepancy in `coherence.md` under exact standalone headings (`## Critical Issues`, `## Important Issues`, `## Minor Improvements`).
6. **Reconcile & Record Decisions (`decisions.md` + `meal-context-manager`)**: Correct confirmed cross-file inconsistencies in affected artifacts, record suggested indicator revisions and unresolved choices under numbered `MEAS-D1`, `MEAS-D2`, ... IDs in `decisions.md`, and sync verified updates to `project-context/indicator-ledger.md` and `project-context/decision-log.md`.

## Expected Artifacts
- `indicator-review.md`
- `burden.md`
- `reference-sheets.md`
- `me-plan.md`
- `coherence.md`
- `decisions.md`

## Save, Handover, and Resumption
- Number every unresolved decision with `MEAS-D*` consistently across all files.
- If pausing mid-workflow, save completed artifacts and update `project-context/handover.md` via `meal-context-manager`.
- On resume, re-validate inherited facts and status claims (`explicitly confirmed`, `explicitly contradicted`, `unconfirmed`) against original source documents; never carry forward negative or positive status claims without a supporting record, and never upgrade a `proposed` item into an approved commitment.
