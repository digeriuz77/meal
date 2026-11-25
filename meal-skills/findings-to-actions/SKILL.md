---
name: findings-to-actions
description: Convert verified Education evaluation or review findings into a traceable Management Response and Action Register, or synthesize an Executive Evaluation Findings Brief from supplied evidence without fabricating commitments, owners, or deadlines. Use before independent evaluation-report-review.
---

# Findings to Management Actions and Evaluation Synthesis

## Purpose and Trigger
Operate across two complementary Construct outputs grounded strictly in verified evidence:
1. **Management Response & Action Register Mode**: Translate evaluation, audit, or DQA findings into traceable management responses and trackable action plans while keeping evidence, evaluator recommendations, management decisions, and proposed actions strictly separate.
2. **Executive Evaluation Findings Brief Mode**: When raw evaluation findings, TOR questions, and verified evidence tables are supplied, synthesize a structured, evidence-anchored Executive Findings Brief (following standard evaluation report logic: Context -> Purpose/TOR Questions -> Methodology & Limitations -> Findings -> Evidence-Bound Conclusions -> Recommendations, introducing zero external claims).

This skill never approves findings, assigns real organizational owners, or invents institutional commitments. Follow outputs with independent `evaluation-report-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Findings, conclusions, recommendations, or audit/review issues with verifiable sources.
- Sufficient program/Education context to interpret feasibility and governance.
- Existing management positions, owners, budgets, or deadlines if already decided.

State the active intake mode (`project-context/`, designated folder, or explicit files) and exact files/versions reviewed.

## Procedure

### Mode 1: Management Response & Action Matrix
1. **Confirm Scope**: Identify intake mode and whether the request covers findings extraction, management response drafting, or action tracking.
2. **Extract Findings and Recommendations with Provenance**: Capture each finding, recommendation, supporting data/sample size/method, confidence/limitations, and any existing organizational response with Evidence IDs (`filename#heading`, page, table, row).
3. **Trace Evidence Chains**: Verify `evidence -> finding -> evaluation question/DAC criterion -> conclusion -> recommendation -> management decision -> response -> action -> completion evidence`. Flag broken links (such as recommendations lacking supporting findings or findings lacking data citations); never silently strengthen weak findings.
4. **Separate Decision Authority from Proposals**:
   - Preserve supplied management positions (`Accept / Partially Accept / Reject / Defer / Clarify`); otherwise mark `"Pending management decision"`.
   - Record management rationale grounded in Education feasibility, equity, safeguarding, or strategic alignment without inventing institutional consensus.
5. **Specify Trackable Actions Without Inventing Commitments**:
   - State an observable deliverable or operational change (avoid vague items like `"strengthen teacher support"`).
   - Use ONLY supplied owner names/roles and due dates; otherwise write `"Owner to be assigned"` and `"Timing to be decided"` (any suggested relative timeline must carry a `proposed` label and rationale).
   - Name verifiable completion evidence (e.g., revised teacher coaching rubric, updated EMIS validation rule, termly review record) labeled `proposed` until adopted.
   - Surface budget, policy, Ministry/school coordination, or safeguarding dependencies rather than assuming resources exist.
6. **Prioritize Transparently**: Rank actions using supplied criteria (risk, child safeguarding urgency, equity impact, academic-calendar dependency); otherwise label prioritization as `proposed`.
7. **Return Register**: Populate [Finding-to-Action Matrix Template](./template.md) and list `EVAL-D*` / `REP-D*` decisions requiring sign-off. Never fabricate status tags like `"In progress"` when absent.

### Mode 2: Executive Evaluation Findings Brief Synthesis
1. Map verified findings directly to TOR evaluation questions and relevant OECD-DAC criteria (only those required by the TOR).
2. Enforce strict evidence-chain discipline:
   - Every **Finding** cites data sources, learner/school sample size, methods, and exact metrics (avoid vague quantifiers like `"most schools"`).
   - Every **Conclusion** derives ONLY from presented findings (zero new external claims or ungrounded causal assumptions).
   - Every **Recommendation** links to a specific conclusion, names a target actor role (`proposed`), and specifies concrete Education actions with limitations carried forward.
3. Explicitly preserve methodology limitations, gender/disability/equity gaps, and unresolved contradictions for review via `evaluation-report-review`.

## Missing, Conflicting, or Unsuitable Inputs
- **Finding lacks supporting data**: Record as an unverified claim requesting source evidence; propose only an information-verification check rather than a definitive operational response.
- **Conflicting findings across sources**: Present both evidence paths with Evidence IDs and log a reconciliation decision.
- **No owner, budget, or deadline supplied**: Leave unassigned/undecided explicitly.
- **Non-MEAL request**: State boundary and stop.

## Completion Checklist
- Every action traces to an evidenced finding (or is labeled a verification proposal).
- Findings, recommendations, management decisions, responses, and actions remain visibly distinct.
- Owners, dates, budgets, and completion statuses are source-evidenced or visibly unresolved.
- Conclusions in synthesis briefs introduce no external facts absent from findings.
- Next step queues independent `evaluation-report-review`.
