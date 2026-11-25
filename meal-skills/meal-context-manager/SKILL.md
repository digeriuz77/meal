---
name: meal-context-manager
description: Initialize, update, validate, and hand over persistent ongoing project information in project-context/ for an Education MEAL/MERL program. Use when starting a project workspace, onboarding new source documents or indicator actuals, checking upstream-to-downstream document staleness, or preparing a session handover.
---

# MEAL Context Manager

## Purpose and Trigger
Maintain a single, auditable, ongoing project memory in `project-context/` so every Education MEAL/MERL overview, plan, TOR, and report draws from verified facts, consistent indicator definitions, and explicit decision records rather than chat memory.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Managed Workspace Files
Create and maintain these five editable Markdown files under `project-context/` using the templates in this skill:
1. [Project Brief Template](./templates/project-brief.md): Program identity, education sub-sector (ECE, K-12, TVET, Higher Ed, Non-formal/EdTech), geography, academic calendar, funder format, scope, stakeholders, and M&E document inventory.
2. [Indicator Ledger Template](./templates/indicator-ledger.md): Canonical framework indicators, definitions, result levels, baselines, periodic targets, verified actuals, variances, DQA status, and equity disaggregation tracking.
3. [Evidence Register Template](./templates/evidence-register.md): Inventory of source documents, versions/dates, approval status (`explicitly confirmed` vs. `not supplied`), and key extracted facts with `filename#heading` / table / row citations.
4. [Decision Log Template](./templates/decision-log.md): Stage-prefixed decisions (`DES-D*`, `MEAS-D*`, `REP-D*`, `EVAL-D*`) separating `unresolved_decision`, `proposed_recommendation`, and `approved_decision`.
5. [Handover Template](./templates/handover.md): Session pause/resume checkpoint tracking completed artifacts, verified calculations, three-state evidence checks, and exact next steps.

## Intake and Operating Modes
Support four explicit modes and state the active mode at the start of every response:
- **Initialize**: Scan a user-designated project folder (using discovery patterns in [Funder Formats](../../meal-references/funder-formats.md)) or explicitly supplied files, confirm ambiguous files with the user, and populate initial `project-context/` drafts.
- **Ingest / Update**: Incorporate newly supplied documents, baseline results, periodic indicator actuals, or approved stakeholder decisions; preserve prior versions in the Evidence Register and flag conflicts rather than overwriting silently.
- **Staleness & Lineage Check**: Trace the Education MEAL dependency chain (`Proposal -> Theory of Change -> Logframe -> M&E Plan -> IRS -> Baseline / Sampling / Tools -> DQA -> Progress Reports -> Evaluation TOR -> Evaluation Report -> Management Response`) and mark any downstream artifact whose upstream source changed.
- **Handover / Resume**: Write `project-context/handover.md` before pausing, or validate inherited claims against original source files when resuming a session.

## Procedure
1. Confirm mode (`initialize`, `update`, `lineage-check`, or `handover/resume`) and intake mode (`project-context/`, designated folder, or explicit files).
2. Read existing `project-context/*.md` files first if present, along with newly supplied files.
3. Extract program scope, academic calendar, education sub-sector, funder format, indicators, baselines, targets, actuals, and governance approvals with exact Evidence IDs (`filename#heading`, page, table, or row).
4. Reconcile new inputs against existing `project-context/` records:
   - Never overwrite an `approved_decision` or signed indicator wording silently.
   - When an upstream source changes (e.g., Logframe revised after M&E Plan approval), log a conflict in `decision-log.md` and mark affected downstream artifacts `STALE (upstream updated)`.
   - Keep `blank / not reported` distinct from `0`, and keep period values distinct from cumulative values.
5. Update only the affected `project-context/*.md` files, inspect the written files on disk, and return a concise summary of changes, conflicts detected, stale artifacts, and next decisions.

## Missing, Conflicting, or Unsuitable Inputs
- **Empty or minimal inputs**: Create bounded `project-context/` skeletons with `[Pending: ...]` placeholders and an explicit list of missing core documents.
- **Conflicting versions**: Record both versions with Evidence IDs in `evidence-register.md` and log a governing-source decision in `decision-log.md`. If one version is explicitly signed/approved and a newer draft is unsigned, mark the signed version as working baseline (`proposed`) and flag that the newer draft requires user determination.
- **Unverified resumed claims**: If a handover asserts a fact or approval without a verifiable record in supplied sources, downgrade its status to `unconfirmed / unknown` until verified.
- **Non-MEAL request**: State that this skill manages MEAL/MERL project context and stop.

## Completion Checklist
- Every extracted fact, baseline, target, actual, and approval status carries a traceable Evidence ID (or states `"location unavailable"` / `"approval/status not supplied"`).
- Facts, assumptions, proposals, unresolved decisions, and approved decisions are strictly separated.
- Downstream staleness flags accurately reflect upstream source changes.
- `project-context/` files were inspected on disk after writing.
