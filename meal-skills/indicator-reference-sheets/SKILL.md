---
name: indicator-reference-sheets
description: Draft or update editable Education Indicator Reference Sheets (IRS / PIRS) with exact operational definitions, numerator/denominator formulas, equity disaggregation, data quality risks, and change-control records. Use when indicators need standardized operationalization before independent indicator-quality-review.
---

# Indicator Reference Sheets (IRS / PIRS)

## Purpose and Trigger
Turn approved or proposed Education indicators into traceable, operational reference sheets. This skill documents definitions, calculations, sources, and unresolved decisions; it does not silently alter approved wording, baselines, targets, or funder commitments. After drafting or updating sheets, invoke `indicator-quality-review` independently.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Indicator name(s) or result statement(s).
- Target learner/educator population or result level, if known.
- Available framework, M&E plan, data sources, collection tools, baselines, targets, or reporting requirements.

State the active intake mode (`project-context/`, designated folder, or explicit files) and files reviewed.

## Procedure
1. **Confirm Scope**: Identify intake mode, indicator list, and whether the job is new drafting, documentation, or revision. Preserve existing approved wording unless explicitly authorized to revise.
2. **Extract Source Record**: Extract indicator ID, framework row, result level, population, baseline, target, source, method, frequency, and approval status (`"approval/status not supplied"` if missing) with Evidence IDs (`filename#heading`, page, table, row).
3. **Separate Epistemic States**: Place facts, assumptions, proposed fixes, and conflicts (with both Evidence IDs) in distinct fields.
4. **Verify Education Result-Chain Placement**: Classify as Activity, Output, Intermediate Outcome, Outcome, or Goal along the [Education Causal Chain Ladder](../../meal-references/education-meal-standards.md#1-education-causal-chain-ladder). Flag misplacements (e.g., `"teachers trained"` placed at Outcome level, or `"post-school employment"` placed at Output level). Write `"unclear"` when result anchor is absent.
5. **Define Exact Operationalization**:
   - **Counts**: Define the unit counted (unique learners vs. attendance events vs. teacher coaching sessions vs. LMS logins) and deduplication rules across schools/terms.
   - **Percentages / Rates**: Define numerator, denominator, eligibility/exclusions, unit, population universe, and observation/academic window. Never retrofit an unstated denominator silently; propose it separately.
   - **Learning & Transition Metrics**: For pre/post assessments, specify matched cohort rules, test versions/language, floor/ceiling controls, and attrition handling. For LMS indicators, separate enrolled, active, completed, and competency-verified learners.
   - **Composites / Rubrics**: Name the instrument, sub-components, scoring/weighting rule, inter-rater reliability (IRR) check, and validation evidence; never claim validation without source citation.
6. **Check Source, Frequency, Equity, and Safeguarding**:
   - Distinguish **collection frequency** (e.g., weekly attendance register, termly assessment) from **reporting frequency** (e.g., semi-annual donor report).
   - Check [Education Equity Disaggregation](../../meal-references/education-meal-standards.md#3-education--equity-disaggregation-schema) categories (sex, age/grade band, disability via WG/CFM, rural/urban + admin tier, institution type, field of study, language/vulnerability) against collection feasibility and small-cell suppression rules.
   - Specify safeguarding, consent/assent, and PII handling rules for learner-level records.
7. **Check Across Sheets**: Flag duplicate constructs, mismatched denominators across linked indicators, conflicting academic windows, and results-chain gaps without rewriting indicators to force consistency.
8. **Assemble Sheets**: Use [IRS Template](./template.md). Leave unconfirmed fields as `"Not supplied"`, `"Not confirmed"`, or `"Decision required"`. Recommend independent review via `indicator-quality-review`.

## Missing, Conflicting, or Unsuitable Inputs
- **Incomplete indicator**: Produce a bounded IRS with visible gaps rather than guessed targets, owners, or denominators.
- **Conflicting definitions or targets**: Show both versions with Evidence IDs and log a change-control decision (`MEAS-D*`). If a signed/approved source conflicts with an unsigned later draft, use the signed version as working baseline (`proposed`) and flag the conflict for user choice.
- **Unvalidated composite score**: Flag validation provenance as unconfirmed and avoid endorsing it.
- **Non-MEAL request**: State scope and stop.

## Completion Checklist
- Every supplied indicator has an editable sheet linked to Evidence IDs.
- Approval status of wording, baselines, targets, roles, and tools is never inferred from mere presence; mark `"approval/status not supplied"` unless explicitly evidenced.
- Numerator, denominator, unit, population, academic/observation window, and deduplication rules are explicit or flagged.
- Collection frequency and reporting frequency are listed separately.
- Missing data, not applicable, and zero are distinguished cleanly.
- Independent `indicator-quality-review` is queued as the next check.
