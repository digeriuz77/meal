---
name: workflow-evaluation-planning
description: Run the end-to-end Education evaluation planning pipeline chaining prioritized evaluation questions, question-to-method matrix, ten-section TOR draft, independent TOR review, revised TOR, and backward cross-artifact synchronization in project-context/. Use when preparing a commissioning-ready evaluation package.
---

# Evaluation Planning Workflow

## Purpose and Trigger
Chain question design, evidence/method alignment, TOR drafting, independent TOR quality review, revision, and strict cross-file synchronization into a complete Education evaluation commissioning package (`EVAL-D*`), updating `project-context/` via `meal-context-manager`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Evaluation purpose, program documents (ToC, Logframe, M&E Plan, Baseline/Progress reports), intended users/decisions, and known timeline, school calendar, or budget constraints (or active `project-context/`).
- Keep separate case studies or evaluations strictly separate; never merge unrelated programs.

State intake mode (`project-context/`, designated folder, or explicit files) and exact source filenames/versions.

## Chained Execution Sequence
Execute these stages in order, inspecting each saved Markdown artifact on disk:
1. **Frame Evaluation Questions (`evaluation-tor-draft` in `questions` mode)**: Draft 3 to 5 prioritized, answerable, decision-linked questions using purpose-matched criteria; write `questions.md`.
2. **Align Evidence & Methods (`evaluation-tor-draft` in `matrix` mode)**: Map every question to constructs, indicators, confirmed vs. candidate sources (EMIS, LMS, learning assessments, classroom observations, surveys/KIIs), sampling/safeguarding limits, and academic windows; write `matrix.md`.
3. **Draft Initial 10-Section TOR (`evaluation-tor-draft` in `full-tor` mode)**: Assemble the complete commissioning draft with `[To be confirmed: ...]` placeholders for unverified budget, effort, or permissions; write `tor-draft.md`. Preserve `tor-draft.md` separately for comparison.
4. **Independent TOR Quality & Alignment Review (`evaluation-tor-review`)**: Review `tor-draft.md` against supplied constraints, academic calendar windows, child safeguarding requirements, and framework alignment; write `review.md` preserving exact standalone headings `## Critical Issues`, `## Important Issues`, and `## Minor Improvements`.
5. **Revise TOR & Record Changes (`tor-revised.md` + `change-record.md`)**: Resolve review findings into `tor-revised.md` and document every material finding, edit, rationale, and unresolved commissioner decision (`EVAL-D1`, `EVAL-D2`, ...) in `change-record.md`.
6. **Backward Synchronize All Artifacts & Update Context (`meal-context-manager`)**:
   - Synchronize `questions.md` and `matrix.md` to match the final TOR (`tor-revised.md`) identically on question IDs, exact wording, core/optional status, priorities, evaluator day allocations, and schedule so zero conflicting versions remain.
   - Verify every final question has a complete evidence/method row in `matrix.md`.
   - Verify all school interviews, classroom observations, and fieldwork dates fall inside supplied fieldwork windows and academic terms; distinguish later desk analysis from school fieldwork.
   - If a day cap is supplied, verify task day allocations reconcile exactly. Treat core/optional splits, day allocations, and intermediate dates as `proposed` with stated basis; leave unestimable items unresolved rather than inventing effort or commitments.
   - Keep conditional sources (`unconfirmed access/consent`) conditional; never promote them to confirmed access. Sync updated status and `EVAL-D*` decisions to `project-context/`.

## Expected Artifacts
- `questions.md`
- `matrix.md`
- `tor-draft.md` (preserved unchanged for baseline comparison)
- `review.md`
- `tor-revised.md`
- `change-record.md`

## Save, Handover, and Resumption
- Number every decision consistently with `EVAL-D*` across all six artifacts.
- If interrupted, save completed files and update `project-context/handover.md`.
- On resume, re-validate inherited claims (`explicitly confirmed`, `explicitly contradicted`, `unconfirmed`) against original source documents; downgrade unsupported claims to `"unknown"` and never convert proposals, assumptions, or pending choices into commissioner approvals.
