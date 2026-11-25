---
name: theory-of-change-draft
description: Draft or revise a structured Education Theory of Change from program proposals, logframes, or context documents with causal pathway mapping, risk-classified assumptions, and weighted quality self-checks. Use when constructing or updating a Theory of Change before independent review.
---

# Theory of Change Draft

## Purpose and Trigger
Create or revise an Education Theory of Change through a structured pipeline: extract core program logic, clarify the change hypothesis, draft all 8 required elements, validate causal pathway completeness across the Education causal chain, and run a weighted quality self-check before handoff to independent review (`theory-of-change-review`).

Apply [Epistemic Contract](../../meal-references/epistemic-contract.md), [Education MEAL Standards](../../meal-references/education-meal-standards.md), and [Funder Formats](../../meal-references/funder-formats.md).

## Minimum Inputs
- Proposal, concept note, project brief, OR logframe/results framework (proposal preferred for problem analysis and strategy).
- Optional: M&E plan, baseline report, prior evaluations, or an existing ToC being revised.

State the active intake mode (`project-context/`, designated folder, or explicit files) and confirm ambiguous files before drafting.

## Workflow

### Step 1: Discover and Extract
Read confirmed source documents (and `project-context/` if active) and extract only directly stated content with Evidence IDs (`filename#heading`, page, table, or row):
1. **Goal / Impact**: Long-term educational or societal change the program contributes to.
2. **Outcomes**: Medium-term changes in educator practice, institutional capacity, learner attendance/retention, learning competency, or transition.
3. **Outputs**: Direct program deliverables (e.g., teachers coached, curricula adapted, learning materials delivered, LMS modules deployed).
4. **Activities**: What the program executes to produce each output.
5. **Assumptions & Context**: External conditions, preconditions, problem analysis data, and cited causal evidence.

Show an extraction summary noting results counts, assumptions found, problem-analysis source, evidence base, gaps, and any contradictions across documents.

### Step 2: Clarify Open Logic Questions
Ask concise clarifying questions only where source documents are silent:
- **Core Change Hypothesis**: What mechanism links inputs/training to learner outcomes (e.g., "If teachers receive structured coaching AND schools use formative assessments, classroom instruction improves and early-grade literacy gains follow")?
- **Multiple Pathways**: Are there parallel pathways (educator pedagogy, learner access/equity, school governance/EMIS, family/community engagement, EdTech/LMS)?
- **Contribution vs. Attribution**: Is the program one contributor within a public/institutional system?
- **Uncertain Links & Audience**: Which pathways carry highest uncertainty, and who is the primary audience?

### Step 3: Draft the Eight Required Elements
Use direct, declarative prose. Remove filler adjectives (`unprecedented`, `groundbreaking`, `transformative`, `game-changing`, `holistic approach`, `robust framework`). Cite every extracted fact; mark gaps as `[NEEDS USER INPUT]` or `"Not specified in source documents."`

1. **Problem Statement**: Ground in supplied needs-assessment data: what problem exists, who is affected, root causes across Education barriers, and scale evidence. Do not describe the program here.
2. **Target Population**: Primary beneficiaries (learners by age/grade/level/equity group), secondary beneficiaries (teachers, school leaders, parents, institutions), geographic boundaries, and expected temporal horizon for outcomes vs. impact.
3. **Causal Pathways**: Map each pathway explicitly across the [Education Causal Chain Ladder](../../meal-references/education-meal-standards.md#1-education-causal-chain-ladder):
   ```text
   PATHWAY [N]: [Name]
   Activities: [list] -> Outputs: [list] -> Intermediate Outcomes: [list] -> Outcomes: [list] -> Impact contribution
   Mechanism: [Why does each link occur?]
   Assumptions: [External conditions required]
   Evidence: [Cited source or "Program team experience; no published citation supplied"]
   ```
   Verify no skipped links (for example, teacher training must not jump straight to student test gains without classroom practice change, or enrollment to learning without attendance/engagement).
4. **Assumptions**: Classify every testable assumption:
   `| Assumption | Level Transition | Likelihood (H/M/L) | Impact if False (H/M/L) | Monitoring Trigger | Contingency |`
   Example of testable phrasing: `"District education officers conduct at least 3 of 4 scheduled termly school-support visits"` (avoid vague phrasing like `"Stakeholders cooperate"`).
5. **Evidence Base**: Classify support for each causal link: published research (cited in supplied docs), prior program evaluation, program team experience (stated honestly), theoretical framework, or `[No evidence identified in supplied sources]`.
6. **Preconditions**: Conditions required before start (e.g., Ministry/institutional MOU signed, curriculum/assessment approvals granted, baseline collected before instructional term starts).
7. **Indicators**: Map existing framework indicators onto pathway levels and flag unmonitored links.
8. **Narrative**: Coherent 500 to 800 word explanation synthesizing problem, pathways, mechanisms, key assumptions, and evidence limits without contradicting the pathway tables.

### Step 4: Self-Check and Targeted Revision
Verify internal consistency across the 8 elements, normalize formatting (no em-dashes, clean `- ` lists), and run a self-check against 5 weighted dimensions (`0.00-1.00` in `0.05` steps):
- `LOGICAL_COHERENCE` (`0.30`): Bottom-up causal progression, no skipped Education levels, explicit mechanisms, multiple pathways where needed.
- `ASSUMPTION_QUALITY` (`0.25`): Testable external assumptions at each transition, likelihood/impact rated, monitoring triggers included.
- `EVIDENCE_GROUNDING` (`0.20`): Causal links backed by cited evidence or honestly labeled team experience.
- `MEASURABILITY` (`0.15`): Results operationally clear, indicators mapped, measurement gaps flagged.
- `COMPLETENESS` (`0.10`): All 8 elements present and consistent with narrative.

Compute `OVERALL = 0.30*COHERENCE + 0.25*ASSUMPTION + 0.20*EVIDENCE + 0.15*MEASURABILITY + 0.10*COMPLETENESS` (`>= 0.85` PASS, `0.70-0.84` REVISE, `< 0.70` FAIL). Revise any dimension below threshold (up to 2 passes) and log what changed.

### Step 5: Finalize and Hand Off for Independent Review
Deliver the editable Markdown ToC with pathway count, assumption count, evidence coverage, unresolved decisions (`DES-D*`), and explicit recommendation to run `theory-of-change-review` independently before updating `project-context/`.

## Missing, Conflicting, or Unsuitable Inputs
- **Only a bare idea or partial notes**: Produce a bounded ToC skeleton highlighting missing problem data, unverified mechanisms, and `[NEEDS USER INPUT]` gaps.
- **Conflicting proposal and logframe**: Document both versions with Evidence IDs and log a `DES-D*` governing-source decision rather than guessing.
- **Non-MEAL request**: State scope boundary and stop.

## Completion Checklist
- All 8 ToC elements are present and mutually consistent.
- Education causal chain steps (inputs, educator practice, enrollment, attendance, retention, learning, transition) are explicit with no skipped links.
- Facts, assumptions, cited evidence, and proposals are clearly separated.
- Next step points to independent `theory-of-change-review`.
