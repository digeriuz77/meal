# Education MEAL / MERL Standards and Schemas

This reference establishes Education-specific technical standards across Early Childhood Education (ECE), K-12 / basic education, Technical and Vocational Education and Training (TVET), higher education, and non-formal / EdTech programs.

## 1. Education Causal Chain Ladder

Education programs commonly span long, multi-stage causal chains. Every Theory of Change, Logframe, M&E Plan, and Overview must verify intermediate links across this ladder rather than leaping across stages:

```text
Inputs & Resources (curriculum, learning materials, facilities, grants, EdTech infrastructure)
  -> Educator Capacity & Learning Environment (teacher/facilitator training, mentoring, safe/inclusive classrooms)
    -> Access & Enrollment (eligible learner registration, fee/barrier removal)
      -> Active Participation & Attendance (regular attendance, LMS active engagement, coaching dosage)
        -> Retention, Progression & Completion (term-to-term persistence, grade promotion, course completion)
          -> Measured Learning & Competency Outcomes (literacy/numeracy, TVET skill mastery, socio-emotional skills)
            -> Post-Education Transition & Livelihoods (secondary/tertiary transition, credentialing, employment, civic outcomes)
```

### Causal Jump Red Flags
Flag these common Education logic failures during construction and review:
- Treating **teacher/facilitator training completion** as proof of changed classroom pedagogy or improved student learning without classroom observation or assessment links.
- Conflating **enrollment** (registered on roster) with **attendance** (present on observed days) or **retention/completion** (still enrolled and completing the cycle).
- Treating **contact events or LMS logins/page views** as mastery or competency gain.
- Using **post-education transition or employment** as an output indicator when placement depends on external labor-market and institutional assumptions.

## 2. Longitudinal Indicator Performance Table Schema

Use this standardized table schema across `project-context/indicator-ledger.md`, `meal-overview-builder`, and `progress-report-draft` so indicator baselines, periodic targets, actuals, and data quality status stay synchronized across documents:

| indicator_id | indicator_name | result_level | unit | frequency | baseline_year | baseline_value | period | target | actual | variance | dqa_status | source_id |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| [ID] | [Exact framework wording] | [Goal/Outcome/Output] | [%/count/score/ratio] | [Monthly/Term/Annual] | [Year/Term] | [Quantified or Not yet measured] | [Reporting window] | [Period target] | [Verified actual or Not reported] | [Actual vs. Target; absolute & %/pp] | [Verified/Pending/Flagged] | [filename#section] |

### Operational Table Rules
- Maintain separate rows or explicit labels for **period actuals** vs. **cumulative actuals**.
- Keep **pre-test**, **mid-test**, and **post-test** score metrics linked to matched cohorts (`cohort_id`, `round`) and record attrition (`n_pre`, `n_post`, `n_matched`).
- For digital/EdTech and LMS indicators, distinguish **enrolled**, **active** (threshold defined), **completed**, and **competency-verified** learners.
- Separate **service delivery counts** (trainings, workshops, mentoring visits, textbooks distributed) from **unique participant/learner counts** and **downstream outcome indicators**.

## 3. Education & Equity Disaggregation Schema

Unless a framework explicitly justifies narrower scope, check indicators and instruments for disaggregation across these Education equity dimensions:

| Dimension | Standard Education Categories & Notes |
|---|---|
| **Sex / Gender** | Female, Male, and locally appropriate inclusive categories where safe and ethical; report missing/unclassified separately. |
| **Age & Grade / Cohort Band** | Age bands matched to sub-sector (e.g., ECE 3-5, Primary 6-11, Lower/Upper Secondary 12-17, TVET/Higher Ed 18-24, Adult) plus Grade/Level/Cohort round. |
| **Disability Status & Functional Type** | Screen with Washington Group Short Set (adults/youth) or UNICEF/Washington Group Child Functioning Module (children) rather than binary self-report alone; track functional domain where sample size permits without re-identification risk. |
| **Geography & Setting** | Rural / Peri-urban / Urban plus administrative tiers (Region, Zone/District, Sub-city/Woreda/School cluster). |
| **Institution Type & Sub-Sector** | Public, Private, Community/NGO, Faith-based; ECE, Primary, Secondary, TVET/Polytechnic, University, Non-formal / Accelerated Learning Center. |
| **Program / Field of Study** | Academic track, TVET trade/occupation, STEM vs. non-STEM, language track (for secondary/TVET/higher ed). |
| **Language & Equity Vulnerability** | Home language vs. language of instruction (LOI), displacement/refugee status, first-generation status, or poverty proxy (only where safe, consented, and protective). |

- Verify that disaggregated sub-totals reconcile to the headline total; report `"unknown / not recorded"` separately rather than dropping uncategorized learners.
- For small schools or rare disability/vulnerability cells, enforce suppression thresholds (e.g., `n < 5` or `n < 10`) in public reports to prevent deductive identification of learners.

## 4. Academic Calendar, Assessment, and Sampling Rules

1. **Academic Calendar Alignment**: Align baselines, midlines, endlines, and progress periods to school terms, semesters, exam cycles, and holidays. Comparing start-of-year scores in one cohort against end-of-year scores in another introduces seasonal maturation bias.
2. **Cohort vs. Cross-Sectional Tracking**: Specify explicitly whether longitudinal gains reflect the **same tracked learners** (panel cohort, requiring attrition analysis) or **different cohorts in the same grade** (cross-sectional, sensitive to shifting intake composition).
3. **Assessment Validity & Reliability**:
   - Standardize administration protocols, scoring rubrics, timing rules, and enumerator training (e.g., EGRA/EGMA, ASER, national curriculum tests, TVET practical competency checklists).
   - Check for **ceiling effects** (test too easy at baseline), **floor effects** (zero-score clustering), **practice/test-retest bias**, and **language-of-assessment mismatch**.
   - Require **inter-rater reliability (IRR)** checks for classroom observation tools and practical skill rubrics.
4. **School & Classroom Sampling**:
   - Distinguish **school-based frames** (miss out-of-school, chronically absent, or dropped-out children) from **household-based frames**.
   - Multi-stage sampling (District -> School -> Classroom -> Learner) requires an explicit **Intra-Cluster Correlation (ICC)** assumption and **Design Effect (DEFF)** inflation factor; never apply simple random sampling formulas to clustered school data without adjustment.
   - Account for expected learner absenteeism on assessment day and term-to-term attrition when sizing samples.
5. **EMIS & LMS Data Quality (VIPRT)**: Check Education Management Information Systems (EMIS), school registers, and LMS exports for ghost/duplicate enrollments, incentives that inflate headcounts (capitation bias), delayed term reporting, and teacher workload burdens.

## 5. Child and Learner Safeguarding and Data Ethics

- **Assent & Consent**: Require documented **parent/guardian informed consent** plus age-appropriate **child/learner assent** (in clear local language) for minors; obtain institutional/Ministry/IRB approvals before collecting primary school data.
- **Data Protection & PII**: Minimize collection of student names, national/student IDs, phone numbers, and exact home addresses (kebele/street/GPS); store identifiers separately under role-based access and encryption; never publish school- or learner-level tables that expose vulnerable children or poorly performing individual teachers to retaliation.
- **Safeguarding & Referral**: Assessment teams, classroom observers, and enumerators interacting with learners must complete safeguarding training/background checks and carry clear, locally verified referral protocols for disclosure of abuse, violence, or severe distress.
