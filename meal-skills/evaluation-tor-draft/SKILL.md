---
name: evaluation-tor-draft
description: Draft prioritized Education evaluation questions, build a question-to-evidence/method matrix, and draft a ten-section Evaluation Terms of Reference (TOR / SOW) with gaps, child safeguarding, and academic calendar feasibility explicit. Use when commissioning an evaluation across three callable modes (questions, matrix, full-tor) before independent evaluation-tor-review.
---

# Evaluation TOR Draft (Questions, Method Matrix, and Ten-Section TOR)

## Purpose and Trigger
Support Education evaluation commissioning across three callable modes (invoked individually or sequentially), producing editable Markdown drafts for technical and commissioner review rather than approved procurement commitments. Follow with independent `evaluation-tor-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Callable Modes
State the active mode and intake mode (`project-context/`, designated folder, or explicit files) at the start of every output:
1. **`questions` Mode**: Frame 3 to 5 prioritized, answerable evaluation questions linked to stated decisions and purpose-matched criteria.
2. **`matrix` Mode**: Map evaluation questions to constructs, indicators, confirmed vs. candidate data sources, methods, timing, feasibility, and limitations using [Question-Method Matrix Template](./templates/question-method-matrix.md).
3. **`full-tor` Mode**: Draft the complete 10-section Education Evaluation TOR with explicit `[To be confirmed: ...]` placeholders for unknown budget, days, roles, or procurement rules.

## Minimum Inputs
- **Questions Mode**: Evaluation purpose/commissioning reason, intended users/decisions (if known), Education program/stage, and scope boundaries.
- **Matrix Mode**: Evaluation questions or purpose, learner/educator population context, known sources/EMIS/assessments, and constraints.
- **Full-TOR Mode**: Program description/framework, evaluation purpose, intended users, and known scope, timing, academic calendar, or budget constraints.

## Procedure by Mode

### Mode 1: Prioritized Evaluation Questions (`questions`)
1. Confirm purpose, stage (baseline, formative/midterm, summative/endline), intended users, decisions, scope, and constraints. Extract program facts with Evidence IDs (`filename#heading`, page, table, row).
2. Identify decisions questions must inform; if none are supplied, mark decision link unresolved and offer provisional options only.
3. Select criteria fit to purpose (do not include all OECD-DAC criteria by default; justify every selected criterion).
4. Draft 3 to 5 primary questions (subquestions only where clarifying scope). Enforce all question checks:
   - **Relevance & Focus**: Tied to a stated decision; one construct per question (split double-barreled questions).
   - **Neutrality & Scope**: Non-leading wording; explicit learner/educator population, geography, and academic period when supported.
   - **Answerability & Causal Precision**: Match question wording to plausible evidence. Reserve `"caused"` or `"effect"` strictly for designs capable of counterfactual attribution; use `"what changed"` or `"what factors contributed"` for descriptive/pre-post designs.
   - **Priority Transparency**: Rank by decision value, answerability, and scope fit labeled `proposed` (no invented numeric scores).
5. Output: purpose/intake mode; source summary & evidence register; facts/assumptions/proposals; prioritized question matrix (`priority; criterion/rationale; primary question; subquestions; decision/use; evidence needed; answerability note; evidence IDs`); deferred/excluded questions with reasons; `EVAL-D*` open decisions & checklist.

### Mode 2: Question-to-Method Alignment (`matrix`)
1. Classify each question as descriptive, explanatory, comparative, or causal; flag counterfactual wording unsupported by design.
2. Identify minimum evidence, indicator/construct, unit of analysis (learner, classroom, teacher, school, district; never mix units silently), population, academic timeframe, and comparison group (if authorized).
3. Map confirmed sources first (EMIS, LMS logs, baseline/progress trackers, standardized assessments) separately from candidate new collection (learning tests, classroom observations, surveys, KIIs/FGDs). Distinguish participation/attendance records from changed pedagogy or learning gains.
4. Check triangulation (corroborating across independent sources, not repeating one source), mixed-methods integration rationale, sampling/frame status (never invent sample sizes), academic-calendar alignment (avoiding exam/holiday blackouts unless intended), and child safeguarding/assent/consent requirements.
5. Output using [Question-Method Matrix Template](./templates/question-method-matrix.md) with cross-cutting decisions (`EVAL-D*`).

### Mode 3: Ten-Section Education Evaluation TOR (`full-tor`)
1. Extract program logic, results framework, M&E plan, baseline/progress findings, funder rules, timing, budget, and governance strictly from supplied sources with Evidence IDs.
2. Incorporate refined questions and method expectations (leaving appropriate evaluator methodological room without prescribing invalid methods).
3. Draft all 10 required sections, keeping unknown figures as `[To be confirmed: specific item]` and never translating absence from files into a claim that the program lacks the item:
   1. **Background and Context** (Education sub-sector, results logic, implementation stage; no promotional claims as findings)
   2. **Evaluation Purpose and Intended Use** (intended users and concrete decisions)
   3. **Scope and Boundaries** (geography, institution types, learner/educator groups, academic period, explicit exclusions)
   4. **Evaluation Questions and Criteria** (numbered set linked to purpose-selected criteria)
   5. **Methodology Expectations and Evidence Needs** (question-method fit, learning assessment validity, cohort/comparison limits, desk review vs. school fieldwork separation)
   6. **Team Composition and Expertise** (expertise tied to scope/Education assessments/safeguarding; never invent years of experience or LOE)
   7. **Deliverables, Timeline, and Review Process** (inception, fieldwork inside academic terms, draft report, validation, final report; separate desk days from school fieldwork days; if a day cap is given, verify task days reconcile)
   8. **Budget and Logistics** (ceiling, inclusions/exclusions, translation, enumerator training, safeguarding checks; unknown values remain placeholders)
   9. **Ethics, Safeguarding, and Data Protection** (parent/guardian informed consent, age-appropriate child assent, Ministry/IRB approvals, minor PII protection, enumerator background checks & referral protocols; mark unconfirmed consent records as conditional, never assert `"no consent was obtained"` merely from silence)
   10. **Management, Governance, and Quality Assurance** (commissioner vs. evaluator independence, technical review vs. management sign-off; distinguish decision owner from budget holder/approver unless specified)
4. Check internal cross-section consistency (questions <-> methods <-> scope <-> team <-> academic calendar <-> day cap/budget) and return the 10-section TOR, evidence register, facts/assumptions/proposals, unresolved `EVAL-D*` decisions, consistency/feasibility notes, and completion checklist. Queue independent `evaluation-tor-review`.

## Missing, Conflicting, or Unsuitable Inputs
- **Missing purpose/users/budget**: Deliver bounded drafts with `[To be confirmed: ...]` placeholders and prioritized `EVAL-D*` questions.
- **Cohort-level vs. site-level targets**: Never apply a cohort-level target automatically to individual schools or centers without a source statement.
- **Conflicting versions**: Show both sources with Evidence IDs without harmonizing silently.
- **Non-evaluation request**: State scope and stop.

## Completion Checklist
- Mode (`questions`, `matrix`, or `full-tor`) and intake mode are explicit.
- Every factual claim has an Evidence ID or is marked an assumption/proposal.
- Causal wording matches plausible design capacity.
- Academic calendar windows, child/learner safeguarding, minor PII, and assessment/observation validity are explicitly addressed.
- Unknown budgets, day allocations, sample sizes, owners, and procurement approvals remain explicitly unresolved (`EVAL-D*`).
- Next step recommends independent `evaluation-tor-review`.
