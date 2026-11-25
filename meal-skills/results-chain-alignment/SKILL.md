---
name: results-chain-alignment
description: Compare and align a Theory of Change, Logframe, Results Framework, Proposal, or Indicator Register bidirectionally, preserving source versions and authority decisions; or draft an Education Logframe shell from an approved Theory of Change or Proposal. Use when results documents diverge or when translating a ToC into a structured logframe.
---

# Results-Chain Alignment and Logframe Drafting

## Purpose and Trigger
Operate in two complementary Construct modes:
1. **Cross-Document Alignment Mode**: Compare supplied design artifacts bidirectionally to show where they align, diverge, conflict, or leave causal/measurement links unsupported while preserving exact source wording and authority status.
2. **Logframe Shell Drafting Mode**: When no Logframe exists (or a revised shell is requested from a ToC/Proposal), draft a structured Education Logframe skeleton preserving source taxonomies and marking unverified targets/baselines as unresolved decisions.

This skill does not validate empirical causal effects or silently override approved frameworks. Follow with independent `logframe-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- **Alignment Mode**: At least two distinct artifacts, including at least one results-chain/results-framework document (ToC, Logframe, Results Framework, Proposal, or Indicator Register).
- **Logframe Shell Mode**: A Theory of Change, Proposal/Concept Note, or approved results hierarchy plus preferred funder format (if known).

State the intake mode (`project-context/`, designated folder, or explicit files) and exact files/versions reviewed. Do not treat system dates as evidence of whether a supplied document is "late" or "stale" unless a superseding source record establishes it; otherwise write `"status unknown from supplied files"`.

## Reproducible Procedure

### Mode A: Bidirectional Cross-Document Alignment
1. **Register Sources**: List filename, document type, date/version, and explicit approval status (`approval/status not supplied` if absent).
2. **Extract Each Source Independently**: Extract exact result statements, level labels, indicator wording/definitions, target learner/educator populations, geography, academic periods, assumptions, resources/budget, and pathways with Evidence IDs (`filename#heading`, page, table, row, or diagram label).
3. **Preserve Source Taxonomies**: Do not equate donor labels (e.g., `Specific Objective` vs. `Outcome`) automatically. Show any crosswalk as a **proposed** mapping for team confirmation using [Funder Formats](../../meal-references/funder-formats.md#1-results-hierarchy-terminology-mapping).
4. **Compare Bidirectionally**: Map ToC/proposal elements to the Logframe/Results Framework AND framework elements back to the ToC/proposal. Classify each relationship strictly:
   - `Aligned`: Compatible scope and result logic (does not prove empirical truth).
   - `Partial`: Shared content with differing or incomplete scope, population, academic period, level, or construct.
   - `Conflict`: Incompatible statements (targets, counts, locations, definitions, level assignments) that cannot both govern as written.
   - `Not found in supplied sources`: Absent in reviewed files only (do not assert non-existence elsewhere).
   - `Not assessable`: Missing context prevents defensible judgment.
5. **Trace Causal Links, Equity, and Resources**:
   - Distinguish asserted hypothesis, cited rationale/evidence, observed results, and demonstrated causal effect across the Education causal chain.
   - Compare indicators without rewriting: exact wording/version, definition, unit, learner population, observation window, and result anchor.
   - Compare required equity disaggregations (sex, age/grade, disability, geography, institution type) and supplied budget/staffing commitments against activities/results without inventing capacity judgments when resource data are silent.
6. **Handle Version Conflicts Strictly**: Never pick a winner by apparent recency alone. When a formally signed/approved document conflicts with a later unsigned draft, use the signed document as the working version labeled `proposed`, and log a `DES-D*` decision flagging that the later document may govern if approved.
7. **Return Structured Matrix**: Use [Alignment Matrix Template](./template.md). If invoked as a targeted check, include exact standalone headings `## Critical Issues`, `## Important Issues`, and `## Minor Improvements`.

### Mode B: Education Logframe Shell Drafting
1. Confirm the governing funder terminology (Standard Goal/Outcome/Output, LFA Overall/Specific Objective/Result/OVI/SoV, Results Framework IR/Sub-IR, or UN format).
2. Map pathways from the supplied ToC/Proposal into a clean bottom-up `IF-THEN` hierarchy: Activities -> Outputs -> Outcomes -> Goal.
   - Verify no activity is mislabeled an output (`"Conduct teacher workshops"` = activity; `"120 teachers trained"` = output; `"Teachers apply formative assessment in 75% of observed lessons"` = outcome).
   - Keep enrollment, attendance, retention, learning mastery, and post-education transition at their proper hierarchy levels.
3. Populate the four core columns (`Result Statement`, `Indicators with Baseline & Target`, `Means of Verification / Data Sources`, `Testable External Assumptions / Pre-conditions`). Leave unquantified baselines/targets as `[Pending: Decision DES-D*]` rather than inventing numbers.
4. Recommend running `logframe-review` independently on the completed shell.

## Missing, Conflicting, or Unsuitable Inputs
- **Only one artifact supplied in Alignment Mode**: Provide source extraction only and name the missing comparison artifact; issue no alignment verdict.
- **Missing indicator definitions**: Compare labels as labels only and request definitions before claiming construct alignment.
- **No identifiable result structure**: Extract stated claims and mark hierarchy alignment `"Not assessable"`.
- **Non-MEAL request**: State boundary and stop.

## Completion Checklist
- Intake mode, files, versions, and approval statuses are explicit.
- Source-specific taxonomies and exact indicator wording are preserved without silent edits.
- Comparisons ran bidirectionally and conflicts display both Evidence IDs.
- Facts, assumptions, proposed crosswalks/resolutions, and unresolved `DES-D*` decisions are separate.
- Next step recommends independent `logframe-review`.
