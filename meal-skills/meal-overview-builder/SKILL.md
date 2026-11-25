---
name: meal-overview-builder
description: Construct tailored Education MEAL/MERL overviews (Executive Overview, Donor/Board Brief, Inception Summary, or Annual Learning Brief) grounded in project-context/ and supplied program documents. Use when creating a unified program MEAL overview, synthesis brief, or multi-document status summary before independent review.
---

# MEAL / MERL Overview Builder

## Purpose and Trigger
Construct a structured, traceable Education MEAL/MERL overview that brings together program results logic, longitudinal indicator performance, equity disaggregation, data quality status, learning adaptations, and unresolved decisions into one decision-ready document.

This is a **Construct** skill. After generating an overview, recommend running `meal-system-audit` (or `progress-report-review` for period-performance briefs) as an independent review gate.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Overview Formats
Select the format matching the user's request (confirm if ambiguous):
1. **`executive-overview`**: Whole-program MERL snapshot covering theory of change, results framework status, longitudinal indicator performance, equity reach, evaluation readiness, and open decisions.
2. **`donor-board-brief`**: Concise funder-aligned accountability and learning brief matching the specified funder format (Results Framework, LFA, VfM, UN, or Foundation), highlighting variances, Value for Money / equity signals, and governance actions.
3. **`inception-summary`**: Design-stage and baseline-readiness overview mapping ToC/Logframe coherence, M&E system coverage, baseline plans, DQA risks, and pre-implementation decisions.
4. **`annual-learning-brief`**: Reflection and adaptation overview synthesizing year-over-year or cohort outcomes, learning questions answered, evaluation findings, and proposed program adjustments.

## Minimum Inputs
- Active `project-context/` files (maintained via `meal-context-manager`) OR at least two core program/MEAL documents (e.g., Proposal/Logframe/M&E Plan + Progress/Baseline/Evaluation reports or indicator tracker).
- Target audience and desired overview format.

State intake mode (`project-context/`, designated folder, or explicit files) at the top of the output.

## Procedure
1. **Confirm Scope and Format**: Identify intake mode, requested overview format, education sub-sector(s), reporting window, and funder terminology preference.
2. **Audit Source Coverage**: Inventory supplied sources and flag any missing links in the Education MEAL chain (`Proposal -> ToC -> Logframe -> M&E Plan -> IRS -> Baseline -> Progress Data -> Evaluations`).
3. **Verify Results Logic**: Summarize the program's Education causal chain (`inputs -> educator practice -> enrollment -> attendance -> retention/completion -> learning outcomes -> transition`) with `[Source: ...]` citations. Flag any missing intermediate steps or upstream-downstream conflicts rather than smoothing them over.
4. **Build Longitudinal Indicator Performance Table**: Populate the standardized indicator table from verified baseline, target, and periodic actual records.
   - Keep `period` vs. `cumulative` values explicit.
   - Show exact numerator/denominator and variance arithmetic; never treat missing/blank as zero.
   - Apply the single-period no-trend rule and distinguish unique learner counts from training/contact events.
5. **Synthesize Equity and Learning Outcomes**: Report disaggregated reach and learning/transition outcomes across Education equity dimensions (sex, age/grade, disability, geography, institution type, language/vulnerability), reporting unclassified counts separately.
6. **Document Data Quality, Limitations, and Safeguarding Status**: Summarize DQA/VIPRT status, sampling/assessment limitations (calendar shifts, attrition, floor/ceiling effects, non-comparable cohorts), and child/learner safeguarding compliance.
7. **Extract Learning and Proposed Adaptations**: Connect observed evidence to concrete program learning and proposed management actions, explicitly tagging recommendations as `proposed` rather than approved commitments.
8. **Assemble Output**: Use [Overview Template](./template.md), preserve `[Source: ...]` IDs on every factual claim, list unresolved decisions and missing documents, and invite an independent review via `meal-system-audit` or `progress-report-review`.

## Missing, Conflicting, or Unsuitable Inputs
- **Only one document supplied**: Note the single-source limitation clearly; construct a bounded overview for covered sections and mark uncovered sections `"Not assessable from supplied files."`
- **Conflicting figures across documents**: Display both figures with their Evidence IDs in the overview and log a reconciliation decision rather than choosing silently.
- **No actuals or baseline values**: Populate the overview with framework structure and `[Not yet measured / Not reported]` placeholders; never invent performance numbers.
- **Non-MEAL request**: Explain scope and stop.

## Completion Checklist
- Format, education sub-sector, intake mode, and governing sources are explicit.
- Every number, target, baseline, and programmatic claim links to a verifiable Evidence ID.
- Confirmed facts, assumptions, proposed recommendations, and unresolved decisions are separated.
- No trend claim is made from single-period data and no causal impact claim is made from routine monitoring alone.
- Independent review (`meal-system-audit` or `progress-report-review`) is explicitly listed as the next step.
