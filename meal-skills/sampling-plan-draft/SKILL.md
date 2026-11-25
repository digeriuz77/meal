---
name: sampling-plan-draft
description: Draft an Education M&E sampling plan, or verify an existing plan's sample size calculations, school/classroom cluster design, and selection rules from purpose, population, frame, and constraints. Use when designing or checking a sample before independent sampling-plan-review.
---

# Sampling Plan Draft

## Purpose and Trigger
Create a prospective, reproducible Education sampling plan (for monitoring, baselines, learning assessments, or evaluations), or check an existing sampling plan's sizing and selection logic against design rules without overriding approved choices. Follow with independent `sampling-plan-review`.

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md) and [Education MEAL Standards](../../meal-references/education-meal-standards.md).

## Minimum Inputs
- Study purpose, indicator(s) or evaluation question(s), target population/unit (learners, classrooms, teachers, schools, households), and known frame details.
- Precision, MDE/power, or comparison requirements, mode, geography, academic timing, required equity subgroups, and operational constraints (if available).

State intake mode (`project-context/`, designated folder, or explicit files) and exact files reviewed. Supplied dates govern; never extrapolate execution dates or claim respondents were selected.

## Reproducible Sequence
1. **Define Estimand and Inference Population**: Name the target estimand or qualitative question, eligibility/exclusions, selection vs. analysis units (e.g., schools vs. classrooms vs. individual learners vs. teachers/parents), geography, academic term dates, and whether the job is descriptive estimation, subgroup/domain comparison, causal evaluation, or qualitative explanation. Random sampling does not establish causal attribution without a valid comparison/assignment design.
2. **Audit the Sampling Frame**: Document source/date (e.g., EMIS school registry, enrollment roster, LMS list, household census), unique IDs, coverage errors, omissions (e.g., out-of-school youth, unregistered non-formal centers, absent learners), duplicates, and access permissions. Larger sample sizes do not fix frame bias. Propose frame repair or explicitly scoped population adjustments without exposing student/staff PII.
3. **Select Sampling Approach with Rationale**: Evaluate census, simple random, stratified, systematic, multi-stage cluster (e.g., District -> School -> Grade/Class -> Learner), or purposive qualitative design. Note that probability area/school frames can substitute when individual learner lists are absent. Purposive selection requires explicit variation criteria and never carries a survey margin of error.
4. **Size Only the Applicable Design**: Show inputs, formula, substitutions, rounding, units, and source/scenario labels for every parameter. Independently recompute supplied and proposed arithmetic step by step; flag any discrepancies. If required parameters (such as ICC, response/attendance rate, or baseline variance) are missing and scenarios were not requested, output an unresolved sizing specification checklist rather than fabricating numbers.
5. **Specify Reproducible Field Selection Rules**: Detail each selection stage, frame freeze date, reproducible randomization method/seed tracking (for future execution), contact/re-visit spacing, absentee/attrition handling, guardian consent + child assent refusal logging, and pre-declared reserve-school/reserve-learner rules. Never replace absent/refusing learners with convenience substitutes in the classroom.
6. **Verify Design Weights, Domain Precision, and Feasibility**: Specify design weights, inverse selection probabilities, cluster-robust/survey-design-aware variance estimation, and domain precision limits (sufficient total `n` or `n >= 30` does not guarantee precision for small equity domains like learners with disabilities). Check fieldwork visits against academic calendars, exam blackouts, and available resources without certifying an underpowered budget-capped design.
7. **Plan Pilot Validation and Decisions**: Define a pre-fieldwork frame/tool audit, decision criteria, conditions before fieldwork, and change control.

## Sizing Rules and Boundaries

### Single Proportion (Simple Random Sampling Without Replacement Only)
Use ONLY for a two-sided approximate confidence interval for one unclustered proportion:
- `n0 = z^2 * p * (1 - p) / e^2`
- Apply finite population correction `n = n0 / (1 + (n0 - 1) / N)` only when finite eligible population `N` warrants adjustment.
- Round required completions up once after adjustment; then `invitations = ceil(required_completions / r)` where `r` accounts for expected absenteeism, attrition, and nonresponse.
- Require explicit sources or `scenario` labels for `z`, `p`, absolute margin `e` (e.g., `0.05` = 5 percentage points), `N`, and `r`. Never silently default to 95%, 5 percentage points, or 80% attendance/response. Validate `0 < p < 1`, `0 < e < 1`, `0 < r <= 1`, `z > 0`, `N > 0`. If `invitations > N`, flag infeasibility rather than capping silently.
- Do NOT apply this formula to means, clustered school assessments, paired pre/post learning gains, impact evaluations, or small subgroup domains.

### Education Cluster, Multi-Stage, Stratified, and Power Designs
- **Cluster / Multi-Stage (School / Classroom)**: Classroom and school clustering strongly inflates variance due to peer, teacher, and socioeconomic homogeneity. Document clusters, stages, selection probabilities, and source-backed Intraclass Correlation (`ICC`) / Design Effect (`DEFF`). `1 + (m - 1) * ICC` is an equal-cluster-size approximation only; unknown ICC or too few clusters cannot be fixed by an arbitrary default multiplier (such as multiplying `n` by `2.0`).
- **Comparison / Power (e.g., Pre/Post or Treatment vs. Control Schools)**: Require outcome scale, cluster count vs. cluster size, baseline mean/SD or rate, Minimum Detectable Effect (MDE), alpha, power, repeated-measure correlation, and term-to-term attrition. Escalate complex multi-level power specs for formal statistical review rather than guessing from simple formulas.
- **Stratified / Equity Domain Estimates**: Allocate sample specifically for reported subgroups (e.g., girls vs. boys, rural vs. urban, disability status, TVET trades); state weight adjustments for oversampling.
- **Qualitative (Classroom KIIs / Student & Parent FGDs)**: Define purposive stratification, consent/assent, saturation review rules, and clear non-prevalence limits.

## Output Structure
Return one editable Markdown artifact using [Sampling Plan Template](./template.md) covering all 9 sections (scope/status; source register/conflicts; population/frame/inference; proposed approach/alternatives; verified sizing or unresolved calculation checklist; selection/nonresponse/safeguarding; weights/domain precision/limitations; feasibility/pilot/decisions; completion & change record).

When checking an existing plan, additionally include exact standalone headings `## Critical Issues`, `## Important Issues`, and `## Minor Improvements`.

## Missing, Conflicting, or Unsuitable Inputs
- **Missing frame or population**: Deliver a bounded design shell with exact unresolved decisions; do not compute a representative `n`.
- **Conflicting target domains or numbers**: Show both sources with Evidence IDs and flag the sizing impact.
- **Non-MEAL request**: State scope boundary and stop.

## Completion Checklist
- Every requested indicator/domain and school/learner unit is addressed or marked unresolved.
- Cluster effects (ICC/DEFF), school absenteeism, and term attrition are handled explicitly, never hidden behind simple SRS defaults.
- All arithmetic was independently recomputed and units reconcile (`completions` vs. `invitations`, `schools` vs. `learners`).
- Child safeguarding, parent consent, minor assent, and non-substitution rules are explicit.
- Next step queues independent `sampling-plan-review`.
