---
name: evaluation-tor-review
description: Independently review an Education evaluation Terms of Reference (TOR), SOW, or commissioning brief across ten quality dimensions, and verify cross-document alignment of evaluation questions against the logframe and M&E plan. Use after evaluation-tor-draft or before procurement.
---

# Evaluation TOR Review and Alignment Check

## Purpose and Trigger
Conduct an independent methodological and feasibility review of an Education evaluation TOR, Scope of Work (SOW), commissioning brief, or evaluation RFP across 10 scored sections, AND optionally cross-check TOR questions against the project's logframe and M&E plan for orphan questions, missing indicators, or impossible counterfactual claims.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Support two complementary modes (or run combined when framework files are also supplied):
- **Mode A (TOR Quality Review)**: Assess a Full TOR, Commissioning Brief, SOW, RFP extract, Draft/Concept Note, Template, Partially Filled draft, or Narrative description across 10 sections. Calibrate expectations by document type (e.g., do not penalize a commissioning brief for intentionally omitted procurement boilerplate; mark unfilled sections `"Not Assessed"`).
- **Mode B (Question-to-Framework Alignment Check)**: Compare the TOR against the Logframe / Results Framework (required) and M&E Plan (optional but valuable) to detect unanswerable questions, ignored outcome/goal indicators, design mismatches, and scope drift.
- **No TOR supplied**: State `"No TOR was supplied in this input"` (never claim no TOR exists or was approved elsewhere) and return a bounded preparation note.
- **Non-MEAL input**: Return suitability note and stop.

State intake mode (`project-context/`, designated folder, or explicit files), document type, evaluation type, and Evidence IDs (`filename#heading`, page, table, row).

## Scoring Thresholds (Mode A)
- **PASS**: Complete, coherent, ethical, and feasible.
- **PARTIAL**: Present with significant gaps or ambiguities.
- **FAIL**: Missing, unethical, infeasible, or unable to answer core questions.

**Overall Rating:**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, exactly `2 PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL` (and treat severe child safeguarding/ethics or impossible counterfactual-budget failures as Critical Issues blocking procurement).

## Ten TOR Quality Dimensions (Mode A)
1. **Completeness**: Background/ToC, purpose/decisions, scope, questions, methodology expectations, team/LOE, deliverables/timeline, budget, ethics/safeguarding, and governance.
2. **Evaluation Questions Quality**: Purpose-matched OECD-DAC criteria (do NOT require all 6 by default; justify selected ones), answerable with feasible data, non-leading, well-scoped, manageable count (`>10` is a red flag), zero counterfactual phrasing without counterfactual design.
3. **Methodology**: Methods fit questions (preserving evaluator independence to propose final design), mixed methods justified, sampling scope coherent, and Education flags addressed: school/academic calendar alignment for fieldwork, classroom observation/assessment protocols, and EMIS/LMS data access.
4. **Ethical Compliance and Child Safeguarding**: Voluntary participation, guardian informed consent + age-appropriate child/learner assent, do-no-harm, Ministry/IRB ethics review, minor PII security, data retention/destruction, and safeguarding referral pathways proportionate to context (without imposing unprovided universal checklists).
5. **Team Composition and Level of Effort**: Specific methodological and Education expertise, national/local expertise, gender/inclusion balance, realistic LOE covering inception, school travel, analysis, and revisions.
6. **Deliverables and Timeline**: Clear deliverables (inception, tools, draft, final, brief/presentation), review turnaround cycles, QA process, and realistic day allocations relative to supplied effort, academic terms, and school access.
7. **Budget Realism**: Ceiling/range, inclusions/exclusions (travel, translation, IRB/Ministry fees, enumerator/assessor training), payment terms, and resource-to-scope realism (missing cost assumptions are an unresolved feasibility decision, not an automatic fail against an arbitrary dollar threshold).
8. **Standards Alignment**: Alignment with OECD-DAC guidance, UNEG Norms and Standards, AEA Guiding Principles, and any named funder's verified evaluation policy (never invent donor rules).
9. **Practical Readiness**: Inventory of available monitoring/EMIS/baseline data, prior reviews, multi-language/translation needs, stakeholder engagement, and dissemination/use plan.
10. **Internal Consistency**: Cross-check Scope <-> Budget <-> Questions <-> Methodology <-> Academic Timeline <-> Team <-> Ethics; cite both statements on contradictions.

## Cross-Document Question Alignment Checks (Mode B)
When Logframe / M&E Plan files are supplied:
1. Build flat indicator and collection inventory (Result Level, Indicator, Baseline, Target, Source, Method, Frequency, Latest Data).
2. Map every TOR question to DAC criterion, Logframe result(s), mapped indicator(s), data availability, and required method (`ALIGNED / PARTIAL / GAP / NO MATCH`).
3. Flag **Question-side gaps** (unmapped questions, counterfactual asks lacking comparison design, duplicate questions), **Indicator-side gaps** (key outcome/goal indicators ignored by all questions, or unmeasured M&E plan indicators assumed available), and **Scope misalignments** (geography, school levels, or period mismatch). Not every output indicator needs its own question; focus on strategic coverage of key outcomes and goal.

## Output Format
Provide concrete insertable question/TOR revision language, not vague advice:
1. **TOR Review Summary**: Intake Mode, Document Type, Evaluation Type, Overall Rating, and 10-row Score Summary table (plus Alignment Coverage Matrix if Mode B ran).
2. **Strengths**: Concrete well-designed elements.
3. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Never abbreviate or omit; write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
4. **Detailed Findings** (Sections 1 to 10, plus Alignment Matrix & Question Revision Suggestions if Mode B ran) and **Unresolved Decisions (`EVAL-D*`)**.

## Output Rules and Resumption
- Calibrate post-hoc reviews (evaluations already underway/completed) as lessons for future commissioning rather than blocking edits. Refer users needing framework logic review to `logframe-review`.
- Keep supplied facts, assumptions, and proposed wording separate. On resume, re-verify inherited claims against original source documents.
