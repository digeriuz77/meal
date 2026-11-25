# AGENTS.md: Education MEAL / MERL Workspace

This workspace provides a streamlined, Antigravity-native suite of **29 Education-focused MEAL/MERL skills** under `meal-skills/` (registered via `.agents/skills.json`) plus shared standards under `meal-references/`. Its core purpose is constructing traceable Education MEAL/MERL overviews, plans, and reports grounded in ongoing project context, paired with **strictly independent review skills**.

## 1. Operating Principles

1. **Construct vs. Review Separation**: Always construct or update deliverables using a Construct skill, then invoke the paired Review skill independently against the draft and original source files. Never skip the independent review gate on final overviews, plans, TORs, or reports.
2. **Ongoing Project Context (`project-context/`)**: Maintain persistent program state across sessions in `project-context/` using `meal-context-manager`:
   - `project-context/project-brief.md` (program identity, education sub-sector, academic calendar, funder format, document inventory)
   - `project-context/indicator-ledger.md` (longitudinal indicator table, baselines, targets, periodic actuals, variance, DQA status, equity disaggregations)
   - `project-context/evidence-register.md` (source filenames, versions/dates, approval status, extracted facts)
   - `project-context/decision-log.md` (stage-prefixed decisions `DES-D*`, `MEAS-D*`, `REP-D*`, `EVAL-D*`)
   - `project-context/handover.md` (session resumption checkpoint)
3. **Upstream Dependency Chain**: Track lineage from upstream to downstream (`Proposal -> Theory of Change -> Logframe -> M&E Plan -> IRS -> Baseline / Sampling / Tools -> DQA -> Progress Reports -> Evaluation TOR -> Evaluation Report -> Management Response`). When an upstream file changes, flag affected downstream files in `project-context/` for re-check.
4. **Epistemic & Education Standards**: Follow `meal-references/epistemic-contract.md`, `meal-references/education-meal-standards.md`, and `meal-references/funder-formats.md` in every task:
   - Keep **Confirmed Facts** (with `[Source: filename#section]` IDs), **Assumptions**, **Proposed Recommendations**, **Unresolved Decisions**, and **Approved Decisions** strictly distinct.
   - Never fabricate targets, baselines, budgets, sample sizes, owners, dates, or approvals.
   - Treat blank/missing values separately from zero; never infer trends from a single period; never claim causal impact from routine monitoring or simple pre/post change alone.
   - Apply Education rigor: distinguish enrollment, attendance, retention, completion, learning gains, and transition; align to academic calendars; enforce child/learner assent, parent consent, and minor PII protection.

## 2. Skill Routing Table (29 Skills)

### Ongoing Context and Overviews (Group A)
| Need | Skill | Output |
|---|---|---|
| Initialize, update, or resume ongoing project context | `meal-context-manager` | Synchronized `project-context/` Markdown files + staleness flags |
| Construct a MEAL/MERL overview, executive brief, donor summary, or learning brief | `meal-overview-builder` | Traceable Education MEAL overview (then run `meal-system-audit` or `progress-report-review`) |

### Construct <-> Independent Review Pairs (Groups B and C)
| MEAL Deliverable / Stage | Construct Skill | Independent Review Skill |
|---|---|---|
| Theory of Change | `theory-of-change-draft` | `theory-of-change-review` |
| Logframe / Results Chain Alignment | `results-chain-alignment` | `logframe-review` |
| Indicator Definitions & Burden | `indicator-reference-sheets`, `measurement-feasibility` | `indicator-quality-review` |
| M&E / MEL / MEAL Plan | `me-plan-draft` | `me-plan-review` |
| Baseline Plan / Study Report | `baseline-planning` | `baseline-report-review` |
| Sampling & Data Collection Tools | `sampling-plan-draft` | `sampling-plan-review`, `survey-tool-review` |
| Data Quality Assessment (VIPRT) | `data-quality-planning` | `data-quality-review` |
| Progress / Quarterly / Annual / Donor Report | `progress-report-draft` | `progress-report-review` |
| Evaluation TOR / SOW & Questions | `evaluation-tor-draft` | `evaluation-tor-review` |
| Evaluation Synthesis & Management Response | `findings-to-actions` | `evaluation-report-review` |
| Proposal M&E Section / RFP Compliance | `me-plan-draft`, `results-chain-alignment` | `proposal-me-review` |
| Cross-Document System Health | `meal-overview-builder` | `meal-system-audit` |

### Chained Construct -> Review -> Sync Workflows (Group D)
| End-to-End Job | Workflow Skill | Decision Prefix |
|---|---|---|
| Indicator review -> burden -> IRS -> M&E plan -> coherence check | `workflow-feasible-measurement` | `MEAS-D*` |
| Evidence reconciliation -> progress report -> review -> revision -> actions | `workflow-reporting-to-action` | `REP-D*` |
| Evaluation questions -> method matrix -> TOR -> review -> revised TOR sync | `workflow-evaluation-planning` | `EVAL-D*` |

## 3. Standard Review Output Rule

All Review skills (`*-review` and `meal-system-audit`) must emit these exact standalone headings without numbering or abbreviations:
- `## Critical Issues`
- `## Important Issues`
- `## Minor Improvements`
