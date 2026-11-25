---
name: evaluation-report-review
description: Independently review an Education evaluation report or findings brief across six quality dimensions (completeness, finding quality, evidence anchoring, limitation awareness, recommendation specificity, accessibility) and check TOR compliance against evaluation questions, methodology, and deliverables. Use after evaluation synthesis or when reviewing any draft/final evaluation report.
---

# Evaluation Report Review and TOR Compliance Check

## Purpose and Trigger
Conduct an independent quality review of an Education evaluation report across 6 scored dimensions AND optionally audit TOR compliance (evaluating whether every TOR evaluation question, methodology requirement, and deliverable was met). Technical review complements rather than replaces sectoral pedagogical judgment.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Input Classification and Intake
Support two complementary modes (or run combined when the TOR/Logframe are also supplied):
- **Mode A (Evaluation Report Quality Review)**: Classify document type before scoring: Full Final Report, Findings Brief, Performance Report, Impact Assessment, Mid-Term Evaluation Report (respecting `"preliminary/emerging findings"` disclaimers), Rapid Assessment, Narrative Summary, or Data Summary/Annex (assess as source material rather than narrative findings).
- **Mode B (TOR Compliance Check)**: Compare the evaluation report against its TOR (and Logframe if supplied) to audit question coverage (`ADDRESSED / PARTIAL / MISSING`), methodology adherence (`MET / PARTIAL / NOT MET`), and deliverable completeness (`Present / Missing`). Respect documented inception-stage TOR amendments when verified.
- **Non-MEAL input**: Return suitability note and stop.

State intake mode (`project-context/`, designated folder, or explicit files), document classification, evaluation type, and Evidence IDs (`filename#heading`, page, table, row).

## Scoring Thresholds (Mode A)
- **PASS**: Complete, evidence-grounded, candid about limitations, and clear.
- **PARTIAL**: Present with significant evidence, logic, or clarity gaps.
- **FAIL**: Missing, unsubstantiated, misleading, or hides critical limitations.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Evidence Anchoring (Section 3)** or **Limitation Awareness (Section 4)** automatically triggers **Major Issues** regardless of other scores.

## Six Quality Review Dimensions (Mode A)

### 1. Structural Completeness
Executive Summary (matches report body), Methodology (questions, design, sources, sample, limitations), Findings organized by evaluation question/outcome, Evidence citations, Limitations (scope, design, implementation), Conclusions (strictly derived from findings), and Recommendations linked to findings.

### 2. Finding Quality
- Grounded in quantitative, qualitative, or mixed data with magnitudes (`"74% of observed classrooms"`, not `"most teachers"`), triangulation, and exceptions noted.
- Answers intended evaluation questions; distinguishes correlation/pre-post learning gains from causal attribution unless counterfactual design supports causal inference; reconciles mixed results rather than hiding shortfalls.
- Clear implications for action without dense academic jargon.

### 3. Evidence Anchoring (Critical Weight)
- Specific citations for every claim (e.g., `"Grade 3 EGRA survey, n=640 across 32 schools"`, `"KIIs with 14 headteachers"`), never vague `"stakeholders reported"`.
- Sufficiency (no broad generalizations from single quotes), sample size/response rates/attrition disclosed, data quality/DQA issues disclosed, multi-source triangulation, and conflicting data addressed transparently.

### 4. Limitation Awareness (Critical Weight)
- **Scope transparency**: Geography, institution types, learner subgroups (e.g., enrolled vs. out-of-school), and academic period limits explicit.
- **Design limitations**: Comparison/counterfactual status, school/classroom cluster limits, sampling/selection/recall/observer bias, floor/ceiling test effects, and missingness disclosed.
- **Implementation limitations**: School closures, exam clashes, language barriers, attrition, and TOR deviations explained alongside what those constraints mean for finding credibility (never buried in an appendix).

### 5. Recommendation Specificity
- Concrete, feasible actions (who, what, where, operational mechanism, expected result), prioritized and sequenced with trade-offs noted, traceable directly to findings/conclusions without inventing out-of-scope program redesigns (refer design issues to `logframe-review` or TOR design issues to `evaluation-tor-review`).

### 6. Tone and Accessibility
- Audience-appropriate language, acronyms defined, balanced presentation of strengths and failures, clear executive summary, helpful tables/visuals, and technical annexes separated from main narrative.

## TOR Compliance Audit (Mode B)
When the TOR (or amended inception scope) is supplied:
1. Inventory every TOR evaluation question (with DAC criteria/sub-questions), methodology requirement (e.g., mixed methods, minimum 40 schools / 800 learners assessed, equity/gender/disability analysis), team/independence expectation, ethics/safeguarding rule, and deliverable.
2. Score each question (`ADDRESSED / PARTIAL / MISSING`) alongside evidence quality and triangulation depth.
3. Audit Methodology Compliance (`MET / PARTIAL / NOT MET`, noting justified field deviations) and Deliverables Checklist (`Present / Missing`, noting separately delivered items not verifiable from the report alone).

## Output Format
Provide concrete insertable text revisions for missing limitations, evidence anchors, or partial question answers:
1. **Evaluation Report Review Summary**: Intake Mode, Document Type, Evaluation Type, Overall Rating, and 6-row Score Summary table (plus Compliance Summary & Question Compliance Matrix if Mode B ran).
2. **Strengths**.
3. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
4. **Detailed Findings** (Sections 1 to 6, plus Question-by-Question TOR Compliance Analysis if Mode B ran) and **Unresolved Decisions (`EVAL-D*`)**.

## Output Rules and Resumption
- Calibrate depth to context (e.g., small project rapid assessment vs. multi-year impact study) while never excusing hidden limitations or unsupported causal claims.
- Keep facts, interpretations, and proposed fixes separate. On resume, re-verify inherited claims against original report and TOR files.
