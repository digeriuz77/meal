---
name: theory-of-change-review
description: Independently review an Education Theory of Change, causal pathway, or results chain for logical coherence, assumption quality, evidence base, measurability, and scope clarity. Use after theory-of-change-draft or when assessing an existing ToC against Education MEAL standards.
---

# Theory of Change Review

## Purpose and Trigger
Conduct an independent quality review of an Education Theory of Change (or results chain) across 7 dimensions with section ratings (`PASS` / `PARTIAL` / `FAIL`), critical-weighting overrides, Education causal-chain checks, and exact severity classifications. Technical methodology review complements rather than replaces program and pedagogical validation by domain teams.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Full ToC document**: Narrative + visual description across all 8 elements -> apply full review.
- **Diagram only**: Visual/pathway map without narrative -> reconstruct logic table, focus on logical coherence, flag missing narrative.
- **Embedded in proposal**: Extract ToC content and assess as standalone.
- **Results chain / impact pathway**: Linear pathway -> assess causal logic; note simplified scope.
- **Narrative description**: Reconstruct each pathway first; flag silent elements as `"not confirmed present"` rather than `"missing"`.
- **Partial / Draft**: Review present components; flag gaps as `"needs development"` rather than `FAIL` unless foundational logic breaks.

State the active intake mode, document classification, and exact source IDs reviewed (`filename#heading`, page, table, row). If non-MEAL text is supplied, return a brief suitability note and stop.

## Scoring Thresholds
- **PASS**: Complete, evidence-informed, and internally consistent.
- **PARTIAL**: Present with significant gaps, unsupported links, or missing assumptions.
- **FAIL**: Missing, logically flawed, or disconnected from Education program reality.

**Overall Rating (apply critical override first, then most severe applicable band):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Logical Coherence** automatically triggers **Major Issues** regardless of other scores.

## Seven Review Dimensions

### 1. Logical Coherence (Critical Weight)
- Activities -> Outputs (direct, controllable) -> Intermediate Outcomes (educator practice, school environment, enrollment/attendance) -> Outcomes (retention, measured learning, transition) -> Goal/Impact contribution.
- No skipped steps across the [Education Causal Chain Ladder](../../meal-references/education-meal-standards.md#1-education-causal-chain-ladder) (e.g., training teachers jumping straight to improved literacy without classroom practice links; enrollment equating to attendance or learning).
- No circular logic or conflation of deliverables (`"150 teachers trained"`) with behavioral/learning outcomes (`"Teachers apply inclusive reading pedagogy"`).
- Multiple pathways represented for multi-component Education programs (supply, pedagogy, equity/access, governance/EMIS).

### 2. Assumptions Quality
- External assumptions documented between every level transition (distinct from risks and internal management execution).
- Classified by likelihood (`H/M/L`) and impact if false (`H/M/L`), with testable phrasing, monitoring triggers, and contingencies.

### 3. Evidence Base
- Causal links cite supporting research, prior evaluations, theoretical frameworks, or explicitly labeled team experience.
- Context relevance evaluated (flag outdated research >10 years old or cross-context transfers lacking justification).

### 4. Completeness
Assess the 8 standard ToC elements: (1) Problem statement grounded in data; (2) Target population with boundaries; (3) Causal pathways; (4) Assumptions at each level; (5) Evidence base; (6) Preconditions; (7) Implicit or explicit indicators at each level; (8) Narrative alongside diagram.
- `FAIL` if `3+` elements entirely missing; `PARTIAL` if `1-2` elements missing or skeleton-only (in Full ToC documents).

### 5. Measurability
- Outcomes and intermediate changes are operationally clear enough to support indicator design.
- Impact statements are bounded realistically; implied evidence needs match Education metrics (learning assessments, observation rubrics, EMIS/LMS records).

### 6. Scope and Boundaries
- Clear learner/educator demographic, grade/sub-sector, geographic, and temporal boundaries (when outcomes vs. impact are expected).
- Contribution vs. attribution explicitly acknowledged for higher-level Education outcomes.

### 7. Pathways and Complexity
- Multi-pathway structure for complex Education systems, feedback loops (e.g., teacher coaching -> classroom observation -> tailored mentoring), external disruptors (term closures, teacher attrition), and unintended/safeguarding risks addressed.

## Common Design Flaws (Fold Into Sections Above)
Diagram without narrative; aspirational unmeasurable impact; static proposal-stage ToC never revisited; missing intermediate pedagogy/attendance outcomes; assumption-free chain; evidence-free `"best practice"` claims; scope creep.

## Output Format
Produce clean editable Markdown with:
1. **Theory of Change Review Summary**: Intake Mode, Document Type, Overall Rating, and 7-row Score Summary table (`PASS / PARTIAL / FAIL / Not Assessed`).
2. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Never abbreviate or omit; write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty. Cite Evidence ID, consequence, and feasible fix for each issue.)
3. **Priority Recommendations** (top 3 to 5 ordered by severity).
4. **Detailed Findings** (1 through 7 with `PASS / PARTIAL / FAIL / Not Assessed`, stating what is present vs. missing on `PARTIAL` scores and keeping facts, assumptions, and proposed fixes distinct).
5. **Design Flaw Flags & Unresolved Decisions (`DES-D*`)**.

## Output Rules and Resumption
- Distinguish `"not present"` from `"not confirmed present"` for verbal/partial inputs and `"Not Assessed"` when input scope omits a dimension (label partial overall ratings provisional).
- Keep supplied dates and approval statuses untouched (`"approval status not supplied"` unless explicitly confirmed).
- On resume, re-validate inherited claims against original sources and flag changes in source files.
