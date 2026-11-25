---
name: meal-system-audit
description: Perform a comprehensive seven-dimension Education MEAL/MERL system audit across all project documents and project-context/ files (or independently verify a meal-overview-builder deliverable), checking cross-document consistency, indicator coherence, reporting plausibility, evaluation alignment, and gaps. Use for holistic quality assurance.
---

# Education MEAL System Audit

## Purpose and Trigger
Conduct an independent, comprehensive audit of an entire Education MEAL/MERL document ecosystem (or audit an overview built by `meal-overview-builder` against underlying source files). Maps the dependency chain, cross-checks consistency across every document, rates 7 system dimensions on a traffic-light dashboard (`GREEN / YELLOW / RED / GREY`), and produces a prioritized remediation roadmap. System audit identifies structural and cross-document defects; pedagogical and field validation remains with program teams.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## M&E Document Dependency Chain
Trace every downstream link against its upstream authority:
```text
Proposal / ProDoc
  -> Theory of Change
    -> Logframe / Results Framework
      -> M&E / MEL / MEAL Plan + Evaluation TOR
        -> Indicator Reference Sheets (IRS) + Baseline / Sampling / Tools -> DQA
          -> Progress Reports + Evaluation Report -> Management Response
```

## Intake and Document Discovery
1. **Discover and Confirm Scope**: Scan `project-context/` or the user-designated folder using [Funder Formats](../../meal-references/funder-formats.md#3-education-meal-document-discovery-patterns). Read the opening 50 to 100 lines of candidate files, classify them (`Present / Missing / Partial`), flag unrecognized files or multiple program versions, and confirm the exact audit scope with the user before full extraction (if explicit files are already named, proceed directly).
2. **Audit Strategy for Large Folders**: Read governing design files first (`project-context/`, Proposal, ToC, Logframe, M&E Plan), then Baseline/Reports/Evaluations, then Tools/Guidelines.
3. **Non-MEAL input**: Return suitability note and stop.

## Extraction and Cross-Document Consistency Checks
Extract exact text and Evidence IDs (`filename#heading`, page, table, row) across all confirmed files for:
- **Indicator Names & Operational Definitions**: Logframe <-> M&E Plan <-> IRS <-> Progress Reports (exact wording/construct match?).
- **Indicator Targets & Baselines**: Logframe <-> M&E Plan <-> IRS <-> Baseline Report <-> Progress Reports (same numbers and denominators?).
- **Education Equity & Target Populations**: Proposal <-> ToC <-> Logframe <-> M&E Plan <-> Reports (same learner/school counts, grade levels, and disaggregation categories?).
- **Geographic Scope & Institutions**: Proposal <-> Logframe <-> M&E Plan <-> Reports (e.g., 45 target schools vs. 30 schools).
- **Academic Calendar & Program Timeline**: Proposal <-> Logframe <-> M&E Plan <-> TOR (consistent start/end dates and school terms?).
- **Result Statements & M&E Budget**: ToC <-> Logframe <-> Proposal <-> M&E Plan (wording and resource alignment?).
- **Data Sources & Methods**: M&E Plan <-> IRS <-> Assessment/Survey Tools <-> DQA (methods, units, and frequency match?).
- **Evaluation Questions & Evidence**: Eval TOR <-> Eval Report <-> Monitoring Data <-> Management Response.

## Seven Audit Dimensions
Rate each dimension using the Traffic Light System:
- **GREEN**: `0` critical issues, max `2` important issues.
- **YELLOW**: `0` critical + `3+` important issues, OR `1` critical issue already marked resolved/addressed with evidence.
- **RED**: `2+` unresolved critical issues (or `1` unresolved critical systemic failure blocking use).
- **GREY**: Insufficient documents in the supplied set to assess this dimension (never assign `FAIL` or `RED` simply because an optional file was omitted).

**Overall System Health Roll-Up:**
- **Healthy**: All dimensions `GREEN` or `GREY`.
- **Manageable**: Zero `RED` dimensions, some `YELLOW`.
- **At Risk**: `1` `RED` dimension.
- **Critical**: `2+` `RED` dimensions.

Assess all 7 dimensions:
1. **Design Coherence**: ToC <-> Logframe vertical `IF-THEN` alignment across the Education causal chain (educator practice, enrollment, attendance, retention, learning, transition); testable assumptions; zero orphan results.
2. **Indicator System Quality**: SMART/result-level accuracy, quantified baselines, evidence-grounded targets, Education equity disaggregation (sex, age/grade, disability, geography, institution type), standard SDG 4 / UIS indicator integrity.
3. **Data Collection Alignment**: Methods fit indicator constructs, collection vs. reporting frequency coherence, EMIS/LMS/school access confirmed, VIPRT DQA and observation IRR protocols, child safeguarding/assent coverage.
4. **Document Consistency**: Exact cross-document alignment across indicators, baselines, targets, learner counts, schools/geography, timelines, and budget. (Target/scope/definition contradictions = **Critical**; wording drift = **Minor**.)
5. **Reporting Quality**: Progress reports cover framework indicators, arithmetic/denominators reconcile, single-period no-trend rule respected, narrative aligns with shortfalls, equity disaggregated.
6. **Evaluation Alignment**: TOR questions map to logframe/M&E data, reports answer TOR questions with grounded evidence and candid limitations, findings align with monitoring records, actions link to findings.
7. **Gap Analysis**: Missing documents in the chain, incomplete sections, broken upstream-downstream links, stale downstream drafts after upstream edits, missing DQA/safeguarding quality gates.

## Output Format
Serve both leadership (dashboard) and technical MEAL teams (detailed evidence table):
1. **M&E System Audit Summary**: Intake Mode, Scope, Documents Audited (`N`), Overall System Health (`Healthy / Manageable / At Risk / Critical`), and **Document Inventory Table**.
2. **System Health Dashboard**: `Dimension | Rating (GREEN/YELLOW/RED/GREY) | Critical | Important | Minor | Summary`.
3. **Cross-Document Consistency Findings Table**: `Check | Documents Compared | Discrepancy & Evidence IDs | Severity`.
4. **Exact Standalone Severity Headings**:
   - `## Critical Issues` (Fix Immediately: system-level contradictions invalidating credibility or safeguarding)
   - `## Important Issues` (Fix This Quarter/Term: document-level gaps)
   - `## Minor Improvements` (Terminology, formatting, incremental disaggregation)
   *(If 50+ issues exist, show top 10 Critical and Important issues here and offer the full register separately. Write `"None identified from supplied files."` or `"Not assessable from supplied files."` under empty headings.)*
5. **Missing Documents & Stale Artifacts**, **Priority Action Plan** (`Immediate / Short-term / Medium-term / Structural`), **Detailed Findings by Dimension**, and **Unresolved Decisions (`DES-D*` / `MEAS-D*` / `REP-D*` / `EVAL-D*`)**.

## Output Rules and Resumption
- Distinguish document absence in the supplied set (`GREY` / `"not supplied"`) from confirmed non-existence in the real program.
- Keep confirmed facts, discrepancies, assumptions, and proposed fixes separate. On resume, re-check updated upstream sources and clear or retain staleness flags accordingly.
