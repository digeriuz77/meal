---
name: data-quality-planning
description: Plan a risk-based Education Data Quality Assessment (DQA) across VIPRT dimensions from supplied indicators, EMIS/LMS data flows, risks, access, and capacity constraints, with proposed checks, owners, and timing. Use when planning a DQA before independent data-quality-review. Does not certify data or report verification findings.
---

# Data Quality Assessment (DQA) Planning

## Purpose and Boundary
Create a prospective, risk-based DQA plan to assess Education monitoring data and the systems producing them (EMIS, school attendance registers, classroom observations, learning assessments, LMS logs, and partner trackers). This skill **plans** checks; it never certifies data, reports verification findings, or treats planned procedures as completed evidence. Follow completed DQA execution or reports with independent `data-quality-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md) and [Education MEAL Standards](../../meal-references/education-meal-standards.md).

## Minimum Inputs
- Indicator definitions, intended use, learner/educator population, academic period, and reported values/requirements (if available).
- Data flow from classroom/school/LMS capture through aggregation, cleaning, review, and reporting.
- Known data risks, prior DQA findings, capacity, permissions, and approved tolerance thresholds (if any).

If no indicator or data stream is supplied, request it first. If data flow or capacity constraints are absent, deliver a bounded planning outline flagging unresolved items. Never infer that unmentioned controls or records do not exist. State intake mode (`project-context/`, designated folder, or explicit files) and evidence locations. Supplied dates govern.

## Method
1. **Set Scope and Boundary**: Define decision use, academic/reporting period, indicators, institution types, locations, and explicit exclusions. Separate facts from proposals.
2. **Map the Education Data Flow**: Trace each indicator across: source record (paper register, assessment sheet, LMS log, EMIS entry) -> collector (teacher, school head, enumerator) -> data entry/digitization -> aggregation -> QA review -> report. Label every link `confirmed`, `candidate`, or `unknown`, noting versions and roles only where supplied.
3. **Prioritize Risk Explicitly**: Prioritize sites/indicators using supplied decision importance, funder accountability weight, known variances, definition ambiguity, ghost/duplicate-enrollment risks, capitation/reporting bias, LMS drop-offs, missing records, or hard-to-reach populations. State the rationale for each priority; never invent numeric risk weights, fixed intervals, or arbitrary sample percentages.
4. **Plan Checks Across the Five VIPRT Lenses**: Treat each lens as a planned verification question, not a pre-scored result:
   - **Validity**: Do school registers, test rubrics, or LMS triggers actually measure the indicator construct (e.g., attendance vs. enrollment; LMS completion vs. skill mastery)?
   - **Reliability**: Would independent re-abstraction, duplicate test scoring, or second-observer classroom checks reproduce the same result?
   - **Precision**: Are denominators, grade/age bands, disability categories, and unit definitions exact enough for decisions?
   - **Integrity**: Are register edits, system exports, approvals, and student PII protected from unauthorized alteration or exposure? Missing logs are a control gap to check, not proof of tampering.
   - **Timeliness**: Do termly capture, EMIS sync, and submission schedules meet reporting deadlines?
5. **Separate Check Procedures Clearly**:
   - *Completeness*: Expected school/term submissions vs. received records.
   - *Reconciliation*: Recompute school -> district -> summary totals; note that matching a report to its summary sheet confirms arithmetic consistency, not source truth.
   - *Source Verification*: Trace selected reported numbers back to physical attendance books, graded assessment scripts, or raw LMS activity logs via authorized access.
   - *Accuracy / Independent Validity*: Spot-check against independent headcounts, classroom observations, or re-testing where authorized.
   - *Reliability*: Duplicate abstraction or inter-rater reliability (IRR) checks where resources allow.
   - *Timeliness & Integrity*: Trace timestamps, version logs, access controls, and approval trails.
6. **Choose Records and Sites Defensibly**: Prefer census verification where small volumes allow; otherwise define the selection frame, risk-based vs. probability rationale, and unresolved sample size pending record volume confirmation. Explicitly warn that purposive/risk-based spot-checks find exceptions but cannot generalize an error rate across all schools.
7. **Verify Safeguarding, Consent, and Ethics**: Confirm Ministry/school authorization, IRB/ethics clearance (if contacting learners), child/guardian protection, minimum necessary student PII access, and secure data transport before planning any site visits or re-interviews.
8. **Specify Tolerance Rules and Prior-Action Follow-Up**: Apply only supplied approved tolerance thresholds; otherwise record counts/variances for review and mark threshold adoption `Decision required` (`MEAS-D*`). If prior DQA actions exist, add verification checks for claimed closures (a "closed" label is a claim to test, not proof).
9. **Define Conditional Escalation**: Specify what pauses a check (minor privacy breach, safeguarding risk, suspected deliberate alteration, material source conflict) and who receives escalation without making unverified accusations.
10. **Deliver Blank Assessment Record**: Provide the DQA plan with blank completion fields reserved strictly for post-fieldwork execution.

## Output Format
Return editable Markdown with these 8 sections:
1. **Plan Status and Purpose**: Explicitly state `"Draft DQA plan; checks not yet performed"`, intake mode, decision use, academic/reporting period, and exclusions.
2. **Evidence Register**: Source IDs (`filename#heading`, page, table, row), supplied facts, unknowns, and proposals kept distinct.
3. **Indicator and Risk Selection**: Indicator, use, data-flow status, priority level with evidence rationale, and exclusions.
4. **Planned Check Matrix**: Indicator/site/stage; check type and VIPRT lens; procedure/evidence needed; selection method (`proposed` if aligned to supplied capacity); responsible role (`proposed` from supplied roles or unresolved); timing (within supplied academic calendar/review gates, or unresolved); permissions/safeguards; threshold rule; limits.
5. **Selection and Feasibility**: Frame, census vs. sample rationale, non-representativeness warning for purposive samples, capacity dependencies (no invented sample sizes, days, or costs).
6. **Unresolved Decisions and Approvals (`MEAS-D*`)**: Missing definitions, school/EMIS access, thresholds, safeguarding sign-offs, escalation authority.
7. **Conditional Escalation Protocol**: Pause triggers and escalation routing without pre-judging findings.
8. **Blank Completion Record (For Future Assessment Use Only)**: Empty fields for execution dates, schools/records checked, verified variances, limitations, and assessor sign-off.

## Missing, Conflicting, or Unsuitable Inputs
- **No indicator or data stream**: Ask what data stream requires assessment and stop.
- **Unconfirmed access or permissions**: Make affected field/record checks explicitly conditional on documented authorization.
- **Request to certify data accuracy before checks**: State boundary clearly and provide only the prospective DQA plan.
- **Non-MEAL request**: State scope and stop.

## Completion Checklist
- Plan explicitly states checks have not been executed and leaves no fabricated findings or certifications.
- All five VIPRT lenses and Education data-flow risks (EMIS, registers, assessments, LMS) are addressed cleanly.
- Thresholds, sample sizes, roles, timing, and permissions distinguish supplied facts, proposals, and unresolved `MEAS-D*` decisions.
- Safeguarding and minor PII rules are explicit before any site/record contact.
