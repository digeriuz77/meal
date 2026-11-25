---
name: workflow-reporting-to-action
description: Run the end-to-end Education reporting-to-action pipeline chaining evidence reconciliation, progress report drafting, independent progress-report review, revised report synthesis, management action register creation, and project-context/ synchronization. Use when turning monitoring data into verified reports and trackable actions.
---

# Reporting to Action Workflow

## Purpose and Trigger
Chain evidence verification, structured progress report authoring, independent quality review, and management action planning into synchronized Markdown artifacts (`REP-D*`), updating `project-context/` via `meal-context-manager`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Monitoring actuals/extracts, prior period reports (if available), draft progress report (if already started), and governing framework/indicator definitions (or active `project-context/`).
- Treat separate case datasets independently; never combine unrelated periods or cohorts silently. Single-period cases explicitly enforce the no-trend boundary.

State intake mode (`project-context/`, designated folder, or explicit files) and exact source filenames/versions.

## Chained Execution Sequence
Execute these stages in order, inspecting each saved Markdown artifact on disk:
1. **Reconcile Evidence (`progress-report-draft` Stage 1)**: Verify indicator coverage, numerators/denominators, arithmetic, period vs. cumulative basis, unique learners vs. attendance/contact events, equity disaggregation sums, and comparison eligibility; write `evidence.md`.
2. **Preserve or Draft Report (`progress-report-draft` Stage 2)**: If a draft report was supplied, save it unchanged as `report-draft.md` for audit comparison; if none was supplied, construct an initial draft from `evidence.md` and label it `report-draft.md` (draft).
3. **Independent Quality Review (`progress-report-review`)**: Review `report-draft.md` against `evidence.md` and source frameworks; write `review.md` preserving exact standalone headings `## Critical Issues`, `## Important Issues`, and `## Minor Improvements`.
4. **Revise Report (`report-revised.md`)**: Address confirmed arithmetic, narrative-data alignment, missingness, and single-period boundary issues while preserving unresolved conflicts explicitly.
   - Ensure zero cross-period trend claims on single-period data.
   - Ensure qualitative anecdotes or classroom examples are never stated as population prevalence or causal proof.
   - Reconcile every figure identically across `evidence.md`, `report-revised.md`, and `actions.md`.
5. **Convert Supported Findings to Actions (`findings-to-actions`)**: Map verified shortfalls, off-track indicators, and learning insights into `actions.md`. Keep suggested owners and due dates explicitly `proposed` unless committed in a source record.
6. **Log Changes & Sync Context (`change-record.md` + `meal-context-manager`)**: Document every material revision and unresolved decision (`REP-D1`, `REP-D2`, ...) in `change-record.md`, and sync reconciled actuals, limitations, and decisions into `project-context/indicator-ledger.md` and `project-context/decision-log.md`.

## Expected Artifacts
- `evidence.md`
- `report-draft.md`
- `review.md`
- `report-revised.md`
- `actions.md`
- `change-record.md`

## Save, Handover, and Resumption
- Number every decision with `REP-D*` consistently across all six files.
- If interrupted, update `project-context/handover.md` with original source IDs, completed files, verified arithmetic, and remaining steps.
- On resume, re-validate inherited claims (`explicitly confirmed`, `explicitly contradicted`, `unconfirmed`) against original sources; mark unsupported claims `"unknown"` rather than copying them forward, and never upgrade proposed actions/owners into organizational commitments.
