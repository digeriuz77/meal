---
name: survey-tool-review
description: Independently review Education data collection instruments (student/teacher/household surveys, learning assessments, classroom observation rubrics, KII/FGD guides, LMS feedback forms, or intake/enrollment forms) for framework alignment, structure, question quality, sampling coverage, child safeguarding/ethics, and feasibility. Use before pre-testing or fieldwork.
---

# Education Survey and Data Collection Tool Review

## Purpose and Trigger
Conduct an independent quality review of Education data collection instruments across 6 scored dimensions to verify that tools collect valid, unbiased, feasible, and ethically safe data aligned to program indicators or evaluation questions. Field language, cognitive testing, and local safeguarding nuances should also be reviewed with local Education teams.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md) and [Education MEAL Standards](../../meal-references/education-meal-standards.md).

## Instrument Classification and Intake
Accept inputs via `project-context/`, designated folder, or explicit paste/files:
- **Student / Teacher / Household Survey** -> full 6-section review.
- **Learning Assessment / Competency Rubric** -> full review; emphasize Section 3 (administration standardization, floor/ceiling risk, language match, scoring clarity) and Section 6 (duration/fatigue).
- **Classroom Observation Rubric** -> emphasize Section 3 (objective behavioral anchors) and Section 6 (inter-rater reliability protocol, training).
- **KII / FGD Guide** (educators, parents, learners, school leaders) -> apply Sections 1, 3, and 5 fully; evaluate open-ended probing and group dynamics in Sections 2/4 rather than closed-response options.
- **Self-Administered / LMS Feedback / Exit Form** -> emphasize Sections 2, 3, 5, and 6 (brevity, plain language, navigation).
- **Enrollment / Registration / Intake Form** -> focus on Sections 3 and 6 plus PII minimization in Section 5.
- **Question list only (no intro/consent/demographics)** -> score Section 3 in full; mark Sections 1, 2, 5, and 6 `"Not Assessed"` (provisional rating).
- **Translated / multi-language tool** -> flag potential translation bias or back-translation gaps.
- **Non-MEAL input** -> return suitability note and stop.

State intake mode, instrument classification, and Evidence IDs (`filename#heading`, item number).

## Scoring Thresholds
- **PASS**: Meets standards with minor refinements only.
- **PARTIAL**: Present with significant gaps affecting reliability or usability.
- **FAIL**: Missing or contains severe bias, invalidity, or safeguarding/ethical harm risk.

**Overall Rating (apply critical overrides first):**
- **Strong**: `0 FAIL`, max `1 PARTIAL`.
- **Adequate**: `0 FAIL`, `2+ PARTIAL`.
- **Needs Revision**: `1 FAIL`, or `3+ PARTIAL`.
- **Major Issues**: `2+ FAIL`, OR **Critical Override**: `FAIL` in **Ethical Compliance and Child Safeguarding** automatically triggers **Major Issues** regardless of other scores.

## Six Review Dimensions

### 1. Purpose and Framework Alignment
- Purpose clear; questions map directly to specific framework indicators or evaluation questions.
- Target respondent matches indicator denominators and generates exact numerator inputs without topic bloat.

### 2. Instrument Structure and Flow
- Required sections present: Introduction (who/why), Informed Consent/Assent (before content items), Socio-demographic & Equity section, Logical Content sections (sensitive items placed later), and Wrap-up/Closing (including support/referral contacts if sensitive).
- Consistent numbering, section headers, and explicitly marked skip logic (`IF Q4 = No -> SKIP TO Q8`).

### 3. Question Quality
- **Neutrality & Non-Leading Framing**: Free of loaded phrasing (`"Don't you agree..."`), presuppositions (`"Since the new curriculum helped you..."`), and social desirability pressure; neutral enumerator prompts included.
- **Clarity & Single Concept**: Zero double-barreled items (`"Was the teacher coaching clear and frequent?"`), clear pronouns, explicit academic recall windows (`"During Term 2..."`), and defined units.
- **Response Formats**: Mutually exclusive, collectively exhaustive categories (with `"Other"`), balanced Likert scales, `"Don't know"` / `"Prefer not to answer"` where appropriate, and consistent scale polarity within sections.
- **Standard Indicators & Tools**: Flag validated standard items (e.g., Washington Group / Child Functioning Module disability items, EGRA/EGMA protocols) so they are NOT accidentally reworded.

### 4. Sampling, Coverage, and Equity Disaggregation
- Target group, selection/purposive logic (e.g., diverse sample of `"male and female learners, teachers, school heads, parents"`), and minimum Education disaggregations captured (sex, age/grade band, disability status, geography, institution type).

### 5. Ethical Compliance and Child Safeguarding (Critical Weight)
- Voluntary participation, purpose disclosure, data storage/confidentiality, and right to stop without school/grade penalty clearly stated.
- **Elevated Education Safeguarding Checks**:
  - **Minors / Students**: Parent/guardian informed consent AND age-appropriate learner assent required; adult/teacher interviews never conducted inside unsafe or non-private coercion settings.
  - **School Violence, Bullying, Safeguarding, Distress**: Trauma-informed framing and verified referral pathways mandatory.
  - **Displacement / Vulnerability & Digital PII**: Strict minimization of student names, national/student IDs, phone numbers, and GPS/device IDs with clear disclosure.

### 6. Practical Feasibility and Pre-Testing
- Appropriate cognitive length (`20-40` min field surveys, `< 10` min exit checks, age-calibrated for learners), clear enumerator/observer instructions, inter-rater reliability (IRR) plans for observations, and documented cognitive pre-testing/back-translation plans.

## Common Design Flaws (Fold Into Sections 1 to 6)
Topic bloat; checkbox-only consent; undefined recall windows; missing `"Don't know"`; missing observation IRR protocol; reworded standard items; absent back-translation plan.

## Output Format
1. **Survey Instrument Review Summary**: Intake Mode, Instrument Type, Overall Rating, and 6-row Score Summary table.
2. **Exact Standalone Severity Headings**:
   - `## Critical Issues`
   - `## Important Issues`
   - `## Minor Improvements`
   (Prioritize safeguarding/ethical defects first; write `"None identified from supplied files."` or `"Not assessable from supplied files."` if empty.)
3. **Priority Recommendations** (citing exact question numbers and quoted text).
4. **Detailed Findings** (Sections 1 to 6) and **Design Flaw Flags**.
5. **Unresolved Decisions (`MEAS-D*` / `EVAL-D*`)**.

## Output Rules and Resumption
- Quote exact problematic item numbers and text; do not recommend shortening an instrument without naming specific low-priority items to cut.
- Never assume unstated consent or IRB records do not exist in the program; classify unverified records as `"not confirmed present"` and gate fieldwork on verification.
